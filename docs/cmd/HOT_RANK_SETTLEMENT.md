# 限时热门榜上榜信息 (HOT_RANK_SETTLEMENT)

## 下发条件

当前直播间在结算时于限时热门榜上榜后。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| cmd | str | `HOT_RANK_SETTLEMENT` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| area_name | str | 分区名称 |  |
| cache_key | str | ? |  |
| dm_msg | str | 弹幕提示信息 |  |
| dmscore | num | ? |  |
| face | str | 主播头像 URL |  |
| icon | str | 图标 URL |  |
| rank | num | 排名 |  |
| timestamp | num | 时间 | UNIX 秒级时间戳 |
| uname | str | 主播用户名 |  |
| url | str | 排行榜 URL |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "HOT_RANK_SETTLEMENT",
	"data": {
		"area_name": "虚拟主播",
		"cache_key": "2f8baf923a6b7df5a045df6c7181984c",
		"dm_msg": "恭喜主播 <% 白黑卡扣 %> 荣登限时热门榜虚拟主播榜top9! 即将获得热门流量推荐哦！",
		"dmscore": 144,
		"face": "http://i0.hdslb.com/bfs/face/ddfcd696213e07884ce227c6ba6d23a007a08c02.jpg",
		"icon": "https://i0.hdslb.com/bfs/live/63217712edb588864b2c714225992e7f46b0b917.png",
		"rank": 9,
		"timestamp": 1651041000,
		"uname": "白黑卡扣",
		"url": "https://live.bilibili.com/p/html/live-app-hotrank/result.html?is_live_half_webview=1&hybrid_half_ui=1,5,250,200,f4eefa,0,30,0,0,0;2,5,250,200,f4eefa,0,30,0,0,0;3,5,250,200,f4eefa,0,30,0,0,0;4,5,250,200,f4eefa,0,30,0,0,0;5,5,250,200,f4eefa,0,30,0,0,0;6,5,250,200,f4eefa,0,30,0,0,0;7,5,250,200,f4eefa,0,30,0,0,0;8,5,250,200,f4eefa,0,30,0,0,0&areaId=9&cache_key=2f8baf923a6b7df5a045df6c7181984c"
	}
}
```

</details>
