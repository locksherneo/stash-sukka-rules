# Sukka -> Stash V1.4.2.1 Conversion Report

## Upstream

https://ruleset.skk.moe/

## Pipeline

```text
Sukka List
 -> Remove comments / blank lines
 -> Detect Sukka Marker
 -> Remove Marker
 -> Filter iOS PROCESS rules
 -> Analyze provider behavior
 -> Convert / normalize
 -> Deduplicate
 -> Rule conservation audit
 -> Stash semantic validation
 -> Output
```

## Semantic Integrity

# Semantic Integrity Audit

Generator:

`Sukka List -> Stash V1.4.2.1 Semantic Integrity Bugfix Final`

## Global Rule Conservation

| Metric | Count |
|---|---:|
| Source files | 68 |
| Active files | 63 |
| Deprecated files | 5 |
| Source rules total | 378988 |
| Deprecated source rules | 77761 |
| Sukka Markers removed | 62 |
| iOS PROCESS rules filtered | 75 |
| Duplicates removed | 0 |
| Final output rules | 301090 |
| Unaccounted rules | 0 |

## Output

| Behavior | Providers | Rules |
|---|---:|---:|
| domain | 20 | 291257 |
| ipcidr | 11 | 5261 |
| classical | 26 | 4572 |

## Conservation Equation

```text
source_rules_total
=
deprecated_source_rules
+ markers_removed
+ ios_process_filtered
+ duplicates_removed
+ output_rules
```

```text
378988
=
77761
+ 62
+ 75
+ 0
+ 301090
```

## Result

```text
unaccounted_rules = 0
```

`0` means every source rule has been accounted for.

## Removed Sukka Markers

```text
domainset/apple_cdn.conf: 7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
domainset/cdn.conf: 7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
domainset/game-download.conf: 7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
domainset/icloud_private_relay.conf: 7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
domainset/reject.conf: 7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
domainset/reject_phishing.conf: 7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
domainset/speedtest.conf: 7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
domainset/speedtest.conf: 7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/ai.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/apple_cn.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/apple_intelligence.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/apple_services.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/cdn.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/cloudmounter.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/direct.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/domestic.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/download.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/gitlab.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/global.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/lan.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/microsoft.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/microsoft_cdn.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/my_direct.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/my_git.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/my_plus.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/my_proxy.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/my_reject.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/my_tw.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/my_us.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/neteasemusic.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/reject-drop.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/reject-no-drop.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/reject-url-regex.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/reject.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/sogouinput.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/stream.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/stream_eu.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/stream_hk.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/stream_jp.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/stream_kr.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/stream_tw.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/stream_us.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
non_ip/telegram.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
ip/ai.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
ip/apple_services.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
ip/cdn.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
ip/china_ip.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
ip/china_ip_ipv6.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
ip/domestic.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
ip/download.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
ip/lan.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
ip/neteasemusic.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
ip/reject.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
ip/stream.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
ip/stream_eu.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
ip/stream_hk.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
ip/stream_jp.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
ip/stream_kr.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
ip/stream_tw.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
ip/stream_us.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
ip/telegram.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
ip/telegram_asn.conf: DOMAIN,7h15.ru1353t.1s.m4d3.by.5ukk4w.skk.moe
```

## iOS PROCESS Rules Filtered

```text
non_ip/apple_services.conf: PROCESS-NAME,com.apple.geod
non_ip/apple_services.conf: PROCESS-NAME,mapspushd
non_ip/apple_services.conf: PROCESS-NAME,com.apple.Maps
non_ip/apple_services.conf: PROCESS-NAME,apsd
non_ip/apple_services.conf: PROCESS-NAME,fmfd
non_ip/apple_services.conf: PROCESS-NAME,findmydevice-user-agent
non_ip/apple_services.conf: PROCESS-NAME,CoreLocationAgent
non_ip/apple_services.conf: PROCESS-NAME,WeatherWidget
non_ip/direct.conf: PROCESS-NAME,v2ray
non_ip/direct.conf: PROCESS-NAME,xray
non_ip/direct.conf: PROCESS-NAME,ss-local
non_ip/direct.conf: PROCESS-NAME,clash
non_ip/direct.conf: PROCESS-NAME,ClashX
non_ip/direct.conf: PROCESS-NAME,trojan
non_ip/direct.conf: PROCESS-NAME,trojan-go
non_ip/direct.conf: PROCESS-NAME,privoxy
non_ip/direct.conf: PROCESS-NAME,cloudflared
non_ip/direct.conf: PROCESS-NAME,aria2c
non_ip/direct.conf: PROCESS-NAME,fdm
non_ip/direct.conf: PROCESS-NAME,Folx
non_ip/direct.conf: PROCESS-NAME,NetTransport
non_ip/direct.conf: PROCESS-NAME,Thunder
non_ip/direct.conf: PROCESS-NAME,ThunderVIP
non_ip/direct.conf: PROCESS-NAME,Transmission
non_ip/direct.conf: PROCESS-NAME,transmission-daemon
non_ip/direct.conf: PROCESS-NAME,transmission-qt
non_ip/direct.conf: PROCESS-NAME,BitComet
non_ip/direct.conf: PROCESS-NAME,uTorrent
non_ip/direct.conf: PROCESS-NAME,qbittorrent*
non_ip/direct.conf: PROCESS-NAME,DownloadService
non_ip/direct.conf: PROCESS-NAME,qBittorrent
non_ip/direct.conf: PROCESS-NAME,qbittorrent-nox
non_ip/direct.conf: PROCESS-NAME,WebTorrent
non_ip/direct.conf: PROCESS-NAME,WebTorrent Helper
non_ip/direct.conf: PROCESS-NAME,amuled
non_ip/direct.conf: PROCESS-NAME,LocalSend
non_ip/direct.conf: PROCESS-NAME,UUBooster
non_ip/direct.conf: PROCESS-NAME,tailscaled
non_ip/direct.conf: PROCESS-NAME,parsecd
non_ip/direct.conf: PROCESS-NAME,SunloginClient_Desktop
non_ip/direct.conf: PROCESS-NAME,SunloginClient_Helper
non_ip/direct.conf: PROCESS-NAME,BaiduNetdisk_mac
non_ip/direct.conf: PROCESS-NAME,Logi Options
non_ip/direct.conf: PROCESS-NAME,Logi Options Daemon
non_ip/my_direct.conf: PROCESS-NAME,nmap
non_ip/my_reject.conf: PROCESS-NAME,Tencent Lemon
non_ip/my_reject.conf: PROCESS-NAME,LemonMonitor
non_ip/my_reject.conf: PROCESS-NAME,LemonDaemon
non_ip/my_reject.conf: PROCESS-NAME,LemonAgent
non_ip/my_reject.conf: PROCESS-NAME,LemonService
non_ip/sogouinput.conf: PROCESS-NAME,SogouInput
non_ip/sogouinput.conf: PROCESS-NAME,SogouTaskManager
non_ip/sogouinput.conf: PROCESS-NAME,SogouServices
non_ip/stream.conf: PROCESS-NAME,com.amazon.avod.thirdpartyclient
non_ip/stream.conf: PROCESS-NAME,tv
non_ip/stream.conf: PROCESS-NAME,music
non_ip/stream.conf: PROCESS-NAME,com.bstar.intl
non_ip/stream.conf: PROCESS-NAME,com.hulu.plus
non_ip/stream.conf: PROCESS-NAME,com.tencent.ibg.joox
non_ip/stream.conf: PROCESS-NAME,com.linecorp.linetv
non_ip/stream.conf: PROCESS-NAME,com.netflix.mediaclient
non_ip/stream.conf: PROCESS-NAME,com.twgood.android
non_ip/stream.conf: PROCESS-NAME,tv.twitch.android.app
non_ip/stream.conf: PROCESS-NAME,com.viu.pad
non_ip/stream.conf: PROCESS-NAME,com.viu.phone
non_ip/stream.conf: PROCESS-NAME,com.vuclip.viu
non_ip/stream.conf: PROCESS-NAME,com.hktve.viutv
non_ip/stream_biliintl.conf: PROCESS-NAME,com.bstar.intl
non_ip/stream_hk.conf: PROCESS-NAME,com.viu.pad
non_ip/stream_hk.conf: PROCESS-NAME,com.viu.phone
non_ip/stream_hk.conf: PROCESS-NAME,com.vuclip.viu
non_ip/stream_hk.conf: PROCESS-NAME,com.hktve.viutv
non_ip/stream_hk.conf: PROCESS-NAME,com.bstar.intl
non_ip/stream_tw.conf: PROCESS-NAME,com.linecorp.linetv
non_ip/stream_us.conf: PROCESS-NAME,com.hulu.plus
```

## non_ip Promoted to domain

- domainset/apple_cdn.conf
- domainset/cdn.conf
- domainset/game-download.conf
- domainset/icloud_private_relay.conf
- domainset/reject.conf
- domainset/reject_phishing.conf
- domainset/speedtest.conf
- non_ip/apple_cn.conf
- non_ip/apple_intelligence.conf
- non_ip/gitlab.conf
- non_ip/lan.conf
- non_ip/my_direct.conf
- non_ip/my_git.conf
- non_ip/my_plus.conf
- non_ip/my_proxy.conf
- non_ip/my_tw.conf
- non_ip/my_us.conf
- non_ip/reject-drop.conf
- non_ip/stream_biliintl.conf
- non_ip/telegram.conf

## IP Promoted to ipcidr

- ai
- apple_services
- cdn
- china_ip
- china_ip_ipv6
- domestic
- download
- lan
- neteasemusic
- stream
- telegram

## ipcidr Providers Requiring no-resolve

- ai
- apple_services
- domestic
- download
- neteasemusic
- stream
- telegram

## Skipped Sources

- DEPRECATED: domainset/download.conf
- DEPRECATED: domainset/reject_extra.conf
- DEPRECATED: domainset/reject_sukka.conf
- DEPRECATED: non_ip/apple_cdn.conf
- DEPRECATED: non_ip/global_plus.conf
- EMPTY AFTER CLEAN: ip/stream_eu.conf
- EMPTY AFTER CLEAN: ip/stream_hk.conf
- EMPTY AFTER CLEAN: ip/stream_jp.conf
- EMPTY AFTER CLEAN: ip/stream_kr.conf
- EMPTY AFTER CLEAN: ip/stream_tw.conf
- EMPTY AFTER CLEAN: ip/stream_us.conf
