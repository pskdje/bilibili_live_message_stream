# 礼物连击 (COMBO_SEND)

## 下发条件

连续赠送相同的礼物。

## JSON消息

根对象:

| 字段 | 类型 | 内容   | 备注 |
| ---- | ---- | ------ | ---- |
| cmd | str | `COMBO_SEND` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型   | 内容  | 备注    |
| ---- | ------ | ------ | ------ |
| action | str | 礼物操作，一般为"投喂" |  |
| batch_combo_id | str | 待调查 |  |
| batch_combo_num | num | 连击礼物数量 |  |
| combo_id | str | 待调查 |  |
| combo_num | str | 连击礼物数量 |  |
| combo_total_coin | num | 待调查 |  |
| dmscore | num | 待调查 |  |
| gift_id | num | 待调查 |  |
| gift_name | str | 连击礼物的名称 |  |
| gift_num | num | 0 |  |
| is_join_receiver | bool | 待调查 |  |
| is_naming | bool | 待调查 |  |
| is_show | num | 待调查 |  |
| medal_info | obj | 礼物投喂者的粉丝勋章信息 |  |
| name_color | str | 待调查 |  |
| r_uname | str | 主播的名称 |  |
| receive_user_info | obj | 主播的UID和名称 |  |
| ruid | num | 主播的UID |  |
| send_master | | 待调查 |  |
| total_num | num | 连击礼物数量 |  |
| uid | num | 礼物投喂者的UID |  |
| uname | str | 礼物投喂者的名称 |  |

`data.receive_user_info` 对象:

| 字段 | 类型   | 内容  | 备注    |
| ---- | ------ | ----- | ------ |
| uid | number | 礼物接收者的UID | 一般为主播的UID |
| uname | string | 礼物接收者的名称 | 一般为主播的名称 |

## 示例

<details>
<summary>查看消息示例：</summary>

```json
{
	"cmd": "COMBO_SEND",
	"data": {
		"action": "投喂",
		"batch_combo_id": "batch:gift:combo_id:3493090830584635:29857468:31036:1673774515.6190",
		"batch_combo_num": 2,
		"combo_id": "gift:combo_id:3493090830584635:29857468:31036:1673774515.6180",
		"combo_num": 2,
		"combo_total_coin": 200,
		"dmscore": 112,
		"gift_id": 31036,
		"gift_name": "小花花",
		"gift_num": 0,
		"is_join_receiver": false,
		"is_naming": false,
		"is_show": 1,
		"medal_info": {
			"anchor_roomid": 0,
			"anchor_uname": "",
			"guard_level": 0,
			"icon_id": 0,
			"is_lighted": 1,
			"medal_color": 6067854,
			"medal_color_border": 6067854,
			"medal_color_end": 6067854,
			"medal_color_start": 6067854,
			"medal_level": 3,
			"medal_name": "爱珞珞",
			"special": "",
			"target_id": 3493076559465366
		},
		"name_color": "",
		"r_uname": "露萌不要雨草",
		"receive_user_info": {
			"uid": 29857468,
			"uname": "露萌不要雨草"
		},
		"ruid": 29857468,
		"send_master": null,
		"total_num": 2,
		"uid": 3493090830584635,
		"uname": "DOC-Neo"
	}
}
```

</details>
