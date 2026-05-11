# 用户进场特效 (ENTRY_EFFECT)

## 下发条件

有进场特效的用户进入直播间时。

## JSON消息

根对象:

| 字段 | 类型 | 内容           | 备注 |
| ---- | ---- | -------------- | ---- |
| cmd  | str  | `ENTRY_EFFECT` |      |
| data | obj  | 信息本体       |      |

`data` 对象:

| 字段                    | 类型  | 内容             | 备注 |
| ----------------------- | ----- | ---------------- | ---- |
| id                      | num   | ?                |      |
| uid                     | num   | 进场用户 mid     |      |
| target_id               | num   | 主播 mid?        |      |
| mock_effect             | num   | ?                |      |
| face                    | str   | 进场用户头像 URL |      |
| privilege_type          | num   | ?                |      |
| copy_writing            | str   | 进场欢迎文本     |      |
| copy_color              | str   | 进场欢迎文本颜色 | 16 进制 |
| highlight_color         | str   | 高亮颜色?        | 16 进制 |
| priority                | num   | 优先级?          |      |
| basemap_url             | str   | 进场特效背景 URL | APP 端 |
| show_avatar             | num   | 是否显示用户头像 | 1: 显示<br/>0: 不显示 |
| effective_time          | num   | ?                |      |
| web_basemap_url         | str   | 进场特效背景 URL | 网页端 |
| web_effective_time      | num   | 进场特效生存时间 | 网页端 |
| web_effect_close        | num   | ?                |      |
| web_close_time          | num   | ?                |      |
| business                | num   | ?                |      |
| copy_writing_v2         | str   | 进场欢迎文本     | APP 端? |
| icon_list               | array | 空?              |      |
| max_delay_time          | num   | 最大等待时间?    |      |
| trigger_time            | num   | 触发时间戳       | UNIX 纳秒时间戳 |
| identities              | num   | 标识符?          |      |
| effect_silent_time      | num   | ?                |      |
| effective_time_new      | num   | ?                |      |
| web_dynamic_url_webp    | str   | ?                |      |
| web_dynamic_url_apng    | str   | ?                |      |
| mobile_dynamic_url_webp | str   | ?                |      |
| wealthy_info            | obj   | 荣耀等级信息       |      |
| new_style               | num   | ?                |      |
| is_mystery              | bool  | ?                |      |
| uinfo                   | obj   | 用户信息          |      |
| full_cartoon_id         | num   | ?                |      |
| priority_level          | num   | ?                |      |
| wealth_style_info       | obj   | 荣耀等级样式信息    |      |

## 示例

<details>
<summary>查看消息示例：</summary>

```json
{
	"cmd": "ENTRY_EFFECT",
	"data": {
		"id": 380,
		"uid": 31382283,
		"target_id": 12892411,
		"mock_effect": 0,
		"face": "https://i0.hdslb.com/bfs/face/876e30e89faa5672858cc17bdb357362ec96bc29.jpg",
		"privilege_type": 0,
		"copy_writing": "<%WYCBat%> 来了",
		"copy_color": "#F7F7F7",
		"highlight_color": "#FFFFFF",
		"priority": 1,
		"basemap_url": "",
		"show_avatar": 0,
		"effective_time": 0,
		"web_basemap_url": "https://i0.hdslb.com/bfs/live/mlive/19e7564ed9d466b02f341abfa979c6e38c2ffffb.png",
		"web_effective_time": 4,
		"web_effect_close": 1,
		"web_close_time": 900,
		"business": 6,
		"copy_writing_v2": "<%WYCBat%> 来了",
		"icon_list": [],
		"max_delay_time": 7,
		"trigger_time": 1748545763327647435,
		"identities": 1,
		"effect_silent_time": 0,
		"effective_time_new": 0,
		"web_dynamic_url_webp": "",
		"web_dynamic_url_apng": "",
		"mobile_dynamic_url_webp": "",
		"wealthy_info": {
			"uid": 0,
			"level": 17,
			"level_total_score": 0,
			"cur_score": 0,
			"upgrade_need_score": 0,
			"status": 0,
			"dm_icon_key": ""
		},
		"new_style": 1,
		"is_mystery": false,
		"uinfo": {
			"uid": 31382283,
			"base": {
				"name": "WYCBat",
				"face": "https://i0.hdslb.com/bfs/face/876e30e89faa5672858cc17bdb357362ec96bc29.jpg",
				"name_color": 0,
				"is_mystery": false,
				"risk_ctrl_info": null,
				"origin_info": null,
				"official_info": null,
				"name_color_str": ""
			},
			"medal": null,
			"wealth": {
				"level": 17,
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
		"full_cartoon_id": 1802,
		"priority_level": 0,
		"wealth_style_info": {
			"url": "https://i0.hdslb.com/bfs/live/b6f2bf3e27f22b3039594842f0005b05a0dc5dae.png"
		}
	}
}
```

</details>
