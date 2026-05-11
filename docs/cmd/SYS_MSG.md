# 系统信息 (SYS_MSG)

## 下发条件

*未知*

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| cmd | str | `SYS_MSG` |  |
| msg | str | 提示信息 |  |
| url | str | 跳转 URL |  |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "SYS_MSG",
	"msg": "争夺开启，时间周五20点至周日20点，逾期不候哟！",
	"url": ""
}
```

</details>
