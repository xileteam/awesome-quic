![Awesome QUIC Logo](https://gitee.com/fanweixiao/awesome-quic/raw/main/yomo-quic-weekly-social-graph.jpg)
# Awesome QUIC [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

关于QUIC协议的论文、IETF进展、博客、视频等等

**QUIC** 的全称是 Quick UDP Internet Connections protocol, 由 Google 设计提出，目前由 IETF 工作组推动进展。其设计的目标是替代 TCP 成为 HTTP/3 的数据传输层协议。熹乐科技在物联网（IoT）和边缘计算（Edge Computing）场景也一直在打造底层基于 QUIC 通讯协议的边缘计算微服务框架 [YoMo](https://github.com/yomorun/yomo)，长时间关注 QUIC 协议的发展，遂整理该文集并配以适当的中文翻译，方便更多关注 QUIC 协议的人学习。

---

# QUIC Weekly - 每周一草

在线社区：🍖[discord/quic](https://discord.gg/CTH3wv9) 

维护者：🦖[YoMo](http://github.com/yomorun/yomo)

## QUIC Weekly - 20210414期

* curl之父[@Daniel Stenberg](https://twitter.com/bagder)的新博客《WHERE IS HTTP/3 RIGHT NOW?》：SPEC已经全部完成了，正在排队等待最终的审核，就能拿到RFC版号（比如RFC2616，这个2616就是HTTP/1.1的第一版被assign的RFC number），然后就能发布了。这也就意味着大家可以拿着现在的SPEC（按照Draft-29版本提交的）来写自己的QUIC实现了
* [netray.io](https://quic.netray.io/stats.html) 每周扫描一次IPv4下的QUIC落地速率，他们最近的一次扫描显示已经有210万主机在应用HTTP/3：
![](https://daniel.haxx.se/blog/wp-content/uploads/2021/04/ietf-quic-support-in-ipv.png)
* 浏览器方面，Chrome和Edge是默认开启QUIC支持的，Firefox也马上要加入这个行列，其他的都需要手工开启（如何在iOS上开启QUIC可参考之前的QUIC-Weekly文章）
![](https://daniel.haxx.se/blog/wp-content/uploads/2021/04/Screenshot_2021-04-04-Can-I-use-Support-tables-for-HTML5-CSS3-etc.png)
* [@Robin](http://twitter.com/programart)  Robin Marx整理的HTTP/3与HTTP/2、HTTP/1.1协议栈的详细对比图片，并且也开源了源文件: [https://github.com/rmarx/h3-protocol-stack](https://github.com/rmarx/h3-protocol-stack)
![](https://github.com/rmarx/h3-protocol-stack/blob/main/png/protocol-stack-h2-h3-extended.png?raw=true)
* [微软的QUIC协议开源实现](https://github.com/microsoft/msquic) 将HTTP/3的基础能力融合进Windows Server 2022，被用于[SMB over QUIC](https://techcommunity.microsoft.com/t5/itops-talk-blog/smb-over-quic-files-without-the-vpn/ba-p/1183449)功能。该功能是一个相比WebDAV机制更安全的实现，无须再为VPN方案付出额外的费用和复杂的应用机制。也为SMB服务替换掉了TCP/IP和RDMA的传输机制。

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
* [qlog 0.4.0 released](https://docs.rs/qlog/0.4.0/qlog/index.html), 包括对记录原始字节时的流式序列化的修复，以及对DATAGRAM帧记录的改进。

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

## QUIC Weekly - 20201202期

* 📽 Robin Marx 的 [QUIC和HTTP/3的队头阻塞：细节](https://calendar.perfplanet.com/2020/head-of-line-blocking-in-quic-and-http-3-the-details/) [中文版Chinese Version](https://github.com/rmarx/holblocking-blogpost/blob/master/README_CN.md)
* 📽 Hussein Nasser 的 [QUIC之路 - HTTP/1.1、HTTP/2、HTTP Pipelining、CRIME、HTTP/2队头阻塞、HPACK都错在了哪](https://www.youtube.com/watch?v=jp8lvtZa1a8)
* [Netty的实验版开始支持QUIC](https://github.com/netty/netty-incubator-codec-quic) makes use of [quiche](https://github.com/cloudflare/quiche)
* [GnuTLS 3.7.0 开始支持 QUIC 支持](https://blogs.gnome.org/dueno/whats-new-in-gnutls-3-7-0/)

## QUIC Weekly - 20201125期

* Wikipedia 上更新了关于 HTTP/3 的章节：[HTTP/3 - Wikipedia](https://en.wikipedia.org/wiki/HTTP/3)
* [IETF-QUIC 的标准依赖树](https://datatracker.ietf.org/wg/quic/deps/svg/)
* Daniel Stenberg 的新 Keynote [HTTP/3 是下一代 HTTP](https://www2.slideshare.net/bagder/http3-is-next-generation-http?qid=5d7f42ff-797b-4e2f-b4b6-ba223a6afb5a&v=&b=&from_search=1)
* QUIC 在 5G 网络中的实验：[QUIC Throughput and Fairness over Dual Connectivity](https://www.ida.liu.se/~nikca89/papers/mascots20a.slides.pdf)
* [Google's cloud gaming platform Stadia is using QUIC](https://www.reddit.com/r/Stadia/comments/dxam9f/protocol_used_to_stream_games_on_stadia_qos/)
* [跟坚哥学QUIC系列：4 - 连接迁移（Connection Migration）](https://zhuanlan.zhihu.com/p/311221111)
* [跟坚哥学QUIC系列：3 - 加密和传输握手](https://zhuanlan.zhihu.com/p/301505712)
* [跟坚哥学QUIC系列：2 - 地址验证（Address Validation）](https://zhuanlan.zhihu.com/p/290694322)
* [跟坚哥学QUIC系列：1 - 版本协商（Version Negotiation）](https://zhuanlan.zhihu.com/p/286328927)
* 📈 [Builtwith 的 QUIC 应用状况监测](https://trends.builtwith.com/Server/QUIC)

## QUIC Weekly - 20201118期

* 📽 Throwback to [乘坐时光机回到2016年7月QUIC工作组的成立会议](https://www.youtube.com/watch?v=aGvFuvmEufs)，这次会议是基于 Google 当时的实践经验，讨论 QUIC 是否应该成为 IETF 的标准
* 📽 [Robin Marx 讲述 QUIC 和 HTTP/3 的基本功能，开放了他研究的问题及他再 qlog 和 qvis 这两个调试工具上的进展](https://www.youtube.com/watch?v=SuSpghHP0uI&feature=youtu.be)。
* [lsquic 发布了 v2.24.4](https://github.com/litespeedtech/lsquic), 修复了拥塞控制和 CID 生命周期的相关问题。
* [iOS 14 和 macOS Big Sur 包含了 HTTP/3 实验版本的支持](https://developer.apple.com/videos/play/wwdc2020/10111/?time=701) ，并讲述了如何开启 QUIC 的使用，比如在 macOS Big Sur 上，执行: `defaults write -g CFNetworkHTTP3Override -int 3`就可以了。
* Fastly 的官方博客 [《QUIC 成熟时》](https://www.fastly.com/blog/maturing-of-quic)
* 2020-11-16 发布的 [IETF-109 Slide: Tunneling Internet protocols inside QUIC](https://datatracker.ietf.org/meeting/109/materials/slides-109-intarea-tunneling-internet-protocols-inside-quic-00) Rev.00 版本的发布，意味着 QUIC 在整个现有网络生态兼容性的标准迈出的重要一步，这也是为 RFC 标准发布后整体推进而准备。

## QUIC Weekly - 20201111期

* 📢 关于多路复用技术的WG值得关注 **MASQUE Working Group** [Multiplexed Application Substrate over QUIC Encryption (masque)](https://datatracker.ietf.org/wg/masque/about/)

## QUIC Weekly - 20201104期

* 📢 **load-balancers** [Merged了使用POSIX timestamp的PR，这才对嘛](https://github.com/quicwg/load-balancers/pull/56/files)
* 📢 **load-balancers** [draft-ietf-quic-load-balancers-05出来了，相比draft-04的更新参考这里](https://www.ietf.org/rfcdiff?url1=draft-ietf-quic-load-balancers-04&url2=draft-ietf-quic-load-balancers-05)
* **应用** [水果公司的多通道Multipath transport使用场景](https://github.com/quicwg/wg-materials/blob/master/interim-20-10/Multipath%20transports%20at%20Apple.pdf)
* **最佳实践** [IETF QUIC相比HTTP over TLS 1.3 over TCP有显著提升，YouTube缓冲时间降低9%](https://blog.chromium.org/2020/10/chrome-is-deploying-http3-and-ietf-quic.html)
* **最佳实践** [Facebook在视频领域应用QUIC后请求错误率降低8%，卡顿率降低20%](https://engineering.fb.com/2020/10/21/networking-traffic/how-facebook-is-bringing-quic-to-billions/)
* **最佳实践** [Fastly: QUIC and HTTP/3 2020 最新状态](https://zhuanlan.zhihu.com/p/270650394)
* **最佳实践** [Cloudflare: 通往 QUIC 之路（The Road to QUIC）](https://zhuanlan.zhihu.com/p/268171460)
* **知乎** 深入浅出讲解QUIC协议，包含了最近一年的更新 [QUIC 协议简介](https://zhuanlan.zhihu.com/p/276147925)
* **知乎** QUIC的革新带来了后端处理服务的革新机会：[如何设计一款比JSON性能好10倍的编解码器？](https://zhuanlan.zhihu.com/p/274321939)
* **开源** [QUIC 开源实现列表（持续更新）](https://zhuanlan.zhihu.com/p/270628018)
* **开源** [lsquic 2.24.1 发布，@sumams为其增加了新功能，也包含了一些bug修复 🔧.](https://github.com/litespeedtech/lsquic)
* **工具** [Wireshark 3.4.0发布，支持IETF QUIC](https://www.wireshark.org/docs/relnotes/wireshark-3.4.0.html）

## QUIC Weekly - 20201028期

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
  * IoT设备是应用QUIC协议的一个好场景，因为这些设备通常工作在无线（蜂窝）网络下（Cellular network），且需要快速建连、0-RTT和重传。但是，这些设备CPU能力普遍较弱。QUIC的作者其实多次提到QUIC对IoT应用场景有很大的提升，可惜的是，至今还没有一套为这个场景设计的协议栈（其实有啊：基于QUIC协议的Edge Computing框架: [🦖YoMo](https://github.com/yomorun/yomo/)）

## QUIC Weekly - 20201021期

* 📢 QUIC 协议终于出现在 [IETF last call](https://mailarchive.ietf.org/arch/msg/ietf-announce/py1vC4Iuzq18Je4rwF69029oVOI/) 中。
* 📢 QUIC 草案32文件已出：
  * 运输：https://tools.ietf.org/html/draft-ietf-quic-transport-32
  * 恢复：https://tools.ietf.org/html/draft-ietf-quic-recovery-32
  * TLS：https://tools.ietf.org/html/draft-ietf-quic-tls-32
  * HTTP：https://tools.ietf.org/html/draft-ietf-quic-http-32
  * QPACK：https://tools.ietf.org/html/draft-ietf-quic-qpack-19
* **Adoption** 现在 Facebook 已经使用 #QUIC + ＃HTTP3 来处理其全球所有本机应用流量的75％以上！他们从新协议中看到了令人印象深刻的性能提升，尤其是在他们的视频流使用案例中。 [Facebook 如何将 QUIC 带给数十亿人](https://engineering.fb.com/networking-traffic/how-facebook-is-bringing-quic-to-billions/)
* **Adoption** [Node.js 15首次支持 QUIC 和 HTTP/3](https://www.infoworld.com/article/3586354/nodejs-15-debuts-support-for-http3-transport.html)。

## QUIC Weekly - 20201014期

* **Adoption** [Chrome 正在部署 HTTP/3 和 IETF QUIC](https://blog.chromium.org/2020/10/chrome-is-deploying-http3-and-ietf-quic.html)
  * 当前最新的 Google QUIC 版本（Q050）与 IETF QUIC 有很多相似之处。但是到目前为止，大多数 Chrome 用户在未启用某些命令行选项的情况下没有与 IETF QUIC 服务器通信。
  * Google 搜索延迟减少了2％以上。 YouTube 的重新缓冲时间减少了9％以上，而台式机的客户端吞吐量增加了3％以上，移动设备的客户端吞吐量增加了7％以上。我们很高兴地宣布，Chrome 即将推出对 IETF QUIC（特别是草稿版本 H3-29）的支持。
  * 目前，有25％的 Chrome 稳定用户正在使用 H3-29。我们计划在接下来的几周内增加该数字，并继续监控性能数据。
  * Chrome 将积极支持 IETF QUIC H3-29 和 Google QUIC Q050，让支持 Q050 的服务器有时间更新到 IETF QUIC。
* **Adoption** Cloudflare 向用户发送电子邮件，通知从本月开始 [H3 将自动启用](https://cloudflare-quic.com/)。
* CDN 最近被误解了。跨站点的浏览器缓存并不是那么重要，重要的是在存在点（POP）进行缓存。这种 POP 与你的终端用户的距离如此之近，可带来性能提升，因为TCP的传输距离很差。QUIC 可以通过改用 UDP 来解决此问题。 [HackerNews](https://news.ycombinator.com/item?id=24745794)
* **TechTalk** Lucas Pardue：[QUIC 和 HTTP/3：开放标准和开放源代码](https://www.digitalocean.com/community/tech_talks/quic-http-3-open-standards-and-open-source-code) （2020年10月27日。）
* **OpenSource** [quiche](https://github.com/cloudflare/quiche/commit/75c62c1fe97578173b74f16717a7fe9f2d34d5b0) 已支持 QUIC 和 HTTP/3 不可靠的数据报。在保证数据的传输不是最重要的情况下，它可以降低延迟。
* [在 Haskell 中开发 QUIC 丢失检测和拥塞控制](https://kazu-yamamoto.hatenablog.jp/entry/2020/09/15/121613)。
---

## IETF进展

* [draft-ietf-quic-transport-32](https://datatracker.ietf.org/doc/draft-ietf-quic-transport/) QUIC: A UDP-Based Multiplexed and Secure Transport
* [draft-ietf-quic-tls-32](https://datatracker.ietf.org/doc/draft-ietf-quic-tls/) Using TLS to Secure QUIC
* [draft-ietf-quic-invariants-11](https://datatracker.ietf.org/doc/draft-ietf-quic-invariants/) Version-Independent Properties of QUIC
* [draft-ietf-quic-recovery-32](https://datatracker.ietf.org/doc/draft-ietf-quic-recovery/) QUIC Loss Detection and Congestion Control
* [draft-ietf-quic-version-negotiation-01](https://datatracker.ietf.org/doc/draft-ietf-quic-version-negotiation/) Compatible Version Negotiation for QUIC

## 学习资源

### 1.不在爱了 TCP 💔

* [为什么TCP是个烂协议](https://zhuanlan.zhihu.com/p/20144829)
* 今天 TCP 烂了怎么办？[如何看待谷歌 Google 打算用 QUIC 协议替代 TCP/UDP？](https://www.zhihu.com/question/29705994)

### 2.浅尝 QUIC 科普贴 🎱

* 知乎腾讯技术官号 [科普：QUIC协议原理分析](https://zhuanlan.zhihu.com/p/32553477)
* [新一代互联网传输协议QUIC浅析](https://zhuanlan.zhihu.com/p/76202865)
  
### 3.真干实践大厂贴 🏌️‍♂️

* 腾讯 QUIC 实践 [让互联网更快的协议，QUIC在腾讯的实践及性能优化](https://zhuanlan.zhihu.com/p/32560981)
* 阿里 QUIC 实践 [AliQUIC：场景化高性能传输网络实践](https://developer.aliyun.com/article/643770)
* 七牛 QUIC 实践 [流畅度提高 100%！七牛云 QUIC 推流方案如何实现直播 0 卡顿](https://zhuanlan.zhihu.com/p/33698793)
* 又拍云 QUIC 实践 [QUIC协议详解之Initial包的处理](https://zhuanlan.zhihu.com/p/162914823)
* 华为 QUIC 实践 [Efforts to Improve OTT Video Experience by ICPs](https://www-file.huawei.com/-/media/corporate/pdf/ilab/13-en.pdf)
* Facebook QUIC 实践 [Building Zero protocol for fast, secure mobile connections](https://engineering.fb.com/networking-traffic/building-zero-protocol-for-fast-secure-mobile-connections/)
* Cloudflare QUIC 实践 [The Road to QUIC](https://blog.cloudflare.com/the-road-to-quic/)
* Uber QUIC 实践 [Employing QUIC Protocol to Optimize Uber’s App Performance](https://eng.uber.com/employing-quic-protocol/)
* [Uber Networking: Challenges and Opportunities](https://www.slideshare.net/dhaval2025/uber-mobility-high-performance-networking)
* Fastly QUIC 实践 [Modernizing the internet with HTTP/3 and QUIC](https://www.fastly.com/blog/modernizing-the-internet-with-http3-and-quic)
  
### 4.熬夜充电技术细节贴 🦾

* [让互联网更快的“快”---QUIC协议原理分析](https://zhuanlan.zhihu.com/p/32630510)
* [QUIC 是如何做到 0RTT 的](https://zhuanlan.zhihu.com/p/142794794)
* [快速理解为什么说UDP有时比TCP更有优势](http://www.52im.net/thread-1277-1-1.html)
* [一泡尿的时间，快速读懂QUIC协议](http://www.52im.net/thread-2816-1-1.html)
  
### 5.墙裂推荐英文贴 🍿

* 谷歌官方 2014 年发布的视频：[QUIC: next generation multiplexed transport over UDP](https://www.youtube.com/watch?v=hQZ-0mXFmk8)
* Codevel博客文章 [https://medium.com/codavel-blog/quic-vs-tcp-tls-and-why-quic-is-not-the-next-big-thing-d4ef59143efd](https://medium.com/codavel-blog/quic-vs-tcp-tls-and-why-quic-is-not-the-next-big-thing-d4ef59143efd)
* [How Secure and Quick is QUIC? Provable Security and Performance Analyses](https://www.ietf.org/proceedings/96/slides/slides-96-irtfopen-1.pdf)
* [QUIC at 10,000 feet](https://docs.google.com/document/d/1gY9-YNDNAB1eip-RTPbqphgySwSNSDHLq9D5Bty4FSU/edit)
* 🍿 QUIC WG chair [Dr.Lars Eggert](https://eggert.org/) [QUIC: a new internet transport](https://video.fsmpi.rwth-aachen.de/17ws-quic/12107) (🎬 58:39) @2017
* 🍿 Google's [QUIC: next generation multiplexed transport over UDP](https://www.youtube.com/watch?v=hQZ-0mXFmk8) (🎬 51:40) @2014
* F5 Sr Solution Architect Jason Rahm [What is QUIC?](https://www.youtube.com/watch?v=RIFnXaiRs_o) (🎬 08:35) @2018
* Codavel's [QUIC vs TCP+TLS — and why QUIC is not the next big thing](https://medium.com/codavel-blog/quic-vs-tcp-tls-and-why-quic-is-not-the-next-big-thing-d4ef59143efd)

### Books

* [curl](https://curl.haxx.se/)'s author [Daniel Stenberg](https://daniel.haxx.se/)'s new book: [HTTP/3 Explained](https://daniel.haxx.se/http3-explained/)

## 框架和开源实现

### C/C++

| Name                          | Version                                                       | Roles                                            | Handshake               |
|-------------------------------|---------------------------------------------------------------|--------------------------------------------------|-------------------------|
| Microsoft's [MsQuic](https://github.com/microsoft/msquic)            | draft-27/28/29/30/31/32                                       | client, server                                   | TLS 1.3 RFC             |
| Facebook's [mvfst](https://github.com/facebookincubator/mvfst)              | draft-29                                                      | library, client, server                          | TLS 1.3                 |
| Google's [Chromium](https://www.chromium.org/quic/playing-with-quic)             | Q043, Q046, Q050, T050, T051, draft-27, draft-29              | library, client, server                          | QUIC Crypto, TLS        |
| [ats](https://cwiki.apache.org/confluence/display/TS/QUIC) (Apache Traffic Server)   | draft-29                                                      | client. server                                   | TLS 1.3                 |
| LiteSpeed's [lsquic](https://github.com/litespeedtech/lsquic)            | Draft-32, Draft-29, Draft-28, Draft-27, Q043, Q046, and Q050. | library, client, server                          | QUIC Crypto, RFC 8446   |
| [ngtcp2](https://github.com/ngtcp2/ngtcp2)                        | draft-29, draft-30, draft-31, and draft-32                    | library, client, server                          | TLSv1.3 (RFC 8446)      |
| Cloudflare's [nginx-cloudflare](https://github.com/cloudflare/quiche/tree/master/extras/nginx) | draft-27, draft-28, draft-29                                  | server                                           | TLSv1.3 (RFC8446)       |
| [picoquic](https://github.com/private-octopus/picoquic)                      | draft-32/31/30/29/28/27                                       | library and test tools, test client, test server | TLS 1.3 (using picotls) |
| [Pluginized QUIC](https://github.com/p-quic/pquic)               | draft-29                                                      | library, client, server                          | TLS 1.3 (using picotls) |
| [quant](https://github.com/NTAP/quant)                         | draft-33, draft-34, v1                                              | library, client, server                          | TLS 1.3                 |
| Fastly's [quicly](https://github.com/h2o/quicly)               | draft-27                                                      | client, server                                   | TLS 1.3 (final)         |
| [nginx-quic](https://hg.nginx.org/nginx-quic/)               | draft-27 .. draft-32                                            | server                                   | TLSv1.3 (RFC8446)        |
| [quicX](https://github.com/caozhiyi/quicX) | v1, v2 | library, client, server | TLS 1.3 (RFC 8446) |


### Rust

| Name                   | Version                      | Roles                   | Handshake         |
|------------------------|------------------------------|-------------------------|-------------------|
| Cloudflare's [quiche](https://github.com/cloudflare/quiche)    | draft-27, draft-28, draft-29 | library, client, server | TLSv1.3 (RFC8446) |
| Mozilla/Firefox's [Neqo](https://github.com/mozilla/neqo) | draft-30                     | library, client, server | TLS 1.3           |
| [Quinn](https://github.com/djc/quinn)                  | draft-28                     | library, client, server | TLS 1.3           |

### Go

| Name    | Version                  | Roles                   | Handshake   |
|---------|--------------------------|-------------------------|-------------|
| [quic-go](https://github.com/lucas-clemente/quic-go) | always the current draft | library, client, server | TLS 1.3 RFC |

### Node.js

| Name         | Version  | Roles          | Handshake |
|--------------|----------|----------------|-----------|
| [Node.js QUIC](https://github.com/nodejs/quic) | draft-25 | client, server | TLS 1.3   |

### Python

| Name    | Version  | Roles                   | Handshake |
|---------|----------|-------------------------|-----------|
| [aioquic](https://github.com/aiortc/aioquic) | draft-29 | library, client, server | TLS 1.3   |

### Haskell

| Name         | Version  | Roles                   | Handshake |
|--------------|----------|-------------------------|-----------|
| [Haskell quic](https://github.com/kazu-yamamoto/quic) | draft-29 | library, client, server | TLS 1.3   |

### Java

| Name | Version  | Roles           | Handshake |
|------|----------|-----------------|-----------|
| [kwik](https://bitbucket.org/pjtr/kwik) | draft-29, draft-30, draft-31, draft-32 | library, client | TLS 1.3   |

## Debugging

* [qvis](https://github.com/quiclog/qvis) QUIC and HTTP/3 visualization tools
* [qlog](https://github.com/quiclog/qlog)  This repository contains various programming language integrations for the qlog format.
