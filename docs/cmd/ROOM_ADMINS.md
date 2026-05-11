# 房管列表 (ROOM_ADMINS)

## 下发条件

房管列表更新时。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `ROOM_ADMINS` |  |
| uids | array | 房管 mid 列表 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "ROOM_ADMINS",
	"uids": [ 898424, 384203692, 1309513, 30816752, 23931549, 223134 ]
}
```

</details>
