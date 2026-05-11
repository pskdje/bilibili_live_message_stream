# ??? (RECALL_DANMU_MSG)

## 下发条件

*未知*

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `RECALL_DANMU_MSG` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| recall_type | num | 类型? | `2` |
| target_id | num |  |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "RECALL_DANMU_MSG",
	"data": {
		"recall_type": 2,
		"target_id": 525503743
	}
}
```

</details>
