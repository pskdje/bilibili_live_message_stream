# 用户到达直播间高能榜前三名的消息 (ONLINE_RANK_TOP3)

*已弃用*

## 下发条件

用户成为直播间高能榜前三名时。

## JSON消息

根对象:

| 字段 | 类型 | 内容  | 备注 |
| ---- | ---- | ---- | ---- |
| cmd  | str | `ONLINE_RANK_TOP3` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| dmscore | num | 待调查 |  |
| list | array | 消息内容和高能榜排名 |  |

`data.list[n]` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| msg | str | 消息内容 |  |
| rank | num | 该用户的高能榜排名 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "ONLINE_RANK_TOP3",
	"data": {
		"dmscore": 112,
		"list": [
			{
				"msg": "恭喜 <%你干嘛哈哈哎哟%> 成为高能用户",
				"rank": 1
			}
		]
	}
}
```

</details>
