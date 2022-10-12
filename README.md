# MyClashProfile
MyClashProfile
### bypass
``` yaml
bypass:
  - "*.126.com"
  - "*.126.net"
  - "*.163.com"
  - "*.baidu.com"
  - "*.bing.com"
  - "*.iqiyi.com" # 爱奇艺
  - "*.kuwo.cn" # 酷我音乐
  - "*.microsoft.com"
  - "*.msftncsi.com" # 微软
  - "*.music.126.net" # 网易云
  - "baidu.com"
  - "music.163.com" # 网易云
  - localhost
  - 127.*
  - 10.*
  - 172.16.*
  - 172.17.*
  - 172.18.*
  - 172.19.*
  - 172.20.*
  - 172.21.*
  - 172.22.*
  - 172.23.*
  - 172.24.*
  - 172.25.*
  - 172.26.*
  - 172.27.*
  - 172.28.*
  - 172.29.*
  - 172.30.*
  - 172.31.*
  - 192.168.*
  - <local>
```
### parsers
``` yaml
# append-rules	数组	数组合并至原配置rules数组后
# prepend-rules	数组	数组合并至原配置rules数组前
# append-proxies	数组	数组合并至原配置proxies数组后
# prepend-proxies	数组	数组合并至原配置proxies数组前
# append-proxy-groups	数组	数组合并至原配置proxy-groups数组后
# prepend-proxy-groups	数组	数组合并至原配置proxy-groups数组前
# mix-proxy-providers	对象	对象合并至原配置proxy-providers中
# mix-rule-providers	对象	对象合并至原配置rule-providers中
# mix-object	对象	对象合并至原配置最外层中
# commands	数组	在上面操作完成后执行简单命令操作配置文件
parsers:
  - reg: https://+.+
    yaml:
      prepend-rules:
        - DOMAIN-SUFFIX,xxxxxx.org,DIRECT
        - DOMAIN-SUFFIX,xxxxxx.com,DIRECT
      mix-object:
        hosts:
          "*.cloud.com": 192.168.0.1
```
