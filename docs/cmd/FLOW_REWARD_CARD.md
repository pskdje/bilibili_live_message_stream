# 流量奖励卡 (FLOW_REWARD_CARD)

## 下发条件

每小时随人气榜结算。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| cmd | str | `FLOW_REWARD_CARD` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| anchor_face | str | 主播头像 |  |
| anchor_icon_url | str | “UP”图标链接 |  |
| anchor_name | str | 主播名称 |  |
| button_text | str | 按钮文本 |  |
| cover | str | 直播封面 |  |
| description | str | 推广描述? |  |
| expire_time | num | 过期时间 |  |
| label_url | str | 标签链接 | 人气榜排行图片 |
| rank | num | 人气榜排行 |  |
| room_id | num | 直播间id |  |
| route | str | 直播链接 |  |
| ruid | num | 主播uid |  |

## 示例

<details>
<summary>查看消息示例：</summary>

```json
{
	"cmd": "FLOW_REWARD_CARD",
	"data": {
		"anchor_face": "https://i2.hdslb.com/bfs/face/cb027c15d47d992c220b2a73066b1b54d54c3eb6.jpg",
		"anchor_icon_url": "http://i0.hdslb.com/bfs/live/bbd2718cbce091d39f72b01ecc762b7542e292a7.png",
		"anchor_name": "桑晚Aano",
		"button_text": "去围观",
		"cover": "https://i0.hdslb.com/bfs/live/new_room_cover/7c53d8a834d8465f580e565af1141b0e18e960a5.jpg",
		"description": "【民族/古风】电台圈top级唱见",
		"expire_time": 10,
		"label_url": "http://i0.hdslb.com/bfs/live/96aa77878c4d3f8bf2ed59fb3ae2b2980ac48887.png",
		"rank": 1,
		"room_id": 1748633627,
		"route": "https://live.bilibili.com/1748633627?popular_rank=1&user_from=2&jump_from=28039&live_from=28039",
		"ruid": 22376558
	}
}
```

</details>
