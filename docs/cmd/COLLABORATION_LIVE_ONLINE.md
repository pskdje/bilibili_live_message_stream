# 跨房在线 (COLLABORATION_LIVE_ONLINE)

特定情况下统计相关直播间的在线数据。

## 下发条件

相关数据更新时。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `COLLABORATION_LIVE_ONLINE` |  |
| data | str | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| num | num | 在线人数 | 存在上限 |
| text | str | 在线人数文本 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "COLLABORATION_LIVE_ONLINE",
	"data": {
		"num": 9999,
		"text": "9999+"
	}
}
```

</details>
