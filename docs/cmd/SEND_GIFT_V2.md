# 送礼V2 (SEND_GIFT_V2)

替换 `SEND_GIFT`

## 下发条件

有人为主播送礼后。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| cmd | str | `SEND_GIFT_V2` |  |
| danmu | obj |  |  |
| data | obj | 信息本体 |  |

`danmu` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| area | num |  |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| dmscore | num |  |  |
| pb | str | 使用 base64 编码 protobuf 后的数据 |  |

用于解析protobuf数据的proto文件: [bilibili.live.gift.v1](../../protobuf/bilibili/live/gift/v1.proto)

注: 先用 base64 解码 `data.pb` 内的字符串为字节数据 pb ，再使用 proto 文件解码 pb 数据。

## 示例

<details>
<summary>查看消息示例：</summary>

```json
{
	"cmd": "SEND_GIFT_V2",
	"danmu": {
		"area": 1
	},
	"data": {
		"dmscore": 140,
		"pb": "CODblLYBEhvllpzmrKLmmK/pga7pga7mjqnmjqnnmoTniLEaSmh0dHBzOi8vaTIuaGRzbGIuY29tL2Jmcy9mYWNlLzA4Y2NlNDg0OTg5NDczMzViODMxMzM2ZDU4ODE5OTMxN2RmOWM5N2IuanBnQgBS6wUIvPMBEg/nsonkuJ3lm6Lnga/niYwYASABKGQwZDhkQgRnb2xkShM0ODM3OTM3OTYyNTk3NjQzNzc2UIW00dcGWAFiOmJhdGNoOmdpZnQ6Y29tYm9faWQ6MzgyMDIxMDg4OjE2ODU5ODozMTE2NDoxNzk0Mzk4NzI1Ljg2NjZoCnBkeAWFAQAAgD+IAQGSAQbmipXlloLAAdmKnLwF6gESCgzpgI3pgaXmlaPkuroQlqUKigKrAgiWpQoSpAIKDOmAjemBpeaVo+S6uhJKaHR0cHM6Ly9pMS5oZHNsYi5jb20vYmZzL2ZhY2UvOGE1ZGUyZDc0ODYyNTFlODAzMDdkODYwMGNiZjg2NDllYjQwMzVmZS5qcGcyWgoM6YCN6YGl5pWj5Lq6EkpodHRwczovL2kxLmhkc2xiLmNvbS9iZnMvZmFjZS84YTVkZTJkNzQ4NjI1MWU4MDMwN2Q4NjAwY2JmODY0OWViNDAzNWZlLmpwZzpsCAESQjIwMjXnmb7lpKdVUOS4u+OAgTIwMjHlubTluqblvLnluZXkurrmsJTlpZZVUOOAgeebtOaSremrmOiDveS4u+aSrRok5Luj6KGo5L2c44CK5pWj5Lq65bmy5LiN5q2744CL57O75YiXkgIHCIzg1wIQAZoC5QEKSmh0dHBzOi8vczEuaGRzbGIuY29tL2Jmcy9saXZlL2UwNTFkZmQ0NTU3Njc4ZjhlZGNhYzQ5OTNlZDAwYTA5MzVjYmQ5Y2MucG5nEktodHRwczovL2kwLmhkc2xiLmNvbS9iZnMvbGl2ZS8zMmI3OTkxMjBlMTYxNGZhNjI3NWI2ZDE1ZGE3YTUyYjIxZGQwMTlkLndlYnAqSmh0dHBzOi8vaTAuaGRzbGIuY29tL2Jmcy9saXZlLzgxNmY4YjdhYTIxMzI4ODhmY2U5MjhjZGZiMTdiOWNmMjFjYzA4MjMuZ2lmqgIUCAESBwj1t/ACEAISBwiM4NcCEAFYAWoCCAZ6yQII4NuUtgES4QEKG+WWnOasouaYr+mBrumBruaOqeaOqeeahOeIsRJKaHR0cHM6Ly9pMi5oZHNsYi5jb20vYmZzL2ZhY2UvMDhjY2U0ODQ5ODk0NzMzNWI4MzEzMzZkNTg4MTk5MzE3ZGY5Yzk3Yi5qcGcyaQob5Zac5qyi5piv6YGu6YGu5o6p5o6p55qE54ixEkpodHRwczovL2kyLmhkc2xiLmNvbS9iZnMvZmFjZS8wOGNjZTQ4NDk4OTQ3MzM1YjgzMTMzNmQ1ODgxOTkzMTdkZjljOTdiLmpwZzoLIP///////////wEaXQoG5Yi65YS/EBkYzKoYIPGRogMozKoYMMyqGEgBUJalCmCyPHoJIzNGQjRGNjk5ggEJIzNGQjRGNjk5igEJIzNGQjRGNjk5kgEHI0ZGRkZGRpoBCSMzRkI0RjZFNg=="
	}
}
```

</details>
