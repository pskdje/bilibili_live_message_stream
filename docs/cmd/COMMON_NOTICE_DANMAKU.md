# 广播通知弹幕信息 (COMMON_NOTICE_DANMAKU)

## 下发条件

某个通知要显示在弹幕区时。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ------ | --------- |
| cmd  | str | `COMMON_NOTICE_DANMAKU` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| biz_id | num | 待调查 |  |
| content_segments | array | 文本分段 |  |
| danmaku_style | obj | 文本样式信息 | 可能不存在 |
| danmaku_url | str | 待调查 |  |
| dmscore | num | 待调查 |  |
| terminals | array | 指定显示的终端 | 数字数组 |

`data.content_segments[n]` 数组中的对象

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| background_color | arr 或 null | 背景颜色? | 字符串数组，可能不存在 |
| background_color_dark | arr 或 null | 深色模式背景颜色? | 可能不存在 |
| font_bold | bool | text 字段是否加粗? | 可能不存在 |
| font_color | str | text 字段的十六进制颜色值 |  |
| font_color_dark | str | text 字段的十六进制颜色值 | APP端设置为深色模式时使用，可能不存在 |
| highlight_font_color | str | text 字段高亮部分的十六进制颜色值? | 可能不存在 |
| highlight_font_color_dark | str | text 字段高亮部分的十六进制颜色值? | 深色模式时使用，可能不存在 |
| img_height | num | 图片高度 | 可能不存在 |
| img_url | str | 图片链接 | 可能不存在 |
| img_width | str | 图片宽度 | 可能不存在 |
| text | str | 文本 |  |
| type | num | 文本组件类型 | 1：普通文本<br />2：图片<br />3：链接 |
| uri | str | 链接 | 文本组件类型为 `3` 时存在 |

`data.danmaku_style` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| background_color | str | 文本背景颜色的十六进制颜色值 |  |
| background_color_dark | str | 文本背景颜色的十六进制颜色值 | APP端设置为深色模式时使用 |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "COMMON_NOTICE_DANMAKU",
	"data": {
		"content_segments": [
		{
			"font_color": "#FB7299",
			"text": "春日限时任务：任务即将结束，抓紧完成获取3元红包奖励吧！未完成任务进度将重置",
			"type": 1
		}
		],
		"dmscore": 144,
		"terminals": [
			1,
			2,
			3,
			4,
			5
		]
	}
}
```

```json
{
	"cmd": "COMMON_NOTICE_DANMAKU",
	"data": {
		"biz_id": 0,
		"content_segments": [
			{
				"font_color": "#CCCCCC",
				"font_color_dark": "#CCCCCC",
				"text": "恭喜主播 时雨ioo ",
				"type": 1
			},
			{
				"font_color": "#F494AF",
				"font_color_dark": "#F494AF",
				"text": "成为手游航海当前第5名",
				"type": 1
			}
		],
		"danmaku_style": {
			"background_color": null,
			"background_color_dark": null
		},
		"danmaku_uri": "",
		"dmscore": 144,
		"terminals": [
			1,
			2,
			3
		]
	}
}
```

```json
{
	"cmd": "COMMON_NOTICE_DANMAKU",
	"data": {
		"content_segments": [
			{
				"background_color": null,
				"background_color_dark": null,
				"font_bold": false,
				"font_color": "#F294AE",
				"font_color_dark": "",
				"highlight_font_color": "",
				"highlight_font_color_dark": "",
				"img_height": 0,
				"img_url": "",
				"img_width": 0,
				"text": "疯狂星期五：疯狂任务今日24点结束，请关注任务完成情况~",
				"type": 1
			},
			{
				"background_color": [
					"#FA729A"
				],
				"background_color_dark": null,
				"font_bold": false,
				"font_color": "#FFFFFF",
				"font_color_dark": "",
				"highlight_font_color": "",
				"highlight_font_color_dark": "",
				"img_height": 0,
				"img_url": "",
				"img_width": 0,
				"text": "立即查看",
				"type": 3,
				"uri": "https://live.bilibili.com/p/html/bilili-page-gift-intro-container/index.html?is_live_half_webview=1&hybrid_rotate_d=1&hybrid_half_ui=1,3,100p,70p,0,0,30,100,12;2,2,375,100p,0,0,30,100,0;3,3,100p,544,0,0,30,100,12;4,2,375,100p,0,0,30,100,0;5,3,100p,70p,0,0,30,100,0;6,3,100p,70p,0,0,30,100,0;7,3,100p,70p,0,0,30,100,0;8,3,100p,70p,0,0,30,100,0&gift_id=32251&roomId=6154037&anchorId=194484313&sendTargetUid=194484313&active_tab=1"
			}
		],
		"danmaku_style": {
			"background_color": null,
			"background_color_dark": null
		},
		"dmscore": 1008,
		"terminals": [
			1,
			2,
			3,
			4,
			5
		]
	}
}
```

</details>
