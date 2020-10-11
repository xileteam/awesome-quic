# Awesome Quic

A collection of various awesome lists for videos, pentesters, libraries and frameworks.

> QUIC is the Quick UDP Internet Connections protocol, developed by Google and currently in IETF workgroups for further development. It is being considered for replacing TCP as a transport protocol for HTTP/3.

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

## Library & Frameworks

### C/C++

* Microsoft's [MsQuic](https://github.com/microsoft/msquic)
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

* `draft-27` [Haskell quic](https://github.com/kazu-yamamoto/quic)

### Java

* `draft-29` [kwik](https://bitbucket.org/pjtr/kwik/)
