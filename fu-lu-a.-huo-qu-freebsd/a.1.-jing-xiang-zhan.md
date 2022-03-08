# A.1.镜像站

FreeBSD 项目的官方镜像是由许多机器组成的，这些机器由项目集群管理员操作，并在 GeoDNS 后面引导用户到最近的可用镜像。目前的位置是巴西、日本（两个站点）、马来西亚、荷兰、南非、台湾、英国、美国（加利福尼亚、新泽西和华盛顿）。

官方镜像服务:

| **Service Name** | **Protocols** | **More information** |
| :---:            | :---:         | :---:                |
|**download.FreeBSD.org**|[https](https://download.freebsd.org/) [ftp](ftp://download.freebsd.org/pub/FreeBSD/)|与 ftp.FreeBSD.org 的内容相同，ftp 是一个传统的名字；建议使用 download.FreeBSD.org。|
| **git.FreeBSD.org** | git over `https` and `ssh`|关于使用 git 部分的更多细节|
| **pkg.FreeBSD.org** | [pkg(8)](https://www.freebsd.org/cgi/man.cgi?query=pkg&sektion=8&format=html) over `http` and `https` | pkg(8) 程序所使用的 FreeBSD 官方软件包库。|

所有的官方镜像都支持 IPv4 和 IPv6。

FreeBSD 网站(<https://www.FreeBSD.org> 和 <https://docs.FreeBSD.org>)没有被托管在 GeoDNS 基础设施中；目前正在对其实施进行研究。

http://ftp-archive.FreeBSD.org 不在 GeoDNS 基础设施内，只在一个地方（美国）托管。

该项目正在寻找新的站点；那些愿意赞助的人，请联系群组管理员团队以获得更多信息。

由社区和其他公司维护的镜像列表。

|**Country**|**Hostname**|**Protocols**|
|:---:|:---:|:---:|
|Australia |ftp.au.FreeBSD.org|[http](http://ftp.au.freebsd.org/pub/FreeBSD) [http_v6](http://ftp.au.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.au.FreeBSD.org) [rsync_v6](rsync://ftp.au.FreeBSD.org)|
| |ftp3.au.FreeBSD.org|[http](http://ftp3.au.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp3.au.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp3.au.FreeBSD.org)|
| Austria | ftp.at.FreeBSD.org  | [http](http://ftp.at.freebsd.org/pub/FreeBSD/) [http_v6](http://ftp.at.freebsd.org/pub/FreeBSD/) [ftp](ftp://ftp.at.freebsd.org/pub/FreeBSD/) [ftp_v6](ftp://ftp.at.freebsd.org/pub/FreeBSD/) [rsync](rsync://ftp.at.FreeBSD.org/pub/FreeBSD/) [rsync_v6](rsync://ftp.at.FreeBSD.org/pub/FreeBSD/) |
| Brazil  | ftp2.br.FreeBSD.org | [http](http://ftp2.br.freebsd.org/FreeBSD) [rsync](rsync://ftp2.br.FreeBSD.org) [rsync_v6](rsync://ftp2.br.FreeBSD.org) |
|          | ftp3.br.FreeBSD.org | [http](http://ftp3.br.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp3.br.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp3.br.FreeBSD.org) |
| Bulgaria | ftp.bg.FreeBSD.org  | [ftp](ftp://ftp.bg.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp.bg.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.bg.FreeBSD.org) [rsync_v6](rsync://ftp.bg.FreeBSD.org) |
| Czech Republic | ftp.cz.FreeBSD.org | [http](http://ftp.cz.freebsd.org/pub/FreeBSD) [http_v6](http://ftp.cz.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.cz.FreeBSD.org) [rsync_v6](rsync://ftp.cz.FreeBSD.org) |
| Denmark        | ftp.dk.FreeBSD.org | [http](http://ftp.dk.freebsd.org/FreeBSD/) [http_v6](http://ftp.dk.freebsd.org/FreeBSD/) [ftp](ftp://ftp.dk.freebsd.org/FreeBSD/) [ftp_v6](ftp://ftp.dk.freebsd.org/FreeBSD/) [rsync](rsync://ftp.dk.FreeBSD.org/FreeBSD/) [rsync_v6](rsync://ftp.dk.FreeBSD.org/FreeBSD/) |
| Finland | ftp.fi.FreeBSD.org | [ftp](ftp://ftp.fi.freebsd.org/pub/FreeBSD)                  |
| France  | ftp.fr.FreeBSD.org | [http](http://ftp.fr.freebsd.org/pub/FreeBSD) [http_v6](http://ftp.fr.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.fr.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp.fr.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.fr.FreeBSD.org) [rsync_v6](rsync://ftp.fr.FreeBSD.org) |
| |ftp3.fr.FreeBSD.org|[ftp](ftp://ftp3.fr.freebsd.org/pub/FreeBSD)|
| |ftp6.fr.FreeBSD.org|[http](http://ftp6.fr.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp6.fr.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp6.fr.FreeBSD.org)|
| Germany | ftp.de.FreeBSD.org  | [ftp](ftp://ftp.de.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp.de.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.de.FreeBSD.org) [rsync_v6](rsync://ftp.de.FreeBSD.org) |
|         | ftp1.de.FreeBSD.org | [http](http://ftp1.de.freebsd.org/pub/FreeBSD) [http_v6](http://ftp1.de.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp1.de.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp1.de.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp1.de.FreeBSD.org) [rsync_v6](rsync://ftp1.de.FreeBSD.org) |
||ftp2.de.FreeBSD.org|[http](http://ftp2.de.freebsd.org/pub/FreeBSD) [http_v6](http://ftp2.de.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp2.de.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp2.de.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp2.de.FreeBSD.org) [rsync_v6](rsync://ftp2.de.FreeBSD.org)|
|      | ftp5.de.FreeBSD.org | [ftp](ftp://ftp5.de.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp5.de.freebsd.org/pub/FreeBSD) |
|      | ftp7.de.FreeBSD.org | [http](http://ftp7.de.freebsd.org/pub/FreeBSD) [http_v6](http://ftp7.de.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp7.de.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp7.de.freebsd.org/pub/FreeBSD) |
| Greece | ftp.gr.FreeBSD.org  | [http](http://ftp.gr.freebsd.org/pub/FreeBSD) [http_v6](http://ftp.gr.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.gr.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp.gr.freebsd.org/pub/FreeBSD) |
|        | ftp2.gr.FreeBSD.org | [http](http://ftp2.gr.freebsd.org/pub/FreeBSD) [http_v6](http://ftp2.gr.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp2.gr.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp2.gr.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp2.gr.FreeBSD.org) |
|Japan|ftp.jp.FreeBSD.org|[http](http://ftp.jp.freebsd.org/pub/FreeBSD) [http_v6](http://ftp.jp.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.jp.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp.jp.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.jp.FreeBSD.org) [rsync_v6](rsync://ftp.jp.FreeBSD.org)|
| |ftp2.jp.FreeBSD.org|[ftp](ftp://ftp2.jp.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp2.jp.FreeBSD.org) [rsync_v6](rsync://ftp2.jp.FreeBSD.org)|
| |ftp3.jp.FreeBSD.org|[http](http://ftp3.jp.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp3.jp.FreeBSD.org)|
| |ftp4.jp.FreeBSD.org|[ftp](ftp://ftp4.jp.freebsd.org/pub/FreeBSD)|
| |ftp6.jp.FreeBSD.org|[http](http://ftp6.jp.freebsd.org/pub/FreeBSD) [http_v6](http://ftp6.jp.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp6.jp.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp6.jp.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp6.jp.FreeBSD.org) [rsync_v6](rsync://ftp6.jp.FreeBSD.org)|
|Korea|ftp.kr.FreeBSD.org|[http](http://ftp.kr.freebsd.org/pub/FreeBSD) [https](https://ftp.kr.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.kr.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.kr.FreeBSD.org)|
| |ftp2.kr.FreeBSD.org|[rsync](rsync://ftp2.kr.FreeBSD.org)|
|Latvia|ftp.lv.FreeBSD.org|[ http](http://ftp.lv.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.lv.freebsd.org/pub/FreeBSD)|
|Netherlands|ftp.nl.FreeBSD.org|[http](http://ftp.nl.freebsd.org/pub/FreeBSD) [http_v6](http://ftp.nl.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.nl.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp.nl.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.nl.FreeBSD.org) [rsync_v6](rsync://ftp.nl.FreeBSD.org)|
| |ftp2.nl.FreeBSD.org|[http](http://ftp2.nl.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp2.nl.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp2.nl.FreeBSD.org)|
|New Zealand|ftp.nz.FreeBSD.org|[http](http://ftp.nz.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.nz.freebsd.org/pub/FreeBSD)|
|Norway|ftp.no.FreeBSD.org|[ftp](ftp://ftp.no.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp.no.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.no.FreeBSD.org) [rsync_v6](rsync://ftp.no.FreeBSD.org)|
| Poland | ftp.pl.FreeBSD.org | [http](http://ftp.pl.freebsd.org/pub/FreeBSD) [http_v6](http://ftp.pl.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.pl.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.pl.FreeBSD.org) [rsync_v6](rsync://ftp.pl.FreeBSD.org) |
| Russia | ftp.ru.FreeBSD.org | [http](http://ftp.ru.freebsd.org/pub/FreeBSD) [http_v6](http://ftp.ru.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.ru.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp.ru.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.ru.FreeBSD.org) [rsync_v6](rsync://ftp.ru.FreeBSD.org) |
|          | ftp2.ru.FreeBSD.org | [https](https://ftp2.ru.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp2.ru.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp2.ru.FreeBSD.org) |
| Slovenia | ftp.si.FreeBSD.org  | [http](http://ftp.si.freebsd.org/pub/FreeBSD) [http_v6](http://ftp.si.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.si.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp.si.freebsd.org/pub/FreeBSD) |
| South Africa | ftp.za.FreeBSD.org  | [https](https://ftp.za.freebsd.org/pub/FreeBSD) [https_v6](https://ftp.za.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.za.FreeBSD.org) [rsync_v6](rsync://ftp.za.FreeBSD.org) |
|              | ftp2.za.FreeBSD.org | [http](http://ftp2.za.freebsd.org/pub/FreeBSD) [http_v6](http://ftp2.za.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp2.za.freebsd.org/pub/FreeBSD) |
| |ftp4.za.FreeBSD.org|[http](http://ftp4.za.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp4.za.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp4.za.FreeBSD.org)|
|Sweden|ftp.se.FreeBSD.org|[http](http://ftp.se.freebsd.org/pub/FreeBSD) [http_v6](http://ftp.se.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.se.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp.se.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.se.FreeBSD.org) [rsync_v6](rsync://ftp.se.FreeBSD.org)|
|Taiwan|ftp4.tw.FreeBSD.org|[https](https://ftp4.tw.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp4.tw.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp4.tw.FreeBSD.org)|
||ftp5.tw.FreeBSD.org|[http](http://ftp5.tw.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp5.tw.freebsd.org/pub/FreeBSD)|
|Ukraine|ftp.ua.FreeBSD.org|[http](http://ftp.ua.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.ua.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp.ua.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.ua.FreeBSD.org) [rsync_v6](rsync://ftp.ua.FreeBSD.org)|
|United Kingdom|ftp.uk.FreeBSD.org|[http](http://ftp.uk.freebsd.org/pub/FreeBSD) [http_v6](http://ftp.uk.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.uk.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp.uk.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.uk.FreeBSD.org) [rsync_v6](rsync://ftp.uk.FreeBSD.org)|
||ftp2.uk.FreeBSD.org|[http](http://ftp2.uk.freebsd.org/pub/FreeBSD) [http_v6](http://ftp2.uk.freebsd.org/pub/FreeBSD) [https](https://ftp2.uk.freebsd.org/pub/FreeBSD) [https_v6](https://ftp2.uk.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp2.uk.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp2.uk.freebsd.org/pub/FreeBSD)|
|United States of America|ftp11.FreeBSD.org|[http](http://ftp11.freebsd.org/pub/FreeBSD) [http_v6](http://ftp11.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp11.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp11.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp11.FreeBSD.org) [rsync_v6](rsync://ftp11.FreeBSD.org)|
||ftp14.FreeBSD.org|[ftp](ftp://ftp14.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp14.FreeBSD.org) (Former official tier 1)|
||ftp5.FreeBSD.org|[http](http://ftp5.freebsd.org/pub/FreeBSD) [http_v6](http://ftp5.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp5.freebsd.org/pub/FreeBSD) [ftp_v6](ftp://ftp5.freebsd.org/pub/FreeBSD)|

目前社区镜像支持的协议列表最后一次更新是在 2022-01-31，但并做不保证。
