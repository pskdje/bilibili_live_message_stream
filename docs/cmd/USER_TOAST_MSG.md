# 用户庆祝消息 (USER_TOAST_MSG)

## 下发条件

用户购买 舰长 / 提督 / 总督 后的庆祝消息，内容包含用户陪伴天数。

## JSON消息

根对象:

| 字段 | 类型 | 内容             | 备注 |
| ---- | ---- | ---------------- | ---- |
| cmd  | str  | `USER_TOAST_MSG` |      |
| data | obj  | 信息本体         |      |

`data` 对象:

| 字段 | 类型  | 内容 | 备注  |
| ---- |-----|-----|-----|
| anchor_show | bool | 是否显示 |     |
| color | str | 颜色 |     |
| dmscore | num | 待调查  |     |
| effect_id | num | 待调查 |     |
| face_effect_id | num | 待调查  |     |
| gift_id | num | 礼物id |     |
| group_name | str | 待调查  |     |
| group_op_type | num | 待调查   |     |
| group_role_name | str | 待调查  |     |
| guard_level | num | 大航海等级       | 1: 总督<br />2:<br />提督<br />3:舰长 |
| is_group | num | 待调查 |     |
| is_show | num | 待调查 |     |
| num | num | 上舰个数  |     |
| op_type | num | 待调查 |     |
| payflow_id | str | 待调查 |     |
| price | num | 实际金瓜子标价 | 即 CNY\*1000 |
| role_name | str | 身份名称 |     |
| room_effect_id | num | 待调查 |     |
| room_group_effect_id | num | 待调查 |     |
| start_time | num | 待调查 |     |
| svga_block | num | 待调查 |     |
| target_guard_count | str | 庆祝消息正文 |     |
| toast_msg | num | 待调查 |     |
| uid | num | 上舰人UID |     |
| unit | str | 购买身份时间单位 |     |
| user_show | bool | 待调查 |     |
| username | str | 上舰人用户名 |     |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "USER_TOAST_MSG",
	"data": {
		"anchor_show": true,
		"color": "#00D1F1",
		"dmscore": 90,
		"effect_id": 397,
		"end_time": 1702580687,
		"face_effect_id": 44,
		"gift_id": 10003,
		"group_name": "",
		"group_op_type": 0,
		"group_role_name": "",
		"guard_level": 3,
		"is_group": 0,
		"is_show": 0,
		"num": 1,
		"op_type": 1,
		"payflow_id": "2312150304155852173446521",
		"price": 138000,
		"role_name": "舰长",
		"room_effect_id": 590,
		"room_group_effect_id": 1337,
		"start_time": 1702580687,
		"svga_block": 0,
		"target_guard_count": 146,
		"toast_msg": "<%无光之日%> 在主播Mia米娅-的直播间开通了舰长，今天是TA陪伴主播的第1天",
		"uid": 79667344,
		"unit": "月",
		"user_show": true,
		"username": "无光之日"
	}
}
```

</details>
