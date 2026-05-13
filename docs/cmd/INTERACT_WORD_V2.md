# 用户交互消息V2 (INTERACT_WORD_V2)

该cmd已将 `INTERACT_WORD` 替换。

## 下发条件

与 [用户交互消息 (INTERACT_WORD)](INTERACT_WORD.md) 相同。

## JSON消息

参见 [用户交互消息 (INTERACT_WORD)](INTERACT_WORD.md) 。

根对象:

| 字段 | 类型 | 内容   | 备注      |
| ---- | ---- | ------ | --------- |
| cmd  | str  | `INTERACT_WORD_V2` |  |
| data | obj  | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| dmscore | num |  |  |
| pb | str | 使用 base64 编码 protobuf 后的数据 | 解析后数据基本与`INTERACT_WORD`的`data`相同 |

用于解析protobuf数据的proto文件: [bilibili.live.xuserreward.v1](../../protobuf/bilibili/live/xuserreward/v1.proto)

注: 先用 base64 解码 `data.pb` 内的字符串为字节数据 pb ，再使用 proto 文件解码 pb 数据。

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "INTERACT_WORD_V2",
	"data": {
		"dmscore": 3,
		"pb": "CJTwwNEBEgpTdGFyU2VhMjQ2IgIDASgBMNWgITispaTDBkDUubHe/jJKLAiv8CkQEhoG55Sf5oCBIKS6ngYopLqeBjCkup4GOKS6ngZAAWDVoCFo9JQRYgB4gZ/v1tmc1qcYmgEAsgHPAQiU8MDRARJYCgpTdGFyU2VhMjQ2EkpodHRwczovL2kwLmhkc2xiLmNvbS9iZnMvZmFjZS8xMDliNzg3YzVmMTEzYzRhM2M3NDE1YmI5YmY2YjgyYmMzM2JjNGUyLmpwZxpnCgbnlJ/mgIEQEhikup4GIKS6ngYopLqeBjCkup4GOP/hAUgBUK/wKWD0lBF6CSNEQzZCNkI5OYIBCSNEQzZCNkI5OYoBCSNEQzZCNkI5OZIBCSNGRkZGRkZGRpoBCSM4MTAwMUY5OSICCAkyALoBAA=="
	}
}
```

</details>
