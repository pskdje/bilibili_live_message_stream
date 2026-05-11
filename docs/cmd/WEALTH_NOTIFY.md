# 荣耀等级通知 (WEALTH_NOTIFY)

## 下发条件

荣耀等级变化时。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `WEALTH_NOTIFY` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| flag | num | 标志? |  |
| info | obj | 信息 |  |

`data.info`:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| effect_key | num | (?) |  |
| has_items_changed | num | (?) |  |
| level | num | 达到的等级 |  |
| send_time | num | 发送时间 | UNIX 毫秒时间戳 |
| status | num | 状态? |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "WEALTH_NOTIFY",
	"data": {
		"flag": 3,
		"info": {
			"effect_key": 1073,
			"has_items_changed": 1,
			"level": 5,
			"send_time": 1743337942833,
			"status": 1
		}
	}
}
```

</details>
