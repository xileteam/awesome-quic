A collection of various awesome lists for videos, pentesters, libraries and frameworks.

> **QUIC** is the Quick UDP Internet Connections protocol, developed by Google and currently in IETF workgroups for further development. It is being considered for replacing TCP as a transport protocol for HTTP/3. We are building an Open source project for IoT & Edge Computing atop QUIC called 🦖[YoMo](https://yomo.run/)

Online Community: 🍖[discord/quic](https://discord.gg/CTH3wv9) 
Maintainer: 🦖[YoMo](https://yomo.run/)

QUIC Weekly - 20201028
---

Online Community：[discord/quic](https://discord.gg/CTH3wv9)

* 📢 [DNS-over-QUIC](https://tools.ietf.org/html/draft-ietf-dprive-dnsoquic-01)
* **Paper** [Implementation and analysis of QUIC for MQTT](https://www.researchgate.net/publication/329835020_Implementation_and_analysis_of_QUIC_for_MQTT)
  * Transport and security protocols are essential to ensure reliable and secure communication between two parties. For IoT applications, these protocols must be lightweight, since IoT devices are usually resource constrained. Unfortunately, the existing transport and security protocols – namely TCP/TLS and UDP/DTLS – fall short in terms of connection overhead, latency, and connection migration when used in IoT applications. In this paper, after studying the root causes of these shortcomings, we show how utilizing QUIC in IoT scenarios results in a higher performance. Based on these observations, and given the popularity of MQTT as an IoT application layer protocol, we integrate MQTT with QUIC. By presenting the main APIs and functions developed, we explain how connection establishment and message exchange functionalities work. We evaluate the performance of MQTTw/QUIC versus MQTTw/TCP using wired, wireless, and long-distance testbeds. Our results show that MQTTw/QUIC reduces connection overhead in terms of the number of packets exchanged with the broker by up to 56%. In addition, by eliminating half-open connections, MQTTw/QUIC reduces processor and memory usage by up to 83% and 50%, respectively. Furthermore, by removing the head-of-line blocking problem, delivery latency is reduced by up to 55%. We also show that the throughput drops experienced by MQTTw/QUIC when a connection migration happens is considerably lower than that of MQTTw/TCP.
* **Article** [HTTP/3: Everything you need to know about the next-generation web protocol](https://portswigger.net/daily-swig/http-3-everything-you-need-to-know-about-the-next-generation-web-protocol)
* **Article** [QUIC and IoT](https://calendar.perfplanet.com/2018/quic-and-http-3-too-big-to-fail/)
  * One of the oft-touted use cases for QUIC is in Internet-of-Things (IoT) devices, as they often need intermittent (cellular) network access and low-latency connection setup, 0-RTT and better loss resilience are quite interesting in those cases. However, those devices often also have quite slow CPUs.. There are many issues where QUIC’s designers mention the IoT use case and how a certain decision might impact this, though as far as I know there is no stack that has been tested on such hardware yet. Similarly, many issues mention taking into account a hardware QUIC implementation, but at my experience level it’s unclear if this is more wishful thinking and handwaving rather than a guarantee.
* **Article** [The New Internet: HTTP/3 — No More TCP, let’s QUIC fix it](https://thexbhpguy.medium.com/the-new-internet-http-3-no-more-tcp-lets-quic-fix-it-6a4cbb6280c7)
