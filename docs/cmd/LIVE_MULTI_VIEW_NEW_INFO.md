# 多个直播视角信息 (LIVE_MULTI_VIEW_NEW_INFO)

## 下发条件

部分活动直播间会下发。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `LIVE_MULTI_VIEW_NEW_INFO` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| title | str | 活动标题 | 活动结束后为`""` |
| room_id | num | 主直播间id | 活动结束后为`0` |
| copy_writing | str | 提示文本 | 活动结束后为`""` |
| bg_image | str | 背景图片 | 活动结束后为`""` |
| sub_slt_color | str | 切换按钮颜色? | 活动结束后为`""` |
| sub_bg_color | str | 切换按钮背景颜色? | 活动结束后为`""` |
| sub_text_color | str | 切换按钮文本颜色? | 活动结束后为`""` |
| view_type | num |  |  |
| room_list | arr | 房间列表 | 不包括“未直播”状态的直播间，活动结束后为`null` |
| relation_view | arr | 详细关系? | 不包括“未直播”状态的直播间，活动结束后为`null` |
| view_pattern | num |  |  |
| gather_room_list | arr | 空数组? | 活动结束后为`null` |

`data.room_list` 数组中对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| order_id | num | 顺序id |  |
| room_id | num | 直播间id | 似乎是长号 |
| room_name | str | 主播名称 |  |
| live_status | num | 直播状态 | 1：直播中<br />2：轮播中 |
| jump_url | str | 加入直播间的链接 |  |

`data.relation_view` 数组中对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| order_id | num | 顺序id |  |
| view_type | num |  |  |
| view_id | num | 直播间id |  |
| view_name | str | 主播名称 |  |
| title | str | 直播间标题 |  |
| cover | str | 直播间封面 |  |
| jump_url | str | 加入直播间的链接 |  |
| switch | bool |  |  |
| num | num | 看过人数 |  |
| watch_icon | str | 看过图标 |  |
| live_status | num | 直播状态 | 同`data.room_list[i].live_status` |
| text_small | str | 看过人数文本 |  |
| use_view_vt | bool |  |  |
| anchor_face | str | 主播头像 |  |
| match_live_room | bool |  |  |
| match_info | null |  |  |
| duration | num |  |  |
| up_name | str | `""` |  |
| pub_date | str |  |  |
| gather_id | num |  |  |
| sub_name | str |  |  |

## 示例

<details>
<summary>查看响应示例:</summary>

```json
{
	"cmd": "LIVE_MULTI_VIEW_NEW_INFO",
	"data": {
		"title": "战地风云6公开测试",
		"room_id": 5050,
		"copy_writing": "更多视角",
		"bg_image": "https://i0.hdslb.com/bfs/live/edaa9477a1d8325dd0c36c419b6fd5f9646b2419.png",
		"sub_slt_color": "#FFFFFF",
		"sub_bg_color": "#333333",
		"sub_text_color": "#FFFFFF",
		"view_type": 0,
		"room_list": [
			{
				"order_id": 2,
				"room_id": 6154037,
				"room_name": "Asaki大人",
				"live_status": 2,
				"jump_url": "https://live.bilibili.com/6154037?broadcast_type=0&is_room_feed=1&live_from=28022"
			},
			{
				"order_id": 4,
				"room_id": 1521765,
				"room_name": "南云鸟羽",
				"live_status": 1,
				"jump_url": "https://live.bilibili.com/1521765?broadcast_type=0&is_room_feed=1&live_from=28022"
			},
			{
				"order_id": 8,
				"room_id": 24065,
				"room_name": "闻香识",
				"live_status": 1,
				"jump_url": "https://live.bilibili.com/24065?broadcast_type=0&is_room_feed=1&live_from=28022"
			},
			{
				"order_id": 14,
				"room_id": 38528,
				"room_name": "乔伊奥斯托雷",
				"live_status": 1,
				"jump_url": "https://live.bilibili.com/38528?broadcast_type=0&is_room_feed=1&live_from=28022"
			},
			{
				"order_id": 15,
				"room_id": 21263282,
				"room_name": "Yommyko",
				"live_status": 2,
				"jump_url": "https://live.bilibili.com/21263282?broadcast_type=0&is_room_feed=1&live_from=28022"
			},
			{
				"order_id": 16,
				"room_id": 5513659,
				"room_name": "狙佬-zuener",
				"live_status": 1,
				"jump_url": "https://live.bilibili.com/5513659?broadcast_type=0&is_room_feed=1&live_from=28022"
			},
			{
				"order_id": 18,
				"room_id": 146007,
				"room_name": "Kisflow",
				"live_status": 1,
				"jump_url": "https://live.bilibili.com/146007?broadcast_type=0&is_room_feed=1&live_from=28022"
			},
			{
				"order_id": 19,
				"room_id": 1163043,
				"room_name": "人形鹿头自走炮",
				"live_status": 1,
				"jump_url": "https://live.bilibili.com/1163043?broadcast_type=0&is_room_feed=1&live_from=28022"
			},
			{
				"order_id": 20,
				"room_id": 3343118,
				"room_name": "版尤黑紫",
				"live_status": 1,
				"jump_url": "https://live.bilibili.com/3343118?broadcast_type=0&is_room_feed=1&live_from=28022"
			},
			{
				"order_id": 21,
				"room_id": 25212992,
				"room_name": "贝施汀",
				"live_status": 1,
				"jump_url": "https://live.bilibili.com/25212992?broadcast_type=0&is_room_feed=1&live_from=28022"
			},
			{
				"order_id": 22,
				"room_id": 11313,
				"room_name": "丧心病狂的魔笑",
				"live_status": 1,
				"jump_url": "https://live.bilibili.com/11313?broadcast_type=0&is_room_feed=1&live_from=28022"
			},
			{
				"order_id": 24,
				"room_id": 902302,
				"room_name": "LF叶绿",
				"live_status": 1,
				"jump_url": "https://live.bilibili.com/902302?broadcast_type=0&is_room_feed=1&live_from=28022"
			}
		],
		"relation_view": [
			{
				"order_id": 2,
				"view_type": 0,
				"view_id": 6154037,
				"view_name": "Asaki大人",
				"title": "猪猪猪",
				"cover": "https://i0.hdslb.com/bfs/live/new_room_cover/87e0332a5c3c8cd73fa7616045111b90b0199087.jpg",
				"jump_url": "https://live.bilibili.com/6154037?broadcast_type=0&is_room_feed=1&live_from=28022",
				"switch": true,
				"num": 2305,
				"watch_icon": "https://i0.hdslb.com/bfs/live/a725a9e61242ef44d764ac911691a7ce07f36c1d.png",
				"live_status": 2,
				"text_small": "2305",
				"use_view_vt": false,
				"anchor_face": "https://i1.hdslb.com/bfs/face/84a861facfa041b46f7a30897e9ed3f2e05e0519.jpg",
				"match_live_room": false,
				"match_info": null,
				"duration": 0,
				"up_name": "",
				"pub_date": "",
				"gather_id": 0,
				"sub_name": ""
			},
			{
				"order_id": 4,
				"view_type": 0,
				"view_id": 1521765,
				"view_name": "南云鸟羽",
				"title": "【战地6B测】下午四点开！聊天摸鱼",
				"cover": "https://i0.hdslb.com/bfs/live/new_room_cover/a8216e0b5469949fcbcc72458c7955b562838a89.jpg",
				"jump_url": "https://live.bilibili.com/1521765?broadcast_type=0&is_room_feed=1&live_from=28022",
				"switch": true,
				"num": 36987,
				"watch_icon": "https://i0.hdslb.com/bfs/live/a725a9e61242ef44d764ac911691a7ce07f36c1d.png",
				"live_status": 1,
				"text_small": "3.6万",
				"use_view_vt": false,
				"anchor_face": "https://i1.hdslb.com/bfs/face/f4744b6346ddaccb4642a0f05f25d798fb5d8474.jpg",
				"match_live_room": false,
				"match_info": null,
				"duration": 0,
				"up_name": "",
				"pub_date": "",
				"gather_id": 0,
				"sub_name": ""
			},
			{
				"order_id": 8,
				"view_type": 0,
				"view_id": 24065,
				"view_name": "闻香识",
				"title": "4点战地6！！",
				"cover": "https://i0.hdslb.com/bfs/live/new_room_cover/6e309306fcb7bdeeb5e72f8b4c2d1ed7ba7e1e29.jpg",
				"jump_url": "https://live.bilibili.com/24065?broadcast_type=0&is_room_feed=1&live_from=28022",
				"switch": true,
				"num": 32408,
				"watch_icon": "https://i0.hdslb.com/bfs/live/a725a9e61242ef44d764ac911691a7ce07f36c1d.png",
				"live_status": 1,
				"text_small": "3.2万",
				"use_view_vt": false,
				"anchor_face": "https://i0.hdslb.com/bfs/face/df21869b067816e03c517bc774f6ebf5a86563de.jpg",
				"match_live_room": false,
				"match_info": null,
				"duration": 0,
				"up_name": "",
				"pub_date": "",
				"gather_id": 0,
				"sub_name": ""
			},
			{
				"order_id": 14,
				"view_type": 0,
				"view_id": 38528,
				"view_name": "乔伊奥斯托雷",
				"title": "[战地六B测]捞薯条，吃薯条，谁是薯条？",
				"cover": "https://i0.hdslb.com/bfs/live/new_room_cover/a89ebcd8b4f3e841ddb7cb53fbdc6013a9956013.jpg",
				"jump_url": "https://live.bilibili.com/38528?broadcast_type=0&is_room_feed=1&live_from=28022",
				"switch": true,
				"num": 3660,
				"watch_icon": "https://i0.hdslb.com/bfs/live/a725a9e61242ef44d764ac911691a7ce07f36c1d.png",
				"live_status": 1,
				"text_small": "3660",
				"use_view_vt": false,
				"anchor_face": "https://i1.hdslb.com/bfs/face/82ef4b09c26751649da2a48960d23fd87baa6db5.jpg",
				"match_live_room": false,
				"match_info": null,
				"duration": 0,
				"up_name": "",
				"pub_date": "",
				"gather_id": 0,
				"sub_name": ""
			},
			{
				"order_id": 15,
				"view_type": 0,
				"view_id": 21263282,
				"view_name": "Yommyko",
				"title": "和广东双马尾搏斗！禁闭求生2",
				"cover": "https://i0.hdslb.com/bfs/live/new_room_cover/86ac43cf0c1db277b92a5e83324558ceab2bb108.jpg",
				"jump_url": "https://live.bilibili.com/21263282?broadcast_type=0&is_room_feed=1&live_from=28022",
				"switch": true,
				"num": 1583,
				"watch_icon": "https://i0.hdslb.com/bfs/live/a725a9e61242ef44d764ac911691a7ce07f36c1d.png",
				"live_status": 2,
				"text_small": "1583",
				"use_view_vt": false,
				"anchor_face": "https://i2.hdslb.com/bfs/face/9718e4c59c2cfcc9f8b747ad8ea5006fad78a76a.jpg",
				"match_live_room": false,
				"match_info": null,
				"duration": 0,
				"up_name": "",
				"pub_date": "",
				"gather_id": 0,
				"sub_name": ""
			},
			{
				"order_id": 16,
				"view_type": 0,
				"view_id": 5513659,
				"view_name": "狙佬-zuener",
				"title": "战地6！开玩！七年之约已到！",
				"cover": "https://i0.hdslb.com/bfs/live/new_room_cover/b1779156686031460633d31362205456d1bb53df.jpg",
				"jump_url": "https://live.bilibili.com/5513659?broadcast_type=0&is_room_feed=1&live_from=28022",
				"switch": true,
				"num": 30035,
				"watch_icon": "https://i0.hdslb.com/bfs/live/a725a9e61242ef44d764ac911691a7ce07f36c1d.png",
				"live_status": 1,
				"text_small": "3.0万",
				"use_view_vt": false,
				"anchor_face": "https://i0.hdslb.com/bfs/face/bdb4b214d3446aca7c11b408ae6f35c89f52a5cc.jpg",
				"match_live_room": false,
				"match_info": null,
				"duration": 0,
				"up_name": "",
				"pub_date": "",
				"gather_id": 0,
				"sub_name": ""
			},
			{
				"order_id": 18,
				"view_type": 0,
				"view_id": 146007,
				"view_name": "Kisflow",
				"title": "战地6 BETA 战场老登职业哥",
				"cover": "https://i0.hdslb.com/bfs/live/new_room_cover/0007988a93c06215f0ffd96f7a4e3834d1396408.jpg",
				"jump_url": "https://live.bilibili.com/146007?broadcast_type=0&is_room_feed=1&live_from=28022",
				"switch": true,
				"num": 7839,
				"watch_icon": "https://i0.hdslb.com/bfs/live/a725a9e61242ef44d764ac911691a7ce07f36c1d.png",
				"live_status": 1,
				"text_small": "7839",
				"use_view_vt": false,
				"anchor_face": "https://i1.hdslb.com/bfs/face/5761dbf3f03b1a31ad8a6aec01452c97e93c16c0.jpg",
				"match_live_room": false,
				"match_info": null,
				"duration": 0,
				"up_name": "",
				"pub_date": "",
				"gather_id": 0,
				"sub_name": ""
			},
			{
				"order_id": 19,
				"view_type": 0,
				"view_id": 1163043,
				"view_name": "人形鹿头自走炮",
				"title": "神秘远光84男",
				"cover": "https://i0.hdslb.com/bfs/live/new_room_cover/cea622fe174d8c3fd26e58ea5a7e3b709fd8aee4.jpg",
				"jump_url": "https://live.bilibili.com/1163043?broadcast_type=0&is_room_feed=1&live_from=28022",
				"switch": true,
				"num": 20796,
				"watch_icon": "https://i0.hdslb.com/bfs/live/a725a9e61242ef44d764ac911691a7ce07f36c1d.png",
				"live_status": 1,
				"text_small": "2.0万",
				"use_view_vt": false,
				"anchor_face": "https://i2.hdslb.com/bfs/face/259c1f3b485ad5e2182446246fccb87114701ed8.jpg",
				"match_live_room": false,
				"match_info": null,
				"duration": 0,
				"up_name": "",
				"pub_date": "",
				"gather_id": 0,
				"sub_name": ""
			},
			{
				"order_id": 20,
				"view_type": 0,
				"view_id": 3343118,
				"view_name": "版尤黑紫",
				"title": "爽玩！战地6B测",
				"cover": "https://i0.hdslb.com/bfs/live/user_cover/039be5f223d26d4108941f1f056ee5842e3e5720.jpg",
				"jump_url": "https://live.bilibili.com/3343118?broadcast_type=0&is_room_feed=1&live_from=28022",
				"switch": true,
				"num": 1704,
				"watch_icon": "https://i0.hdslb.com/bfs/live/a725a9e61242ef44d764ac911691a7ce07f36c1d.png",
				"live_status": 1,
				"text_small": "1704",
				"use_view_vt": false,
				"anchor_face": "https://i2.hdslb.com/bfs/face/3cdcbc8945d18575279ac55c75f4da9f0a7dbc9e.jpg",
				"match_live_room": false,
				"match_info": null,
				"duration": 0,
				"up_name": "",
				"pub_date": "",
				"gather_id": 0,
				"sub_name": ""
			},
			{
				"order_id": 21,
				"view_type": 0,
				"view_id": 25212992,
				"view_name": "贝施汀",
				"title": "战地6还没开服，先直播剪会儿视频聊聊天",
				"cover": "https://i0.hdslb.com/bfs/live/new_room_cover/fb0227b71dca8555588c9c6c0af329cf250123a9.jpg",
				"jump_url": "https://live.bilibili.com/25212992?broadcast_type=0&is_room_feed=1&live_from=28022",
				"switch": true,
				"num": 2207,
				"watch_icon": "https://i0.hdslb.com/bfs/live/a725a9e61242ef44d764ac911691a7ce07f36c1d.png",
				"live_status": 1,
				"text_small": "2207",
				"use_view_vt": false,
				"anchor_face": "https://i0.hdslb.com/bfs/face/7242e856562166a27e8be4a184e4cddbaed8177f.jpg",
				"match_live_room": false,
				"match_info": null,
				"duration": 0,
				"up_name": "",
				"pub_date": "",
				"gather_id": 0,
				"sub_name": ""
			},
			{
				"order_id": 22,
				"view_type": 0,
				"view_id": 11313,
				"view_name": "丧心病狂的魔笑",
				"title": "等待测试开启！但是先直播周边开箱！",
				"cover": "https://i0.hdslb.com/bfs/live/new_room_cover/48fb912da0f665427eb230ef3273defdb1a33fa4.jpg",
				"jump_url": "https://live.bilibili.com/11313?broadcast_type=0&is_room_feed=1&live_from=28022",
				"switch": true,
				"num": 2924,
				"watch_icon": "https://i0.hdslb.com/bfs/live/a725a9e61242ef44d764ac911691a7ce07f36c1d.png",
				"live_status": 1,
				"text_small": "2924",
				"use_view_vt": false,
				"anchor_face": "https://i2.hdslb.com/bfs/face/e672848bc2718b79ca2f44eb447e84282c6f806d.jpg",
				"match_live_room": false,
				"match_info": null,
				"duration": 0,
				"up_name": "",
				"pub_date": "",
				"gather_id": 0,
				"sub_name": ""
			},
			{
				"order_id": 24,
				"view_type": 0,
				"view_id": 902302,
				"view_name": "LF叶绿",
				"title": "《田 野 打 架 6》",
				"cover": "https://i0.hdslb.com/bfs/live/new_room_cover/3b18086f9e70f719917c5d4561c25defdd13cd82.jpg",
				"jump_url": "https://live.bilibili.com/902302?broadcast_type=0&is_room_feed=1&live_from=28022",
				"switch": true,
				"num": 1897,
				"watch_icon": "https://i0.hdslb.com/bfs/live/a725a9e61242ef44d764ac911691a7ce07f36c1d.png",
				"live_status": 1,
				"text_small": "1897",
				"use_view_vt": false,
				"anchor_face": "https://i2.hdslb.com/bfs/face/5e3570095f5af77d20188ea45d45da216a31e52d.jpg",
				"match_live_room": false,
				"match_info": null,
				"duration": 0,
				"up_name": "",
				"pub_date": "",
				"gather_id": 0,
				"sub_name": ""
			}
		],
		"view_pattern": 1,
		"gather_room_list": []
	}
}
```

</details>
