# 切断 (CUT_OFF)

## 下发条件

直播间被切断时。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| cmd | str | `CUT_OFF` |  |
| msg | str | 切断原因 |  |
| roomid | num | 直播间 ID |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "CUT_OFF",
	"msg": "违反直播言论规范，请立即调整",
	"roomid": 23993070
}
```

</details>
