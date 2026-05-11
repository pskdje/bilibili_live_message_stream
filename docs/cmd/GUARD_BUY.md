# 上舰通知 (GUARD_BUY)

## 下发条件

当有用户购买 舰长 / 提督 / 总督 时下发。

## JSON消息

| 字段 | 类型 | 内容        | 备注 |
| ---- | ---- | ----------- | ---- |
| cmd  | str  | `GUARD_BUY` |      |
| data | obj  | 信息本体    |      |

`data` 对象:

| 字段 | 类型  | 内容                       | 备注  |
| ---- |-----|--------------------------|-----|
| uid | num | 用户ID                     |     |
| username | str | 用户名称                     |     |
| guard_level | num | 大航海等级  |  1: 总督<br />2: 提督<br />3:舰长     |
| num | num | 数量                       |     |
| price | num | 原金瓜子标价                      | 即 CNY\*1000 |
| gift_id | num | 礼物id                     |     |
| gift_name | str | 礼物名称                     |     |
| start_time | num | 待调查                      |     |
| end_time | num | 待调查                      |     |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "GUARD_BUY",
	"data": {
		"uid": 14225357,
		"username": "妙妙喵喵妙妙喵O_O",
		"guard_level": 3,
		"num": 1,
		"price": 198000,
		"gift_id": 10003,
		"gift_name": "舰长",
		"start_time": 1677069316,
		"end_time": 1677069316
	}
}
```

</details>
