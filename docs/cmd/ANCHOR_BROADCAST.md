# 直播小助手? (ANCHOR_BROADCAST)

## 下发条件

第一次达到了某种条件时。

已知：达到特定直播时长、特定分享数量。

原先用于记录的 issue 已不可用，无法补充。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `ANCHOR_BROADCAST` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| sender | str | 标题? | `直播小助手` |
| msg | str | 提示消息 |  |
| platform | num | 平台标识? | `0` |
| button_info | obj | 按钮信息? |  |
| milestone_type | str | 里程碑类型? | `session_livetime`，`first_share`，`session_share` |
| milestone_value | num | 里程值? |  |
| milestone_index | num | 里程碑类型的索引? | `1`，`5`，`6`，`7` |

`data.button_info` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| button_name | str |  |  |
| blink_button_type | str |  |  |
| blink_button_target | str |  |  |
| blink_button_extra | str |  |  |
| blink_button_label | num |  |  |
| hime_button_type | str |  |  |
| hime_button_target | str |  |  |
| hime_button_extra | str |  |  |
| hime_button_h5_type | str |  |  |
| hime_button_label | num |  |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "ANCHOR_BROADCAST",
	"data": {
		"sender": "直播小助手",
		"msg": "恭喜你，开播时长达到180分钟！",
		"platform": 0,
		"button_info": {
			"button_name": "",
			"blink_button_type": "",
			"blink_button_target": "",
			"blink_button_extra": "",
			"blink_button_label": 0,
			"hime_button_type": "",
			"hime_button_target": "",
			"hime_button_extra": "",
			"hime_button_h5_type": "",
			"hime_button_label": 0
		},
		"milestone_type": "session_livetime",
		"milestone_value": 10800,
		"milestone_index": 6
	}
}
```

</details>
