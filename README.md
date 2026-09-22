# rules
rules 分流规则-比较通用的机场规则
rules:
  # 本地及局域网
  - IP-CIDR,127.0.0.0/8,DIRECT
  - IP-CIDR,10.0.0.0/8,DIRECT
  - IP-CIDR,172.16.0.0/12,DIRECT
  - IP-CIDR,192.168.0.0/16,DIRECT
  - IP-CIDR,169.254.0.0/16,DIRECT

  # 常见国内服务
  - DOMAIN-SUFFIX,baidu.com,DIRECT
  - DOMAIN-SUFFIX,qq.com,DIRECT
  - DOMAIN-SUFFIX,taobao.com,DIRECT
  - DOMAIN-SUFFIX,jd.com,DIRECT
  - DOMAIN-SUFFIX,bilibili.com,DIRECT
  - DOMAIN-SUFFIX,aliyun.com,DIRECT
  - DOMAIN-SUFFIX,alipay.com,DIRECT
  - DOMAIN-SUFFIX,wechat.com,DIRECT

  # Google
  - DOMAIN-SUFFIX,google.com,PROXY
  - DOMAIN-SUFFIX,googleapis.com,PROXY
  - DOMAIN-SUFFIX,gstatic.com,PROXY

  # YouTube
  - DOMAIN-SUFFIX,youtube.com,PROXY
  - DOMAIN-SUFFIX,googlevideo.com,PROXY
  - DOMAIN-SUFFIX,ytimg.com,PROXY

  # ChatGPT / OpenAI
  - DOMAIN-SUFFIX,openai.com,PROXY
  - DOMAIN-SUFFIX,chatgpt.com,PROXY
  - DOMAIN-SUFFIX,oaistatic.com,PROXY

  # Claude
  - DOMAIN-SUFFIX,anthropic.com,PROXY
  - DOMAIN-SUFFIX,claude.ai,PROXY

  # GitHub
  - DOMAIN-SUFFIX,github.com,PROXY
  - DOMAIN-SUFFIX,githubusercontent.com,PROXY

  # Telegram
  - DOMAIN-SUFFIX,telegram.org,PROXY
  - DOMAIN-SUFFIX,t.me,PROXY

  # X / Twitter
  - DOMAIN-SUFFIX,x.com,PROXY
  - DOMAIN-SUFFIX,twitter.com,PROXY

  # Facebook / Instagram
  - DOMAIN-SUFFIX,facebook.com,PROXY
  - DOMAIN-SUFFIX,instagram.com,PROXY

  # Netflix
  - DOMAIN-SUFFIX,netflix.com,PROXY
  - DOMAIN-SUFFIX,netflix.net,PROXY
  - DOMAIN-SUFFIX,nflxvideo.net,PROXY

  # 其他全部直连
  - MATCH,DIRECT

  - 这里的 PROXY 必须对应你配置里的代理策略组名称。如果你的机场策略组叫 🚀 节点选择、Proxy 或 机场节点，就需要把 PROXY 全部换成对应的策略组名称。
