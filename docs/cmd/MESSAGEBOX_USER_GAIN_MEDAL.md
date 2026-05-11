# 获得粉丝勋章 (MESSAGEBOX_USER_GAIN_MEDAL)

## 下发条件

获得粉丝勋章时下发。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `MESSAGEBOX_USER_GAIN_MEDAL` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| type | num | 类型 | 0 |
| uid | num | 用户mid |  |
| up_uid | num | 主播uid |  |
| medal_id | num | 勋章id |  |
| medal_name | str | 勋章名称 |  |
| medal_level | num | 勋章等级 |  |
| medal_color | num | 勋章颜色 |  |
| medal_color_start | num | 十进制勋章起始颜色 |  |
| medal_color_end | num | 十进制勋章结束颜色 |  |
| medal_color_border | num | 十进制勋章边框颜色 |  |
| msg_title | str | 消息标题 |  |
| msg_content | str | 消息内容 |  |
| normal_color | num | (?) |  |
| highlight_color | num | (?) |  |
| intimacy | num | 当前亲密度 |  |
| next_intimacy | num | 升级所需亲密度 |  |
| today_feed | num | 今日亲密度 |  |
| day_limit | num | 今日亲密度上限 |  |
| is_wear | num | (?) |  |
| guard_level | num | 大航海等级 |  |
| is_received | num | (?) |  |
| is_lighted | num | 是否点亮? | 1：点亮? |
| is_lighted_v2 | bool | 是否点亮v2? |  |
| toast | str | 提示 |  |
| fan_name | str | 粉丝名称 |  |
| uinfo_medal | obj | 粉丝勋章信息 | 参见 ~~[指定用户的所有粉丝勋章信息](https://github.com/pskdje/bilibili-API-collect/blob/main/docs/user/medals.md#指定用户的所有粉丝勋章信息)~~ `data.list[n].uinfo_medal` 对象 |

`data.uinfo_medal` 对象:

参见 ~~[指定用户的所有粉丝勋章信息](https://github.com/pskdje/bilibili-API-collect/blob/main/docs/user/medals.md#指定用户的所有粉丝勋章信息)~~ json回复的 `data.list[n].uinfo_medal` 对象。

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "MESSAGEBOX_USER_GAIN_MEDAL",
	"data": {
		"type": 0,
		"uid": 438160221,
		"up_uid": 11602644,
		"medal_id": 19252517,
		"medal_name": "广药",
		"medal_level": 1,
		"medal_color": 6067854,
		"medal_color_start": 6067854,
		"medal_color_end": 6067854,
		"medal_color_border": 6067854,
		"msg_title": "恭喜你获得【WuGuangYao】的粉丝勋章~",
		"msg_content": "获得100点亲密度\n你的粉丝勋章达到1级",
		"normal_color": 7697781,
		"highlight_color": 16478873,
		"intimacy": 100,
		"next_intimacy": 201,
		"today_feed": 100,
		"day_limit": 2000,
		"is_wear": 0,
		"guard_level": 0,
		"is_received": 1,
		"is_lighted": 1,
		"is_lighted_v2": true,
		"toast": "成功入团并关注主播，得1级大礼包",
		"fan_name": "weatfe",
		"uinfo_medal": {
			"name": "广药",
			"level": 1,
			"color_start": 6067854,
			"color_end": 6067854,
			"color_border": 6067854,
			"color": 6067854,
			"id": 19252517,
			"typ": 0,
			"is_light": 1,
			"ruid": 11602644,
			"guard_level": 0,
			"score": 0,
			"guard_icon": "",
			"honor_icon": "",
			"v2_medal_color_start": "#5762A799",
			"v2_medal_color_end": "#5762A799",
			"v2_medal_color_border": "#5762A799",
			"v2_medal_color_text": "#FFFFFFFF",
			"v2_medal_color_level": "#000B7099",
			"user_receive_count": 0
		}
	}
}
```

</details>
