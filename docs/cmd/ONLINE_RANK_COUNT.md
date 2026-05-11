# 直播间高能用户数量 (ONLINE_RANK_COUNT)

## 下发条件

data 对象内的数据有更新后。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| cmd | str | `ONLINE_RANK_COUNT` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容   | 备注      |
| ---- | ---- | ------ | --------- |
| count | num | 直播间高能用户数量 | 存在上限 |
| count_text | str | 直播间高能用户数量文本 |  |
| online_count | num | 直播间在线用户数量 | 存在上限 |
| online_count_text | str | 直播间在线用户数量文本 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "ONLINE_RANK_COUNT",
	"data": {
		"count": 1084,
		"count_text": "1084",
		"online_count": 1084,
		"online_count_text": "1084"
	}
}
```

</details>
