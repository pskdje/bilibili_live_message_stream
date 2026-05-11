# 主播准备中 (PREPARING)

直播结束。

## 下发条件

手动请求结束直播接口、3分钟内未进行推流。

## JSON消息

根对象:

| 字段 | 类型 | 内容   | 备注      |
| ---- | ---- | ------ | --------- |
| cmd | str | `PREPARING` |  |
| round | num | 轮播状态:<br/>1正在轮播<br/>0未轮播 | 开启轮播时存在 |
| roomid | str | 直播间ID | 未知是真实ID还是短号 | 类型似乎从num改为str |
| msg_id | str | 信息id? |  |
| p_is_ack | bool |  | 未知 |
| p_msg_type | num | `1` | 未知 |
| send_time | num | 发送时间 | UNIX 毫秒时间戳 |

## 示例

<details>
<summary>有启用轮播:</summary>

```json
{
	"cmd": "PREPARING",
	"msg_id": "26964930181741056:1000:1000",
	"p_is_ack": true,
	"p_msg_type": 1,
	"roomid": "1899237171",
	"round": 1,
	"send_time": 1739985402716
}
```
</details>

<details>
<summary>未启用轮播:</summary>

```json
{
	"cmd": "PREPARING",
	"msg_id": "27040425357932032:1000:1000",
	"p_is_ack": true,
	"p_msg_type": 1,
	"roomid": "1017",
	"send_time": 1740129398337
}
```

</details>
