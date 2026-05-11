# 开启等级禁言 (ROOM_SILENT_ON)

## 下发条件

开启等级禁言。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| data | obj | 信息本体 |  |
| cmd | str | `ROOM_SILENT_ON` |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| type | str | 类型? |  |
| level | num | 等级? |  |
| second | num | 时间? | UNIX 秒级时间戳 |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"data": {
		"type": "member",
		"level": 1,
		"second": 1651000426
	},
	"cmd": "ROOM_SILENT_ON"
}
```

</details>
