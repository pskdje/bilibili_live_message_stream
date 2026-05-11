# 礼物星球进度更新 (WIDGET_GIFT_STAR_PROCESS)

## 下发条件

礼物星球内礼物的进度更新时。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `WIDGET_GIFT_STAR_PROCESS` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| start_date | num | 开始时间? | 一个年月日数字，格式 `Number(String(年) + String(月) + String(日))`，详见消息示例 |
| process_list | arr | 礼物进度列表 |  |
| finished | bool | 是否完成? |  |
| ddl_timestamp | num | 截止时间? | Unix 秒时间戳 |
| version | num | 更新时间 | Unix 毫秒时间戳 |
| reward_gift | num |  |  |
| reward_gift_img | str |  |  |
| reward_gift_name | str |  |  |
| level_info | null | (?) |  |

`data.process_list` 数组:

| 索引 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| 0 | obj | 礼物需求1 |  |
| 1 | obj | 礼物需求2 |  |
| 2 | obj | 礼物需求3 |  |

`data.process_list` 数组中对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| gift_id | num | 礼物id |  |
| gift_img | str | 礼物图片 |  |
| gift_name | str | 礼物名称 | `礼物星球` |
| completed_num | num | 当前数量 |  |
| target_num | num | 目标数量 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "WIDGET_GIFT_STAR_PROCESS",
	"data": {
		"start_date": 20250728,
		"process_list": [
			{
				"gift_id": 33988,
				"gift_img": "https://s1.hdslb.com/bfs/live/7164c955ec0ed7537491d189b821cc68f1bea20d.png",
				"gift_name": "礼物星球",
				"completed_num": 155,
				"target_num": 1000
			},
			{
				"gift_id": 31036,
				"gift_img": "https://s1.hdslb.com/bfs/live/8b40d0470890e7d573995383af8a8ae074d485d9.png",
				"gift_name": "礼物星球",
				"completed_num": 123,
				"target_num": 500
			},
			{
				"gift_id": 34382,
				"gift_img": "https://s1.hdslb.com/bfs/live/3a1cc7ca50da48670d9f7aa6c8d3cd874228f7b0.png",
				"gift_name": "礼物星球",
				"completed_num": 0,
				"target_num": 1
			}
		],
		"finished": false,
		"ddl_timestamp": 1754236800,
		"version": 1754030237877,
		"reward_gift": 0,
		"reward_gift_img": "",
		"reward_gift_name": "",
		"level_info": null
	}
}
```

</details>
