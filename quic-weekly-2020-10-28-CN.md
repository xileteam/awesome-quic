QUIC Weekly - 20201028期
---

在线社区：🍖[discord/quic](https://discord.gg/CTH3wv9)  🦖[YoMo](https://yomo.run/)

* 📢 [DNS-over-QUIC](https://tools.ietf.org/html/draft-ietf-dprive-dnsoquic-01)：
  * 对科学那啥可是个好东西，太敏感，咱也不敢多说...
* **Paper** [基于QUIC的MQTT协议的实现和分析](https://www.researchgate.net/publication/329835020_Implementation_and_analysis_of_QUIC_for_MQTT)
  * 在端到端的通讯中，确保可靠和安全通信的基础是Transport和Security协议。对于IoT应用，这些协议必须是轻量级的，毕竟IoT设备通常都是硬件能力受限。不幸的是，目前广为流行的TCP/TLS和UDP/DTLS这两种方式，在建连、时延、连接迁移等方面有很多的不足。这篇论文研究了这些缺陷的根源，展示了如何借助QUIC协议优化IoT场景从而达到更高的网络性能，以IoT领域使用范围较广的MQTT协议为例，团队实现了主要的API和功能，并比较了使用QUIC和TCP构建的MQTT协议在有线网络、无线网络和长距离实验场景（long-distance testbeds）中的差异。
  * 测试的结果标明，基于QUIC协议实现的MQTT协议降低建连开销达56%
  * 在半连接场景下，对CPU和内存的消耗分别降低了83%和50%
  * 因为避免了队头阻塞（HOL Blocking）的问题，数据分发时延降低了55%
  * 数据传输速率的抖动也因为QUIC的连接迁移特性得到明显的改善。
* **Article** [HTTP/3: 你需要知道的下一代互联内网协议](https://portswigger.net/daily-swig/http-3-everything-you-need-to-know-about-the-next-generation-web-protocol)
* **Article** [QUIC和物联网IoT](https://calendar.perfplanet.com/2018/quic-and-http-3-too-big-to-fail/)
  * IoT设备是应用QUIC协议的一个好场景，因为这些设备通常工作在无线（蜂窝）网络下（Cellular network），且需要快速建连、0-RTT和重传。但是，这些设备CPU能力普遍较弱。QUIC的作者其实多次提到QUIC对IoT应用场景有很大的提升，可惜的是，至今还没有一套为这个场景设计的协议栈（其实有啊：基于QUIC协议的Edge Computing框架: [🦖YoMo](https://yomo.run/)）
* **Article** [未来的Internet: HTTP/3 — No More TCP, let’s QUIC fix it（谐音梗我翻不出来了...）](https://thexbhpguy.medium.com/the-new-internet-http-3-no-more-tcp-lets-quic-fix-it-6a4cbb6280c7)
