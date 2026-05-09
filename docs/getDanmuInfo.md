# 获取信息流连接和认证秘钥

> https://api.live.bilibili.com/xlive/web-room/v1/index/getDanmuInfo

*请求方法: GET*

认证方式: Cookie(SESSDATA)

鉴权方式：Wbi 签名

认证可选，若未认证视作未登录，将会受到限制。

## URL参数

| 参数名       | 类型 | 内容         | 必要性 | 备注 |
| ------------ | ---- | ------------ | ------ | ---- |
| id           | num  | 直播间真实id | 必须   |      |
| type         | num  | (?)          | 可选   | 作用尚不明确 |
| web_location | str  | (?)          | 可选   | 作用尚不明确 |
| w_rid        | str  | Wbi 签名     | 必须   | Wbi 签名 |
| wts          | num  | 当前时间戳    | 必须   | Wbi 签名 |

## JSON回复

根对象：

| 字段    | 类型 | 内容     | 备注   |
| ------- | ---- | -------- | ------ |
| code    | num  | 返回值   | -352: 风控校验失败<br />0: 成功<br />1: 错误<br />60009: 分区不存在<br />65530: token 错误 (登录错误)<br />1002002: 房间号错误 |
| message | str  | 错误信息 | 默认为空  |
| ttl     | num  | 1        |      |
| data    | obj  | 信息本体 |      |

`data` 对象：

| 字段               | 类型  | 内容                 | 备注 |
| ------------------ | ----- | -------------------- | ---- |
| group              | str   | live                 |      |
| business_id        | num   | 0                    |      |
| refresh_row_factor | num   | 0.125                |      |
| refresh_rate       | num   | 100                  |      |
| max_delay          | num   | 5000                 |      |
| token              | str   | 认证秘钥             |      |
| host_list          | array | 信息流服务器节点列表 |      |

`data.host_list[n]` 对象：

| 字段     | 类型 | 内容       | 备注 |
| -------- | ---- | ---------- | ---- |
| host     | str  | 服务器域名 |      |
| port     | num  | TCP 端口   |      |
| wss_port | num  | WSS 端口   |      |
| ws_port  | num  | WS 端口    |      |

## 示例

获得直播间 `1017` 的信息流认证秘钥

```shell
curl 'https://api.live.bilibili.com/xlive/web-room/v1/index/getDanmuInfo?id=1017&type=0&web_location=444.8&w_rid=cf24f88ea0cbb61e7b29aed0c070187d&wts=1748266797'
```

<details>
<summary>查看响应示例:</summary>

```json
{
  "code": 0,
  "message": "0",
  "ttl": 1,
  "data":{
    "group": "live",
    "business_id": 0,
    "refresh_row_factor": 0.125,
    "refresh_rate": 100,
    "max_delay": 5000,
    "token": "gZ2Pp2T4rIc2HfD0e53FHhQAwKWjb6-QDD84AcxXi8sk3S89XcdvPWOgClZIMZ5mESr19-JKTOFxayX4IjeSQuckWqohE5Y0aHn-agpc2uU7aPXW3-Xmra3QEKljMZS5fM3q2vCf2XcAsjc8Xup7MVAc8SLWWXhQz0s7f1alCkaJBAIPA-i2nS39Ri4O",
    "host_list":[
      {
        "host": "zj-cn-live-comet.chat.bilibili.com",
        "port": 2243,
        "wss_port": 2245,
        "ws_port": 2244
      },
      {
        "host": "zj-cn-live-comet.chat.bilibili.com",
        "port": 2243,
        "wss_port": 2245,
        "ws_port": 2244
      },
      {
        "host": "bd-sz-live-comet-14.chat.bilibili.com",
        "port": 2243,
        "wss_port": 2245,
        "ws_port": 2244
      },
      {
        "host": "bd-bj-live-comet-09.chat.bilibili.com",
        "port": 2243,
        "wss_port": 2245,
        "ws_port": 2244
      },
      {
        "host": "broadcastlv.chat.bilibili.com",
        "port": 2243,
        "wss_port": 2245,
        "ws_port": 2244
      }
    ]
  }
}
```

</details>

## 历史

| 日期 | 记录 |
| ---- | ---- |
| 2025年5月26日 | 强制要求Wbi签名 |
| 2025年6月27日 | 强制要求 `buvid3` Cookie |
| 2026年前的某一天 | 不再强制要求 `buvid3` Cookie |
