# 礼物星球点亮 (GIFT_STAR_PROCESS)

## 下发条件

主播的礼物星球其一点亮之后。

## JSON消息

根对象:

| 字段 | 类型 | 内容   | 备注      |
| ---- | ---- | ------ | --------- |
| cmd | str | `GIFT_STAR_PROCESS` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型   | 内容  | 备注    |
| ---- | ------ | ------ | ----- |
| status | num | 待调查 |  |
| tip | str | 点亮礼物星球的消息文本 |  |

## 示例

<details>
<summary>查看消息示例：</summary>

```json
{
	"cmd": "GIFT_STAR_PROCESS",
	"data": {
		"status": 1,
		"tip": "情书已点亮"
	}
}
```

</details>
