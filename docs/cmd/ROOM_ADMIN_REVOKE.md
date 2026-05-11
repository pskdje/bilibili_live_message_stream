# 撤销房管 (ROOM_ADMIN_REVOKE)

## 下发条件

撤销用户的房管权限时。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `ROOM_ADMIN_REVOKE` |  |
| msg | str | 提示信息 |  |
| uid | num | 用户 mid |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "ROOM_ADMIN_REVOKE",
	"msg": "撤销房管",
	"uid": 6791627
}
```

</details>
