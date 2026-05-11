# 醒目留言删除 (SUPER_CHAT_MESSAGE_DELETE)

## 下发条件

要删除某条醒目留言时下发。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `SUPER_CHAT_MESSAGE_DELETE` |  |
| data | obj | 消息本体 |  |
| roomid | num | 直播间ID |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| ids | arr | 待删除的醒目留言 ID 列表 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "SUPER_CHAT_MESSAGE_DELETE",
	"data": {
		"ids": [
			3897503
		]
	},
	"roomid": 23708804
}
```

</details>
