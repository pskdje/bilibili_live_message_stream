# 天选时刻合法检查 (ANCHOR_LOT_CHECKSTATUS)

## 下发条件

天选时刻合法检查后。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| cmd | str | `ANCHOR_LOT_CHECKSTATUS` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| id | num | 天选时刻id |  |
| reject_reason | str | 失败提示 |  |
| status | num | 审核状态 |  |
| uid | num | 主播 uid |  |

## 示例

<details>
<summary>查看响应示例:</summary>

```json
{
	"cmd": "ANCHOR_LOT_CHECKSTATUS",
	"data": {
		"id": 2553641,
		"reject_reason": "由于奖品格式不合格,请仔细检查后再提交哦",
		"status": 5,
		"uid": 1827176970
	}
}
```

</details>
