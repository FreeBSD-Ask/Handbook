# A.1.镜像站

FreeBSD 项目的官方镜像由项目集群管理员操作的多台机器组成，并通过 GeoDNS 在用户最接近的镜像上提供服务。当前的位置包括澳大利亚、巴西、德国、日本（两个站点）、马来西亚、南非、瑞典、台湾、英国、美国（加利福尼亚州、新泽西州和华盛顿州）。

官方镜像服务：

| 服务名称                            | 协议                            | 更多信息                                                                   |
| ------------------------------------- | --------------------------------- | ---------------------------------------------------------------------------- |
| **docs.FreeBSD.org**             | [https](https://docs.freebsd.org/)               | FreeBSD Documentation Portal.                                                           |
| **download.FreeBSD.org**             | [https](https://download.freebsd.org/) [ftp](ftp://download.freebsd.org/pub/FreeBSD/)              | Same content as `ftp.FreeBSD.org`, `ftp` is a legacy name; `download.FreeBSD.org` is recommended.                                   |
| **git.FreeBSD.org**             | git over `https` and `ssh` | More details on [using git](https://docs.freebsd.org/en/books/handbook/mirrors/#git) section.                                                               |
| **pkg.FreeBSD.org**             | [pkg(8)](https://man.freebsd.org/cgi/man.cgi?query=pkg&sektion=8&format=html) over `http` and `https`    | Official FreeBSD package repositories used by the [pkg(8)](https://man.freebsd.org/cgi/man.cgi?query=pkg&sektion=8&format=html) program.                             |
| **vuxml.FreeBSD.org** / **<www.VuXML.org>**          | [https](https://www.vuxml.org/)               | FreeBSD Project VuXML web page. `pkg audit` fetches the list of vulnerabilities from this service. |
| **<www.FreeBSD.org>**             | [https](https://www.freebsd.org/)               | FreeBSD Website.

所有官方镜像都支持 IPv4 和 IPv6。

<http://ftp-archive.FreeBSD.org> 不在 GeoDNS 基础设施中，仅在一个位置（美国）托管。

该项目正在寻找新的位置；愿意赞助的人，请联系集群管理员团队获取更多信息。

社区和其他公司维护的镜像列表：

| 区域           | 主机名 | 协议                   |
| ---------------- | -------- | ------------------------ |
| Australia                | ftp.au.FreeBSD.org      | [http](http://ftp.au.freebsd.org/pub/FreeBSD) [httpv6](http://ftp.au.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.au.FreeBSD.org) [rsyncv6](rsync://ftp.au.FreeBSD.org)                        |
|                          | ftp3.au.FreeBSD.org     | [http](http://ftp3.au.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp3.au.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp3.au.FreeBSD.org)                         |
| Austria                  | ftp.at.FreeBSD.org      | [http](http://ftp.at.freebsd.org/pub/FreeBSD/) [httpv6](http://ftp.at.freebsd.org/pub/FreeBSD/) [ftp](ftp://ftp.at.freebsd.org/pub/FreeBSD/) [ftpv6](ftp://ftp.at.freebsd.org/pub/FreeBSD/) [rsync](rsync://ftp.at.FreeBSD.org/pub/FreeBSD/) [rsyncv6](rsync://ftp.at.FreeBSD.org/pub/FreeBSD/)                      |
| Brazil                   | ftp2.br.FreeBSD.org     | [http](http://ftp2.br.freebsd.org/FreeBSD) [rsync](rsync://ftp2.br.FreeBSD.org) [rsyncv6](rsync://ftp2.br.FreeBSD.org)                         |
|                          | ftp3.br.FreeBSD.org     | [http](http://ftp3.br.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp3.br.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp3.br.FreeBSD.org)                         |
| Bulgaria                 | ftp.bg.FreeBSD.org      | [ftp](ftp://ftp.bg.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp.bg.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.bg.FreeBSD.org) [rsyncv6](rsync://ftp.bg.FreeBSD.org)                        |
| Czech Republic           | ftp.cz.FreeBSD.org      | [http](http://ftp.cz.freebsd.org/pub/FreeBSD) [httpv6](http://ftp.cz.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.cz.FreeBSD.org) [rsyncv6](rsync://ftp.cz.FreeBSD.org)                        |
| Denmark                  | ftp.dk.FreeBSD.org      | [http](http://ftp.dk.freebsd.org/FreeBSD/) [httpv6](http://ftp.dk.freebsd.org/FreeBSD/) [ftp](ftp://ftp.dk.freebsd.org/FreeBSD/) [ftpv6](ftp://ftp.dk.freebsd.org/FreeBSD/) [rsync](rsync://ftp.dk.FreeBSD.org/FreeBSD/) [rsyncv6](rsync://ftp.dk.FreeBSD.org/FreeBSD/)                      |
| Finland                  | ftp.fi.FreeBSD.org      | [ftp](ftp://ftp.fi.freebsd.org/pub/FreeBSD)                           |
| France                   | ftp.fr.FreeBSD.org      | [http](http://ftp.fr.freebsd.org/pub/FreeBSD) [httpv6](http://ftp.fr.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.fr.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp.fr.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.fr.FreeBSD.org) [rsyncv6](rsync://ftp.fr.FreeBSD.org)                      |
|                          | ftp3.fr.FreeBSD.org     | [ftp](ftp://ftp3.fr.freebsd.org/pub/FreeBSD)                           |
|                          | ftp6.fr.FreeBSD.org     | [http](http://ftp6.fr.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp6.fr.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp6.fr.FreeBSD.org)                         |
| Germany                  | ftp.de.FreeBSD.org      | [ftp](ftp://ftp.de.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp.de.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.de.FreeBSD.org) [rsyncv6](rsync://ftp.de.FreeBSD.org)                        |
|                          | ftp1.de.FreeBSD.org     | [http](http://ftp1.de.freebsd.org/pub/FreeBSD) [httpv6](http://ftp1.de.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp1.de.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp1.de.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp1.de.FreeBSD.org) [rsyncv6](rsync://ftp1.de.FreeBSD.org)                      |
|                          | ftp2.de.FreeBSD.org     | [http](http://ftp2.de.freebsd.org/pub/FreeBSD) [httpv6](http://ftp2.de.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp2.de.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp2.de.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp2.de.FreeBSD.org) [rsyncv6](rsync://ftp2.de.FreeBSD.org)                      |
|                          | ftp5.de.FreeBSD.org     | [ftp](ftp://ftp5.de.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp5.de.freebsd.org/pub/FreeBSD)                          |
|                          | ftp7.de.FreeBSD.org     | [http](http://ftp7.de.freebsd.org/pub/FreeBSD) [httpv6](http://ftp7.de.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp7.de.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp7.de.freebsd.org/pub/FreeBSD)                        |
| Greece                   | ftp.gr.FreeBSD.org      | [http](http://ftp.gr.freebsd.org/pub/FreeBSD) [httpv6](http://ftp.gr.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.gr.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp.gr.freebsd.org/pub/FreeBSD)                        |
|                          | ftp2.gr.FreeBSD.org     | [http](http://ftp2.gr.freebsd.org/pub/FreeBSD) [httpv6](http://ftp2.gr.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp2.gr.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp2.gr.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp2.gr.FreeBSD.org)                       |
| Japan                    | ftp.jp.FreeBSD.org      | [http](http://ftp.jp.freebsd.org/pub/FreeBSD) [httpv6](http://ftp.jp.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.jp.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp.jp.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.jp.FreeBSD.org) [rsyncv6](rsync://ftp.jp.FreeBSD.org)                      |
|                          | ftp2.jp.FreeBSD.org     | [ftp](ftp://ftp2.jp.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp2.jp.FreeBSD.org) [rsyncv6](rsync://ftp2.jp.FreeBSD.org)                         |
|                          | ftp3.jp.FreeBSD.org     | [http](http://ftp3.jp.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp3.jp.FreeBSD.org)                          |
|                          | ftp4.jp.FreeBSD.org     | [ftp](ftp://ftp4.jp.freebsd.org/pub/FreeBSD)                           |
|                          | ftp6.jp.FreeBSD.org     | [http](http://ftp6.jp.freebsd.org/pub/FreeBSD) [httpv6](http://ftp6.jp.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp6.jp.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp6.jp.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp6.jp.FreeBSD.org) [rsyncv6](rsync://ftp6.jp.FreeBSD.org)                      |
| Kazakhstan               | mirror.ps.kz            | [http](http://mirror.ps.kz/freebsd) [ftp](ftp://mirror.ps.kz/freebsd)                          |
|                          | mirror.neolabs.kz       | [http](http://mirror.neolabs.kz/freebsd) [ftp](ftp://mirror.neolabs.kz/freebsd)                          |
| Korea                    | ftp.kr.FreeBSD.org      | [http](http://ftp.kr.freebsd.org/pub/FreeBSD) [https](https://ftp.kr.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.kr.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.kr.FreeBSD.org)                        |
|                          | ftp2.kr.FreeBSD.org     | [rsync](rsync://ftp2.kr.FreeBSD.org)                           |
| Latvia                   | ftp.lv.FreeBSD.org      | [http](http://ftp.lv.freebsd.org/freebsd) [ftp](ftp://ftp.lv.freebsd.org/freebsd)                          |
| Netherlands              | ftp.nl.FreeBSD.org      | [http](http://ftp.nl.freebsd.org/pub/FreeBSD) [httpv6](http://ftp.nl.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.nl.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp.nl.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.nl.FreeBSD.org) [rsyncv6](rsync://ftp.nl.FreeBSD.org)                      |
|                          | ftp2.nl.FreeBSD.org     | [http](http://ftp2.nl.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp2.nl.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp2.nl.FreeBSD.org)                         |
|                          | mirror.nl.altushost.com | [https](https://mirror.nl.altushost.com/FreeBSD)                           |
| New Zealand              | ftp.nz.FreeBSD.org      | [http](http://ftp.nz.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.nz.freebsd.org/pub/FreeBSD)                          |
| Norway                   | ftp.no.FreeBSD.org      | [ftp](ftp://ftp.no.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp.no.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.no.FreeBSD.org) [rsyncv6](rsync://ftp.no.FreeBSD.org)                        |
| Poland                   | ftp.pl.FreeBSD.org      | [http](http://ftp.pl.freebsd.org/pub/FreeBSD) [httpv6](http://ftp.pl.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.pl.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.pl.FreeBSD.org) [rsyncv6](rsync://ftp.pl.FreeBSD.org)                       |
| Russia                   | ftp.ru.FreeBSD.org      | [http](http://ftp.ru.freebsd.org/pub/FreeBSD) [httpv6](http://ftp.ru.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.ru.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp.ru.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.ru.FreeBSD.org) [rsyncv6](rsync://ftp.ru.FreeBSD.org)                      |
|                          | ftp2.ru.FreeBSD.org     | [https](https://ftp2.ru.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp2.ru.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp2.ru.FreeBSD.org)                         |
| Slovenia                 | ftp.si.FreeBSD.org      | [http](http://ftp.si.freebsd.org/pub/FreeBSD) [httpv6](http://ftp.si.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.si.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp.si.freebsd.org/pub/FreeBSD)                        |
| South Africa             | ftp.za.FreeBSD.org      | [https](https://ftp.za.freebsd.org/pub/FreeBSD) [httpsv6](https://ftp.za.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.za.FreeBSD.org) [rsyncv6](rsync://ftp.za.FreeBSD.org)                        |
|                          | ftp2.za.FreeBSD.org     | [http](http://ftp2.za.freebsd.org/pub/FreeBSD) [httpv6](http://ftp2.za.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp2.za.freebsd.org/pub/FreeBSD)                         |
|                          | ftp4.za.FreeBSD.org     | [http](http://ftp4.za.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp4.za.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp4.za.FreeBSD.org)                         |
| Sweden                   | ftp.se.FreeBSD.org      | [http](http://ftp.se.freebsd.org/pub/FreeBSD) [httpv6](http://ftp.se.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.se.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp.se.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.se.FreeBSD.org) [rsyncv6](rsync://ftp.se.FreeBSD.org)                      |
|                          | mirror.se.altushost.com | [https](https://mirror.se.altushost.com/FreeBSD)                           |
| Taiwan                   | ftp4.tw.FreeBSD.org     | [https](https://ftp4.tw.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp4.tw.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp4.tw.FreeBSD.org)                         |
|                          | ftp5.tw.FreeBSD.org     | [http](http://ftp5.tw.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp5.tw.freebsd.org/pub/FreeBSD)                          |
| Ukraine                  | ftp.ua.FreeBSD.org      | [http](http://ftp.ua.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.ua.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp.ua.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.ua.FreeBSD.org) [rsyncv6](rsync://ftp.ua.FreeBSD.org)                       |
| United Kingdom           | ftp.uk.FreeBSD.org      | [http](http://ftp.uk.freebsd.org/pub/FreeBSD) [httpv6](http://ftp.uk.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp.uk.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp.uk.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp.uk.FreeBSD.org) [rsyncv6](rsync://ftp.uk.FreeBSD.org)                      |
|                          | ftp2.uk.FreeBSD.org     | [http](http://ftp2.uk.freebsd.org/pub/FreeBSD) [httpv6](http://ftp2.uk.freebsd.org/pub/FreeBSD) [https](https://ftp2.uk.freebsd.org/pub/FreeBSD) [httpsv6](https://ftp2.uk.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp2.uk.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp2.uk.freebsd.org/pub/FreeBSD)                      |
| United States of America | ftp11.FreeBSD.org       | [http](http://ftp11.freebsd.org/pub/FreeBSD) [httpv6](http://ftp11.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp11.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp11.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp11.FreeBSD.org) [rsyncv6](rsync://ftp11.FreeBSD.org)                      |
|                          | ftp14.FreeBSD.org       | [ftp](ftp://ftp14.freebsd.org/pub/FreeBSD) [rsync](rsync://ftp14.FreeBSD.org) (Former official tier 1) |
|                          | ftp5.FreeBSD.org        | [http](http://ftp5.freebsd.org/pub/FreeBSD) [httpv6](http://ftp5.freebsd.org/pub/FreeBSD) [ftp](ftp://ftp5.freebsd.org/pub/FreeBSD) [ftpv6](ftp://ftp5.freebsd.org/pub/FreeBSD)                        |

社区镜像支持的协议列表最后更新于 2022-01-31，不能保证是最新的。
