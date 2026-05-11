# 直播间内容审核报告 (ROOM_CONTENT_AUDIT_REPORT)

## 下发条件

更新直播间标题且使用主播的登录信息才会下发，更新直播间标题后一般不会立刻下发。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| cmd | str | `ROOM_CONTENT_AUDIT_REPORT` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| audit_content_type | num | 审核内容类型? |  |
| room_id | num | 直播间ID | 未知是真实ID还是短号 |
| anchor_uid | num | 主播的用户mid |  |
| audit_status | num | 审核状态? |  |
| audit_title | str | 被审核的直播间标题 |  |
| audit_reason | str | 审核结果 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "ROOM_CONTENT_AUDIT_REPORT",
	"data": {
		"audit_content_type": 1,
		"room_id": 1899237171,
		"anchor_uid": 438160221,
		"audit_status": 2,
		"audit_title": "崩坏学园2",
		"audit_reason": "一审通过"
	}
}
```

</details>
