QUIC Weekly - 20201014期
（TODO：翻译 @fiftyloops）
---

Telegram Group: [t.me/quic_weekly](https://t.me/quic_weekly)

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
