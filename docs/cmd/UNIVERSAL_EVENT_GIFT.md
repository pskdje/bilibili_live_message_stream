# 连线礼物信息 (UNIVERSAL_EVENT_GIFT)

## 下发条件

多人同屏连线时多次下发。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `UNIVERSAL_EVENT_GIFT` |  |
| data | obj | 信息本体 |  |
| msg_id | str |  |  |
| p_is_ack | bool |  |  |
| p_msg_type | num |  |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| anchor_uid | num | 主播uid |  |
| info | obj | 连线信息 |  |
| room_id | num | 直播间id |  |

`data.info` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| biz_session_id | str | 连线会话id? |  |
| business_label | str |  |  |
| interact_channel_id | str | 频道id? |  |
| interact_connect_type | num |  |  |
| interact_max_users | num | 最大连线数? |  |
| interact_mode | obj |  |  |
| interact_template | obj | 展示模板 |  |
| invoking_time | num |  |  |
| members | arr | 连线成员 | 参见 `UNIVERSAL_EVENT_GIFT_V2` 的 `data.members` ，缺少部分字段 |
| members_version | num |  |  |
| multi_conn_info | obj | 连线信息 |  |
| room_owner | num | 发起者uid |  |
| room_start_at | str |  |  |
| room_start_at_ts | num |  |  |
| room_status | num |  |  |
| session_start_at | str |  |  |
| session_start_at_ts | num |  |  |
| session_status | num |  |  |
| system_time_unix | num | 服务器时间戳 | Unix 秒时间戳 |
| trace_id | str |  |  |
| version | num | 数据版本 | Unix 毫秒时间戳 |

`data.info.interact_mode` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| apply_timeout | num | 超时? |  |
| interact_mode_type | num |  |  |
| invite_timeout | num | 邀请超时? |  |
| join_types | arr | 加入类型? | 数字数组 |
| position_mode | num |  |  |

`data.info.interact_template` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| is_variable_layout | bool | 布局是否可变? |  |
| layout_data | obj | 布局信息 |  |
| layout_id | str | 布局id |  |
| layout_list | null | ? |  |
| show_interact_ui | bool | 显示交互UI? |  |
| template_id | str | 模板id? |  |

`data.info.interact_template.layout_data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| best_area_show_pos | num |  |  |
| cells | arr | 具体布局信息 |  |
| default_cell | obj |  |  |
| height | num |  |  |
| rtc_resolution | obj |  |  |
| width | num |  |  |

`data.info.interact_template.layout_data.cells` 数组中对象:

与 `data.info.interact_template.layout_data.default_cell` 对象相同

`data.info.interact_template.layout_data.default_cell` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| can_zoom | num |  |  |
| default_open | num |  |  |
| height | num |  |  |
| mobile_avatar_size | num |  |  |
| mobile_font_size | num |  |  |
| pc_web_avatar_size | num |  |  |
| pc_web_font_size | num |  |  |
| position | num | 定位? |  |
| width | num |  |  |
| x | num |  |  |
| y | num |  |  |
| z_index | num |  |  |

`data.info.interact_template.layout_data.rtc_resolution` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| code_rate_init | num |  |  |
| code_rate_max | num |  |  |
| code_rate_min | num |  |  |
| horizontal_height | num |  |  |
| horizontal_width | num |  |  |
| vertical_height | num |  |  |
| vertical_width | num |  |  |

`data.info.members` 数组中对象:

参见 [`UNIVERSAL_EVENT_GIFT_V2`](#连线礼物信息v2-universal_event_gift_v2) 的 `data.members` 数组中对象，本cmd缺少部分字段。

`data.info.multi_conn_info` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| room_owner | num | 发起人uid |  |
| scores | arr | 礼物信息 |  |
| show_score | num | 是否显示? |  |

`data.info.multi_conn_info.scores` 数组中对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| price | num | 礼物累计价值 | CNY × 100 |
| price_text | str | 礼物累计价值文本 |  |
| uid | num | 对应主播uid |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "UNIVERSAL_EVENT_GIFT",
	"data": {
		"anchor_uid": 1950658,
		"info": {
			"biz_session_id": "17545643420522077733317",
			"business_label": "universal_multi_conn",
			"interact_channel_id": "4679025140177408",
			"interact_connect_type": 0,
			"interact_max_users": 9,
			"interact_mode": {
				"apply_timeout": 20,
				"interact_mode_type": 0,
				"invite_timeout": 30,
				"join_types": [
					1,
					2
				],
				"position_mode": 0
			},
			"interact_template": {
				"is_variable_layout": true,
				"layout_data": {
					"best_area_show_pos": 0,
					"cells": [
						{
							"can_zoom": 2,
							"default_open": 0,
							"height": 48,
							"mobile_avatar_size": 64,
							"mobile_font_size": 0,
							"pc_web_avatar_size": 112,
							"pc_web_font_size": 0,
							"position": 0,
							"width": 30,
							"x": 0,
							"y": 0,
							"z_index": 0
						},
						{
							"can_zoom": 1,
							"default_open": 0,
							"height": 0,
							"mobile_avatar_size": 0,
							"mobile_font_size": 0,
							"pc_web_avatar_size": 0,
							"pc_web_font_size": 0,
							"position": 1,
							"width": 0,
							"x": 30,
							"y": 0,
							"z_index": 0
						},
						{
							"can_zoom": 1,
							"default_open": 0,
							"height": 0,
							"mobile_avatar_size": 0,
							"mobile_font_size": 0,
							"pc_web_avatar_size": 0,
							"pc_web_font_size": 0,
							"position": 2,
							"width": 0,
							"x": 45,
							"y": 0,
							"z_index": 0
						},
						{
							"can_zoom": 1,
							"default_open": 0,
							"height": 0,
							"mobile_avatar_size": 0,
							"mobile_font_size": 0,
							"pc_web_avatar_size": 0,
							"pc_web_font_size": 0,
							"position": 3,
							"width": 0,
							"x": 30,
							"y": 16,
							"z_index": 0
						},
						{
							"can_zoom": 1,
							"default_open": 0,
							"height": 0,
							"mobile_avatar_size": 0,
							"mobile_font_size": 0,
							"pc_web_avatar_size": 0,
							"pc_web_font_size": 0,
							"position": 4,
							"width": 0,
							"x": 45,
							"y": 16,
							"z_index": 0
						},
						{
							"can_zoom": 1,
							"default_open": 0,
							"height": 0,
							"mobile_avatar_size": 0,
							"mobile_font_size": 0,
							"pc_web_avatar_size": 0,
							"pc_web_font_size": 0,
							"position": 5,
							"width": 0,
							"x": 30,
							"y": 32,
							"z_index": 0
						},
						{
							"can_zoom": 1,
							"default_open": 0,
							"height": 0,
							"mobile_avatar_size": 0,
							"mobile_font_size": 0,
							"pc_web_avatar_size": 0,
							"pc_web_font_size": 0,
							"position": 6,
							"width": 0,
							"x": 45,
							"y": 32,
							"z_index": 0
						}
					],
					"default_cell": {
						"can_zoom": 0,
						"default_open": 1,
						"height": 16,
						"mobile_avatar_size": 40,
						"mobile_font_size": 10,
						"pc_web_avatar_size": 72,
						"pc_web_font_size": 14,
						"position": 0,
						"width": 15,
						"x": 0,
						"y": 0,
						"z_index": 0
					},
					"height": 48,
					"rtc_resolution": {
						"code_rate_init": 500,
						"code_rate_max": 700,
						"code_rate_min": 375,
						"horizontal_height": 400,
						"horizontal_width": 500,
						"vertical_height": 576,
						"vertical_width": 360
					},
					"width": 60
				},
				"layout_id": "left1_right6",
				"layout_list": null,
				"show_interact_ui": true,
				"template_id": "multi_conn_grid"
			},
			"invoking_time": 1,
			"members": [
				{
					"face": "https://i1.hdslb.com/bfs/face/2ddb513f600c203f21aefb9725ab0eb84f093943.jpg",
					"gender": 0,
					"join_time": 1754564992,
					"link_id": "44479117",
					"position": 0,
					"room_id": 41682,
					"uid": 1950658,
					"uname": "早稻叽"
				},
				{
					"face": "https://i1.hdslb.com/bfs/face/5958bb6814f25d832775ca37043d38f893b4a478.jpg",
					"gender": -1,
					"join_time": 1754564347,
					"link_id": "44478459",
					"position": 1,
					"room_id": 26376408,
					"uid": 2077733317,
					"uname": "烛不遥"
				},
				{
					"face": "https://i0.hdslb.com/bfs/face/7c862b4ad1a29cdd2b849bcea3c3812b67770d21.jpg",
					"gender": 0,
					"join_time": 1754564347,
					"link_id": "44478460",
					"position": 2,
					"room_id": 1774970222,
					"uid": 1035559935,
					"uname": "新砂Athia"
				},
				{
					"face": "https://i0.hdslb.com/bfs/face/81c1f45b45958c19523bb7cbae7fc3fa99b4aae1.jpg",
					"gender": -1,
					"join_time": 1754564361,
					"link_id": "44478500",
					"position": 3,
					"room_id": 31361500,
					"uid": 3546581471070432,
					"uname": "颂温暖_Swanna"
				},
				{
					"face": "https://i2.hdslb.com/bfs/face/eceb8fa58c41b7cd733bebafcd7c1f3e33b37b07.jpg",
					"gender": 0,
					"join_time": 1754564385,
					"link_id": "44478528",
					"position": 4,
					"room_id": 1937830041,
					"uid": 3546768203582225,
					"uname": "暴躁小辣jo"
				},
				{
					"face": "https://i0.hdslb.com/bfs/face/12c1cd0df2ee6e6bb09b279b0553cdc9ae4af4f0.jpg",
					"gender": -1,
					"join_time": 1754564774,
					"link_id": "44478875",
					"position": 5,
					"room_id": 23090250,
					"uid": 475912512,
					"uname": "抵抗Resistance"
				}
			],
			"members_version": 3974722551,
			"multi_conn_info": {
				"room_owner": 2077733317,
				"scores": [
					{
						"price": 82900,
						"price_text": "829",
						"uid": 1950658
					},
					{
						"price": 21200,
						"price_text": "212",
						"uid": 2077733317
					},
					{
						"price": 30400,
						"price_text": "304",
						"uid": 1035559935
					},
					{
						"price": 675600,
						"price_text": "6756",
						"uid": 3546581471070432
					},
					{
						"price": 96800,
						"price_text": "968",
						"uid": 3546768203582225
					},
					{
						"price": 79200,
						"price_text": "792",
						"uid": 475912512
					}
				],
				"show_score": 1
			},
			"room_owner": 2077733317,
			"room_start_at": "",
			"room_start_at_ts": 0,
			"room_status": 1,
			"session_start_at": "",
			"session_start_at_ts": 0,
			"session_status": 1,
			"system_time_unix": 1754568295,
			"trace_id": "",
			"version": 1754568295428
		},
		"room_id": 41682
	},
	"msg_id": "34610565842749442:1000:1000",
	"p_is_ack": true,
	"p_msg_type": 1,
	"send_time": 1754568295441
}
```

</details>
