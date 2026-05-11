# ??? (PLAYTOGETHER_ICON_CHANGE)

## 下发条件

部分主播切换分区时。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `PLAYTOGETHER_ICON_CHANGE` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| area_id | num | 直播分区id |  |
| has_perm | num |  |  |
| show_count | num |  |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "PLAYTOGETHER_ICON_CHANGE",
	"data": {
		"area_id": 40,
		"has_perm": 0,
		"show_count": 0
	}
}
```

</details>
