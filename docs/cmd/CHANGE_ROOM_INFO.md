# 直播间背景图片修改 (CHANGE_ROOM_INFO)

## 下发条件

直播间背景图片修改时。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `CHANGE_ROOM_INFO` |  |
| background | str | 背景图 URL |  |
| roomid | num | 直播间 ID |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "CHANGE_ROOM_INFO",
	"background": "https://i0.hdslb.com/bfs/live/2388faed3728f3396052273ad4c3c9af21c411fc.jpg",
	"roomid": 23993070
}
```

</details>
