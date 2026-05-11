# 直播间皮肤变更 (ROOM_SKIN_MSG)

## 下发条件

直播间皮肤变更时。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `ROOM_SKIN_MSG` |  |
| skin_id | num | 皮肤 ID |  |
| status | num | 状态? |  |
| end_time | num | 皮肤结束时间? | UNIX 秒级时间戳 |
| current_time | num | 当前时间 | UNIX 秒级时间戳 |
| only_local | bool | 仅在本地显示? |  |
| scatter | obj | ? |  |
| skin_config | obj | 皮肤配置 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "ROOM_SKIN_MSG",
	"skin_id": 353,
	"status": 1,
	"end_time": 1652620669,
	"current_time": 1652015870,
	"only_local": false,
	"scatter": {
		"min": 1,
		"max": 200
	},
	"skin_config": {
		"android": {
			"1": {
				"zip": "https://i0.hdslb.com/bfs/live/fab943a5d7eeb871ecf06413283d17536e67ab91.zip",
				"md5": "011EBB3E14192212FD50852245DC74FA"
			}
		},
		"ios": {
			"1": {
				"zip": "https://i0.hdslb.com/bfs/live/e7d8768dcb3975d82d794fe6b39756317916a7fe.zip",
				"md5": "B1223577FE9C5C248EC1326CDACF8379"
			}
		},
		"ipad": {
			"1": {
				"zip": "https://i0.hdslb.com/bfs/live/0856e17be073d75b70098609ae26572ba1534605.zip",
				"md5": "481AE75FFD0E0DE91EAFB5B6E0F8936B"
			}
		},
		"web": {
			"1": {
				"zip": "https://i0.hdslb.com/bfs/live/0b3770980e600f23629c8445fd211d4a12ec4b6f.zip",
				"md5": "8F98F79F02DEFE8B69EE2F6DE7416DFF",
				"platform": "web",
				"version": "1",
				"headInfoBgPic": "https://i0.hdslb.com/bfs/live/d293e69b70af34df0fef086a86552b1761a33a75.jpg",
				"giftControlBgPic": "https://i0.hdslb.com/bfs/live/1a124c5547c784f41dc3d7f65f446c56c4cbb73e.jpg",
				"rankListBgPic": "https://i0.hdslb.com/bfs/live/af8580a956d0eac6ea1d2cc97ea743d435a86874.jpg",
				"mainText": "#FFffffff",
				"normalText": "#FFffffff",
				"highlightContent": "#FFffd119",
				"border": "#FFaec2ff",
				"buttonText": "#FF123ab2"
			}
		}
	}
}
```

</details>
