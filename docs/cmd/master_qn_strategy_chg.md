# ??? (master_qn_strategy_chg)

## 下发条件

*未知*

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `master_qn_strategy_chg` |  |
| data | str | 信息本体 | JSON文本 |

`data` JSON解析后对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| mtime | num | (?) | Unix秒时间戳 |
| scatter | arr | (?) |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "master_qn_strategy_chg",
	"data": "{\"mtime\":1744380444,\"scatter\":[0,300]}"
}
```

</details>
