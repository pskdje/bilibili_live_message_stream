# 醒目留言 (SUPER_CHAT_MESSAGE)

## 下发条件

有人购买任意醒目留言后。

## JSON消息

根对象:

| 字段   | 类型 | 内容                  | 备注 |
| ------ | ---- | --------------------- | ---- |
| cmd    | str  | `SUPER_CHAT_MESSAGE`  |      |
| data   | obj  | 信息本体              |      |
| roomid | num  | 直播间房间号 (非短号) |      |

`data` 对象:

| 字段 | 类型  | 内容 | 备注    |
| ---- | ----- | ----- | ------- |
| background_bottom_color | str | 待调查 |  |
| background_color | str | 待调查 |  |
| background_color_end | str | 待调查 |  |
| background_color_start | str | 待调查 |  |
| background_icon | str | 待调查 |  |
| background_image | str | 待调查 |  |
| background_price_color | str | 待调查 |  |
| color_point | num | 待调查 |  |
| dmscore | num | 待调查 |  |
| end_time | num | 待调查 |  |
| gift | obj | 礼物信息 |  |
| id | num | 醒目留言 ID |  |
| is_ranked | num | 待调查 |  |
| is_send_audit | num | 待调查 |  |
| medal_info | obj | SC发送用户佩戴的粉丝牌信息 |  |
| message | str | sc内容 |  |
| message_font_color | str | SC文本颜色 |  |
| message_trans | str | 机翻sc内容 |  |
| price | num | sc金额 | 为 CNY 价值 |
| rate | num | 待调查 |  |
| start_time | num | 待调查 |  |
| time | num | sc持续时间 |  |
| token | num | 待调查 |  |
| trans_mark | num | 待调查 |  |
| ts | num | 待调查 |  |
| uid | num | 发送用户uid |  |
| user_info | obj | 发送用户信息 |  |

`data.gift` 对象:

| 字段 | 类型  | 内容 | 备注   |
| ---- | ---- | ---- | ---- |
| gift_id | num | 礼物id |      |
| gift_name | str | 礼物名称 | 一般均为"醒目留言" |
| num | num | 数量   |      |

`data.medal_info` 对象:

| 字段 | 类型  | 内容  | 备注   |
| ---- | ---- | ----- | ------ |
| anchor_roomid | num | 房间号         | 包含短号 |
| anchor_uname | str | 主播昵称        |  |
| guard_level | num | 大航海等级       | 1: 总督<br/>2: 提督<br />3: 舰长 |
| icon_id | num | 待调查         |  |
| is_lighted | num | 待调查         |  |
| medal_color | str | 待调查         |  |
| medal_color_border | num | 待调查         |  |
| medal_color_end | num | 待调查         |  |
| medal_color_start | num | 待调查         |  |
| medal_level | num | 粉丝牌等级       |  |
| medal_name | str | 粉丝牌名称       |  |
| special | str | 待调查         |  |
| target_id | num | 粉丝牌对应的主播mid |  |

`data.user_info` 对象:

| 字段 | 类型  | 内容    | 备注   |
| ---- | --- | ----- | ---- |
| face | num | 用户头像  |  |
| face_frame | num | 头像边框  |  |
| guard_level | num | 大航海等级 | 1: 总督<br />2: 提督<br />3: 舰长 |
| is_main_vip | num | 待调查   |  |
| is_svip | num | 待调查   |  |
| is_vip | num | 待调查   |  |
| level_color | str | 待调查   |  |
| manager | num | 待调查   |  |
| name_color | str | 待调查   |  |
| title | str | 待调查   |  |
| uname | str | 用户名称  |  |
| user_level | num | 待调查   |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "SUPER_CHAT_MESSAGE",
	"data": {
		"background_bottom_color": "#2A60B2",
		"background_color": "#EDF5FF",
		"background_color_end": "#405D85",
		"background_color_start": "#3171D2",
		"background_icon": "",
		"background_image": "https://i0.hdslb.com/bfs/live/a712efa5c6ebc67bafbe8352d3e74b820a00c13e.png",
		"background_price_color": "#7497CD",
		"color_point": 0.7,
		"dmscore": 120,
		"end_time": 1677069095,
		"gift": {
			"gift_id": 12000,
			"gift_name": "醒目留言",
			"num": 1
		},
		"id": 6522809,
		"is_ranked": 1,
		"is_send_audit": 0,
		"medal_info": {
			"anchor_roomid": 732,
			"anchor_uname": "Asaki大人",
			"guard_level": 3,
			"icon_id": 0,
			"is_lighted": 1,
			"medal_color": "#1a544b",
			"medal_color_border": 6809855,
			"medal_color_end": 5414290,
			"medal_color_start": 1725515,
			"medal_level": 21,
			"medal_name": "ASAKI",
			"special": "",
			"target_id": 194484313
		},
		"message": "猪播完美预测自己第一个死，这就是鹅鸭杀高玩吗",
		"message_font_color": "#A3F6FF",
		"message_trans": "",
		"price": 30,
		"rate": 1000,
		"start_time": 1677069035,
		"time": 60,
		"token": "7BED5681",
		"trans_mark": 0,
		"ts": 1677069035,
		"uid": 294094150,
		"user_info": {
			"face": "https://i1.hdslb.com/bfs/face/7a11b48e0a3055e220fa8b4c7d938cd4bcac2577.jpg",
			"face_frame": "https://i0.hdslb.com/bfs/live/80f732943cc3367029df65e267960d56736a82ee.png",
			"guard_level": 3,
			"is_main_vip": 1,
			"is_svip": 0,
			"is_vip": 0,
			"level_color": "#969696",
			"manager": 0,
			"name_color": "#00D1F1",
			"title": "0",
			"uname": "界原虚",
			"user_level": 6
		}
	},
	"roomid": 6154037
}
```

</details>
