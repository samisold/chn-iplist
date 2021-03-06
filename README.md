# chn-iplist

数据来源 [ APNIC Delegated List](http://ftp.apnic.net/apnic/stats/apnic/delegated-apnic-latest)，将其转化为 txt 文件以在路由器上使用，并以此制作 Shadowrocket、Quantumult、Kitsunebi、acl、BifrostV、v2rayNG、clash、pac 规则和 v2ray 配置内嵌规则，仅包含 chn-ip 列表及部分谷歌和国内常见广告屏蔽规则。每月更新一次。

### Subscribe URL:

chnroute.txt: https://raw.githubusercontent.com/PaPerseller/chn-iplist/master/chnroute.txt

Shadowrocket: https://raw.githubusercontent.com/PaPerseller/chn-iplist/master/Shadowrocket.conf

Quantumult: https://raw.githubusercontent.com/PaPerseller/chn-iplist/master/Quantumult.conf

Quantumult(X) (no chn-ip) : https://raw.githubusercontent.com/PaPerseller/chn-iplist/master/Quantumult(X)_noIP.conf

Kitsunebi: https://raw.githubusercontent.com/PaPerseller/chn-iplist/master/Kitsunebi.conf

Kitsunebi-android: https://raw.githubusercontent.com/PaPerseller/chn-iplist/master/Kitsunebi-android.conf

acl (no ban ads) : https://raw.githubusercontent.com/PaPerseller/chn-iplist/master/chn.acl

acl (ban ads) : https://raw.githubusercontent.com/PaPerseller/chn-iplist/master/chn_banad.acl

pac: https://raw.githubusercontent.com/PaPerseller/chn-iplist/master/chnroute.pac  （默认非 chn-ip 网站走 socks5 localhost:1080 代理）

### 需手动更新：

BifrostV：在[相关文件夹](https://github.com/PaPerseller/chn-iplist/tree/master/BifrostV)下按规则类型复制粘贴至应用内。

v2ray 配置内嵌规则，将[规则文本](https://raw.githubusercontent.com/PaPerseller/chn-iplist/master/v2ray-config_rule.txt)加入配置文件 routing 对应区域。域名解析策略自行选择。

v2rayNG ：分别将[proxy](https://raw.githubusercontent.com/PaPerseller/chn-iplist/master/v2rayNG/proxy.txt)、[direct](https://raw.githubusercontent.com/PaPerseller/chn-iplist/master/v2rayNG/direct.txt)、 [block](https://raw.githubusercontent.com/PaPerseller/chn-iplist/master/v2rayNG/block.txt) 规则复制粘贴至应用内。

clash：https://github.com/PaPerseller/chn-iplist/blob/master/clash/clash.yml 

clash (no chn-ip)：https://github.com/PaPerseller/chn-iplist/blob/master/clash/clash_noIP.yml

### PS.

1. Maxmind 网站需注册后才可下载 Database 和提供 token，原快捷指令已失效。不再提供 Quantumult(no chn-ip) 版本。鉴于 Quantumult(X) 可于软件内更新 GeoLite2，现提供 Quantumult(X) no chn-ip 规则和 自带 chn-ip 的 Quantumult 规则。
2. v2rayNG 规则可与 pc 客户端 v2rayN 通用。 
3. 已加入 ipv6 列表的规则：chnroute.txt、chnroute.pac、chn.acl、clash、v2rayNG、Kitsunebi-android、shadowrocket
4. Kitsunebi android 用户若服务器不支持 ipv6，请于设置中允许地址类型设为仅IPV4。Shadowrocket (ios) 等有ipv6开关的同理。
5. 欢迎知情人通过 issue 告知 clash 内 ipv6 规则语法为 IP-CIDR 还是 IP-CIDR6。


### Todo & Test:

测试中：  

chn-iplist.sh+ipv6 版  
clash 规则  

### 路由器本地脚本使用

使用 `chmod +x /etc/sbin/chn-iplist.sh` 赋予其可执行权限。

### 致谢

- [CIDR2PAC](https://github.com/wspl/CIDR2PAC) - A es6 script for coverting CIDRs list to PAC proxy script.
