# 直播间发红包弹幕 (POPULARITY_RED_POCKET_START)

## 下发条件

开始抽取红包。

## JSON消息

根对象:

| 字段 | 类型 | 内容  | 备注 |
| ---- | ---- | ---- | ---- |
| cmd  | str | `POPULARITY_RED_POCKET_START` |  |
| data | obj | 信息本体 |  |

`data` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| lot_id | num | 发送的红包的ID | | 
| sender_uid | num | 发送者的UID |  |
| sender_name | str | 发送者的名称 |  |
| sender_face | str | 发送者的头像的URL |  |
| join_requirement | num | 待调查 |  |
| danmu | str | 用户参与红包时自动发送的弹幕内容 |  |
| current_time | num | 服务器发送数据包的Unix时间戳 |  |
| start_time | num | 可以开始抢红包的Unix时间戳 |  |
| end_time | num | 抢红包的结束时间Unix时间戳 |  |
| last_time | num | 红包的持续时间（秒） | start_time - end_time |
| remove_time | num | 待调查 |  |
| replace_time | num | 待调查 |  |
| lot_status | num | 待调查 |  |
| h5_url | str | 红包页面的URL |  |
| user_status | num | 用户参与状态，但是不知道是哪个用户 | 1已参与<br />2未参与 |
| awards | array | 红包内包含的礼物的信息 |  |
| lot_config_id | num | 待调查 |  |
| total_price | num | 内含抽取奖品金瓜子总价值 | 目前红包的 20% 会直接交给主播, 所以 20 电池 (2 CNY) 对应 2000 金瓜子的 80% 是 1600 金瓜子 |
| wait_num | num | 待调查 |  |

`data.awards[n]` 对象:

| 字段 | 类型 | 内容 | 备注 |
| ---- | ---- | ---- | ---- |
| gift_id | num | 礼物ID |  |
| gift_name | str | 礼物名称 |  |
| gift_pic | str | 礼物图标URL |  |
| num | num | 该礼物的数量 |  |

## 示例

<details>
<summary>查看消息示例：</summary>

```json
{
  "cmd": "POPULARITY_RED_POCKET_START",
  "data": {
    "lot_id": 2062329,
    "sender_uid": 181851309,
    "sender_name": "毒瘤老肥仔",
    "sender_face": "http://i0.hdslb.com/bfs/face/fed3871b01976ddd35fd3f772ffc2d4949f1391d.jpg",
    "join_requirement": 1,
    "danmu": "老板大气！点点红包抽礼物！",
    "current_time": 1650425344,
    "start_time": 1650425343,
    "end_time": 1650425523,
    "last_time": 180,
    "remove_time": 1650425538,
    "replace_time": 1650425533,
    "lot_status": 1,
    "h5_url": "https://live.bilibili.com/p/html/live-app-red-envelope/popularity.html?is_live_half_webview=1&hybrid_half_ui=1,5,100p,100p,000000,0,50,0,0,1;2,5,100p,100p,000000,0,50,0,0,1;3,5,100p,100p,000000,0,50,0,0,1;4,5,100p,100p,000000,0,50,0,0,1;5,5,100p,100p,000000,0,50,0,0,1;6,5,100p,100p,000000,0,50,0,0,1;7,5,100p,100p,000000,0,50,0,0,1;8,5,100p,100p,000000,0,50,0,0,1&hybrid_rotate_d=1&hybrid_biz=popularityRedPacket&lotteryId=2062329",
    "user_status": 2,
    "awards": [
      {
        "gift_id": 31212,
        "gift_name": "打call",
        "gift_pic": "https://s1.hdslb.com/bfs/live/f75291a0e267425c41e1ce31b5ffd6bfedc6f0b6.png",
        "num": 2
      },
      {
        "gift_id": 31214,
        "gift_name": "牛哇",
        "gift_pic": "https://s1.hdslb.com/bfs/live/b8a38b4bd3be120becddfb92650786f00dffad48.png",
        "num": 3
      },
      {
        "gift_id": 31216,
        "gift_name": "i了i了",
        "gift_pic": "https://s1.hdslb.com/bfs/live/1157a445487b39c0b7368d91b22290c60fa665b2.png",
        "num": 3
      }
    ],
    "lot_config_id": 3,
    "total_price": 1600,
    "wait_num": 0
  }
}
```

</details>
