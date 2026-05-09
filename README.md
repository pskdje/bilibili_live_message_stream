# 哔哩哔哩直播信息流 - 收集整理

本项目旨在对 B 站直播信息流下发的数据进行收集整理，研究用途并对其进行说明。

本项目仅探讨直播信息流相关内容，其余接口均不属于本项目范畴。

本项目的主要内容存放在 [docs](docs/) 目录下。

## 声明

本项目使用 [CC0 1.0](LICENSE) 协议，放弃著作权，但禁止一切商业使用。

本项目仅供学习使用，请勿滥用。

利用本项目提供的资料等造成不良影响及后果与本项目、本项目所有的贡献者无关。

由于本项目的特殊性，可能随时停止开发或删档。

本项目为无著作权开源项目，时效性、有效性均不做保证，不接受任何催更，更不可能存在付费内容。

上传任何信息时请注意脱敏，删去可能泄漏个人信息的数据。

## 概述

直播信息流使用 WebSocket 作为数据传输通道，数据包为消息队列 (Message Queue) ，具体格式为`头部数据 + 正文数据`。

正文数据可能被压缩，表现为多个数据包被压缩到一个数据包的正文中。

连接建立后要立刻发送认证包，还要定期发送心跳包。

## 致谢

本项目继承自 <s title="原项目已失效" href="https://github.com/SocialSisterYi/bilibili-API-collect">bilibili-API-collect</s> 的 <span title="/docs/live/message_stream.md">message_stream.md</span> 文件，提交 `fdc44c9db514acb25662ab73922ff3777c6ce236` 。<!-- https://github.com/pskdje/bilibili-API-collect/commit/fdc44c9db514acb25662ab73922ff3777c6ce236 -->
