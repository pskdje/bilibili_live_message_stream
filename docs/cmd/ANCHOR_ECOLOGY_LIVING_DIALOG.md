# 直播对话框 (ANCHOR_ECOLOGY_LIVING_DIALOG)

用于警告。

## 下发条件

推测在自动检测到画面不怎么变化且没人聊天时警告下发，见 ~~[SocialSisterYi/bilibili-API-collect#1139(issue正文)](https://github.com/SocialSisterYi/bilibili-API-collect/issues/1139#issue-2657488653)~~(已失效) 。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `ANCHOR_ECOLOGY_LIVING_DIALOG` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| dialog_scene | num |  |  |
| timestamp | num | 触发时间戳 | UNIX 秒时间戳 |
| valid_timestamp | num |  |  |
| dialog_top_vertical_img | str |  |  |
| dialog_top_landscape_img | str |  |  |
| dialog_title | str | 对话框标题 |  |
| dialog_message_list | array | 对话框正文列表 | 参见`CUT_OFF_V2` |
| dialog_tip_list | array | 对话框提示信息列表 | 参见`CUT_OFF_V2` |
| dialog_button_list | array | 对话框按钮列表 | 参见`CUT_OFF_V2` |

`data.dialog_message_list` 数组:

同`CUT_OFF_V2`的`data.cut_off_data.cut_off_message_list`数组。

`data.dialog_tip_list` 数组:

同`CUT_OFF_V2`的`data.cut_off_data.cut_off_tip_list`数组。

`data.dialog_button_list` 数组:

同`CUT_OFF_V2`的`data.cut_off_data.cut_off_button_list`数组。

参见 [CUT_OFF_V2](CUT_OFF_V2.md) 。

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "ANCHOR_ECOLOGY_LIVING_DIALOG",
	"data": {
		"dialog_scene": 1,
		"timestamp": 1731504845,
		"valid_timestamp": 0,
		"dialog_top_vertical_img": "https://i0.hdslb.com/bfs/live/ee359d3e89bb044914f72a557a4ac2d3b5ba4004.png",
		"dialog_top_landscape_img": "https://i0.hdslb.com/bfs/live/ee359d3e89bb044914f72a557a4ac2d3b5ba4004.png",
		"dialog_title": "直播间违规",
		"dialog_message_list": [
			{
				"type": 1,
				"label": "处罚结果",
				"content": "警告"
			},
			{
				"type": 1,
				"label": "违规原因",
				"content": "您本场直播存在挂机、录播等消极直播行为，请及时整改"
			},
			{
				"type": 1,
				"label": "处罚时间",
				"content": "2024年11月13日21时34分"
			}
		],
		"dialog_tip_list": [
			{
				"show_platform": [
					1,
					2
				],
				"message_list": [
					{
						"type": 1,
						"content": "请在",
						"link_url": ""
					},
					{
						"type": 2,
						"content": "【处罚中心】",
						"link_url": "https://live.bilibili.com/p/html/live-anchor-galaxy/violation_records/mobile.html?is_live_half_webview=1u0026hybrid_rotate_d=1u0026is_cling_player=1u0026hybrid_half_ui=1,3,100p,70p,0,1,30,100;2,2,375,100p,0,1,30,100;3,3,100p,70p,0,1,30,100;4,2,375,100p,0,1,30,100;5,3,100p,70p,0,1,30,100;6,3,100p,70p,0,1,30,100;7,3,100p,70p,0,1,30,100;8,3,100p,70p,0,1,30,100#/"
					},
					{
						"type": 1,
						"content": "查看你的违规记录",
						"link_url": ""
					}
				]
			},
			{
				"show_platform": [
					3,
					4
				],
				"message_list": [
					{
						"type": 1,
						"content": "请在",
						"link_url": ""
					},
					{
						"type": 2,
						"content": "【处罚中心】",
						"link_url": "https://link.bilibili.com/#/my-room/violation-records?jump_type=browser&app_common=open"
					},
					{
						"type": 1,
						"content": "查看你的违规记录",
						"link_url": ""
					}
				]
			}
		],
		"dialog_button_list": [
			{
				"show_platform": [
					1,
					2,
					3,
					4
				],
				"button_text": "我知道了",
				"button_action": 1,
				"button_link_url": ""
			}
		]
	}
}
```

</details>
