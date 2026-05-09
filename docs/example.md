# 直播信息流客户端示例

编写于: 2026年5月9日

本示例基于浏览器 [Web APIs](https://developer.mozilla.org/docs/Web/API) 编写，最低依赖 [Fetch API](https://developer.mozilla.org/docs/Web/API/Fetch_API) 和 [WebSocket API](https://developer.mozilla.org/docs/Web/API/WebSockets_API) 。这些依赖在2017年3月以后的浏览器均有广泛的支持， Node.js 22 及以上版本也可用。

本示例将忽略[浏览器的同源策略](https://developer.mozilla.org/docs/Web/Security/Defenses/Same-origin_policy)来编写。

本示例将使用较新的API来编写。除了最低依赖的要求，其余API应该有替代实现。

**本示例不会提供 Wbi 签名的算法，有需要的请自行查找。**

*示例仅用于理解流程，请勿直接使用。*

---

```javascript
// Wbi 签名部分
/** Wbi 签名 */
function encWbi(params, img_key, sub_key){
	return query + "&w_rid=" + wbi_sign;
}
/** 获取最新的 key */
async function getWbiKeys(){
	return {
		img_key: "",
		sub_key: "",
	}
}
/** Cookie */
const cookie = "";

// 示例正文

/**
 * 通过位移将整数转换为 Uint8Array
 * @param {number} value 整数
 * @param {number} bytes 字节数
 * @param {boolean} littleEndian 是否小端序
 * @returns {Uint8Array}
 */
function numberToBytes(value, bytes, littleEndian = false){
	const arr = new Uint8Array(bytes);
	for (let i = 0; i < bytes; i++) {
		const shift = littleEndian ? i * 8 : (bytes - 1 - i) * 8;
		arr[i] = (value >>> shift) & 0xff;
	}
	return arr;
}
/**
 * 将32位(4字节)无符号字节数组转换为整数
 * @param {Uint8Array} bytes 字节数组
 * @param {number} offset 偏移量
 */
function readUint32BE(bytes, offset = 0) {
	return (
		(bytes[offset] << 24) |
		(bytes[offset + 1] << 16) |
		(bytes[offset + 2] << 8) |
		bytes[offset + 3]
	) >>> 0;
}
/**
 * 创建数据包
 * @param {BlobPart} body 消息正文
 * @param {number} version 协议版本
 * @param {number} operation 操作码
 * @param {number} sequence 递增
 */
function createPack(body, version = 1, operation = 2, sequence = 0){
	const data = await new Blob([body]).bytes();
	const packLength = 16 + data.byteLength;
	const pack = new Uint8Array(packLength);
	pack.set(numberToBytes(packLength, 4), 0);// 数据包总大小
	pack.set(numberToBytes(16, 2), 4);// 头部大小
	pack.set(numberToBytes(version, 2), 6);// 协议版本
	pack.set(numberToBytes(operation, 4), 8);// 操作码
	pack.set(numberToBytes(sequence, 4), 12);// sequence
	pack.set(data, 16);
	return pack;
}
/**
 * 获取信息流信息
 * @param {number} room_id 真实直播间ID
 * @returns {Promise<Object>} BiliRESTReturn
 */
async function getDanmuInfo(room_id){
	const wbi_key = getWbiKeys();
	const params ={
		room_id,
	};
	const res = await fetch(`https://api.live.bilibili.com/xlive/web-room/v1/index/getDanmuInfo?${encWbi(params,wbi_key.img_key,wbi_key.sub_key)}`,{
		"headers":{
			"Cookie": cookie,
		},
		credentials: "same-origin",
		mode: "cors",
	});
	return await res.json();
}
/** 示例入口函数 */
async function main(){
	// 获取连接
	const ac = await getDanmuInfo(23058);
	if(ac.code !== 0)throw new Error("code != 0");
	// 建立连接
	const data = ac.data;
	const host = data.host_list[0];
	const ws = new WebSocket(`wss://${host.host}:${host.wss_port}/sub`);
	let seq = 0;
	// 发送认证包
	ws.send(createPack(JSON.stringify({
		// 示例只简单提供几个参数
		room_id: 23058,
		key: data.token;
	}), 1, 7));
	// 准备心跳包循环
	setInterval(function(){
		ws.send(createPack("", 1, 2, seq));
		seq ++;
	}, 3e4);
	// 进行数据监听
	ws.addEventListener("message", ev => {
		// 示例仅作简单的处理
		const data = ev.data.bytes();
		switch(readUint32BE(data, 8)){
			case 3:// 心跳包回复
				console.log("人气: ", readUint32BE(data, 16));
				break;
			case 5:// 普通包
				console.debug("数据包: ", data);
				break;
			case 8:// 认证包回复
				console.log("认证回复: ", data.subarray(16));
				break;
		}
	});
	return ws;
}

// 仅在浏览器控制台或特殊环境可用
const ws=await main();
```
