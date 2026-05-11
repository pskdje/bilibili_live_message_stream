# 热抢提示 (HOT_BUY_NUM)

## 下发条件

服务器认为某个商品热抢后。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `HOT_BUY_NUM` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| num | num | 热抢数量 |  |
| goods_id | str | 商品id |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "HOT_BUY_NUM",
	"data": {
		"num": 81,
		"goods_id": "1817875296579985408"
	}
}
```

</details>
