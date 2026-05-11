# 直播间用户点赞 (LIKE_INFO_V3_CLICK)

## 下发条件

有用户给直播间点赞后。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| cmd  | str | `LIKE_INFO_V3_CLICK` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容  | 备注 |
| ---- | ---- | ---- | ---- |
| show_area | num | 待调查 |  |
| msg_type | num | 待调查 |  |
| like_icon | str | 点赞图标的URL |  |
| uid | num | 点赞的用户的UID |  |
| like_text | str | 点赞文本 |  |
| uname | str | 点赞的用户的名称 |  |
| uname_color | str | 点赞的用户的名称颜色 |  |
| identities | array | 待调查 |  |
| fans_medal | obj | 点赞的用户的粉丝勋章信息 |  |
| contribution_info | obj | 待调查 |  |
| dmscore | num | 待调查 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "LIKE_INFO_V3_CLICK",
	"data": {
		"show_area": 0,
		"msg_type": 6,
		"like_icon": "https://i0.hdslb.com/bfs/live/23678e3d90402bea6a65251b3e728044c21b1f0f.png",
		"uid": 32174213,
		"like_text": "为主播点赞了",
		"uname": "MeiDngS",
		"uname_color": "",
		"identities": [
			1
		],
		"fans_medal": {
			"target_id": 0,
			"medal_level": 0,
			"medal_name": "",
			"medal_color": 0,
			"medal_color_start": 12632256,
			"medal_color_end": 12632256,
			"medal_color_border": 12632256,
			"is_lighted": 0,
			"guard_level": 0,
			"special": "",
			"icon_id": 0,
			"anchor_roomid": 0,
			"score": 0
		},
		"contribution_info": {
			"grade": 0
		},
		"dmscore": 20
	}
}
```

</details>
