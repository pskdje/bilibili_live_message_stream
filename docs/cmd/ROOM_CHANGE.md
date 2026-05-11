# 直播间信息更改 (ROOM_CHANGE)

## 下发条件

直播间标题更改、直播间分区更改。

## JSON消息

根对象:

| 字段 | 类型 | 内容  | 备注 |
| ---- | ---- | ---- | ---- |
| cmd  | str | `ROOM_CHANGE` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| title | str | 直播间标题 |  |
| area_id | num | 当前直播间所属二级分区的ID |  |
| parent_area_id | num |  当前直播间所属一级分区的ID |  |
| area_name | str | 当前直播间所属二级分区的名称 |  |
| parent_area_name | str |  当前直播间所属一级分区名称 |  |
| live_key | str | 标记直播场次的key | 未开播更新直播间信息时为`"0"` |
| sub_session_key | str | 待调查 | 未开播更新直播间信息时为`""`(空字符串) |

## 示例

<details>
<summary>查看消息示例:</summary>

已开播:

```json
{
	"cmd": "ROOM_CHANGE",
	"data": {
		"title": "开始白给CS",
		"area_id": 371,
		"parent_area_id": 9,
		"area_name": "虚拟主播",
		"parent_area_name": "虚拟主播",
		"live_key": "320830629635915849",
		"sub_session_key": "320830629635915849sub_time:1673690546"
	}
}
```

未开播:

```json
{
	"cmd": "ROOM_CHANGE",
	"data": {
		"title": "随缘",
		"area_id": 216,
		"parent_area_id": 6,
		"area_name": "我的世界",
		"parent_area_name": "单机游戏",
		"live_key": "0",
		"sub_session_key": ""
	}
}
```

</details>
