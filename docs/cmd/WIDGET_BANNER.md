# 小部件 (WIDGET_BANNER)

网页端在直播画面上方的横幅，手机端在直播界面的右下角，例如 限时任务 等。

## 下发条件

小部件数据更新时。

## JSON消息

| 字段 | 类型 | 内容   | 备注      |
| ---- | ---- | ------ | --------- |
| cmd | str | `WIDGET_BANNER` |  |
| data | obj | 横幅信息 |  |

`data` 对象:

| 字段 | 类型 | 内容   | 备注      |
| ---- | ---- | ------ | --------- |
| timestamp | num | 服务器发送数据包时的Unix时间戳 |  |
| widget_list | obj | 横幅信息 | 待调查 |

`data.widget_list` 对象:

以 横幅 ID 为键, JSON Object 为值的表

`data.widget_list['?']` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| id | num | 横幅ID |  |
| title | str | 待调查 |  |
| cover | str | 待调查 |  |
| web_cover | str | 待调查 |  |
| tip_text | str | 待调查 |  |
| tip_text_color | str | 待调查 |  |
| tip_bottom_color | str | 待调查 |  |
| jump_url | str | 点击横幅后出现小窗的页面的URL |  |
| url | str | 待调查 |  |
| stay_time | num | 待调查 |  |
| site | num | 待调查 |  |
| platform_in | array | 待调查 |  |
| type | num | 待调查 |  |
| band_id | num | 待调查 |  |
| sub_key | str | 待调查 |  |
| sub_data | str | 横幅数据 |  |
| is_add | bool | 待调查 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "WIDGET_BANNER",
	"data": {
		"timestamp": 1673684868,
		"widget_list": {
			"308": {
				"id": 308,
				"title": "一月限时任务",
				"cover": "",
				"web_cover": "",
				"tip_text": "限时任务",
				"tip_text_color": "",
				"tip_bottom_color": "",
				"jump_url": "https://live.bilibili.com/activity/live-activity-battle/index.html?app_name=time_limited_task_jan_2023&is_live_half_webview=1&hybrid_rotate_d=1&hybrid_half_ui=1,3,100p,70p,0,0,0,0,12,0;2,2,375,100p,0,0,0,0,12,0;3,3,100p,70p,0,0,0,0,12,0;4,2,375,100p,0,0,0,0,12,0;5,3,100p,70p,0,0,0,0,12,0;6,3,100p,70p,0,0,0,0,12,0;7,3,100p,70p,0,0,0,0,12,0;8,3,100p,70p,0,0,0,0,12,0&room_id=8618057&uid=29857468#/",
				"url": "",
				"stay_time": 5,
				"site": 1,
				"platform_in": [
					"live",
					"blink",
					"live_link",
					"web",
					"pc_link"
				],
				"type": 1,
				"band_id": 101558,
				"sub_key": "",
				"sub_data": "%7B%22task_status%22%3A0%2C%22current_val%22%3A10%2C%22target_val%22%3A1200%2C%22timeout%22%3A1673687024%2C%22reward_price%22%3A8%2C%22reward_type%22%3A1%7D",
				"is_add": true
			}
		}
	}
}
```

</details>
