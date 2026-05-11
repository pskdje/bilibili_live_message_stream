# 粉丝勋章更新 (MESSAGEBOX_USER_MEDAL_CHANGE)

## 下发条件

当你升级或点亮粉丝勋章时将在你所有的登录会话下发。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `MESSAGEBOX_USER_MEDAL_CHANGE` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| type | num | 提示类型 | 1：升级<br />2：点亮 |
| uid | num | 用户mid |  |
| up_uid | num | 主播mid |  |
| medal_level | num | 粉丝勋章等级 |  |
| medal_name | str | 粉丝勋章名称 |  |
| medal_color_start | num | 十进制粉丝勋章起始颜色 |  |
| medal_color_end | num | 十进制粉丝勋章结束颜色 |  |
| medal_color_border | num | 十进制粉丝勋章边框颜色 |  |
| is_lighted | num | 是否点亮? | 1：点亮? |
| is_lighted_v2 | bool | 是否点亮v2? |  |
| guard_level | num | 大航海等级 |  |
| unlock | num | (?) |  |
| unlock_level | num | (?) |  |
| multi_unlock_level | str | (?) |  |
| upper_bound_content | str | 提示内容 |  |
| uinfo_medal | obj | 粉丝勋章信息 | 参见 ~~[指定用户的所有粉丝勋章信息](https://github.com/pskdje/bilibili-API-collect/blob/main/docs/user/medals.md#指定用户的所有粉丝勋章信息)~~ `data.list[n].uinfo_medal` 对象 |
| effect_id | num | (?) |  |

`data.uinfo_medal` 对象:

参见 ~~[指定用户的所有粉丝勋章信息](https://github.com/pskdje/bilibili-API-collect/blob/main/docs/user/medals.md#指定用户的所有粉丝勋章信息)~~ json回复的 `data.list[n].uinfo_medal` 对象。

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "MESSAGEBOX_USER_MEDAL_CHANGE",
	"data": {
		"type": 2,
		"uid": 438160221,
		"up_uid": 407045223,
		"medal_level": 3,
		"medal_name": "研究猿",
		"medal_color_start": 6067854,
		"medal_color_end": 6067854,
		"medal_color_border": 6067854,
		"is_lighted": 1,
		"is_lighted_v2": true,
		"guard_level": 0,
		"unlock": 0,
		"unlock_level": 0,
		"multi_unlock_level": "",
		"upper_bound_content": "",
		"uinfo_medal": {
			"name": "研究猿",
			"level": 3,
			"color_start": 6067854,
			"color_end": 6067854,
			"color_border": 6067854,
			"color": 0,
			"id": 0,
			"typ": 0,
			"is_light": 1,
			"ruid": 407045223,
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
		},
		"effect_id": 1861
	}
}
```

</details>
