# 直播进度条节点标签 (PLAY_TAG)

## 下发条件

在特定直播间的特定情况下发。

例如: 在[直播间6](https://live.bilibili.com/6)内，有人打出了某种操作。

## JSON消息

根对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| cmd | str | `PLAY_TAG` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| --- | --- | --- | --- |
| tag_id | num | 标签 ID |  |
| pic | str | 标签图标 | 通常显示于进度条之上 |
| timestamp | num | UNIX 秒时间戳 |  |
| type | str | 操作类型 | `ADD`:添加 |

## 示例

<details>
<summary>查看消息示例:</summary>

```json
{
	"cmd": "PLAY_TAG",
	"data": {
		"tag_id": 367751,
		"pic": "https://i0.hdslb.com/bfs/live/0e04525fee9ea6ea6973e8bd1116d9f1f6501d37.png",
		"timestamp": 1740319807,
		"type": "ADD"
	}
}
```

</details>
