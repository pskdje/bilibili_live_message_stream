# 自动关注 (CONFIRM_AUTO_FOLLOW)

## 下发条件

未关注状态下投喂礼物后可能下发。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `CONFIRM_AUTO_FOLLOW` |  |
| data | str | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| type | num | (?) | 作用尚不明确 |
| uid | num | 用户uid |  |
| ruid | num | 主播uid |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "CONFIRM_AUTO_FOLLOW",
	"data": {
		"type": 9,
		"uid": 438160221,
		"ruid": 431073645
	}
}
```

</details>
