# 连线礼物信息V2 (UNIVERSAL_EVENT_GIFT_V2)

## 下发条件

多人同屏连线时多次下发。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `UNIVERSAL_EVENT_GIFT_V2` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| biz_session_id | str | 连线会话id? |  |
| interact_channel_id | str | 频道id? |  |
| interact_template | obj | 交互模板信息 |  |
| members | arr | 连线成员 |  |
| stream_control | null |  |  |
| version | num | 数据版本 | Unix 毫秒时间戳 |
| session_status | num |  |  |
| business_label | str |  |  |
| invoking_time | num |  |  |
| members_version | num |  |  |
| room_status | num |  |  |
| system_time_unix | num | 服务器时间戳 | Unix 秒时间戳 |
| room_owner | num | 发起人uid |  |
| session_start_at | str | 会话开始时间 |  |
| session_start_at_ts | num | 会话经过时间 |  |
| room_start_at | str | 当前直播间加入会话时间 |  |
| room_start_at_ts | num | 当前直播间自加入会话开始经过的时间 |  |
| trace_id | str | 追踪id? |  |
| biz_extra_data | obj |  |  |
| channel_users | arr | 当前连线频道内uid列表 |  |

`data.interact_template` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| template_id | str | 模板id? |  |
| show_interact_ui | bool | 显示交互UI? |  |
| layout_id | str | 样式id? |  |

`data.members` 数组中对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| uid | num | 连线主播uid |  |
| uname | str | 连线主播名称 |  |
| face | str | 连线主播头像 |  |
| position | num | 位置? |  |
| join_time | num | 加入时间 | Unix 秒时间戳 |
| link_id | str |  |  |
| gender | num |  |  |
| room_id | num | 连线主播直播间id |  |
| fans_num | num |  |  |
| display_name | str | 显示名称 |  |
| biz_extra_data | obj |  |  |
| join_time_ts | num |  |  |

`data.members[i].biz_extra_data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| multi_conn | obj |  |  |

`data.members[i].biz_extra_data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| price | num | 礼物累计价值 | CNY × 100 |
| price_text | str | 礼物累计价值文本 |  |

`data.biz_extra_data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| multi_conn | obj |  |  |

`data.biz_extra_data.multi_conn` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| show_score | num |  |  |
| support_full_zoom | num |  |  |

`data.channel_users` 数组:

| 索引 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| 0 | num | 主播uid |  |
| … | num | 主播uid |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "UNIVERSAL_EVENT_GIFT_V2",
	"data": {
		"biz_session_id": "17545643420522077733317",
		"interact_channel_id": "4679025140177408",
		"interact_template": {
			"template_id": "multi_conn_grid",
			"show_interact_ui": true,
			"layout_id": "left1_right6"
		},
		"members": [
			{
				"uid": 1950658,
				"uname": "早稻叽",
				"face": "https://i1.hdslb.com/bfs/face/2ddb513f600c203f21aefb9725ab0eb84f093943.jpg",
				"position": 0,
				"join_time": 1754564992,
				"link_id": "44479117",
				"gender": 0,
				"room_id": 41682,
				"fans_num": 0,
				"display_name": "本房主播",
				"biz_extra_data": {
					"multi_conn": {
						"price": 82900,
						"price_text": "829"
					}
				},
				"join_time_ts": 0
			},
			{
				"uid": 2077733317,
				"uname": "烛不遥",
				"face": "https://i1.hdslb.com/bfs/face/5958bb6814f25d832775ca37043d38f893b4a478.jpg",
				"position": 1,
				"join_time": 1754564347,
				"link_id": "44478459",
				"gender": -1,
				"room_id": 26376408,
				"fans_num": 0,
				"display_name": "烛不遥",
				"biz_extra_data": {
					"multi_conn": {
						"price": 21200,
						"price_text": "212"
					}
				},
				"join_time_ts": 0
			},
			{
				"uid": 1035559935,
				"uname": "新砂Athia",
				"face": "https://i0.hdslb.com/bfs/face/7c862b4ad1a29cdd2b849bcea3c3812b67770d21.jpg",
				"position": 2,
				"join_time": 1754564347,
				"link_id": "44478460",
				"gender": 0,
				"room_id": 1774970222,
				"fans_num": 0,
				"display_name": "新砂Athia",
				"biz_extra_data": {
					"multi_conn": {
						"price": 30400,
						"price_text": "304"
					}
				},
				"join_time_ts": 0
			},
			{
				"uid": 3546581471070432,
				"uname": "颂温暖_Swanna",
				"face": "https://i0.hdslb.com/bfs/face/81c1f45b45958c19523bb7cbae7fc3fa99b4aae1.jpg",
				"position": 3,
				"join_time": 1754564361,
				"link_id": "44478500",
				"gender": -1,
				"room_id": 31361500,
				"fans_num": 0,
				"display_name": "颂温暖_Swanna",
				"biz_extra_data": {
					"multi_conn": {
						"price": 675600,
						"price_text": "6756"
					}
				},
				"join_time_ts": 0
			},
			{
				"uid": 3546768203582225,
				"uname": "暴躁小辣jo",
				"face": "https://i2.hdslb.com/bfs/face/eceb8fa58c41b7cd733bebafcd7c1f3e33b37b07.jpg",
				"position": 4,
				"join_time": 1754564385,
				"link_id": "44478528",
				"gender": 0,
				"room_id": 1937830041,
				"fans_num": 0,
				"display_name": "暴躁小辣jo",
				"biz_extra_data": {
					"multi_conn": {
						"price": 96800,
						"price_text": "968"
					}
				},
				"join_time_ts": 0
			},
			{
				"uid": 475912512,
				"uname": "抵抗Resistance",
				"face": "https://i0.hdslb.com/bfs/face/12c1cd0df2ee6e6bb09b279b0553cdc9ae4af4f0.jpg",
				"position": 5,
				"join_time": 1754564774,
				"link_id": "44478875",
				"gender": -1,
				"room_id": 23090250,
				"fans_num": 0,
				"display_name": "抵抗Resistance",
				"biz_extra_data": {
					"multi_conn": {
						"price": 79200,
						"price_text": "792"
					}
				},
				"join_time_ts": 0
			}
		],
		"stream_control": null,
		"version": 1754568295421,
		"session_status": 1,
		"business_label": "universal_multi_conn",
		"invoking_time": 2,
		"members_version": 1262102210,
		"room_status": 1,
		"system_time_unix": 1754568295,
		"room_owner": 2077733317,
		"session_start_at": "2025-08-07 18:59:06",
		"session_start_at_ts": 3949,
		"room_start_at": "2025-08-07 19:09:52",
		"room_start_at_ts": 3303,
		"trace_id": "55df19c042f09f5c625d7b8b60689496",
		"biz_extra_data": {
			"multi_conn": {
				"show_score": 1,
				"support_full_zoom": 2
			}
		},
		"channel_users": [
			1950658,
			2077733317,
			1035559935,
			3546581471070432,
			3546768203582225,
			475912512
		]
	}
}
```

</details>
