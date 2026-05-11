# 冲榜提示卡 (POPULAR_RANK_GUIDE_CARD)

## 下发条件

排行榜快要结算前，部分排行很高的直播间可能下发。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `POPULAR_RANK_GUIDE_CARD` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| ruid | num | 主播uid |  |
| title | str | 提示标题 |  |
| sub_text | str | 提示副标题 |  |
| icon_img | str | 提示卡图标 | 主播头像 |
| gift_id | num | 礼物id |  |
| countdown | num | 显示时间 |  |
| popup_title | str | 提示文本 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "POPULAR_RANK_GUIDE_CARD",
	"data": {
		"ruid": 194484313,
		"title": "目前人气榜NO.1",
		"sub_text": "帮我投喂人气票冲榜吧~",
		"icon_img": "https://i1.hdslb.com/bfs/face/84a861facfa041b46f7a30897e9ed3f2e05e0519.jpg",
		"gift_id": 33988,
		"countdown": 10,
		"popup_title": "投喂一个人气票帮助主播打榜~"
	}
}
```

</details>
