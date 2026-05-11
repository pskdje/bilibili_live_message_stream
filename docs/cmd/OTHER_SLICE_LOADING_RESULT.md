# 直播剪辑 (OTHER_SLICE_LOADING_RESULT)

## 下发条件

点击剪辑按钮后的几秒内下发，目前只有网页端有这个按钮。（请求接口）

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `OTHER_SLICE_LOADING_RESULT` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| data | array | 剪辑片段数据 |  |
| live_key | str | 标记直播场次的key | 未验证真实性 |

`data.data` 数组:

| 索引 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| 0 | obj | 单个片段数据 |  |

`data.data[i]` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| start_time | num | 片段开始时间时间戳 | UNIX 秒时间戳 |
| end_time | num | 片段结束时间时间戳 | UNIX 秒时间戳 |
| stream | str | 从开始时间到结束时间内的直播视频片段 | 需要使用浏览器用户代理字符串，特别是m3u文件内的视频链接 |
| type | num | 类型? |  |
| ban_ec | bool | ? |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "OTHER_SLICE_LOADING_RESULT",
	"data": {
		"data": [
			{
				"start_time": 1740037738,
				"end_time": 1740038916,
				"stream": "https://jssz-boss.hdslb.com/live2arc_anchor_video/vod_579433011406177273.m3u?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=y4zI4XTQzlOkmSKg%2F20250220%2Fjssz%2Fs3%2Faws4_request&X-Amz-Date=20250220T080858Z&X-Amz-Expires=7200&X-Amz-SignedHeaders=host&X-Amz-Signature=52be315e8e7def8e11f86d3c6d4952362725c3c087a433780926bc0e8c88c2e1",
				"type": 0,
				"ban_ec": false
			}
		],
		"live_key": "579433011406177273"
	}
}
```

</details>
