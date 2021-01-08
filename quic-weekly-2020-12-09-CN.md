关于QUIC协议的论文、IETF进展、博客、视频等等

> QUIC 的全称是 Quick UDP Internet Connections protocol, 由 Google 设计提出，目前由 IETF 工作组推动进展。其设计的目标是替代 TCP 成为 HTTP/3 的数据传输层协议。熹乐科技在物联网（IoT）和边缘计算（Edge Computing）场景也一直在打造底层基于 QUIC 通讯协议的低时延边缘计算框架 [YoMo](https://github.com/yomorun/yomo/)，长时间关注 QUIC 协议的发展，遂整理该文集并配以适当的中文翻译，方便更多关注 QUIC 协议的人学习。

在线社区：🍖[discord/quic](https://discord.gg/CTH3wv9) 

维护者：🦖[YoMo](https://github.com/yomorun/yomo/)

## QUIC Weekly - 20201209期

* Wireshark v3.4.1 发布，[增加了很多与 QUIC 相关的更新](https://www.wireshark.org/docs/relnotes/wireshark-3.4.1.html)
* 📢 [draft-ietf-quic-manageability](https://quicwg.org/ops-drafts/draft-ietf-quic-manageability.html) 讨论了 QUIC 传输协议的可管理性，重点讨论影响 QUIC 流量的网络操作的注意事项，比如，要实现 QUIC 的负载均衡，建议参考该文
* 📢 [Applicability of the QUIC Transport Protocol](https://quicwg.org/ops-drafts/draft-ietf-quic-applicability.html) 讨论了QUIC传输协议的适用性，重点讨论了影响通过QUIC开发和部署应用协议的注意事项，比如，实现0-RTT的过程中要注意的安全问题
* [w3c WebTransport](https://w3c.github.io/webtransport/) 在WebIDL中定义了一组ECMAScript API，允许在浏览器和服务器之间发送和接收数据，在底层实现可插拔协议，在上面实现通用API。本规范使用可插拔的协议，QUIC-TRANSPORT 就是这样一个协议，向服务器发送数据和从服务器接收数据。它可以像WebSockets一样使用，但支持多流、单向流、无序传输、可靠以及不可靠传输。
* 📽 Google 的 David Schinaz 的视频 [QUIC 101](https://www.youtube.com/watch?v=dQ5AND4DPyU)
* Netty [发布了支持 QUIC 的 0.0.1.Final](https://netty.io/news/2020/12/09/quic-0-0-1-Final.html) 该 Codec 实现了 IETF QUIC draft-32 版本，基于 qiuche 项目构建
* Cloudflare 的博客 [为 QUIC 加速 UDP 包传输](https://blog.cloudflare.com/accelerating-udp-packet-transmission-for-quic/)
* [PDF: 软件模拟器 QUIC 协议的性能分析](https://www.researchgate.net/publication/343651688_Performance_analysis_of_Google%27s_Quick_UDP_Internet_Connection_Protocol_under_Software_Simulator)
* 📢 [draft-schinazi-masque-h3-datagram-01](https://tools.ietf.org/html/draft-schinazi-masque-h3-datagram-01) QUIC DATAGRAM 扩展为在 QUIC 上运行的应用协议提供了一种发送不可靠数据的机制，同时利用了QUIC的安全和拥塞控制特性。本文档定义了当在 QUIC 上运行的应用协议是 HTTP/3 时，如何通过在 frame payload 的开头添加一个标识符来使用 QUIC DATAGRAM frame。这允许HTTP消息使用不可靠的DATAGRAM帧来传递相关信息，确保这些帧与HTTP消息正确关联。
