关于QUIC协议的论文、IETF进展、博客、视频等等

> QUIC 的全称是 Quick UDP Internet Connections protocol, 由 Google 设计提出，目前由 IETF 工作组推动进展。其设计的目标是替代 TCP 成为 HTTP/3 的数据传输层协议。熹乐科技在物联网（IoT）和边缘计算（Edge Computing）场景也一直在打造底层基于 QUIC 通讯协议的低时延边缘计算框架 [YoMo](https://github.com/yomorun/yomo/)，长时间关注 QUIC 协议的发展，遂整理该文集并配以适当的中文翻译，方便更多关注 QUIC 协议的人学习。

在线社区：🍖[discord/quic](https://discord.gg/CTH3wv9) 

维护者：🦖[YoMo](https://github.com/yomorun/yomo/)

## QUIC Weekly - 20210106期

* 微软的QUIC协议实现[MSQUIC v1.0正式发布](https://github.com/microsoft/msquic)
* Web的未来传输通道：[WebTransport Explainer](https://github.com/w3c/webtransport/blob/master/explainer.md)
* [WebTransport](https://w3c.github.io/webtransport/) 的SPEC更新，支持可插拔的协议设计, 开始支持QUIC-TRANSPORT。就像WebSocket一样，但是支持了多通道、 无序传输等特性。
* 史上第一个DNS over QUIC resolver [launched by AdGuard](https://itsecuritywire.com/quick-bytes/worlds-first-dns-over-quic-resolver-launched-by-adguard/)
* [DNS transport: The race is on!](https://centr.org/news/blog/ietf109-dns-transport.html)
* IEEE：[通过基于QUIC的代理功能实现高效的卫星-地面混合传输服务](https://ieeexplore.ieee.org/document/9297334/keywords#keywords)
* [DPIFuzz: 一种用于检测QUIC的DPI模糊策略的差分模糊框架](https://dl.acm.org/doi/pdf/10.1145/3427228.3427662)
* [插件化 QUIC](https://cdn.uclouvain.be/groups/cms-editors-ingi/articles/Pluginzing%20QUIC.pdf)
* [优化协议栈的性能透视: TCP+TLS+HTTP/2 vs. QUIC](https://irtf.org/anrw/2019/anrw2019-final25-acmpaginated.pdf)
* 2018: [WebTransport + WebCodecs at W3C Games Workshop](https://www.w3.org/2018/12/games-workshop/slides/21-webtransport-webcodecs.pdf)
* [qlog 0.4.0 released](crates.io/crates/qlog), 包括对记录原始字节时的流式序列化的修复，以及对DATAGRAM帧记录的改进。
