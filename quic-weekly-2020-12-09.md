A collection of various awesome lists for videos, pentesters, libraries and frameworks.

> **QUIC** is the Quick UDP Internet Connections protocol, developed by Google and currently in IETF workgroups for further development. It is being considered for replacing TCP as a transport protocol for HTTP/3. We are building an Open source project for IoT & Edge Computing atop QUIC called 🦖[YoMo](https://github.com/yomorun/yomo/)

Online Community: 🍖[discord/quic](https://discord.gg/CTH3wv9) 

Maintainer: 🦖[YoMo](https://github.com/yomorun/yomo/)

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
