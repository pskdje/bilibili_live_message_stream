# 跨房看过 (COLLABORATION_LIVE_WATCHED)

特定情况下统计相关直播间的看过数据。

## 下发条件

相关数据更新后。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `COLLABORATION_LIVE_WATCHED` |  |
| data | str | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| num | num | 看过人数 |  |
| text_small | str | 看过人数文本 |  |
| text_large | str | 完整看过人数文本 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "COLLABORATION_LIVE_WATCHED",
	"data": {
		"num": 1927773,
		"text_small": "192.7万",
		"text_large": "192.7万人看过"
	}
}
```

</details>
