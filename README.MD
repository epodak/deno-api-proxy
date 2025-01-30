# Deno API代理
# Deno API Proxy

[不要本地部署DeepSeek了，免费光速版API 免费无限量使用DeepSeek最大的70B的蒸馏模型，并且输出速度飞快。这样就不用本地部署DeepSeek，多快好省，节约电费。 #AI #人工智能 #科技 #教程 #计算机 - 抖音](https://www.douyin.com/video/7465347298051001638)

### 作者：技术爬爬虾
B站，YouTube，抖音，公众号 全网同名。转载请注明作者。

## 项目简介
使用Deno将Open AI, Claude, Groq等API代理到国内，打破地域限制。

## Deno部署（推荐）

1. 登录/注册 [https://dash.deno.com/account/projects](https://dash.deno.com/account/projects)
2. 点击右上角的New Playground
3. 把main.ts里面所有代码复制进去
4. 点击 Save & Deploy 
5. 查看部署后的服务的域名（长这样：xxx.deno.dev）
6. 将域名，需要代理的服务名字，API Key填入下方命令中

<b>代理 OepnAI</b>
```
curl --location 'https://YOUR-DOMAIN/api.openai.com/v1/chat/completions' \
--header 'Authorization: Bearer YOUR-API-KEY' \
--header 'Content-Type: application/json' \

--data '{
    "messages": [
        {
            "role": "system",
            "content": "You are a test assistant."
        },
        {
            "role": "user",
            "content": "Testing. Just say hi and nothing else."
        }
    ],
    "model": "gemini-2.0-flash-exp"
}'
```

<b>代理Groq</b>
```
curl --location 'https://YOUR-DOMAIN/api.groq.com/v1/chat/completions' \
--header 'Authorization: Bearer YOUR-API-KEY' \
--header 'Content-Type: application/json' \

--data '{
    "messages": [
        {
            "role": "system",
            "content": "You are a test assistant."
        },
        {
            "role": "user",
            "content": "Testing. Just say hi and nothing else."
        }
    ],
    "model": "gemini-2.0-flash-exp"
}'
```
