# 当前直播间限时热门榜排名改变V2 (HOT_RANK_CHANGED_V2)

## 下发条件

当前直播间在限时热门榜排名改变时。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| cmd | str | `HOT_RANK_CHANGED_V2` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| rank | num | 排名 |  |
| trend | num | 趋势? |  |
| countdown | num | 剩余时间? |  |
| timestamp | num | 当前时间? | UNIX 秒级时间戳 |
| web_url | str | 排行榜 URL |  |
| live_url | str | 排行榜 URL |  |
| blink_url | str | 排行榜 URL |  |
| live_link_url | str | 排行榜 URL |  |
| pc_link_url | str | 排行榜 URL |  |
| icon | str | 图标 URL |  |
| area_name | str | 分区名称 |  |
| rank_desc | str | 排行榜说明 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "HOT_RANK_CHANGED_V2",
	"data": {
		"rank": 31,
		"trend": 0,
		"countdown": 1440,
		"timestamp": 1651037760,
		"web_url": "https://live.bilibili.com/p/html/live-app-hotrank/index.html?clientType=2&area_id=9&parent_area_id=9&second_area_id=371",
		"live_url": "https://live.bilibili.com/p/html/live-app-hotrank/index.html?clientType=1&area_id=9&parent_area_id=9&second_area_id=371&is_live_half_webview=1&hybrid_rotate_d=1&hybrid_half_ui=1,3,100p,70p,f4eefa,0,30,100,12,0;2,2,375,100p,f4eefa,0,30,100,0,0;3,3,100p,70p,f4eefa,0,30,100,12,0;4,2,375,100p,f4eefa,0,30,100,0,0;5,3,100p,70p,f4eefa,0,30,100,0,0;6,3,100p,70p,f4eefa,0,30,100,0,0;7,3,100p,70p,f4eefa,0,30,100,0,0;8,3,100p,70p,f4eefa,0,30,100,0,0",
		"blink_url": "https://live.bilibili.com/p/html/live-app-hotrank/index.html?clientType=3&area_id=9&parent_area_id=9&second_area_id=371&is_live_half_webview=1&hybrid_rotate_d=1&is_cling_player=1&hybrid_half_ui=1,3,100p,70p,f4eefa,0,30,100,0,0;2,2,375,100p,f4eefa,0,30,100,0,0;3,3,100p,70p,f4eefa,0,30,100,0,0;4,2,375,100p,f4eefa,0,30,100,0,0;5,3,100p,70p,f4eefa,0,30,100,0,0;6,3,100p,70p,f4eefa,0,30,100,0,0;7,3,100p,70p,f4eefa,0,30,100,0,0;8,3,100p,70p,f4eefa,0,30,100,0,0",
		"live_link_url": "https://live.bilibili.com/p/html/live-app-hotrank/index.html?clientType=5&area_id=9&parent_area_id=9&second_area_id=371&is_live_half_webview=1&hybrid_rotate_d=1&is_cling_player=1&hybrid_half_ui=1,3,100p,70p,f4eefa,0,30,100,0,0;2,2,375,100p,f4eefa,0,30,100,0,0;3,3,100p,70p,f4eefa,0,30,100,0,0;4,2,375,100p,f4eefa,0,30,100,0,0;5,3,100p,70p,f4eefa,0,30,100,0,0;6,3,100p,70p,f4eefa,0,30,100,0,0;7,3,100p,70p,f4eefa,0,30,100,0,0;8,3,100p,70p,f4eefa,0,30,100,0,0",
		"pc_link_url": "https://live.bilibili.com/p/html/live-app-hotrank/index.html?clientType=4&is_live_half_webview=1&area_id=9&parent_area_id=9&second_area_id=371&pc_ui=338,465,f4eefa,0",
		"icon": "https://i0.hdslb.com/bfs/live/cb2e160ac4f562b347bb5ae6e635688ebc69580f.png",
		"area_name": "虚拟主播",
		"rank_desc": "虚拟主播top50"
	}
}
```

</details>
