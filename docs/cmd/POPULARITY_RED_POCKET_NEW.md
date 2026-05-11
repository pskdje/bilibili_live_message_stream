# 直播间新红包 (POPULARITY_RED_POCKET_NEW)

注: 与 [直播间发红包弹幕](POPULARITY_RED_POCKET_START.md) 不同，那个是发红包的弹幕信息，这个则和 [送礼](SEND_GIFT.md) 的信息相似，但也有前者的一些字段。

## 下发条件

要发新红包。

## JSON消息

根对象:

| 字段 | 类型 | 内容                        | 备注 |
| ---- | ---- | --------------------------- | ---- |
| cmd  | str  | `POPULARITY_RED_POCKET_NEW` |      |
| data | obj  | 信息本体                    |      |

`data` 对象:

| 字段         | 类型 | 内容         | 备注 |
| ------------ | ---- | ------------ | ---- |
| lot_id       | num  | 红包 ID      |      |
| start_time   | num  | 开抢时间     | UNIX 秒级时间戳 |
| current_time | num  | 当前时间     | UNIX 秒级时间戳 |
| wait_num     | num  | 0?           |      |
| uname        | str  | 发送者用户名 |      |
| uid          | num  | 发送者的 mid |      |
| action       | str  | 礼物操作     |      |
| num          | num  | 礼物数量     |      |
| gift_name    | str  | `红包`       |      |
| gift_id      | num  | 礼物 ID?     |      |
| price        | num  | 电池标价     |      |
| name_color   | str  | 用户名颜色   |      |
| medal_info   | obj  | 发送者粉丝牌 |      |

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "POPULARITY_RED_POCKET_NEW",
	"data": {
		"lot_id": 2062329,
		"start_time": 1650425343,
		"current_time": 1650425343,
		"wait_num": 0,
		"uname": "毒瘤老肥仔",
		"uid": 181851309,
		"action": "送出",
		"num": 1,
		"gift_name": "红包",
		"gift_id": 13000,
		"price": 20,
		"name_color": "#00D1F1",
		"medal_info": {
			"target_id": 11909915,
			"special": "",
			"icon_id": 0,
			"anchor_uname": "",
			"anchor_roomid": 0,
			"medal_level": 22,
			"medal_name": "伊克拉",
			"medal_color": 1725515,
			"medal_color_start": 1725515,
			"medal_color_end": 5414290,
			"medal_color_border": 6809855,
			"is_lighted": 1,
			"guard_level": 3
		}
	}
}
```

</details>
