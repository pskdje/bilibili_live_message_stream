# 醒目留言日语 (SUPER_CHAT_MESSAGE_JPN)

基本同 [醒目留言 (SUPER_CHAT_MESSAGE)](SUPER_CHAT_MESSAGE.md)，但多了 `message_jpn` 字段。

## 下发条件

*未知*

## JSON消息

*其余字段参见 [醒目留言 (SUPER_CHAT_MESSAGE)](SUPER_CHAT_MESSAGE.md)

`data` 对象:

| 字段 | 类型  | 内容 | 备注    |
| ---- | ----- | ----- | ------- |
| message_jpn | str | sc内容日语机翻 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "SUPER_CHAT_MESSAGE_JPN",
	"data": {
		"id": "3790747",
		"uid": "394060741",
		"price": 30,
		"rate": 1000,
		"message": "棉花！！转盘中了武器后，上号30抽3武器，救命！！！",
		"message_jpn": "",
		"is_ranked": 1,
		"background_image": "https://i0.hdslb.com/bfs/live/a712efa5c6ebc67bafbe8352d3e74b820a00c13e.png",
		"background_color": "#EDF5FF",
		"background_icon": "",
		"background_price_color": "#7497CD",
		"background_bottom_color": "#2A60B2",
		"ts": 1650363318,
		"token": "24655ABF",
		"medal_info": {
			"icon_id": 0,
			"target_id": 1871001,
			"special": "",
			"anchor_uname": "棉花大哥哥",
			"anchor_roomid": 103,
			"medal_level": 24,
			"medal_name": "棉花花",
			"medal_color": "#1a544b"
		},
		"user_info": {
			"uname": "改了名真的能中吗",
			"face": "http://i1.hdslb.com/bfs/face/e2391f132cd981fb70468a8ce9418513e959eb10.jpg",
			"face_frame": "https://i0.hdslb.com/bfs/live/80f732943cc3367029df65e267960d56736a82ee.png",
			"guard_level": 3,
			"user_level": 11,
			"level_color": "#61c05a",
			"is_vip": 0,
			"is_svip": 0,
			"is_main_vip": 1,
			"title": "0",
			"manager": 0
		},
		"time": 60,
		"start_time": 1650363318,
		"end_time": 1650363378,
		"gift": {
			"num": 1,
			"gift_id": 12000,
			"gift_name": "醒目留言"
		}
	},
	"roomid": "34348"
}
```

</details>
