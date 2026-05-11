# 通知消息 (NOTICE_MSG)

## 下发条件

需要通告或广播时。

## JSON消息

根对象:

| 字段 | 类型 | 内容   | 备注    |
| ---- | ---- | ------ | ------- |
| cmd | str | `NOTICE_MSG` |  |
| id | num | 待调查 |  |
| name | str | 通知名 |  |
| full | obj | 完整显示信息? |  |
| half | obj | 半部显示信息? |  |  |
| side | obj | 边缘显示信息? |  |
| roomid | num | 目标直播间短号 |  |
| real_roomid | num | 目标直播间真实ID |  |
| msg_common | str | 显示的消息内容 |  |
| msg_self | str | 消息内容本身 | 剔除额外文本 |
| link_url | str | 通知消息跳转的URL |  |
| msg_type | num | 待调查 |  |
| shield_uid | num | 待调查 |  |
| business_id | str | 待调查 |  |
| scatter | obj | 待调查 |  |
| marquee_id | str | 待调查 |  |
| notice_type | num | 待调查 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "NOTICE_MSG",
	"id": 804,
	"name": "人气榜第一名",
	"full": {
		"head_icon": "https://i0.hdslb.com/bfs/live/f74b09c7fb83123a0dd66c536b6d5b143d271b08.png",
		"tail_icon": "https://i0.hdslb.com/bfs/live/822da481fdaba986d738db5d8fd469ffa95a8fa1.webp",
		"head_icon_fa": "https://i0.hdslb.com/bfs/live/f74b09c7fb83123a0dd66c536b6d5b143d271b08.png",
		"tail_icon_fa": "https://i0.hdslb.com/bfs/live/38cb2a9f1209b16c0f15162b0b553e3b28d9f16f.png",
		"head_icon_fan": 1,
		"tail_icon_fan": 4,
		"background": "#FFE6BD",
		"color": "#9D5412",
		"highlight": "#FF6933",
		"time": 20
	},
	"half": {
		"head_icon": "https://i0.hdslb.com/bfs/live/f74b09c7fb83123a0dd66c536b6d5b143d271b08.png",
		"tail_icon": "https://i0.hdslb.com/bfs/live/822da481fdaba986d738db5d8fd469ffa95a8fa1.webp",
		"background": "#FFE6BD",
		"color": "#9D5412",
		"highlight": "#FF6933",
		"time": 0
	},
	"side": {
		"head_icon": "",
		"background": "",
		"color": "",
		"highlight": "",
		"border": ""
	},
	"roomid": 23919301,
	"real_roomid": 23919301,
	"msg_common": "恭喜主播<%AG超玩会王者荣耀一诺%>荣获上小时人气榜第<%1%>名！点击传送查看精彩内容！",
	"msg_self": "恭喜主播<%AG超玩会王者荣耀一诺%>荣获上小时人气榜第<%1%>名！",
	"link_url": "https://live.bilibili.com/23919301?broadcast_type=0&is_room_feed=1&from=28003&extra_jump_from=28003",
	"msg_type": 1,
	"shield_uid": -1,
	"business_id": "",
	"scatter": {
		"min": 0,
		"max": 0
	},
	"marquee_id": "",
	"notice_type": 0
}
```

```json
{
	"cmd": "NOTICE_MSG",
	"id": 814,
	"name": "幻影飞船专用",
	"full": {
		"head_icon": "https://i0.hdslb.com/bfs/live/08978f1721200e11328d1f7d6231b21bcca20488.gif",
		"tail_icon": "https://i0.hdslb.com/bfs/live/822da481fdaba986d738db5d8fd469ffa95a8fa1.webp",
		"head_icon_fa": "https://i0.hdslb.com/bfs/live/08978f1721200e11328d1f7d6231b21bcca20488.gif",
		"tail_icon_fa": "https://i0.hdslb.com/bfs/live/38cb2a9f1209b16c0f15162b0b553e3b28d9f16f.png",
		"head_icon_fan": 1,
		"tail_icon_fan": 4,
		"background": "#F09153",
		"color": "#FFFFFF",
		"highlight": "#FFE600",
		"time": 15
	},
	"half": {
		"head_icon": "https://i0.hdslb.com/bfs/live/08978f1721200e11328d1f7d6231b21bcca20488.gif",
		"tail_icon": "",
		"background": "#F09153",
		"color": "#FFFFFFFF",
		"highlight": "#FFE600",
		"time": 15
	},
	"side": {
		"head_icon": "",
		"background": "",
		"color": "",
		"highlight": "",
		"border": ""
	},
	"roomid": 25207004,
	"real_roomid": 25207004,
	"msg_common": "<%咖啡_ミシェル%>投喂<%夜月瓜瓜sukuyi%>1个幻影飞船，向着浩瀚星辰出发！",
	"msg_self": "<%咖啡_ミシェル%>投喂<%夜月瓜瓜sukuyi%>1个幻影飞船，向着浩瀚星辰出发！",
	"link_url": "https://live.bilibili.com/25207004?broadcast_type=0&is_room_feed=1&from=28003&extra_jump_from=28003&live_lottery_type=1",
	"msg_type": 2,
	"shield_uid": -1,
	"business_id": "32356",
	"scatter": {
		"min": 0,
		"max": 0
	},
	"marquee_id": "",
	"notice_type": 0
}
```

</details>
