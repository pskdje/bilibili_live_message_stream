# 文档

此路径下存储了直播信息流的文档数据。

获取信息流认证数据、服务器地址端口见 [getDanmuInfo](getDanmuInfo.md) ；

了解数据包格式、类型、编写方法见 [message_stream](message_stream.md) ；

想要知道某个cmd是做什么的、如何读取就在 [cmd 目录](cmd/) 内检索；

基本的运行示例可查看 [example](example.md) ，仅供参考。

若你在 [cmd 目录](cmd/) 中没有找到某个 cmd 的信息但你知道是做什么的话，欢迎贡献知识。

## 常用内容索引

*不常用的内容需要直接查看目录的文件列表*

- [getDanmuInfo.md](getDanmuInfo.md) 获取信息流连接和认证密钥
- [message_stream.md](message_stream.md) 信息流连接和数据格式
- [cmd/](cmd/) 普通包内JSON数据中按cmd排列的文档

## 常见cmd索引

- [DANMU_MSG](cmd/DANMU_MSG.md) 弹幕
- [INTERACT_WORD](cmd/INTERACT_WORD.md) 用户交互消息，已被V2替换
- [INTERACT_WORD_V2](cmd/INTERACT_WORD_V2.md) 基于protobuf的V2用户交互消息
- [ENTRY_EFFECT](cmd/ENTRY_EFFECT.md) 用户进场特效
- [DM_INTERACTION](cmd/DM_INTERACTION.md) 交互信息合并
- [SUPER_CHAT_MESSAGE](cmd/SUPER_CHAT_MESSAGE.md) 醒目留言
- [SEND_GIFT](cmd/SEND_GIFT.md) 送礼
- [COMBO_SEND](cmd/COMBO_SEND.md) 礼物连击
- [WATCHED_CHANGE](cmd/WATCHED_CHANGE.md) 直播间看过人数
- [ONLINE_RANK_V2](cmd/ONLINE_RANK_V2.md) 直播间高能榜，已被V3替换
- [ONLINE_RANK_V3](cmd/ONLINE_RANK_V3.md) 基于protobuf的V3直播间高能榜
- [LIKE_INFO_V3_CLICK](cmd/LIKE_INFO_V3_CLICK.md) 直播间用户点赞
- [LIKE_INFO_V3_UPDATE](cmd/LIKE_INFO_V3_UPDATE.md) 直播间点赞数更新

*其它cmd需自行检索*
