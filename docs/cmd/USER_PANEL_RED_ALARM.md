# ??? (USER_PANEL_RED_ALARM)

## 下发条件

*未知*

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `USER_PANEL_RED_ALARM` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| module | str | (?) |  |
| alarm_num | num | (?) |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "USER_PANEL_RED_ALARM",
	"data": {
		"module": "user_head_dot",
		"alarm_num": 1
	}
}
```

</details>
