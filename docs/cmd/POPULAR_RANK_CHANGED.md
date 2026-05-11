# 直播间在人气榜的排名改变 (POPULAR_RANK_CHANGED)

## 下发条件

直播间在人气榜的排名改变时。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| cmd  | str | `POPULAR_RANK_CHANGED` |  |
| data | obj | 直播间的人气榜排名信息 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| uid | num | 主播 mid |  |
| rank | num | 人气榜排名 |  |
| countdown | num | 人气榜下轮结算剩余时长 |  |
| timestamp | num | 触发时的Unix时间戳 |  |
| cache_key | str | 待调查 |  |

## 示例

<details>
<summary>查看消息示例：</summary>

```json
{
	"cmd": "POPULAR_RANK_CHANGED",
	"data": {
		"uid": 780791,
		"rank": 36,
		"countdown": 1927,
		"timestamp": 1702578474,
		"cache_key": "rank_change:91a4e81ba3034ae894d61e432aa13081"
	}
}
```

</details>
