# 直播开始 (LIVE)

## 下发条件

请求了开始直播接口、开始向服务器推流。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| cmd | str | `LIVE` |  |
| live_key | str | 标记直播场次的key | 与开始直播接口获得的live_key相同 |
| voice_background | str | ? |  |
| sub_session_key | str | ? |  |
| live_platform | str | 开播平台? | 推测由开播接口决定 |
| live_model | num | ? |  |
| live_time | num | 开播时间 | UNIX 秒级时间戳，只有请求了开始直播后立刻下发的那个数据包里存在 |
| roomid | num | 直播间号 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "LIVE",
	"live_key": "234304209915761953",
	"voice_background": "",
	"sub_session_key": "234304209915761953sub_time:1651036923",
	"live_platform": "pc",
	"live_model": 0,
	"live_time": 1651036923,
	"roomid": 23614753
}
```

</details>
