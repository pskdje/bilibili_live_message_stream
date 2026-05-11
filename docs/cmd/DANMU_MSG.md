# 弹幕 (DANMU_MSG)

注: 10 进制转 16 进制若位数不足则在左侧补 `0`

## 下发条件

当有人发送了服务器认为不需要屏蔽的弹幕后下发。

## JSON消息

根对象:

| 字段  | 类型  | 内容        | 备注 |
| ----- | ----- | ----------- | ---- |
| cmd   | str   | `DANMU_MSG` |      |
| dm_v2 | str   | 空串?       |      |
| info  | array | 弹幕信息    | 感谢 ~~[SocialSisterYi/bilibili-API-collect#1084](https://github.com/SocialSisterYi/bilibili-API-collect/issues/1084)~~ 补充 |
| msg_id | str | 弹幕id?      | 极低概率存在 |
| p_is_ack | bool |          | 极低概率存在 |
| p_msg_type | num |         | 极低概率存在 |
| send_time | num | 发送时间戳 | Unix 毫秒时间戳，极低概率存在 |

`info` 数组:

| 项 | 类型  | 内容               | 备注 |
| -- | ----- | ------------------ | ---- |
| 0  | array | 弹幕信息           | 大部分信息可从 `info[0][15].extra` 获取 |
| 1  | str   | 弹幕文本           |      |
| 2  | array | 发送者信息         | 大部分信息可从 `info[0][15].user` 获取  |
| 3  | array | 发送者粉丝勋章信息 | 若无则为空 |
| 4  | array | 发送者UL等级信息   |      |
| 5  | array | ?                  |      |
| 6  | num   | 0?                 |      |
| 7  | num   | 0?                 |      |
| 8  | null  |                    |      |
| 9  | obj   | 发送时间戳         |      |
| 10 | num   | 0?                 |      |
| 11 | num   | 0?                 |      |
| 12 | null  |                    |      |
| 13 | null  |                    |      |
| 14 | num   | 0?                 |      |
| 15 | num   | ?                  |      |
| 16 | array | ?                  |      |

`info[0]` 数组:

| 项 | 类型 | 内容                     | 备注 |
| -- | ---- | ------------------------ | ---- |
| 0  | num  |                          |      |
| 1  | num  | 弹幕模式                 | 弹幕的 mode 字段 |
| 2  | num  | 弹幕字体大小             | 弹幕的 fontsize 字段 |
| 3  | num  | 弹幕颜色                 | 弹幕的 color 字段<br />十六进制颜色值的十进制数字 |
| 4  | num  | 发送时的 UNIX 毫秒时间戳 | 弹幕的 rnd 字段 |
| 5  | num  |                          | 一个负整数 |
| 6  | num  | 0?                       |      |
| 7  | str  | 可能为颜色?              | 一个 16 进制数 |
| 8  | num  | 0?                       |      |
| 9  | num  | 0?                       |      |
| 10 | num  | 0?                       |      |
| 11 | str  | 空串?                    |      |
| 12 | num  | 0?                       |      |
| 13 | str  | 字符串表示的 JSON Object | 空?  |
| 14 | str  | 字符串表示的 JSON Object | 空?  |
| 15 | obj  | 弹幕补充信息             |      |
| 16 | obj  | 活动相关信息?            |      |
| 17 | num  | 0?                       |      |
| 18 | null |                          |      |

`info[0][15]` 对象:

| 字段             | 类型 | 内容         | 备注 |
| ---------------- | ---- | ------------ | ---- |
| extra            | str  | 弹幕信息     | 字符串表示的 JSON |
| mode             | num  | 弹幕模式?    |      |
| show_player_type | num  | 0?           |      |
| user             | obj  | 用户相关信息 |      |

`info[0][15].extra` 表示的对象:

见下方 JSONC

```jsonc
{
	"send_from_me": false,      // 是否由该接收消息的用户发送
	"mode": 0,                  // 弹幕模式 (info[0][1])
	"color": 9920249,           // 弹幕颜色 (info[0][3])
	"dm_type": 0,
	"font_size": 25,            // 弹幕字体大小 (info[0][2])
	"player_mode": 1,
	"show_player_type": 0,
	"content": "白花300块[热]", // 弹幕文本 (info[1])
	"user_hash": "197700816",
	"emoticon_unique": "",
	"bulge_display": 0,
	"recommend_score": 3,
	"main_state_dm_color": "",
	"objective_state_dm_color": "",
	"direction": 0,             // 弹幕方向?
	"pk_direction": 0,
	"quartet_direction": 0,
	"anniversary_crowd": 0,
	"yeah_space_type": "",
	"yeah_space_url": "",
	"jump_to_url": "",
	"space_type": "",
	"space_url": "",
	"animation": {},
	"emots": {                  // 表情相关信息 (用于文本替换)
		"[热]": {
			"count": 1,
			"descript": "[热]",
			"emoji": "[热]",
			"emoticon_id": 278,
			"emoticon_unique": "emoji_278",
			"height": 20,
			"url": "http://i0.hdslb.com/bfs/live/6df760280b17a6cbac8c1874d357298f982ba4cf.png",
			"width": 20
		}
	},
	"is_audited": false,
	"id_str": "364b06e3c561af3d5921f1253d66c1d575",
	"icon": {
		"prefix": {
			"type": 1,
			"resource": "ChronosWealth_4.png"
		}
	},
	"show_reply": true,         // 显示回复?
	"reply_mid": 0,
	"reply_uname": "",
	"reply_uname_color": "",
	"reply_is_mystery": false,
	"hit_combo": 0
}
```

`info[0][15].user` 对象:

| 字段         | 类型 | 内容       | 备注 |
| ------------ | ---- | ---------- | ---- |
| base         | obj  | 基本信息   |      |
| guard        | null |            |      |
| guard_leader | obj  | ?          |      |
| medal        | obj  | 粉丝牌信息 | 参见 ~~[指定用户的所有粉丝勋章信息](https://github.com/pskdje/bilibili-API-collect/blob/main/docs/user/medals.md#指定用户的所有粉丝勋章信息)~~ `data.list[n].uinfo_medal` |
| title        | obj  | ?          |      |
| uhead_frame  | null |            |      |
| uid          | num  | 发送者 mid |      |
| wealth       | null |            |      |

`info[0][15].user.base` 对象:

| 字段           | 类型 | 内容             | 备注    |
| -------------- | ---- | ---------------- | ------- |
| face           | str  | 发送者头像 URL   |         |
| is_mystery     | bool | 是否是神秘用户?  |         |
| name           | str  | 发送者用户名     |         |
| name_color     | num  | 用户名颜色       | 10 进制 |
| name_color_str | num  | 字符串表示的颜色 |         |
| offical_info   | obj  | 认证信息         | 参见 ~~[用户空间详细信息](https://github.com/pskdje/bilibili-API-collect/blob/main/docs/user/info.md#用户空间详细信息)~~ `data.official` |
| origin_info    | obj  | 同 `face` `name` |         |
| risk_ctrl_info | null |                  |         |

`info[0][15].user.title` 对象:

| 字段             | 类型 | 内容  | 备注 |
| ---------------- | ---- | ----- | ---- |
| old_title_css_id | str  | 空串? |      |
| title_css_id     | str  | 空串? |      |

`info[0][16]` 对象:

| 字段              | 类型 | 内容  | 备注 |
| ----------------- | ---- | ----- | ---- |
| activity_identity | str  | 空串? |      |
| activity_source   | num  | 0?    |      |
| not_show          | num  | 0?    |      |

`info[2]` 数组:

| 项 | 类型 | 内容          | 备注 |
| -- | ---- | ------------- | ---- |
| 0  | num  | 发送者 mid    | 同 `info[0][15].user.uid` |
| 1  | str  | 发送者用户名  | 同 `info[0][15].user.base.name` |
| 2  | num  | 0?            |      |
| 3  | num  | 0?            |      |
| 4  | num  | 0?            |      |
| 5  | num  | 用户权限等级? | 参见 ~~[用户空间详细信息](https://github.com/pskdje/bilibili-API-collect/blob/main/docs/user/info.md#用户空间详细信息)~~ `data.rank` |
| 6  | num  | ?             |      |

`info[3]` 数组:

| 项 | 类型 | 内容                                     | 备注 |
| -- | ---- | ---------------------------------------- | ---- |
| 0  | num  | 同 `info[0][15].user.medal.level`        |      |
| 1  | str  | 同 `info[0][15].user.medal.name`         |      |
| 2  | str  | 粉丝牌创建主播名称                       |      |
| 3  | num  | ?                                        |      |
| 4  | num  | 同 `info[0][15].user.medal.color`        |      |
| 5  | str  | 空串?                                    |      |
| 6  | num  | 0?                                       |      |
| 7  | num  | 同 `info[0][15].user.medal.color_border` |      |
| 8  | num  | 同 `info[0][15].user.medal.color_start`  |      |
| 9  | num  | 同 `info[0][15].user.medal.color_end`    |      |
| 10 | num  | 同 `info[0][15].user.medal.guard_level`  |      |
| 11 | num  | 同 `info[0][15].user.medal.is_light`     |      |
| 12 | num  | 同 `info[0][15].user.medal.ruid`         |      |

`info[4]` 数组:

| 项 | 类型 | 内容 | 备注 |
| -- | ---- | ---- | ---- |
| 0  | num  | ?    |      |
| 1  | num  | ?    |      |
| 2  | num  | ?    |      |
| 3  | num  | ?    |      |
| 4  | num  | ?    |      |

`info[5]` 数组:

| 项 | 类型 | 内容  | 备注 |
| -- | ---- | ----- | ---- |
| 0  | str  | 空串? |      |
| 1  | str  | 空串? |      |

`info[9]` 对象:

| 字段 | 类型 | 内容     | 备注            |
| ---- | ---- | -------- | --------------- |
| ct   | str  | ?        | 16 进制         |
| ts   | num  | 发送时间 | UNIX 秒级时间戳 |

`info[16]` 数组:

| 项 | 类型 | 内容 | 备注 |
| -- | ---- | ---- | ---- |
| 0  | num  | ?    |      |

## 示例

<details>
<summary>查看消息示例(带注释):</summary>

```jsonc
{
	"cmd": "DANMU_MSG",
	"dm_v2": "",
	"info": [
		[
			0,
			1,
			25, //字体大小
			9920249, //弹幕颜色代码(10进制)#975ef9
			1723979200649,
			-1312973962,
			0,
			"0bc8acd0",
			0,
			0,
			0,
			"",
			0,
			"{}",
			"{}",
			{
				"extra": "{\"send_from_me\":false,\"mode\":0,\"color\":9920249,\"dm_type\":0,\"font_size\":25,\"player_mode\":1,\"show_player_type\":0,\"content\":\"白花300块[热]\",\"user_hash\":\"197700816\",\"emoticon_unique\":\"\",\"bulge_display\":0,\"recommend_score\":3,\"main_state_dm_color\":\"\",\"objective_state_dm_color\":\"\",\"direction\":0,\"pk_direction\":0,\"quartet_direction\":0,\"anniversary_crowd\":0,\"yeah_space_type\":\"\",\"yeah_space_url\":\"\",\"jump_to_url\":\"\",\"space_type\":\"\",\"space_url\":\"\",\"animation\":{},\"emots\":{\"[热]\":{\"count\":1,\"descript\":\"[热]\",\"emoji\":\"[热]\",\"emoticon_id\":278,\"emoticon_unique\":\"emoji_278\",\"height\":20,\"url\":\"http://i0.hdslb.com/bfs/live/6df760280b17a6cbac8c1874d357298f982ba4cf.png\",\"width\":20}},\"is_audited\":false,\"id_str\":\"364b06e3c561af3d5921f1253d66c1d575\",\"icon\":{\"prefix\":{\"type\":1,\"resource\":\"ChronosWealth_4.png\"}},\"show_reply\":true,\"reply_mid\":0,\"reply_uname\":\"\",\"reply_uname_color\":\"\",\"reply_is_mystery\":false,\"hit_combo\":0}",
				"mode": 0,
				"show_player_type": 0,
				"user": {
					"base": {
						"face": "https://i1.hdslb.com/bfs/face/5a9bb9cac3afbb58347c808ae76aaa41ca967d07.jpg", //弹幕发送用户头像
						"is_mystery": false,
						"name": "tim1997", //弹幕发送用户名称
						"name_color": 0,
						"name_color_str": "",
						"official_info": {
							"desc": "",
							"role": 0,
							"title": "",
							"type": -1
						},
						"origin_info": {
							"face": "https://i1.hdslb.com/bfs/face/5a9bb9cac3afbb58347c808ae76aaa41ca967d07.jpg",
							"name": "tim1997"
						},
						"risk_ctrl_info": null
					},
					"guard": null,
					"guard_leader": {
						"is_guard_leader": false
					},
					"medal": {
						"color": 2951253, //粉丝牌颜色(10进制)#2d0855
						"color_border": 16771156, //粉丝牌边框颜色(10进制)#ffe854
						"color_end": 10329087, //粉丝牌渐变颜色结束(10进制)#9d9bff
						"color_start": 2951253, //粉丝牌渐变颜色开始(10进制)#2d0855
						"guard_icon": "https://i0.hdslb.com/bfs/live/1d16bf0fcc3b1b768d1179d60f1fdbabe6ab4489.png", //粉丝牌左边的图标
						"guard_level": 1, //类型 1.总督 2.提督 3，舰长
						"honor_icon": "",
						"id": 1279130,
						"is_light": 1,
						"level": 29, //粉丝牌等级
						"name": "果咩吖", //粉丝牌名称
						"ruid": 3546569288714792, //粉丝牌创建者UID
						"score": 50427312,
						"typ": 0,
						"user_receive_count": 0,
						"v2_medal_color_border": "#D47AFFFF", //粉丝牌边框颜色(APP)
						"v2_medal_color_end": "#9660E5CC", //粉丝牌渐变颜色结束(APP)
						"v2_medal_color_level": "#6C00A099", //粉丝牌右边等级数字颜色(APP)
						"v2_medal_color_start": "#9660E5CC", //粉丝牌渐变颜色开始(APP)
						"v2_medal_color_text": "#FFFFFFFF" //粉丝牌右边圆形颜色(APP)
					},
					"title": {
						"old_title_css_id": "",
						"title_css_id": ""
					},
					"uhead_frame": null,
					"uid": 6088969, //弹幕发送用户UID
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
		"白花300块[热]", //弹幕内容
		[
			6088969, //同info[0][15].user.uid
			"tim1997", //同info[0][15].user.base.name
			0,
			0,
			0,
			10000,
			1,
			""
		],
		[
			29, //同info[0][15].user.medal.level
			"果咩吖", //同info[0][15].user.medal.name
			"果宝Official", //粉丝牌创建主播名称
			31180317,
			2951253, //同info[0][15].user.medal.color
			"",
			0,
			16771156, //同info[0][15].user.medal.color_border
			2951253, //同info[0][15].user.medal.color_start
			10329087, //同info[0][15].user.medal.color_end
			1, //同info[0][15].user.medal.guard_level
			1, //同info[0][15].user.medal.is_light
			3546569288714792 //同info[0][15].user.medal.ruid
		],
		[
			39,
			0,
			10512625,
			42523,
			2
		],
		[
			"",
			""
		],
		0,
		0,
		null,
		{
			"ct": "AFFF4206",
			"ts": 1723979200 //时间戳(秒级)
		},
		0,
		0,
		null,
		null,
		0,
		1040,
		[
			49
		],
		null
	]
}
```

</details>
