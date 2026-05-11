# 醒目留言按钮 (SUPER_CHAT_ENTRANCE)

## 下发条件

*未知*

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| cmd  | str | `SUPER_CHAT_ENTRANCE` |  |
| data | obj | 醒目留言按钮的信息 |  |
| roomid | num | 直播间ID | 未知是短号还是真实ID |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| status | num | 待调查 |  |
| jump_url | str | 按下“醒目留言”按钮后弹出小窗的页面URL |  |
| icon | str | “醒目留言”按钮图标的URL |  |
| broadcast_type | num | 待调查 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "SUPER_CHAT_ENTRANCE",
	"data": {
		"status": 1,
		"jump_url": "https://live.bilibili.com/p/html/live-app-superchat2/index.html?is_live_half_webview=1&hybrid_half_ui=1,3,100p,70p,ffffff,0,30,100;2,2,375,100p,ffffff,0,30,100;3,3,100p,70p,ffffff,0,30,100;4,2,375,100p,ffffff,0,30,100;5,3,100p,60p,ffffff,0,30,100;6,3,100p,60p,ffffff,0,30,100;7,3,100p,60p,ffffff,0,30,100",
		"icon": "https://i0.hdslb.com/bfs/live/0a9ebd72c76e9cbede9547386dd453475d4af6fe.png",
		"broadcast_type": 1
	},
	"roomid": "8618057"
}
```

</details>
