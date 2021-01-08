关于QUIC协议的论文、IETF进展、博客、视频等等

> QUIC 的全称是 Quick UDP Internet Connections protocol, 由 Google 设计提出，目前由 IETF 工作组推动进展。其设计的目标是替代 TCP 成为 HTTP/3 的数据传输层协议。熹乐科技在物联网（IoT）和边缘计算（Edge Computing）场景也一直在打造底层基于 QUIC 通讯协议的低时延边缘计算框架 [YoMo](https://github.com/yomorun/yomo/)，长时间关注 QUIC 协议的发展，遂整理该文集并配以适当的中文翻译，方便更多关注 QUIC 协议的人学习。

在线社区：🍖[discord/quic](https://discord.gg/CTH3wv9) 

维护者：🦖[YoMo](https://github.com/yomorun/yomo/)

QUIC Weekly - 20201118期
---

* 📽 Throwback to [乘坐时光机回到2016年7月QUIC工作组的成立会议](https://www.youtube.com/watch?v=aGvFuvmEufs)，这次会议是基于 Google 当时的实践经验，讨论 QUIC 是否应该成为 IETF 的标准
* 📽 [Robin Marx 讲述 QUIC 和 HTTP/3 的基本功能，开放了他研究的问题及他再 qlog 和 qvis 这两个调试工具上的进展](https://www.youtube.com/watch?v=SuSpghHP0uI&feature=youtu.be)。
* [lsquic 发布了 v2.24.4](https://github.com/litespeedtech/lsquic), 修复了拥塞控制和 CID 生命周期的相关问题。
* [iOS 14 和 macOS Big Sur 包含了 HTTP/3 实验版本的支持](https://developer.apple.com/videos/play/wwdc2020/10111/?time=701) ，并讲述了如何开启 QUIC 的使用，比如在 macOS Big Sur 上，执行: `defaults write -g CFNetworkHTTP3Override -int 3`就可以了。
* Fastly 的官方博客 [《QUIC 成熟时》](https://www.fastly.com/blog/maturing-of-quic)
* 2020-11-16 发布的 [IETF-109 Slide: Tunneling Internet protocols inside QUIC](https://datatracker.ietf.org/meeting/109/materials/slides-109-intarea-tunneling-internet-protocols-inside-quic-00) Rev.00 版本的发布，意味着 QUIC 在整个现有网络生态兼容性的标准迈出的重要一步，这也是为 RFC 标准发布后整体推进而准备。
