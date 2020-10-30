![Awesome QUIC Logo](https://gitee.com/fanweixiao/awesome-quic/raw/main/awesome-quic-logo.png)
# Awesome Quic [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

关于QUIC协议的论文、IETF进展、博客、视频等等

**QUIC** 的全称是 Quick UDP Internet Connections protocol, 由 Google 设计提出，目前由 IETF 工作组推动进展。其设计的目标是替代 TCP 成为 HTTP/3 的数据传输层协议。熹乐科技在物联网（IoT）和边缘计算（Edge Computing）场景也一直在打造底层基于 QUIC 通讯协议的边缘计算微服务框架 [YoMo](https://yomo.run)，长时间关注 QUIC 协议的发展，遂整理该文集并配以适当的中文翻译，方便更多关注 QUIC 协议的人学习。

---

# QUIC Weekly - 每周一草

在线社区：🍖[discord/quic](https://discord.gg/CTH3wv9)  🦖[YoMo](https://yomo.run/)

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
  * IoT设备是应用QUIC协议的一个好场景，因为这些设备通常工作在无线（蜂窝）网络下（Cellular network），且需要快速建连、0-RTT和重传。但是，这些设备CPU能力普遍较弱。QUIC的作者其实多次提到QUIC对IoT应用场景有很大的提升，可惜的是，至今还没有一套为这个场景设计的协议栈（其实有啊：基于QUIC协议的Edge Computing框架: [🦖YoMo](https://yomo.run/)）
* **Article** [未来的Internet: HTTP/3 — No More TCP, let’s QUIC fix it（谐音梗我翻不出来了...）](https://thexbhpguy.medium.com/the-new-internet-http-3-no-more-tcp-lets-quic-fix-it-6a4cbb6280c7)

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

* Microsoft's [MsQuic](https://github.com/microsoft/msquic) `draft-31`
* Facebook's [mvfst](https://github.com/facebookincubator/mvfst) 
* [ats](https://cwiki.apache.org/confluence/display/TS/QUIC) is QUIC implementation in Apache Traffic Server  
* [Chromium](https://www.chromium.org/quic/playing-with-quic)'s QUIC Implementation (`draft-29` supported in Chrome 85.0.4171.0 and later)
* LiteSpeed QUIC and HTTP/3 library [Isquic](https://github.com/litespeedtech/lsquic)
* [ngtcp2](https://github.com/ngtcp2/ngtcp2) `draft-29`,`draft-30`,`draft-31`
* Cloudflare [nginx-cloudflare](https://github.com/cloudflare/quiche/tree/master/extras/nginx) `draft-27`,`draft-28`,`draft-29`

### Rust

* Cloudflare [quiche](https://github.com/cloudflare/quiche)
* Mozilla/Firefox [Neqo](https://github.com/mozilla/neqo)
* [Quinn](https://github.com/djc/quinn) based on tokio/futures, rustls for TLS `draft-28`

### Go

* [quic-go](https://github.com/lucas-clemente/quic-go) `draft-31`

### Node.js

* [Node.js QUIC](https://github.com/nodejs/quic) `draft-25`

### Python

* [aioquic](https://github.com/aiortc/aioquic) based on asyncio

### Haskell

* [Haskell quic](https://github.com/kazu-yamamoto/quic) `draft-27`

### Java

* [kwik](https://bitbucket.org/pjtr/kwik/) `draft-29`
