# 直播间点赞数更新 (LIKE_INFO_V3_UPDATE)

## 下发条件

直播间点赞数量更新后。

## JSON消息

根对象:

| 字段 | 类型 | 内容  | 备注 |
| ---- | ---- | ---- | ---- |
| cmd  | str | `LIKE_INFO_V3_UPDATE` |  |
| data | obj | 直播间点赞数 |  |

`data` 对象:

| 字段 | 类型 | 内容  | 备注 |
| ---- | ---- | ---- | ---- |
| click_count | num | 直播间点赞数 |  |

## 示例

<details>
<summary>查看消息示例：</summary>

```json
{
	"cmd": "LIKE_INFO_V3_UPDATE",
	"data": {
		"click_count": 3227
	}
}
```

</details>
