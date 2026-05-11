# 设立房管 (room_admin_entrance)

该 cmd 为小写。

## 下发条件

用户被设为房管时。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `room_admin_entrance` |  |
| dmscore | num | 弹幕分数? |  |
| level | num | 等级? |  |
| msg | str | 提示信息 |  |
| uid | num | 用户 mid |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "room_admin_entrance",
	"dmscore": 45,
	"level": 1,
	"msg": "系统提示：你已被主播设为房管",
	"uid": 223134
}
```

</details>
