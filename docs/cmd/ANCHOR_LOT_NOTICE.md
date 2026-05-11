# 天选时刻通知 (ANCHOR_LOT_NOTICE)

## 下发条件

部分主播开播时。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `ANCHOR_LOT_NOTICE` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| notice_type | num | 通知卡片类型? |  |
| lottery_card | obj | 通知卡片内容 |  |

`data.lottery_card` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| show_time | num | 显示时间? |  |
| button_text | str | 按钮文本? |  |
| icon | str | 图标 |  |
| title | str | 标题? |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"data": {
		"notice_type": 1,
		"lottery_card": {
			"show_time": 30,
			"button_text": "去发奖",
			"icon": "https://i0.hdslb.com/bfs/live/95970204111233f181fc28622502aaf1a9359b9a.png",
			"title": "发天选有助于人气累积"
		}
	},
	"cmd": "ANCHOR_LOT_NOTICE"
}
```

</details>
