## 允许合法机器人爬虫

```
(cf.client.bot) or (http.user_agent contains "duckduckgo") or (http.user_agent contains "facebookexternalhit") or (http.user_agent contains "Feedfetcher-Google") or (http.user_agent contains "LinkedInBot") or (http.user_agent contains "Mediapartners-Google") or (http.user_agent contains "msnbot") or (http.user_agent contains "Slackbot") or (http.user_agent contains "TwitterBot") or (http.user_agent contains "ia_archive") or (http.user_agent contains "yahoo")
```

## 阻止恶意流量

```
(cf.threat_score ge 5 and not cf.client.bot) or (not http.request.version in {"HTTP/1.2" "HTTP/2" "HTTP/3" "SPDY/3.1"}) or (not http.user_agent contains "Mozilla/")
```

