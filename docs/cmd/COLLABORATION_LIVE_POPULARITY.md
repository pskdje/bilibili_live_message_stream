# 跨房人气 (COLLABORATION_LIVE_POPULARITY)

特定情况下统计相关直播间的人气数据。

## 下发条件

相关数据更新时。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `COLLABORATION_LIVE_POPULARITY` |  |
| data | str | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| num | num | 人气值 |  |
| text | str | 人气值文本 |  |
| text_large | str | 完整人气值文本 |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "COLLABORATION_LIVE_POPULARITY",
	"data": {
		"num": 8201776,
		"text": "820.1万",
		"text_large": "820.1万人气"
	}
}
```

</details>
