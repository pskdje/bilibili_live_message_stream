# 人气值更新 (POPULARITY_CHANGE)

## 下发条件

在会计算人气值的直播间中定时下发，时间间隔约 1 分钟。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| cmd | str | `POPULARITY_CHANGE` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| type | num | (?) |  |
| popularity | num | 人气值 | 与心跳包回复的人气值相同 |
| popularity_text | str | 人气文本 |  |

## 示例

<details>
<summary>查看消息示例：</summary>

```json
{
	"cmd": "POPULARITY_CHANGE",
	"data": {
		"type": 2,
		"popularity": 55638,
		"popularity_text": "5.6万人气"
	}
}
```

</details>
