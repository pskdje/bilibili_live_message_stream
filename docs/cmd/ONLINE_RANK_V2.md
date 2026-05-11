# 直播间高能榜 (ONLINE_RANK_V2)

在线榜已被 `ONLINE_RANK_V3` 替换

## 下发条件

直播间高能用户数据刷新。

## JSON消息

根对象:

| 字段 | 类型 | 内容   | 备注      |
| ---- | ---- | ------ | --------- |
| cmd | str | `ONLINE_RANK_V2` |  |
| data | obj | 直播间高能用户数据 |  |

`data` 对象:

| 字段 | 类型 | 内容   | 备注      |
| ---- | ---- | ------ | --------- |
| list | array | 在直播间高能用户中的用户信息 | |
| rank_type | str | 榜单类型 |  |

`data.list[n]` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| uid | num | 用户 mid |  |
| face | str | 用户头像 URL |  |
| score | str | 该用户的贡献值 |  |
| uname | str | 用户名称 |  |
| rank | num | 该用户在高能榜中的排名 |  |
| guard_level | num | 大航海等级? |  |
| is_mystery | bool |  |  |
| uinfo | obj | 用户信息 |  |

## 示例

<details>
<summary>查看消息示例：</summary>

```json
{
	"cmd": "ONLINE_RANK_V2",
	"data": {
		"list": [
			{
				"uid": 2082621455,
				"face": "https://i2.hdslb.com/bfs/face/9de6050277fa13d830eb97e3453d89843de46a31.jpg",
				"score": "20",
				"uname": "8级萌新_小华",
				"rank": 1,
				"guard_level": 0
			},
			{
				"uid": 50500335,
				"face": "https://i0.hdslb.com/bfs/face/ca722209251478ef0ffb45c3adeafb9dab283c57.jpg",
				"score": "20",
				"uname": "属官一号",
				"rank": 2,
				"guard_level": 0
			},
			{
				"uid": 29857468,
				"face": "https://i1.hdslb.com/bfs/face/7b4ae2e7e950f2dfb2bd969859c813487ce3b64c.jpg",
				"score": "12",
				"uname": "露萌不要雨草",
				"rank": 3,
				"guard_level": 0
			}
		],
		"rank_type": "gold-rank"
	}
}
```

</details>
