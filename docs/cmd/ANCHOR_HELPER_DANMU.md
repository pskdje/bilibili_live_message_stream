# 直播小助手? (ANCHOR_HELPER_DANMU)

几乎与`ANCHOR_BROADCAST`一同下发。

## 下发条件

参见 [ANCHOR_BROADCAST](ANCHOR_BROADCAST.md) 。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `ANCHOR_HELPER_DANMU` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| sender | str | 标题? | `直播小助手` |
| msg | str | 提示消息 |  |
| platform | num | 平台标识? |  |
| button_platform | num |  |  |
| button_name | str |  |  |
| button_target | str |  |  |
| button_label | num |  |  |
| report_type | str | 上报类型? |  |
| report | str |  |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "ANCHOR_HELPER_DANMU",
	"data": {
		"sender": "直播小助手",
		"msg": "恭喜你，开播时长达到150分钟！",
		"platform": 3,
		"button_platform": 0,
		"button_name": "",
		"button_target": "",
		"button_label": 0,
		"report_type": "milestone",
		"report": "session_livetime:5:9000"
	}
}
```

</details>
