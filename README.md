![Awesome QUIC Logo](https://github.com/fanweixiao/awesome-quic/blob/main/awesome-quic-logo.png?raw=true)
# Awesome Quic [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A collection of various awesome lists for videos, pentesters, libraries and frameworks.

**QUIC** is the Quick UDP Internet Connections protocol, developed by Google and currently in IETF workgroups for further development. It is being considered for replacing TCP as a transport protocol for HTTP/3. We are building an Open source project for IoT & Edge Computing atop QUIC called 🦖[YoMo](https://yomo.run/)

---

# QUIC Weekly

🍖[discord/quic](https://discord.gg/CTH3wv9)  🦖[YoMo](https://yomo.run/)

## QUIC Weekly - 20201209

* Wireshark v3.4.1 [release with lots of updates to QUIC](https://www.wireshark.org/docs/relnotes/wireshark-3.4.1.html)
* 📢 [draft-ietf-quic-manageability](https://quicwg.org/ops-drafts/draft-ietf-quic-manageability.html) discusses manageability of the QUIC transport protocol, focusing on caveats impacting network operations involving QUIC traffic
* 📢 [Applicability of the QUIC Transport Protocol](https://quicwg.org/ops-drafts/draft-ietf-quic-applicability.html) discusses the applicability of the QUIC transport protocol, focusing on caveats impacting application protocol development and deployment over QUIC
* [w3c WebTransport](https://w3c.github.io/webtransport/) defines a set of ECMAScript APIs in WebIDL to allow data to be sent and received between a browser and server, implementing pluggable protocols underneath with common APIs on top. This specification uses pluggable protocols, with QUIC [QUIC-TRANSPORT] as one such protocol, to send data to and receive data from servers. It can be used like WebSockets but with support for multiple streams, unidirectional streams, out-of-order delivery, and reliable as well as unreliable transport.
* 📽 David Schinaz from Google [QUIC 101](https://www.youtube.com/watch?v=dQ5AND4DPyU)
* [Netty release 0.0.1.Final](https://netty.io/news/2020/12/09/quic-0-0-1-Final.html) This codec provides a QUIC implementation of draft 32 by wrapping quiche and expose QUIC via the Channel API.
* Cloudflare blog [Accelerating UDP packet transmission for QUIC](https://blog.cloudflare.com/accelerating-udp-packet-transmission-for-quic/)
* [PDF: Performance analysis of Google’s Quick UDP Internet Connection Protocol under Software Simulator](https://www.researchgate.net/publication/343651688_Performance_analysis_of_Google%27s_Quick_UDP_Internet_Connection_Protocol_under_Software_Simulator)
* 📢 [draft-schinazi-masque-h3-datagram-01](https://tools.ietf.org/html/draft-schinazi-masque-h3-datagram-01) QUIC DATAGRAM extension provides application protocols running over QUIC with a mechanism to send unreliable data while leveraging the security and congestion-control properties of QUIC. However,QUIC DATAGRAM frames do not provide a means to demultiplex application contexts.  This document defines how to use QUIC DATAGRAM frames when the application protocol running over QUIC is HTTP/3 by adding an identifier at the start of the frame payload. This allows HTTP messages to convey related information using unreliable DATAGRAM frames, ensuring those frames are properly associated with an HTTP message.

## QUIC Weekly - 20201202

* 📽 Robin Marx [Head-of-Line Blocking in QUIC and HTTP/3: The Details](https://calendar.perfplanet.com/2020/head-of-line-blocking-in-quic-and-http-3-the-details/)
* 📽 Hussein Nasser [The Road to QUIC - what’s wrong w/ HTTP/1.1, HTTP/2, HTTP Pipelining, CRIME, HTTP/2 HOL, HPACK](https://www.youtube.com/watch?v=jp8lvtZa1a8)
* Experimental QUIC codec for [netty](https://github.com/netty/netty-incubator-codec-quic) makes use of [quiche](https://github.com/cloudflare/quiche)
* [GnuTLS 3.7.0 add QUIC support](https://blogs.gnome.org/dueno/whats-new-in-gnutls-3-7-0/)

## QUIC Weekly - 20201125

* [HTTP/3 - Wikipedia](https://en.wikipedia.org/wiki/HTTP/3)
* [QUIC dependencies graph](https://datatracker.ietf.org/wg/quic/deps/svg/)
* Daniel Stenberg's new keynote [HTTP/3 is next generation HTTP](https://www2.slideshare.net/bagder/http3-is-next-generation-http?qid=5d7f42ff-797b-4e2f-b4b6-ba223a6afb5a&v=&b=&from_search=1)
* Accelerating QUIC transition to 5G: [QUIC Throughput and Fairness over Dual Connectivity](https://www.ida.liu.se/~nikca89/papers/mascots20a.slides.pdf)
* [Google's cloud gaming platform Stadia is using QUIC](https://www.reddit.com/r/Stadia/comments/dxam9f/protocol_used_to_stream_games_on_stadia_qos/)
* 🇨🇳 _Chinese only_ [跟坚哥学QUIC系列：加密和传输握手](https://zhuanlan.zhihu.com/p/301505712)
* 🇨🇳 _Chinese only_ [跟坚哥学QUIC系列：连接迁移（Connection Migration）](https://www.zhihu.com/people/xiaojian-70-36)
* 📈 [QUIC Usage Statics](https://trends.builtwith.com/Server/QUIC)

## QUIC Weekly - 20201118

* 📽 Throwback to [QUIC BoF session in July 2016](https://www.youtube.com/watch?v=aGvFuvmEufs). A Working Group forming meeting to decide if QUIC should be adopted for standardisation into the IETF, based on the exissting deployment experience of Google.
* 📽 Robin Marx [gave a keynote](https://www.youtube.com/watch?v=SuSpghHP0uI&feature=youtu.be) at IEEE LATINCOM about his experiences doing a PhD on the QUIC and HTTP3 protocols. He talked about their basic features, open research questions and his process in contributing the qlog and qvis debugging tools.
* [lsquic release 2.24.4](https://github.com/litespeedtech/lsquic), contains fixes to congestion controller and to CID lifecycle.
* [iOS 14 and macOS Big Sur include an experimental preview of HTTP/3 support](https://developer.apple.com/videos/play/wwdc2020/10111/?time=701) for your apps that use URLSession, which you can enable in developer settings. To enable HTTP/3 macOS Big Sur: `defaults write -g CFNetworkHTTP3Override -int 3`.
* [Fastly: The Maturing of QUIC](https://www.fastly.com/blog/maturing-of-quic)
* 2020-11-16 [IETF-109 Slide: Tunneling Internet protocols inside QUIC](https://datatracker.ietf.org/meeting/109/materials/slides-109-intarea-tunneling-internet-protocols-inside-quic-00) Rev.00

## QUIC Weekly - 20201111

* 📢 **MASQUE Working Group** [Multiplexed Application Substrate over QUIC Encryption (masque)](https://datatracker.ietf.org/wg/masque/about/)

## QUIC Weekly - 20201028

* 📢 [DNS-over-QUIC](https://tools.ietf.org/html/draft-ietf-dprive-dnsoquic-01)
* **Paper** [Implementation and analysis of QUIC for MQTT](https://www.researchgate.net/publication/329835020_Implementation_and_analysis_of_QUIC_for_MQTT)
  * Transport and security protocols are essential to ensure reliable and secure communication between two parties. For IoT applications, these protocols must be lightweight, since IoT devices are usually resource constrained. Unfortunately, the existing transport and security protocols – namely TCP/TLS and UDP/DTLS – fall short in terms of connection overhead, latency, and connection migration when used in IoT applications. In this paper, after studying the root causes of these shortcomings, we show how utilizing QUIC in IoT scenarios results in a higher performance. Based on these observations, and given the popularity of MQTT as an IoT application layer protocol, we integrate MQTT with QUIC. By presenting the main APIs and functions developed, we explain how connection establishment and message exchange functionalities work. We evaluate the performance of MQTTw/QUIC versus MQTTw/TCP using wired, wireless, and long-distance testbeds. Our results show that MQTTw/QUIC reduces connection overhead in terms of the number of packets exchanged with the broker by up to 56%. In addition, by eliminating half-open connections, MQTTw/QUIC reduces processor and memory usage by up to 83% and 50%, respectively. Furthermore, by removing the head-of-line blocking problem, delivery latency is reduced by up to 55%. We also show that the throughput drops experienced by MQTTw/QUIC when a connection migration happens is considerably lower than that of MQTTw/TCP.
* **Article** [HTTP/3: Everything you need to know about the next-generation web protocol](https://portswigger.net/daily-swig/http-3-everything-you-need-to-know-about-the-next-generation-web-protocol)
* **Article** [QUIC and IoT](https://calendar.perfplanet.com/2018/quic-and-http-3-too-big-to-fail/)
  * One of the oft-touted use cases for QUIC is in Internet-of-Things (IoT) devices, as they often need intermittent (cellular) network access and low-latency connection setup, 0-RTT and better loss resilience are quite interesting in those cases. However, those devices often also have quite slow CPUs.. There are many issues where QUIC’s designers mention the IoT use case and how a certain decision might impact this, though as far as I know there is no stack that has been tested on such hardware yet. Similarly, many issues mention taking into account a hardware QUIC implementation, but at my experience level it’s unclear if this is more wishful thinking and handwaving rather than a guarantee.
* **Article** [The New Internet: HTTP/3 — No More TCP, let’s QUIC fix it](https://thexbhpguy.medium.com/the-new-internet-http-3-no-more-tcp-lets-quic-fix-it-6a4cbb6280c7)

## QUIC Weekly - 20201021

* 📢 QUIC protocol is finally in [IETF last call](https://mailarchive.ietf.org/arch/msg/ietf-announce/py1vC4Iuzq18Je4rwF69029oVOI/). 
  * Cloudflare: [A Last Call for QUIC, a giant leap for the Internet](https://blog.cloudflare.com/last-call-for-quic/)
* 📢 QUIC draft-32 documents are out:
  * Transport: https://tools.ietf.org/html/draft-ietf-quic-transport-32
  * Recovery: https://tools.ietf.org/html/draft-ietf-quic-recovery-32
  * TLS: https://tools.ietf.org/html/draft-ietf-quic-tls-32
  * HTTP: https://tools.ietf.org/html/draft-ietf-quic-http-32
  * QPACK: https://tools.ietf.org/html/draft-ietf-quic-qpack-19
* **Adoption** Facebook today is already using #QUIC + #HTTP3 for over 75% of all their global native app traffic! They've seen impressive performance gains from the new protocols, especially for their video streaming use cases. [How Facebook is bringing QUIC to billions](https://engineering.fb.com/networking-traffic/how-facebook-is-bringing-quic-to-billions/)
* **Adoption** [Node.js 15 debuts support for QUIC and HTTP/3](https://www.infoworld.com/article/3586354/nodejs-15-debuts-support-for-http3-transport.html).

## QUIC Weekly - 20201014

* **Adoption** [Chrome is deploying HTTP/3 and IETF QUIC](https://blog.chromium.org/2020/10/chrome-is-deploying-http3-and-ietf-quic.html)
  * current latest Google QUIC version (Q050) has many similarities with IETF QUIC. But up until now, the majority of Chrome users didn't communicate with IETF QUIC servers without enabling some command-line options.
  * Google search latency decreases by over 2%. YouTube rebuffer time decreased by over 9%, while client throughput increased by over 3% on desktop and over 7% on mobile. We're happy to announce that Chrome is rolling out support for IETF QUIC (specifically, draft version h3-29)
  * Today 25% of Chrome Stable users are using h3-29, and we plan on increasing that number over the coming weeks as we continue to monitor performance data
  * Chrome will actively support both IETF QUIC h3-29 and Google QUIC Q050 to provide servers that support Q050 with time to update to IETF QUIC.
* **Adoption** Cloudflare begins emailing users that [H3 will be automatically enabled](https://cloudflare-quic.com/) starting this month
* CDNs are misunderstood these days. Caching at the browser across sites is not that important, it caching at a point of presence (POP). This POP being so much closer to your end users brings performance gains because TCP is terrible over distances. QUIC may fix this by it's shift to UDP. [HackerNews](https://news.ycombinator.com/item?id=24745794)
* **TechTalk** Lucas Pardue: [QUIC & HTTP/3: Open Standards and Open Source Code](https://www.digitalocean.com/community/tech_talks/quic-http-3-open-standards-and-open-source-code) October 27, 2020
* **OpenSource** [quiche](https://github.com/cloudflare/quiche/commit/75c62c1fe97578173b74f16717a7fe9f2d34d5b0) landed supported for QUIC & HTTP/3 unreliable datagram into . It can help support low-latency where guaranteed delivery of data is not paramount.
* [Developing QUIC Loss Detection and Congestion Control in Haskell](https://kazu-yamamoto.hatenablog.jp/entry/2020/09/15/121613)
---

## Latest IETF draft

* [draft-ietf-quic-transport-31](https://datatracker.ietf.org/doc/draft-ietf-quic-transport/) QUIC: A UDP-Based Multiplexed and Secure Transport
* [draft-ietf-quic-tls-31](https://datatracker.ietf.org/doc/draft-ietf-quic-tls/) Using TLS to Secure QUIC
* [draft-ietf-quic-invariants-11](https://datatracker.ietf.org/doc/draft-ietf-quic-invariants/) Version-Independent Properties of QUIC
* [draft-ietf-quic-recovery-31](https://datatracker.ietf.org/doc/draft-ietf-quic-recovery/) QUIC Loss Detection and Congestion Control
* [draft-ietf-quic-version-negotiation-01](https://datatracker.ietf.org/doc/draft-ietf-quic-version-negotiation/) Compatible Version Negotiation for QUIC

## Learning Resources

* 🍿 QUIC WG chair [Dr.Lars Eggert](https://eggert.org/) [QUIC: a new internet transport](https://video.fsmpi.rwth-aachen.de/17ws-quic/12107) (🎬 58:39) @2017
* 🍿 Google's [QUIC: next generation multiplexed transport over UDP](https://www.youtube.com/watch?v=hQZ-0mXFmk8) (🎬 51:40) @2014
* F5 Sr Solution Architect Jason Rahm [What is QUIC?](https://www.youtube.com/watch?v=RIFnXaiRs_o) (🎬 08:35) @2018
* Codavel's [QUIC vs TCP+TLS — and why QUIC is not the next big thing](https://medium.com/codavel-blog/quic-vs-tcp-tls-and-why-quic-is-not-the-next-big-thing-d4ef59143efd)

### Books

* [curl](https://curl.haxx.se/)'s author [Daniel Stenberg](https://daniel.haxx.se/)'s new book: [HTTP/3 Explained](https://daniel.haxx.se/http3-explained/)

## Library & Frameworks

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
| [quant](https://github.com/NTAP/quant)                         | draft-32draft-32                                              | library, client, server                          | TLS 1.3                 |
| Fastly's [quicly](https://github.com/h2o/quicly)               | draft-27                                                      | client, server                                   | TLS 1.3 (final)         |
| [nginx-quic](https://hg.nginx.org/nginx-quic/)               | draft-27 .. draft-32                                            | server                                   | TLSv1.3 (RFC8446)        |

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
| [aioquic](https://github.com/aiortc/aioqui) | draft-29 | library, client, server | TLS 1.3   |

### Haskell

| Name         | Version  | Roles                   | Handshake |
|--------------|----------|-------------------------|-----------|
| [Haskell quic](https://github.com/kazu-yamamot) | draft-29 | library, client, server | TLS 1.3   |

### Java

| Name | Version  | Roles           | Handshake |
|------|----------|-----------------|-----------|
| [kwik](https://bitbucket.org/pjtr/kwik) | draft-29, draft-30, draft-31, draft-32 | library, client | TLS 1.3   |

## Debugging

* [qvis](https://github.com/quiclog/qvis) QUIC and HTTP/3 visualization tools
* [qlog](https://github.com/quiclog/qlog)  This repository contains various programming language integrations for the qlog format.
