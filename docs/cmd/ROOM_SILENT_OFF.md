# 关闭等级禁言 (ROOM_SILENT_OFF)

## 下发条件

关闭等级禁言。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| data | obj | 信息本体 |  |
| cmd | str | `ROOM_SILENT_OFF` |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| type | str | 空 |  |
| level | num | 0 |  |
| second | num | 0 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"data": {
		"type": "",
		"level": 0,
		"second": 0
	},
	"cmd": "ROOM_SILENT_OFF"
}
```

</details>
