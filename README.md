![Awesome QUIC Logo](https://github.com/fanweixiao/awesome-quic/blob/main/awesome-quic-logo.png?raw=true)
# Awesome Quic [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A collection of various awesome lists for videos, pentesters, libraries and frameworks.

**QUIC** is the Quick UDP Internet Connections protocol, developed by Google and currently in IETF workgroups for further development. It is being considered for replacing TCP as a transport protocol for HTTP/3. We are building an Open source project for IoT & Edge Computing atop QUIC called 🦖[YoMo](https://yomo.run/)

---

# QUIC Weekly

🍖[discord/quic](https://discord.gg/CTH3wv9)  🦖[YoMo](https://yomo.run/)

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
| [kwik](https://bitbucket.org/pjtr/kwik) | draft-29 | library, client | TLS 1.3   |

