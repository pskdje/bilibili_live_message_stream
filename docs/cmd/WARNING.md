# 警告 (WARNING)

## 下发条件

直播间被警告时。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| cmd | str | `WARNING` |  |
| msg | str | 警告信息 |  |
| roomid | num | 直播间 ID |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "WARNING",
	"msg": "图片内容不适宜，请立即调整",
	"roomid": 22195814
}
```

</details>
