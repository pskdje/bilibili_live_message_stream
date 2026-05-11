# 限时热门榜上榜信息V2 (HOT_RANK_SETTLEMENT_V2)

## 下发条件

当前直播间在结算时于限时热门榜上榜后。

## JSON消息

基本同 [限时热门榜上榜信息](HOT_RANK_SETTLEMENT.md), 但没有 `data.dmscore` 字段

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "HOT_RANK_SETTLEMENT_V2",
	"data": {
		"rank": 9,
		"uname": "白黑卡扣",
		"face": "http://i0.hdslb.com/bfs/face/ddfcd696213e07884ce227c6ba6d23a007a08c02.jpg",
		"timestamp": 1651040700,
		"icon": "https://i0.hdslb.com/bfs/live/cb2e160ac4f562b347bb5ae6e635688ebc69580f.png",
		"area_name": "虚拟主播",
		"url": "https://live.bilibili.com/p/html/live-app-hotrank/result.html?is_live_half_webview=1&hybrid_half_ui=1,5,250,200,f4eefa,0,30,0,0,0;2,5,250,200,f4eefa,0,30,0,0,0;3,5,250,200,f4eefa,0,30,0,0,0;4,5,250,200,f4eefa,0,30,0,0,0;5,5,250,200,f4eefa,0,30,0,0,0;6,5,250,200,f4eefa,0,30,0,0,0;7,5,250,200,f4eefa,0,30,0,0,0;8,5,250,200,f4eefa,0,30,0,0,0&areaId=371&cache_key=693b7b029b66976a399cf4e3485d265a",
		"cache_key": "693b7b029b66976a399cf4e3485d265a",
		"dm_msg": "恭喜主播 <% 白黑卡扣 %> 荣登限时热门榜虚拟主播榜top9! 即将获得热门流量推荐哦！"
	}
}
```

</details>
