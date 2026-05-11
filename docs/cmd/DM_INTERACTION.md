# 交互信息合并 (DM_INTERACTION)

## 下发条件

连续多条相同事件时触发，特定主播触发一次特定事件也下发。

## JSON正文

根对象:

| 字段 | 类型 | 内容             | 备注 |
| ---- | ---- | ---------------- | ---- |
| cmd  | str  | `DM_INTERACTION` |      |
| data | obj  | 信息本体         |      |

`data` 对象:

| 字段     | 类型 | 内容     | 备注 |
| -------- | ---- | -------- | ---- |
| id       | num  | 事件 ID  |      |
| status   | num  | 状态     |      |
| type     | num  | 事件类型 | 101:投票<br />102:弹幕<br />103:关注<br />104:送礼<br />105:分享<br />106:点赞 |
| data     | str  | 事件数据 | 一个JSON字符串 |
| dmsource | num  |          |      |

`data.data` 字符串对象:

内容格式取决于`data.type`的类型，下面将按照`data.data(类型)`进行区分标记。

温馨提示: 要记得先解析`data.data`内的JSON字符串，不要直接使用哦。

`data.data(101)` 对象: (投票)

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| question | str | 投票问题 |  |
| options | obj | 投票详细选项 |  |
| vote_id | num | 投票id |  |
| cnt | num | 弹幕计数 |  |
| duration | num | 持续时间 | 单位毫秒 |
| left_duration | num | 剩余时间 | 单位毫秒 |
| fade_duration | num | (?) |  |
| waiting_duration | num | (?) |  |
| result | num | 投票倾向状态 |  |
| result_text | str | 投票倾向提示 |  |
| component | str | 投票链接 |  |
| natural_die_duration | num | (?) |  |
| my_vote | num | (?) |  |
| component_anchor | str | 投票控制链接 |  |
| audit_reason | str | 审核结果 |  |
| combo | obj | 投票状态展示 |  |

`data.data(101).options` 数组中对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| idx | num | 选项索引 |  |
| desc | str | 选项内容 |  |
| cnt | num | 票数 |  |
| percent | num | 显示占比 |  |

`data.data(101).combo` 数组中对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| id | num | 标识id | 同`data.data.options`数组中对象的`idx` |
| status | num | 状态 | 同`data.status` |
| content | str | 投票选项内容 |  |
| cnt | str | 弹幕计数 |  |
| guide | str | (?) | 空字符串 |
| left_duration | num | 剩余时间 |  |
| fade_duration | num | (?) |  |
| prefix_icon | str | 投票选项图标 |  |

`data.data(102)` 对象: (弹幕)

| 字段                 | 类型  | 内容                 | 备注 |
| -------------------- | ----- | -------------------- | ---- |
| combo                | array | 连续发送弹幕事件信息 |      |
| merge_interval       | num   | 合并弹幕时间间隔     |      |
| card_appear_interval | num   | 弹窗出现时间间隔     |      |
| send_interval        | num   | 发送时间间隔         |      |

`data.data(102).combo[n]` 对象:

| 字段          | 类型 | 内容           | 备注          |
| ------------- | ---- | -------------- | ------------- |
| id            | num  | 标识 ID        |               |
| status        | num  | 状态           |               |
| content       | str  | 重复的弹幕内容 |               |
| cnt           | num  | 重复数量       |               |
| guide         | str  | 标题词         | "他们都在说:" |
| left_duration | num  | 左移时长       |               |
| fade_duration | num  | 淡化时长       |               |

`data.data(103)` 对象: (关注)

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| fade\_duration | num |  |  |
| cnt | num | 关注计数 |  |
| card_appear_interval | num |  |  |
| suffix\_text | str | 提示文本 | `人关注了主播` |
| reset\_cnt | num |  |  |
| display\_flag | num |  |  |

`data.data(104)` 对象: (送礼)

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| fade\_duration | num |  |  |
| cnt | num | 投喂计数 |  |
| card_appear_interval | num |  |  |
| suffix\_text | str | 提示文本 | `人在投喂` |
| reset\_cnt | num |  |  |
| display\_flag | num |  |  |
| gift\_id | num | 礼物 ID |  |
| gift_alert_message | str |  |  |

`data.data(105)` 对象: (分享)

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| fade\_duration | num |  |  |
| cnt | num | 分享计数 |  |
| card_appear_interval | num |  |  |
| suffix\_text | str | 提示文本 | `人分享了直播间` |
| reset\_cnt | num |  |  |
| display\_flag | num |  |  |

`data.data(106)` 对象: (点赞)

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| fade\_duration | num |  |  |
| cnt | num | 点赞计数 |  |
| card_appear_interval | num |  |  |
| suffix\_text | str | 提示文本 | `人正在点赞` |
| reset\_cnt | num |  |  |
| display\_flag | num |  |  |

## 示例

<details>
<summary>type===101</summary>

```json
{
	"cmd": "DM_INTERACTION",
	"data": {
		"data": "{\"question\":\"投票\",\"options\":[{\"idx\":1,\"desc\":\"赞成\",\"cnt\":0,\"percent\":0.5},{\"idx\":2,\"desc\":\"弃权\",\"cnt\":0,\"percent\":0.5}],\"vote_id\":98014370742272,\"cnt\":0,\"duration\":60000,\"left_duration\":60000,\"fade_duration\":1000,\"waiting_duration\":-1,\"result\":1,\"result_text\":\"平局\",\"component\":\"https://live.bilibili.com/p/html/live-app-guessing-game/vote.html?is_live_half_webview=1\\u0026hybrid_half_ui=1,3,100p,245,0,0,30,100,12,0;2,2,375,100p,0,0,30,100,12,0;3,3,100p,245,0,0,30,100,12,0;4,2,375,100p,0,0,30,100,12,0;5,3,100p,70p,0,0,30,100,12,0;6,3,100p,70p,0,0,30,100,12,0;7,3,100p,70p,0,0,30,100,12,0;8,3,100p,70p,0,0,30,100,12,0\",\"natural_die_duration\":30000,\"my_vote\":0,\"component_anchor\":\"https://live.bilibili.com/p/html/live-app-guessing-game/anchor_vote.html?pc_ui=390,428,0,3\\u0026is_live_half_webview=1\\u0026hybrid_half_ui=1,3,100p,448,0,0,30,0,12,0;2,2,375,100p,0,0,30,0,12,0;3,3,100p,448,0,0,30,0,12,0;4,2,375,100p,0,0,30,0,12,0;5,3,100p,448,0,0,30,0,12,0;6,2,320,100p,0,0,30,0,12,0;7,2,320,100p,0,0,30,0,12,0;8,2,320,100p,0,0,30,0,12,0#/\",\"audit_reason\":\"您提交的弹幕投票未审核通过，请修改\",\"combo\":[{\"id\":1,\"status\":2,\"content\":\"赞成\",\"cnt\":0,\"guide\":\"\",\"left_duration\":60000,\"fade_duration\":0,\"prefix_icon\":\"http://i0.hdslb.com/bfs/dm/7d7e3682c9116aa3503418abe3cde6b45ed2e91e.png\"},{\"id\":2,\"status\":2,\"content\":\"弃权\",\"cnt\":0,\"guide\":\"\",\"left_duration\":60000,\"fade_duration\":0,\"prefix_icon\":\"http://i0.hdslb.com/bfs/dm/f83c7280b2a90b4f58a68fd8c594ea7d5667e3cb.png\"}]}",
		"dmscore": 36,
		"id": 98014370742272,
		"status": 2,
		"type": 101
	}
}
```

</details>

<details>
<summary>type===102</summary>

示例内容存疑，未计划修正。有意者可提交拉取请求修正。

```json
{
	"cmd": "DM_INTERACTION",
	"data": {
		"id": 6785480089600,
		"status": 4,
		"type": 102,
		"data": {
			"combo": [
				{
					"id": 6785480089600,
					"status": 4,
					"content": "晚安",
					"cnt": 3,
					"guide": "他们都在说:",
					"left_duration": 20000,
					"fade_duration": 60000
				}
			],
			"merge_interval": 1000,
			"card_appear_interval": 1000,
			"send_interval": 1000
		}
	}
}
```

</details>

<details>
<summary>type===103</summary>

```json
{
	"cmd": "DM_INTERACTION",
	"data": {
		"data": "{\"fade_duration\":10000,\"cnt\":6,\"card_appear_interval\":0,\"suffix_text\":\"人关注了主播\",\"reset_cnt\":0,\"display_flag\":1}",
		"dmscore": 36,
		"id": 94362402889728,
		"status": 4,
		"type": 103
	}
}
```

</details>

<details>
<summary>type===104</summary>

```json
{
	"cmd": "DM_INTERACTION",
	"data": {
		"data": "{\"fade_duration\":10000,\"cnt\":5,\"card_appear_interval\":0,\"suffix_text\":\"人在投喂\",\"reset_cnt\":0,\"display_flag\":1,\"gift_id\":33988,\"gift_alert_message\":\"投喂一个%s支持主播\"}",
		"dmscore": 36,
		"id": 85744481752576,
		"status": 5,
		"type": 104
	}
}
```

</details>

<details>
<summary>type===105</summary>

```json
{
	"cmd": "DM_INTERACTION",
	"data": {
		"data": "{\"fade_duration\":10000,\"cnt\":1,\"card_appear_interval\":0,\"suffix_text\":\"人分享了直播间\",\"reset_cnt\":0,\"display_flag\":1}",
		"dmscore": 36,
		"id": 85743053669888,
		"status": 4,
		"type": 105
	}
}
```

</details>

<details>
<summary>type===106</summary>

```json
{
	"cmd": "DM_INTERACTION",
	"data": {
		"data": "{\"fade_duration\":10000,\"cnt\":11,\"card_appear_interval\":0,\"suffix_text\":\"人正在点赞\",\"reset_cnt\":1,\"display_flag\":1}",
		"dmscore": 36,
		"id": 66159395305984,
		"status": 5,
		"type": 106
	}
}
```

</details>
