# 礼物心愿单进度 (WIDGET_WISH_LIST)

## 下发条件

*未知*

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| cmd | str | `WIDGET_WISH_LIST` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| wish | array | 礼物心愿单信息 |  |
| wish_status | num | (?) |  |
| sid | num | (?) |  |
| wish_status_info | array | (?) |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "WIDGET_WISH_LIST",
	"data": {
		"wish": [
			{
				"type": 3,
				"gift_id": 10003,
				"gift_name": "舰长",
				"gift_img": "https://i0.hdslb.com/bfs/live/f1be2a2d5b227ce72641de1ad64bcc7f9e4111c3.png",
				"gift_price": 198000,
				"target_num": 5,
				"current_num": 0
			},
			{
				"type": 2,
				"gift_id": 3,
				"gift_name": "B坷垃",
				"gift_img": "https://s1.hdslb.com/bfs/live/cc8bfcbc24c8b65937f62ce0d16b31ab987dce47.png",
				"gift_price": 9900,
				"target_num": 5,
				"current_num": 0
			},
			{
				"type": 2,
				"gift_id": 31039,
				"gift_name": "牛哇牛哇",
				"gift_img": "https://s1.hdslb.com/bfs/live/b8a38b4bd3be120becddfb92650786f00dffad48.png",
				"gift_price": 100,
				"target_num": 10,
				"current_num": 0
			}
		],
		"wish_status": 1,
		"sid": 477,
		"wish_status_info": [
			{
				"wish_status_msg": "设定心 愿",
				"wish_status_img": "https://i0.hdslb.com/bfs/live/38f82bac32794e79776f7371269453652bd58a87.png",
				"wish_status": 0
			},
			{
				"wish_status_msg": "达成",
				"wish_status_img": "https://i0.hdslb.com/bfs/live/1dae635924437239fc69e561a1a9467508521249.png",
				"wish_status": 2
			},
			{
				"wish_status_msg": "收集失败",
				"wish_status_img": "https://i0.hdslb.com/bfs/live/3bbd30fdd32d085cc90e9ccd98c65a886dca9a8f.png",
				"wish_status": 3
			}
		],
		"wish_name": "心愿"
	}
}
```

</details>
