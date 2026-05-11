# 粉丝团戳一戳礼物通知 (FANS_CLUB_POKE_GIFT_NOTICE)

## 下发条件

主播使用粉丝团的戳一戳功能后。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `FANS_CLUB_POKE_GIFT_NOTICE` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| icon | str | 图标 |  |
| uface | str | 头像 |  |
| bg_img_url | str | 背景图片 |  |
| text | str | 提示文本 |  |
| highlight_text | str | 高亮文本? |  |
| button_text | str | 按钮文本 |  |
| display_duration | num | 显示时间? |  |
| room_id | num | 房间号 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "FANS_CLUB_POKE_GIFT_NOTICE",
	"data": {
		"icon": "https://i0.hdslb.com/bfs/live/37a2fe03f2af95928c67cbac889e10dab6f7d42a.png",
		"uface": "https://i0.hdslb.com/bfs/face/member/noface.jpg",
		"bg_img_url": "https://i0.hdslb.com/bfs/live/fbe99002b5914157d783f8e07f021e2fd6ba5c1b.png",
		"text": "主播戳了戳你~投喂礼物获5倍亲密度加成",
		"highlight_text": "5倍亲密度加成",
		"button_text": "去投喂",
		"display_duration": 8,
		"room_id": 1899237171
	}
}
```

</details>
