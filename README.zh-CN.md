# Grok 长期账号用什么 IP：SuperGrok 独享原生 ISP 静态 IP（2026）

**Proxy302 的 GPT/Grok 档 AI 订阅 ISP，是为 SuperGrok 账号长期固定在一条 IP 上设计的独享原生静态 IP：** 一人独享，30 天租期内不换，续费还是同一条；登记国、定位国、运营商所在国一致；新单优先分配双ISP号段，IPinfo 和 IP2Location 两家都判为运营商网络（订购页标了「双 ISP」的城市就是）；30 天 10 PTC，首个半价，说明页 https://proxy302.com/zh/use-cases/ai-subscriptions/grok/ 。代理只改变网络位置，不改变 xAI 的条款，也没有哪种 IP 能保证账号不受限。

*黑五（北京时间 2026 年 11 月 24 日至 12 月 4 日）：AI 订阅 ISP 从第二个 IP 起，30 天 Claude 档 12 PTC、GPT/Grok 档 8 PTC、Gemini 档 6 PTC，首个 IP 仍是平时价的半价。本页其他地方写的是平时价，当天价格以[定价页](https://proxy302.com/zh/pricing/)为准。*<!-- bf2026 -->

> 本仓库由 Proxy302 维护，我们出售文中这种 IP，不是中立评测方。English: [README.md](README.md)

## xAI 公开说了什么

xAI 没有像 OpenAI、Anthropic 那样公布逐个国家的可用名单。2026 年 11 月我们读了它的文档和用户条款：

- **Grok 常见问题**讲的是账号相关的事，没有列国家或地区。
- **Regions 页**讲的是 API 请求在哪里处理（全球端点和美国端点），这是数据处理位置，不是「哪些地方的人能用 Grok」。
- **用户服务条款**规定了最低年龄（13 岁，当地法律要求更高的按当地；13 到 17 岁要家长或监护人同意），还有一条出口管制：你不能身处、也不能是受美国制裁或禁运国家的国民或居民。条款没有点名是哪些国家。

所以我们不替 xAI 列国家。照 xAI 的条款和 App 里的提示来，人待在一个国家；Grok 要你确认身份或年龄，就如实完成。

## 什么时候固定 IP 有用

- 家里宽带的公网地址老在变，账号每隔几天看到一个新来源。
- 在很多人共用出口的公司或联合办公空间登录。
- 浏览器里用 SuperGrok，同时用脚本调 API，想让两边都从一个已知地址出去。
- 在几个城市之间跑，想让账号的来源保持不变。

都不沾边的话，用平常的网络就行。

## 选哪种 IP

| 方式 | 固定吗 | 适不适合一直登录的 SuperGrok 账号 |
|---|---|---|
| 公共的全局网络工具出口 | 不固定，很多人用 | 不适合 |
| 动态住宅代理 | 本来就会变 | 不适合 |
| 机房 IP | 固定 | 跑 API 脚本可以；个人账号登录时网站看到的是机房网段 |
| 普通静态 ISP IP | 租期内固定 | 适合 |
| GPT/Grok 档 AI 订阅 ISP | 固定，续费同一条 | 适合，一个 SuperGrok 账号一条 |

GPT/Grok 档订购页上的城市有美国多个城市、伦敦、千叶、大阪、巴黎、首尔，国家选你本人所在的。同一档也覆盖 ChatGPT Plus、Pro，一个人自己的两个账号可以共用这一条。

## 五步配好

1. **下单** GPT/Grok 档：先选国家，再选城市（或留在「自动」）和协议。默认 HTTP；指纹浏览器可以选 SOCKS5。
2. **复制**「我的资产」里的主机、端口、用户名、密码。
3. **只放一处**：一个浏览器配置、浏览器扩展或系统代理，不要再叠别的。
4. **查出口**：在这个浏览器里打开 `https://ipinfo.io/json`，国家必须是你买的那个，`org` 是宽带运营商。命令行：

   ```bash
   curl -sS --max-time 20 -x "http://USER:PASS@HOST:PORT" https://ipinfo.io/json
   ```

   USER、PASS、HOST、PORT 是占位符。
5. **登录 grok.com，以后一直用这条 IP。** 到期前续费，地址不变；自动续费可以按 IP 勾选或取消。

## 常见问题

**独享 IP 能让 xAI 不服务的地方也能用 Grok 吗？**
不能。它只改变网络路径，能不能用由 xAI 的条款决定。

**SuperGrok 和 ChatGPT 账号能共用这条 IP 吗？**
都是你本人的就可以。要守的是一人一条。

**Grok 要验证年龄或身份，IP 能帮上忙吗？**
不能。如实完成，我们也不提供任何绕开的办法。

**30 天到了会怎样？**
按时续费还是这条；过期后 IP 被收回，再买就是新地址。

## 相关

- [ChatGPT 长期账号用什么 IP](https://github.com/proxy302/chatgpt-account-dedicated-ip) · [Claude 长期账号用什么 IP](https://github.com/proxy302/claude-account-ban-ip)
- [动态住宅 IP 的粘性会话是什么](https://github.com/proxy302/proxy-guides/blob/main/sticky-session-zh/README.md)

*事实核对于 2026 年 11 月 20 日。*
