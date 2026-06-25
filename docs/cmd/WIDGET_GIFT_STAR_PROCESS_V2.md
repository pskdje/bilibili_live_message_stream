# ??? (WIDGET_GIFT_STAR_PROCESS_V2)

## 下发条件

*未知*

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| cmd | str | `WIDGET_GIFT_STAR_PROCESS_V2` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| name | str |  |  |
| cur_num | num |  |  |
| total_num | num |  |  |
| version | num | 数据版本 | UNIX 毫秒时间戳 |

## 示例

<details>
<summary>查看消息示例：</summary>

```json
{
	"cmd": "WIDGET_GIFT_STAR_PROCESS_V2",
	"data": {
		"name": "礼物星球",
		"cur_num": 0,
		"total_num": 9,
		"version": 1781588649772
	}
}
```

</details>
