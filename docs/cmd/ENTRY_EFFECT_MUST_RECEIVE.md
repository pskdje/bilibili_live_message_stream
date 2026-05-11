# 必须接受的用户进场特效 (ENTRY_EFFECT_MUST_RECEIVE)

## 下发条件

在部分主播进入自己的直播间时下发。

## JSON消息

结构与 [用户进场特效 (ENTRY_EFFECT)](ENTRY_EFFECT.md) 完全相同。

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "ENTRY_EFFECT_MUST_RECEIVE",
	"data": {
		"id": 135,
		"uid": 438160221,
		"target_id": 438160221,
		"mock_effect": 0,
		"face": "https://i0.hdslb.com/bfs/face/member/noface.jpg",
		"privilege_type": 0,
		"copy_writing": "<%weatfe%> 来了",
		"copy_color": "#000000",
		"highlight_color": "#FFF100",
		"priority": 1,
		"basemap_url": "https://i0.hdslb.com/bfs/live/mlive/da6933ea70f31c4df63f4b68b735891284888357.png",
		"show_avatar": 1,
		"effective_time": 1,
		"web_basemap_url": "https://i0.hdslb.com/bfs/live/mlive/da6933ea70f31c4df63f4b68b735891284888357.png",
		"web_effective_time": 2,
		"web_effect_close": 0,
		"web_close_time": 900,
		"business": 3,
		"copy_writing_v2": "<%weatfe%> 来了",
		"icon_list": [],
		"max_delay_time": 7,
		"trigger_time": 1746031259272981482,
		"identities": 1,
		"effect_silent_time": 0,
		"effective_time_new": 0,
		"web_dynamic_url_webp": "",
		"web_dynamic_url_apng": "",
		"mobile_dynamic_url_webp": "",
		"wealthy_info": null,
		"new_style": 0,
		"is_mystery": false,
		"uinfo": {
			"uid": 438160221,
			"base": {
				"name": "weatfe",
				"face": "https://i0.hdslb.com/bfs/face/member/noface.jpg",
				"name_color": 0,
				"is_mystery": false,
				"risk_ctrl_info": null,
				"origin_info": null,
				"official_info": null,
				"name_color_str": ""
			},
			"medal": {
				"name": "粉丝团",
				"level": 11,
				"color_start": 9272486,
				"color_end": 9272486,
				"color_border": 9272486,
				"color": 9272486,
				"id": 2956282,
				"typ": 0,
				"is_light": 1,
				"ruid": 438160221,
				"guard_level": 0,
				"score": 16000,
				"guard_icon": "",
				"honor_icon": "",
				"v2_medal_color_start": "#596FE099",
				"v2_medal_color_end": "#596FE099",
				"v2_medal_color_border": "#596FE099",
				"v2_medal_color_text": "#FFFFFFFF",
				"v2_medal_color_level": "#000B7099",
				"user_receive_count": 0
			},
			"wealth": {
				"level": 5,
				"dm_icon_key": ""
			},
			"title": null,
			"guard": {
				"level": 0,
				"expired_str": ""
			},
			"uhead_frame": null,
			"guard_leader": null
		},
		"full_cartoon_id": 0,
		"priority_level": 0,
		"wealth_style_info": {
			"url": "https://i0.hdslb.com/bfs/live/24f6ef867c3905064136f5c4e33a8d423d41ebdd.png"
		}
	}
}
```

</details>
