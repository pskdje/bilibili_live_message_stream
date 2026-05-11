# 切断V2 (CUT_OFF_V2)

直播间被切断，且向主播显示对话框。

## 下发条件

直播间被切断时。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `CUT_OFF_V2` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cut_off_scene | num |  |  |
| timestamp | num | 操作时间戳 | UNIX 秒时间戳 |
| cut_off_version | num | 切断提示信息版本? |  |
| cut_off_data | obj | 切断提示信息 |  |

`data.cut_off_data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cut_off_title | str | 对话框窗口标题 |  |
| cut_off_message_list | array | 对话框正文列表 |  |
| cut_off_tip_list | array | 对话框提示信息列表 |  |
| cut_off_button_list | array | 对话框按钮列表 |  |

`data.cut_off_data.cut_off_message_list` 数组:

| 索引 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| 0 | obj | 首个正文信息 |  |
| … | obj | 单个正文信息 |  |
| i | obj | 最后正文信息 |  |

`data.cut_off_data.cut_off_message_list[i]` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| type | num | 显示类别 | `1`:一个“`label`：`content`”格式的信息 |
| label | str | 标签 |  |
| content | str | 内容 |  |

`data.cut_off_data.cut_off_tip_list` 数组:

| 索引 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| 0 | obj | 首个提示行信息 |  |
| … | obj | 单个提示行信息 |  |
| i | obj | 最后提示行信息 |  |

`data.cut_off_data.cut_off_tip_list[i]` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| show_platform | array | 要在哪个客户端显示的指代 |  |
| message_list | array | 提示信息列表 |  |

`data.cut_off_data.cut_off_tip_list[i].message_list` 数组:

| 索引 | 类型 | 内容 | 备注 |
|:---:| --- | --- | --- |
| 0 | obj | 首个提示组件信息 |  |
| … | obj | 单个提示组件信息 |  |
| i1 | obj | 最后提示组件信息 |  |

`data.cut_off_data.cut_off_tip_list[i].message_list[i1]` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| type | num | 显示类型 | `1`:纯文本<br />`2`:链接 |
| content | str | 显示文本 |  |
| link_url | str | 链接 | type为2时有内容 |

`data.cut_off_data.cut_off_button_list` 数组:

| 索引 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| 0 | obj | 首个按钮信息 |  |
| … | obj | 单个按钮信息 |  |
| i | obj | 最后按钮信息 |  |

`data.cut_off_data.cut_off_button_list[i]` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| show_platform | array | 要在那个客户端显示的指代 | `1`和`2`可能是手机直播姬<br />`3`和`4`可能是pc直播姬或网页直播姬 |
| button_text | str | 按钮文本 |  |
| button_action | num | 按钮操作 | `1`:关闭窗口?<br />`2`:跳转到链接? |
| button_link_url | str | 跳转链接 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "CUT_OFF_V2",
	"data": {
		"cut_off_scene": 1,
		"timestamp": 1731590280,
		"cut_off_version": 1,
		"cut_off_data": {
			"cut_off_title": "违规提示",
			"cut_off_message_list": [
				{
					"type": 1,
					"label": "处罚结果",
					"content": "切断本场直播"
				},
				{
					"type": 1,
					"label": "违规原因",
					"content": "您本场直播存在挂机、录播等消极直播行为，因此直播被切断，请您及时整改"
				},
				{
					"type": 1,
					"label": "处罚时间",
					"content": "2024年11月14日21时17分"
				}
			],
			"cut_off_tip_list": [
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
							"link_url": "https://link.bilibili.com/p/center/index?my-room/violation-records#/my-room/violation-records"
						},
						{
							"type": 1,
							"content": "查看你的违规记录",
							"link_url": ""
						}
					]
				}
			],
			"cut_off_button_list": [
				{
					"show_platform": [
						1,
						2
					],
					"button_text": "了解详情",
					"button_action": 2,
					"button_link_url": "https://live.bilibili.com/p/html/live-anchor-galaxy/violation_records/mobile.html?-Abrowser=live&is_live_webview=1"
				},
				{
					"show_platform": [
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
}
```

</details>
