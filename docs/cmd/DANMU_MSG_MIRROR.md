# 跨房弹幕 (DANMU_MSG_MIRROR)

数据结构与 [普通弹幕 (DANMU_MSG)](DANMU_MSG.md) 相同。

## 下发条件

特定情况在相关直播间下发，通常是某些活动。

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "DANMU_MSG_MIRROR",
	"dm_v2": "",
	"info": [
		[
			0,
			1,
			25,
			16777215,
			1765714387241,
			849855473,
			0,
			"8f121833",
			0,
			0,
			0,
			"",
			0,
			"{}",
			"{}",
			{
				"extra": "{\"send_from_me\":false,\"master_player_hidden\":false,\"mode\":0,\"color\":16777215,\"dm_type\":0,\"font_size\":25,\"player_mode\":1,\"show_player_type\":0,\"content\":\"关闭跨房弹幕\",\"user_hash\":\"2400327731\",\"emoticon_unique\":\"\",\"bulge_display\":0,\"recommend_score\":9,\"main_state_dm_color\":\"\",\"objective_state_dm_color\":\"\",\"direction\":0,\"pk_direction\":0,\"quartet_direction\":0,\"anniversary_crowd\":0,\"yeah_space_type\":\"\",\"yeah_space_url\":\"\",\"jump_to_url\":\"\",\"space_type\":\"\",\"space_url\":\"\",\"animation\":{},\"emots\":null,\"is_audited\":false,\"id_str\":\"38419d87819cfb833e2a7b61f8693ea9844\",\"icon\":null,\"show_reply\":true,\"reply_mid\":0,\"reply_uname\":\"\",\"reply_uname_color\":\"\",\"reply_is_mystery\":false,\"reply_type_enum\":0,\"hit_combo\":0,\"esports_jump_url\":\"\",\"is_mirror\":true,\"is_collaboration_member\":false}",
				"mode": 0,
				"show_player_type": 0,
				"user": {
					"base": {
						"face": "https://i2.hdslb.com/bfs/face/68f8c1276eb6487df20fe3c00ffa43a4dafccda5.jpg",
						"is_mystery": false,
						"name": "黑手派",
						"name_color": 0,
						"name_color_str": "",
						"official_info": {
							"desc": "",
							"role": 0,
							"title": "",
							"type": -1
						},
						"origin_info": {
							"face": "https://i2.hdslb.com/bfs/face/68f8c1276eb6487df20fe3c00ffa43a4dafccda5.jpg",
							"name": "黑手派"
						},
						"risk_ctrl_info": null
					},
					"guard": null,
					"guard_leader": {
						"is_guard_leader": false
					},
					"medal": null,
					"title": {
						"old_title_css_id": "",
						"title_css_id": ""
					},
					"uhead_frame": null,
					"uid": 1259043854,
					"wealth": null
				}
			},
			{
				"activity_identity": "",
				"activity_source": 0,
				"not_show": 0
			},
			0
		],
		"关闭跨房弹幕",
		[
			1259043854,
			"黑手派",
			0,
			0,
			0,
			10000,
			1,
			""
		],
		[],
		[
			0,
			0,
			9868950,
			">50000",
			0
		],
		[
			"",
			""
		],
		0,
		0,
		null,
		{
			"ct": "330442D6",
			"ts": 1765714387
		},
		0,
		0,
		null,
		null,
		0,
		39,
		[
			0
		],
		null
	]
}
```

</details>
