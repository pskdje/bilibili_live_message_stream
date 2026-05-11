# 未登录通知 (LOG_IN_NOTICE)

## 下发条件

未使用认证信息进行登录将会下发此数据包，通常于认证包回复后下发，在后续时间里也有可能会下发。

部分受到豁免的直播间不会下发。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `LOG_IN_NOTICE` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| notice\_msg | str | 通知内容 |  |
| image\_web | str | 在网页端使用的通知图片 |  |
| image\_app | str | 在app端使用的图片 | (未确认) |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "LOG_IN_NOTICE",
	"data": {
		"notice_msg": "为保护用户隐私，未登录无法查看他人昵称",
		"image_web": "http://i0.hdslb.com/bfs/dm/75e7c16b99208df259fe0a93354fd3440cbab412.png",
		"image_app": "http://i0.hdslb.com/bfs/dm/b632f7dcd3acf47deffb5f9ccc9546ae97a3415b.png"
	}
}
```

</details>
