# 送礼 (SEND_GIFT)

## 下发条件

有人为主播送礼后。

## JSON消息

根对象:

| 字段 | 类型 | 内容        | 备注 |
| ---- | ---- | ----------- | ---- |
| cmd  | str  | `SEND_GIFT` |      |
| data | obj  | 消息本体    |      |

`data` 对象:

| 字段 | 类型   | 内容  | 备注    |
| ---- | ---- | ----- | ------ |
| action | str | 礼物操作，一般为"投喂" |  |
| batch_combo_id | str | 待调查 | 有时为空字符串 |
| batch_combo_send | obj | 待调查 | 有时为null |
| beatId | str | 待调查 |  |
| biz_source | str | 待调查 |  |
| blind_gift | | 待调查 |  |
| broadcast_id | num | 待调查 |  |
| coin_type | str | 标识金银瓜子礼物对应是否付费? |  |
| combo_resources_id | num | 待调查 |  |
| combo_send | | 待调查 |  |
| comber_stay_time | num | 待调查 |  |
| combo_total_coin | num | 待调查 |  |
| crit_prob | num | 待调查 |  |
| demarcation | num | 待调查 |  |
| discount_price | num | 待调查 |  |
| dmscore | num | 待调查 |  |
| draw | num | 待调查 |  |
| effect | num | 待调查 |  |
| effect_block | num | 待调查 |  |
| face | str | 礼物投喂者的头像URL |  |
| face_effect_id | num | 待调查 |  |
| face_effect_type | num | 待调查 |  |
| float_sc_resource_id | num | 待调查 |  |
| giftId | num | 礼物ID |  |
| giftName | str | 礼物名称 |  |
| giftType | num | 待调查 |  |
| gold | number | 待调查 |  |
| guard_level | num | 待调查 |  |
| is_first | bool | 待调查 |  |
| is_join_receiver | bool | 待调查 |  |
| is_naming | bool | 待调查 |  |
| is_special_batch | num | 待调查 |  |
| magnification | num | 待调查 |  |
| medal_info | obj | 礼物投喂者粉丝奖牌信息 |  |
| name_color | str | 待调查 |  |
| num | num | 该次投喂的礼物数量 |  |
| original_gift_name | str | 待调查 |  |
| price | num | 价值 |  |
| rcost | num | 待调查 |  |
| receive_user_info | obj | 礼物接收者信息，一般是主播 |  |
| remain | num | 待调查 |  |
| rnd | num | 礼物发送时的时间戳，以及后面9位未知数字 |  |
| send_master | | 待调查 |  |
| silver | num | 待调查 |  |
| super | num | 待调查 |  |
| super_batch_gift_num | num | 待调查 |  |
| super_gift_num | num | 待调查 |  |
| svga_block | num | 待调查 |  |
| switch | bool | 待调查 |  |
| tag_image | str | 待调查 |  |
| tid | num | 礼物发送时的时间戳，以及后面9位未知数字 | 似乎与rnd字段相同 |
| timestamp | num | 礼物发送时的时间戳 |  |
| top_list | | 待调查 |  |
| total_coin | num | 实际金银瓜子总价值 | 不是总等于 num*price |
| uid | num | 礼物投喂者的UID |  |
| uname | str | 礼物投喂者的名称 |  |

`data.batch_combo_send` 对象:

| 字段 |    类型   |  内容  |    备注    |
| ---- | -------- | ------ | --------- |
| action | str | 礼物操作，一般为"投喂" | |
| batch_combo_id | str | 待调查 | |
| batch_combo_num | num | 待调查 | |
| blind_gift | | 待调查 | |
| gift_id | num | 待调查 | |
| gift_name | str | 投喂的礼物名称 | 待调查 |
| gift_num | num | 投喂礼物数量 | 待调查 |
| send_master | | 待调查 | |
| uid | num | 礼物投喂者的UID | |
| uname | str | 礼物投喂者的名称 | |

`data.medal_info` 对象:

| 字段 | 类型   | 内容  | 备注    |
| ---- | ----- | ----- | ------- |
| anchor_roomid | num | 待调查 |  |
| anchor_uname | str | 待调查 |  |
| guard_level | num | 待调查 |  |
| icon_id | num | 待调查 |  |
| is_lighted | num | 待调查 |  |
| medal_color | num | 礼物投喂者的粉丝奖牌颜色 | 十六进制颜色值转为了十进制表示 |
| medal_border_color | num | 礼物投喂者的粉丝奖牌边框颜色 | 十六进制颜色值的十进制表示 |
| medal_color_end | num | 待调查 |  |
| medal_color_start | num | 待调查 |  |
| medal_level | num | 礼物投喂者的粉丝奖牌等级 |  |
| medal_name | str | 礼物投喂者的粉丝奖牌名称 |  |
| special | str | 待调查 |  |
| target_id | num | 待调查 |  |

`data.receive_user_info` 对象:

| 字段 | 类型   | 内容  | 备注    |
| ---- | ----- | ----- | ------- |
| uid | num | 礼物接收者的UID | 一般为主播的UID |
| uname | str | 礼物接收者的名称 | 一般为主播的名称 |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "SEND_GIFT",
	"data": {
		"action": "投喂",
		"batch_combo_id": "batch:gift:combo_id:510149209:36047134:31036:1673622464.8445",
		"batch_combo_send": {
			"action": "投喂",
			"batch_combo_id": "batch:gift:combo_id:510149209:36047134:31036:1673622464.8445",
			"batch_combo_num": 1,
			"blind_gift": null,
			"gift_id": 31036,
			"gift_name": "小花花",
			"gift_num": 1,
			"send_master": null,
			"uid": 510149209,
			"uname": "12138额83121"
		},
		"beatId": "",
		"biz_source": "live",
		"blind_gift": null,
		"broadcast_id": 0,
		"coin_type": "gold",
		"combo_resources_id": 1,
		"combo_send": {
			"action": "投喂",
			"combo_id": "gift:combo_id:510149209:36047134:31036:1673622464.8434",
			"combo_num": 1,
			"gift_id": 31036,
			"gift_name": "小花花",
			"gift_num": 1,
			"send_master": null,
			"uid": 510149209,
			"uname": "12138额83121"
		},
		"combo_stay_time": 3,
		"combo_total_coin": 100,
		"crit_prob": 0,
		"demarcation": 1,
		"discount_price": 100,
		"dmscore": 8,
		"draw": 0,
		"effect": 0,
		"effect_block": 0,
		"face": "https://i1.hdslb.com/bfs/face/fb79103e8b33547023e2010030b6889bba2b49bf.jpg",
		"face_effect_id": 0,
		"face_effect_type": 0,
		"float_sc_resource_id": 0,
		"giftId": 31036,
		"giftName": "小花花",
		"giftType": 0,
		"gold": 0,
		"guard_level": 0,
		"is_first": true,
		"is_join_receiver": false,
		"is_naming": false,
		"is_special_batch": 0,
		"magnification": 1,
		"medal_info": {
			"anchor_roomid": 0,
			"anchor_uname": "",
			"guard_level": 0,
			"icon_id": 0,
			"is_lighted": 0,
			"medal_color": 0,
			"medal_color_border": 0,
			"medal_color_end": 0,
			"medal_color_start": 0,
			"medal_level": 0,
			"medal_name": "",
			"special": "",
			"target_id": 0
		},
		"name_color": "",
		"num": 1,
		"original_gift_name": "",
		"price": 100,
		"rcost": 164536872,
		"receive_user_info": {
			"uid": 36047134,
			"uname": "小霖QL"
		},
		"remain": 0,
		"rnd": "1673622464121900003",
		"send_master": null,
		"silver": 0,
		"super": 0,
		"super_batch_gift_num": 1,
		"super_gift_num": 1,
		"svga_block": 0,
		"switch": true,
		"tag_image": "",
		"tid": "1673622464121900003",
		"timestamp": 1673622464,
		"top_list": null,
		"total_coin": 100,
		"uid": 510149209,
		"uname": "12138额83121"
	}
}
```

</details>
