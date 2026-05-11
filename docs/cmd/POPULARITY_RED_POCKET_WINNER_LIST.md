# 直播间抢到红包的用户 (POPULARITY_RED_POCKET_WINNER_LIST)

红包中奖列表。

## 下发条件

红包结算。

## JSON消息

根对象:

| 字段 | 类型 | 内容                                | 备注 |
| ---- | ---- | ----------------------------------- | ---- |
| cmd  | str  | `POPULARITY_RED_POCKET_WINNER_LIST` |      |
| data | obj  | 信息本体                            |      |

`data` 对象:

| 字段        | 类型  | 内容     | 备注 |
| ----------- | ----- | -------- | ---- |
| lot_id      | num   | 红包 ID  |      |
| total_num   | num   | 礼物总数 |      |
| winner_info | array | 中奖信息 |      |
| awards      | obj   | 礼物信息 |      |
| version     | num   |          |      |

`data.winner_info` 数组:

| 项 | 类型  | 内容         | 备注 |
| -- | ----- | ------------ | ---- |
| 0  | array | 中奖者 1     |      |
| …… | array | ……           |      |
| n  | array | 中奖者 (n+1) |      |

`data.winner_info[n]` 数组:

| 项 | 类型 | 内容                   | 备注 |
| -- | ---- | ---------------------- | ---- |
| 0  | num  | 该抢到红包的用户的 mid |      |
| 1  | str  | 该抢到红包的用户的名称 |      |
| 2  | num  | bag_id?                |      |
| 3  | num  | 该用户抢到的礼物的 ID  |      |

`data.awards` 对象:

以 礼物 ID 为键, JSON Object 为值的表

`data.awards['?']` 对象:

| 字段          | 类型 | 内容         | 备注 |
| ------------- | ---- | ------------ | ---- |
| award_type    | num  | 奖品类型?    |      |
| award_name    | str  | 礼物名称     |      |
| award_pic     | str  | 礼物图标 URL |      |
| award_big_pic | str  | 礼物大图 URL |      |
| award_price   | num  | 礼物价值     |      |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "POPULARITY_RED_POCKET_WINNER_LIST",
	"data": {
		"lot_id": 8445764,
		"total_num": 8,
		"winner_info": [
			[
				38554435,
				"我的0019",
				4581509,
				31212
			],
			[
				516174930,
				"云来海遛鸟大爷",
				4606389,
				31212
			]
		],
		"awards": {
			"31212": {
				"award_type": 1,
				"award_name": "打call",
				"award_pic": "https://s1.hdslb.com/bfs/live/461be640f60788c1d159ec8d6c5d5cf1ef3d1830.png",
				"award_big_pic": "https://i0.hdslb.com/bfs/live/9e6521c57f24c7149c054d265818d4b82059f2ef.png",
				"award_price": 500
			},
			"31214": {
				"award_type": 1,
				"award_name": "牛哇",
				"award_pic": "https://s1.hdslb.com/bfs/live/91ac8e35dd93a7196325f1e2052356e71d135afb.png",
				"award_big_pic": "https://i0.hdslb.com/bfs/live/3b74c117b4f265edcea261bc5608a58d3a7c300a.png",
				"award_price": 100
			},
			"31216": {
				"award_type": 1,
				"award_name": "i了i了",
				"award_pic": "https://s1.hdslb.com/bfs/live/1157a445487b39c0b7368d91b22290c60fa665b2.png",
				"award_big_pic": "https://i0.hdslb.com/bfs/live/cfb9c3d9bdd2c25c95b7d859ebaa590ca9362adb.png",
				"award_price": 100
			}
		},
		"version": 1
	}
}
```

</details>
