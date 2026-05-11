# 礼物星球信息 (WIDGET_WISH_INFO)

## 下发条件

*未知*

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `WIDGET_WISH_INFO` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| sid | num | (?) |  |
| wish | arr | 礼物需求信息 |  |
| jump_url | str | 用户端礼物星球界面 |  |
| wish_status | num | 礼物星球状态 |  |
| card_text | str | 卡片提示文本 |  |
| modal_text | str | 需求标题 |  |
| button_text | str | 按钮文本 |  |
| show_time | num | 显示时间 | 单位秒 |
| ts | num | 发送时间戳 | Unix秒时间戳 |
| tid | num | (?) |  |
| wish_status_info | arr | 状态对照信息 |  |
| wish_name | str | 礼物星球名称 |  |

`data.wish` 数组中的对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| gift_id | num | 礼物id |  |
| target_num | num | 需求数量 |  |
| gift_img | str | 礼物图片URL |  |
| gift_price | num | 礼物金瓜子标价 | CNY×1000 |
| gift_name | str | 礼物名称 |  |
| wish_status | num | 该礼物达成状态 |  |

`data.wish_status_info` 数组中的对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| wish_status_msg | str | 状态提示信息 |  |
| wish_status_img | str | 状态图片URL |  |
| wish_status | str | 状态 |  |
| wish_status_desc | str | 状态描述 | 不一定存在 |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "WIDGET_WISH_INFO",
	"data": {
		"sid": 658537,
		"wish": [
			{
				"gift_id": 31036,
				"target_num": 1,
				"gift_img": "https://s1.hdslb.com/bfs/live/8b40d0470890e7d573995383af8a8ae074d485d9.png",
				"gift_price": 100,
				"gift_name": "小花花",
				"wish_status": 1
			},
			{
				"gift_id": 30758,
				"target_num": 1,
				"gift_img": "https://s1.hdslb.com/bfs/live/3ddb10b055b9d1826829ec0fad93ab56484d4a90.png",
				"gift_price": 100,
				"gift_name": "这个好诶",
				"wish_status": 1
			},
			{
				"gift_id": 31039,
				"target_num": 1,
				"gift_img": "https://s1.hdslb.com/bfs/live/91ac8e35dd93a7196325f1e2052356e71d135afb.png",
				"gift_price": 100,
				"gift_name": "牛哇牛哇",
				"wish_status": 1
			}
		],
		"jump_url": "https://live.bilibili.com/p/html/bilili-page-gift-wishes-mix-planet/user.html?is_live_half_webview=1&hybrid_half_ui=1,3,100p,70p,0,0,30,100,15,0;2,2,375,100p,0,0,30,100,15,0;3,3,100p,70p,0,0,30,100,15,0;4,2,375,100p,0,0,30,100,15,0;5,3,100p,70p,0,0,30,100,15,0;6,3,100p,70p,0,0,30,100,15,0;7,3,100p,70p,0,0,30,100,15,0;8,3,100p,70p,0,0,30,100,15,0",
		"wish_status": 1,
		"card_text": "主播今日心愿还未完成",
		"modal_text": "今日心愿礼物",
		"button_text": "去助力",
		"show_time": 5,
		"ts": 1746257134,
		"tid": 6585370000,
		"wish_status_info": [
			{
				"wish_status_msg": "礼物星球待点亮",
				"wish_status_img": "https://i0.hdslb.com/bfs/live/e507f8b101289b2ce6741880a28304215a65f5bf.png",
				"wish_status": -1
			},
			{
				"wish_status_msg": "今日心愿暂未达成",
				"wish_status_img": "https://i0.hdslb.com/bfs/live/e507f8b101289b2ce6741880a28304215a65f5bf.png",
				"wish_status": 1
			},
			{
				"wish_status_msg": "今日心愿已达成",
				"wish_status_img": "https://i0.hdslb.com/bfs/live/e507f8b101289b2ce6741880a28304215a65f5bf.png",
				"wish_status": 2,
				"wish_status_desc": "已完成"
			}
		],
		"wish_name": "心愿礼物"
	}
}
```

</details>
