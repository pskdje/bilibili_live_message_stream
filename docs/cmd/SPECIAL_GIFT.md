# 特殊礼物 (SPECIAL_GIFT)

## 下发条件

*未知*

## JSON消息

根对象:

| 字段 | 类型 | 内容           | 备注 |
| ---- | ---- | -------------- | ---- |
| cmd  | str  | `SPECIAL_GIFT` |      |
| data | obj  | 信息本体       |      |

`data` 对象:

以 数字 为键, JSON Object 为值的表

`data['?']` 对象:

| 字段      | 类型 | 内容         | 备注 |
| --------- | ---- | ------------ | ---- |
| action    | str  | 操作?        |      |
| content   | str  | 内容         |      |
| hadJoin   | num  | 是否加入?    |      |
| id        | str  | ?            | 字符串表示的数字 |
| num       | str  | 数量         |      |
| storm_gif | str  | GIF 动画 URL |      |
| time      | str  | 持续时间?    |      |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "SPECIAL_GIFT",
	"data": {
		"39": {
			"action": "start",
			"content": "可爱即正义~~",
			"hadJoin": 0,
			"id": "3306976431489",
			"num": 1,
			"storm_gif": "http://static.hdslb.com/live-static/live-room/images/gift-section/mobilegift/2/jiezou.gif?2017011901",
			"time": 90
		}
	}
}
```

</details>
