# 有人购买主播推荐商品 (GOTO_BUY_FLOW)

用户昵称会打星号（ `*` ）显示。

## 下发条件

有用户购买主播推荐商品后。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `GOTO_BUY_FLOW` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| text | str | 去购买提示 |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "GOTO_BUY_FLOW",
	"data": {
		"text": "回**正在去买"
	}
}
```

</details>
