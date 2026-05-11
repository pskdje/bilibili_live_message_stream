# 游戏卡片刷新 (AD_GAME_CARD_REFRESH)

## 下发条件

直播间推广某个游戏时可能下发。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `AD_GAME_CARD_REFRESH` |  |
| data | str | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| room_id | num | 直播间id |  |
| card_id | str | 卡片id |  |
| game_card_click_uv | num | 不重复的点击数? |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "AD_GAME_CARD_REFRESH",
	"data": {
		"room_id": "27263119",
		"card_id": "1873643449509744640",
		"game_card_click_uv": "2419"
	}
}
```

</details>
