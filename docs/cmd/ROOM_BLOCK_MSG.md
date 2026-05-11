# 指定观众禁言 (ROOM_BLOCK_MSG)

## 下发条件

将指定观众禁言时。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `ROOM_BLOCK_MSG` |  |
| data | obj | 详细信息 |  |
| uid | num | 禁言用户 mid |  |
| uname | str | 禁言用户名 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| dmscore | num | 弹幕分数? |  |
| operator | num | 操作者? |  |
| uid | num | 禁言用户 mid |  |
| uname | str | 禁言用户名 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "ROOM_BLOCK_MSG",
	"data": {
		"dmscore": 30,
		"operator": 2,
		"uid": 37903025,
		"uname": "玉麟珑"
	},
	"uid": "37903025",
	"uname": "玉麟珑"
}
```

</details>
