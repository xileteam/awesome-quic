关于QUIC协议的论文、IETF进展、博客、视频等等

> QUIC 的全称是 Quick UDP Internet Connections protocol, 由 Google 设计提出，目前由 IETF 工作组推动进展。其设计的目标是替代 TCP 成为 HTTP/3 的数据传输层协议。熹乐科技在物联网（IoT）和边缘计算（Edge Computing）场景也一直在打造底层基于 QUIC 通讯协议的低时延边缘计算框架 [YoMo](https://github.com/yomorun/yomo/)，长时间关注 QUIC 协议的发展，遂整理该文集并配以适当的中文翻译，方便更多关注 QUIC 协议的人学习。

在线社区：🍖[discord/quic](https://discord.gg/CTH3wv9) 

维护者：🦖[YoMo](https://github.com/yomorun/yomo/)

## QUIC Weekly - 20210414期

* curl之父[@Daniel Stenberg](https://twitter.com/bagder)的新博客《WHERE IS HTTP/3 RIGHT NOW?》：SPEC已经全部完成了，正在排队等待最终的审核，就能拿到RFC版号（比如RFC2616，这个2616就是HTTP/1.1的第一版被assign的RFC number），然后就能发布了。这也就意味着大家可以拿着现在的SPEC（按照Draft-29版本提交的）来写自己的QUIC实现了
* [netray.io](https://quic.netray.io/stats.html) 每周扫描一次IPv4下的QUIC落地速率，他们最近的一次扫描显示已经有210万主机在应用HTTP/3：
![](https://daniel.haxx.se/blog/wp-content/uploads/2021/04/ietf-quic-support-in-ipv.png)
* 浏览器方面，Chrome和Edge是默认开启QUIC支持的，Firefox也马上要加入这个行列，其他的都需要手工开启（如何在iOS上开启QUIC可参考之前的QUIC-Weekly文章）
![](https://daniel.haxx.se/blog/wp-content/uploads/2021/04/Screenshot_2021-04-04-Can-I-use-Support-tables-for-HTML5-CSS3-etc.png)
* [@Robin](http://twitter.com/programart)  Robin Marx整理的HTTP/3与HTTP/2、HTTP/1.1协议栈的详细对比图片，并且也开源了源文件: [https://github.com/rmarx/h3-protocol-stack](https://github.com/rmarx/h3-protocol-stack)
![](https://github.com/rmarx/h3-protocol-stack/blob/main/png/protocol-stack-h2-h3-extended.png?raw=true)
* [微软的QUIC协议开源实现](https://github.com/microsoft/msquic) 将HTTP/3的基础能力融合进Windows Server 2022，被用于[SMB over QUIC](https://techcommunity.microsoft.com/t5/itops-talk-blog/smb-over-quic-files-without-the-vpn/ba-p/1183449)功能。该功能是一个相比WebDAV机制更安全的实现，无须再为VPN方案付出额外的费用和复杂的应用机制。也为SMB服务替换掉了TCP/IP和RDMA的传输机制。