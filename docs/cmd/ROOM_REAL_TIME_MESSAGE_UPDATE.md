# 主播信息更新 (ROOM_REAL_TIME_MESSAGE_UPDATE)

## 下发条件

`data`对象内的字段有更新后。

## JSON消息

根对象:

| 字段 | 类型 | 内容   | 备注      |
| ---- | ---- | ------ | --------- |
| cmd | str | `ROOM_REAL_TIME_MESSAGE_UPDATE` | |
| data | obj | 信息本体 | |

`data` 对象:

| 字段 | 类型 | 内容   | 备注      |
| ---- | ---- | ------ | --------- |
| roomid | num | 直播间ID | 未知是真实ID还是短号 |
| fans | num | 主播当前粉丝数 |  |
| red_notice | num | 待调查 |  |
| fans_club | num | 主播粉丝团人数 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "ROOM_REAL_TIME_MESSAGE_UPDATE",
	"data": {
		"roomid": 8618057,
		"fans": 136,
		"red_notice": -1,
		"fans_club": 8
	}
}
```

</details>
