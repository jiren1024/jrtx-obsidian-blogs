---
{"dg-publish":true,"dg-path":"工具教程/我的 Surge 配置和使用教程.md","permalink":"/工具教程/我的 Surge 配置和使用教程/","created":"2024-01-03T10:40:48.465+08:00","updated":"2024-01-03T12:14:29.922+08:00"}
---

#Technomous 

我的 Surge 配置文件的如下所示。整个配置文件的核心在于规则部分的设计，下面将深入讲解规则部分的设计思路和规则的详细含义。其他部分配置的含义可以参考 Surge 的[用户手册]([Overview · GitBook (nssurge.com)](https://manual.nssurge.com/))自行理解。

```
[General]
loglevel = notify
skip-proxy = 127.0.0.1, 192.168.0.0/16, 193.168.0.0/24, 10.0.0.0/8, 172.16.0.0/12, 100.64.0.0/10,localhost,*.local
dns-server = 223.5.5.5, 119.29.29.29, 114.114.114.114, system
internet-test-url = http://connect.rom.miui.com/generate_204
proxy-test-url = http://www.gstatic.com/generate_204
test-timeout = 4
external-controller-access = pwd@0.0.0.0:6170
always-real-ip = *.apple.com, *.srv.nintendo.net, *.stun.playstation.net, xbox.*.microsoft.com, *.xboxlive.com,*.msftncsi.com
http-api-web-dashboard = true
http-api = pwd@127.0.0.1:6166
http-api-tls = true
ipv6 = false
use-local-host-item-for-proxy = true
exclude-simple-hostnames = true
read-etc-hosts = true
show-error-page-for-reject = true
disable-geoip-db-auto-update = false
hijack-dns = *:53
http-listen = 0.0.0.0:8888
socks5-listen = 0.0.0.0:8889
wifi-assist = true
allow-hotspot-access = true
allow-wifi-access = true
wifi-access-http-port = 8888
wifi-access-socks5-port = 8889
allow-hotspot-access = true

[Replica]
hide-apple-request = 1
hide-crashlytics-request = true
hide-udp = 0
keyword-filter-type = none
hide-crash-reporter-request = 1
keyword-filter = (null)

[Proxy]
🇭🇰 Hong Kong丨01 = 
🇭🇰 Hong Kong丨02 = 
🇭🇰 Hong Kong丨03 = 
🇭🇰 Hong Kong丨04 = 
🇭🇰 Hong Kong丨05 = 
🇭🇰 Hong Kong丨06 = 
🇭🇰 Hong Kong丨07 = 
🇭🇰 Hong Kong丨08 = 
🇭🇰 Hong Kong丨09 = 
🇭🇰 Hong Kong丨10 = 
🇨🇳 Taiwan丨01 = 
🇨🇳 Taiwan丨02 = 
🇨🇳 Taiwan丨03 = 
🇨🇳 Taiwan丨04 = 
🇨🇳 Taiwan丨05 = 
🇸🇬 Singapore丨01 = 
🇸🇬 Singapore丨02 = 
🇸🇬 Singapore丨03 = 
🇸🇬 Singapore丨04 = 
🇸🇬 Singapore丨05 = 
🇯🇵 Japan丨01 = 
🇯🇵 Japan丨02 = 
🇯🇵 Japan丨03 = 
🇯🇵 Japan丨04 = 
🇯🇵 Japan丨05 = 
🇺🇸 United States丨01 = 
🇺🇸 United States丨02 = 
🇺🇸 United States丨03 = 
🇺🇸 United States丨04 = 
🇺🇸 United States丨05 = 
🇰🇷 South Korea丨01 = 
🇰🇷 South Korea丨02 = 
🇨🇦 Canada丨01 = 
🇨🇦 Canada丨02 = 
🇬🇧 Great Britain丨01 = 
🇬🇧 Great Britain丨02 = 

[Proxy Group]
Proxy = select, Auto, 🇭🇰 Hong Kong, 🇸🇬 Singapore, 🇯🇵 Japan, 🇰🇷 Korea, 🇨🇦 Canada, 🇺🇸 United States, 🇨🇳 Taiwan, 🇬🇧 Great Britain
Auto = fallback, 🇭🇰 Hong Kong, 🇸🇬 Singapore, 🇯🇵 Japan, 🇺🇸 United States, 🇨🇳 Taiwan, 🇬🇧 Great Britain, 🇨🇦 Canada, 🇰🇷 Korea
OpenAI = select, 🇭🇰 Hong Kong, 🇸🇬 Singapore, 🇯🇵 Japan, 🇺🇸 United States, 🇨🇳 Taiwan, 🇬🇧 Great Britain, 🇨🇦 Canada, 🇰🇷 Korea
Netflix = select, 🇭🇰 Hong Kong, 🇸🇬 Singapore, 🇯🇵 Japan, 🇺🇸 United States, 🇨🇳 Taiwan, 🇬🇧 Great Britain, 🇨🇦 Canada, 🇰🇷 Korea
Telegram = select, 🇭🇰 Hong Kong, 🇸🇬 Singapore, 🇯🇵 Japan, 🇺🇸 United States, 🇨🇳 Taiwan, 🇬🇧 Great Britain, 🇨🇦 Canada, 🇰🇷 Korea
🇭🇰 Hong Kong = select, 🇭🇰 Hong Kong丨01, 🇭🇰 Hong Kong丨02, 🇭🇰 Hong Kong丨03, 🇭🇰 Hong Kong丨04, 🇭🇰 Hong Kong丨05, 🇭🇰 Hong Kong丨06, 🇭🇰 Hong Kong丨07, 🇭🇰 Hong Kong丨08, 🇭🇰 Hong Kong丨09, 🇭🇰 Hong Kong丨10
🇸🇬 Singapore = select, 🇸🇬 Singapore丨01, 🇸🇬 Singapore丨02, 🇸🇬 Singapore丨03, 🇸🇬 Singapore丨04, 🇸🇬 Singapore丨05
🇯🇵 Japan = select, 🇯🇵 Japan丨01, 🇯🇵 Japan丨02, 🇯🇵 Japan丨03, 🇯🇵 Japan丨04, 🇯🇵 Japan丨05
🇰🇷 Korea = select, 🇰🇷 South Korea丨01, 🇰🇷 South Korea丨02
🇨🇦 Canada = select, 🇨🇦 Canada丨01, 🇨🇦 Canada丨02
🇺🇸 United States = select, 🇺🇸 United States丨01, 🇺🇸 United States丨02, 🇺🇸 United States丨03, 🇺🇸 United States丨04, 🇺🇸 United States丨05
🇨🇳 Taiwan = select, 🇨🇳 Taiwan丨01, 🇨🇳 Taiwan丨02, 🇨🇳 Taiwan丨03, 🇨🇳 Taiwan丨04, 🇨🇳 Taiwan丨05
🇬🇧 Great Britain = select, 🇬🇧 Great Britain丨01, 🇬🇧 Great Britain丨02

[Rule]
PROCESS-NAME,Resilio Sync,DIRECT
RULE-SET,SYSTEM,DIRECT
RULE-SET,https://raw.githubusercontent.com/jrtx0/surge-list/master/ruleset/unblock.list,DIRECT
RULE-SET,https://raw.githubusercontent.com/jrtx0/surge-list/master/ruleset/blocked.list,Proxy
RULE-SET,https://raw.githubusercontent.com/jrtx0/surge-list/master/ruleset/openai.list,OpenAI
RULE-SET,https://raw.githubusercontent.com/jrtx0/surge-list/master/ruleset/netflix.list,Netflix
RULE-SET,https://raw.githubusercontent.com/jrtx0/surge-list/master/ruleset/telegram.list,Telegram
RULE-SET,LAN,DIRECT
GEOIP,CN,DIRECT
FINAL,DIRECT,dns-failed

[Host]
*.taobao.com = server:223.5.5.5
*.jd.com = server:223.5.5.5
*.tmall.com = server:223.5.5.5
*.aliyun.com = server:223.5.5.5

[URL Rewrite]
^https?:\/\/(www.)?(g|google)\.cn https://www.google.com.hk 302

[Header Rewrite]
^https?://(www.)?zhihu.com/question/ header-replace User-Agent "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_11_1) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/66.0.3359.45 Safari/537.36"

[SSID Setting]
"Apple Store" suspend=true
"iPhone X" cellular-mode=true

[MITM]
ca-passphrase = 
ca-p12 = 
hostname = *.google.cn, *.google.com, *.openai.com, *.ai.com, *.cloudflareclient.com
hostname-disabled = *.openai.com, *.ai.com
```
# 设计思路

我们无法穷举黑名单列表，同时我们也无法穷举白名单列表，而且这两个列表处于动态的不稳定状态。基于这种认知下，由于我大多数情况下都是使用白名单列表。所有我的 Surge 配置文件规则匹配是基于黑名单模式，默认情况下所有未匹配的域名都直接放行。这样可以减少在使用未知软件时的问题，比如各种银行客户端，支付宝等应用。所有的黑名单由我自己来定制化的维护。一些需要特定区域代理的软件使用单独的 list，比如 openai.list。目前维护的 list 如下：

- unblocked.list：这个规则集用来保存一定不能被代理的域名，算是一种强制性的保障。
- blocked.list：这个规则集用来保存我常用的需要代理的域名。
- openai.list：这个规则集是所有 OpenAI 相关的域名，可以方便的选择不同的区域。
- Netflix：这个规则集是所有 Netflix 相关的域名，可以方便的选择不同的区域。
- Telegram：这个规则集是所有 Telegram 相关的域名，可以方便的选择不同的区域。

# 配置规则

```
PROCESS-NAME,Resilio-Sync,DIRECT
RULE-SET,SYSTEM,DIRECT
RULE-SET,https://raw.githubusercontent.com/jrtx0/surge-list/master/ruleset/unblock.list,DIRECT
RULE-SET,https://raw.githubusercontent.com/jrtx0/surge-list/master/ruleset/blocked.list,Proxy
RULE-SET,https://raw.githubusercontent.com/jrtx0/surge-list/master/ruleset/openai.list,OpenAI
RULE-SET,https://raw.githubusercontent.com/jrtx0/surge-list/master/ruleset/netflix.list,Netflix
RULE-SET,https://raw.githubusercontent.com/jrtx0/surge-list/master/ruleset/telegram.list,Telegram
RULE-SET,LAN,DIRECT
GEOIP,CN,DIRECT
FINAL,DIRECT,dns-failed
```

## Process Rule

```
PROCESS-NAME,Resilio-Sync,DIRECT
```

这是用于匹配软件进程的规则，该规则只在 Surge macOS 版生效，iOS 版会自动忽略这个类型的规则。规则会匹配这个进程名的程序，支持 `*` 和 `?` 两种通配符。

> 你也可以把该进程名的所在目录写清楚。至于如何找到这个名称，对于 macOS 软件包，一般在 .app/Contents/MacOS 位置下。

## Ruleset

从 Surge macOS 3.0 版本、Surge iOS 3.4 版本之后，可以通过 URL 或者文件导入一个规则集，这个规则集里可以包含很多条规则。而 Surge 本身提供两个内置的规则集 - SYSTEM 和 LAN，里面包含了已经写好的预置规则。

```
RULE-SET,SYSTEM,DIRECT
```

SYSTEM 是内置的规则集，这个规则集包含了绝大多数来自 macOS 和 iOS 系统本身所发送的请求，但不包括 App Store、iTunes 和其他内容服务发送的请求。

```
RULE-SET,https://raw.githubusercontent.com/jrtx0/surge-list/master/ruleset/unblock.list,DIRECT
RULE-SET,https://raw.githubusercontent.com/jrtx0/surge-list/master/ruleset/blocked.list,Proxy
RULE-SET,https://raw.githubusercontent.com/jrtx0/surge-list/master/ruleset/openai.list,OpenAI
RULE-SET,https://raw.githubusercontent.com/jrtx0/surge-list/master/ruleset/netflix.list,Netflix
RULE-SET,https://raw.githubusercontent.com/jrtx0/surge-list/master/ruleset/telegram.list,Telegram
```

上面这是自定义的外置规则集，规则集的内容是一行一条规则，但不写对应的策略。

```
RULE-SET,LAN,DIRECT
```

这个规则集包括了 'local' 后缀和私有 IP 地址。注意：这个规则集会触发 DNS 查询。

## IP-based Rule

```
GEOIP,CN,DIRECT
```

如果 GeoIP 测试结果与指定的国家代码匹配，则规则匹配。

## Final Rule

```
FINAL,DIRECT,dns-failed
```

FINAL 规则必须写在所有其他类型的规则之后。当某条请求不匹配上面的任何一条规则，都会与 FINAL 规则匹配。dns-failed 代表当 DNS 查询失败后，也会匹配 FIANL 规则，前提是 FINAL 规则的策略不是 DIRECT。