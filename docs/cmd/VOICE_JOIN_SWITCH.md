# 语音连麦开关 (VOICE_JOIN_SWITCH)

## 下发条件

在直播姬开关连麦功能时。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `VOICE_JOIN_SWITCH` |  |
| data | obj | 信息本体 |  |
| room_id | num | 直播间id |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| room_id | num | 直播间id |  |
| room_status | num | 连麦开关状态 |  |
| root_status | num | 连麦开关状态 |  |

## 示例

<details>
<summary>开:</summary>

```json
{
	"cmd": "VOICE_JOIN_SWITCH",
	"data": {
		"room_id": 1899237171,
		"room_status": 1,
		"root_status": 1
	},
	"room_id": 1899237171
}
```

</details>

<details>
<summary>关:</summary>

```json
{
	"cmd": "VOICE_JOIN_SWITCH",
	"data": {
		"room_id": 1899237171,
		"room_status": 0,
		"root_status": 0
	},
	"room_id": 1899237171
}
```

</details>
