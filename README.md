![Awesome QUIC Logo](https://github.com/fanweixiao/awesome-quic/blob/main/awesome-quic-logo.png?raw=true)
# Awesome Quic [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A collection of various awesome lists for videos, pentesters, libraries and frameworks.

**QUIC** is the Quick UDP Internet Connections protocol, developed by Google and currently in IETF workgroups for further development. It is being considered for replacing TCP as a transport protocol for HTTP/3.

---

# QUIC Weekly

## 14.OCT.2020

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
