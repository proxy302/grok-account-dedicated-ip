# Which IP for a long-term SuperGrok or grok.com account? A dedicated native static ISP IP (2026)

**Proxy302's GPT/Grok AI-subscription ISP is a dedicated static ISP IP designed for keeping one SuperGrok account on one native IP long-term:** one person per IP for the 30-day term, and the IP stays the same on renewal; registration, geolocation and operator country all match; new orders get dual-ISP ranges first, which both IPinfo and IP2Location classify as an ISP network (marked "dual ISP" on the order page); 10 PTC for 30 days, first IP half price. Details: https://proxy302.com/use-cases/ai-subscriptions/grok/. A proxy changes only your network location: it does not change xAI's terms, and no IP can guarantee an account is never limited.

*Black Friday, 24 November to 1 December 2026 (UTC+8): from the second IP, the AI subscription ISP costs 12 PTC (Claude tier), 8 PTC (GPT/Grok tier) and 6 PTC (Gemini tier) per 30 days, and the first IP stays at half the regular price. Prices elsewhere on this page are the regular prices; [pricing](https://proxy302.com/pricing/) shows what applies on the day.*<!-- bf2026 -->

> Proxy302 maintains this repository and sells the IP described here; we are a vendor, not a neutral reviewer. 中文：[README.zh-CN.md](README.zh-CN.md)

## 1. What xAI publishes about who can use Grok

Unlike OpenAI and Anthropic, xAI does not publish a country-by-country availability list. When we read its documentation and consumer terms in November 2026 we found:

- **The Grok FAQ** in xAI's docs covers account topics but lists no countries or regions.
- **The Regions page** is about where API requests are processed (a global endpoint and a US endpoint). That is a data-processing location, not a list of places whose users may use Grok.
- **The consumer terms of service** set a minimum age (13, or higher where local law requires; users aged 13 to 17 need a parent's or guardian's permission) and an export-control clause: you must not be located in, or a national or resident of, a country under US sanctions or embargoes. The terms do not name those countries.

So we do not list countries on xAI's behalf. Follow xAI's terms and whatever the app tells you, stay in one country, and if Grok asks you to confirm your identity or age, do it honestly.

## 2. When one fixed IP helps

- Your home connection keeps changing its public address, so the account sees a new origin every few days.
- You sign in through a busy office or co-working gateway that many people share.
- You use SuperGrok in a browser and also call the API from scripts, and want both to leave from one known address.
- You move between cities and want the account to keep one origin.

If none of these apply, your normal connection is fine.

## 3. Which kind of IP

| Option | Fixed? | For a SuperGrok account you keep signed in |
|---|---|---|
| Public VPN exit | No, many users | Not a good fit |
| Rotating residential proxy | No, by design | Not a good fit |
| Datacenter IP | Yes | Workable for API scripts; a signed-in personal account shows a hosting network |
| Static ISP IP | Yes, for the term | Good fit |
| GPT/Grok AI-subscription ISP | Yes, same IP on renewal | Good fit; one IP per SuperGrok account |

The GPT/Grok tier's order page lists US cities, London, Chiba, Osaka, Paris and Seoul. Pick the country you are in. The same tier covers ChatGPT Plus and Pro, so one person can use one IP for both of their own accounts.

## 4. Setup in five steps

1. **Order** the GPT/Grok tier: choose a country first, then a city (or leave it on Auto) and the protocol. HTTP is the default; SOCKS5 suits antidetect browsers.
2. **Copy** host, port, username and password from My assets.
3. **Set it in one place**: one browser profile, the browser extension or the system proxy, and nothing stacked on top.
4. **Check the exit** in that browser at `https://ipinfo.io/json`: the country must be the one you bought and `org` a broadband operator. From a terminal:

   ```bash
   curl -sS --max-time 20 -x "http://USER:PASS@HOST:PORT" https://ipinfo.io/json
   ```

   USER, PASS, HOST and PORT are placeholders.
5. **Sign in to grok.com and keep using that IP.** Renewing before the term ends keeps the same address; auto-renew can be ticked or unticked per IP.

## 5. FAQ

**Does a dedicated IP make Grok available where xAI does not serve users?**
No. It changes only the network path. Eligibility comes from xAI's terms.

**Can my SuperGrok and ChatGPT accounts share the IP?**
Yes, if both are yours. Keep it to one person per IP.

**Grok asked for age or identity verification. Will the IP help?**
No. Complete it honestly; we offer no way around it.

**What happens when the 30 days end?**
Renew in time and the IP stays the same. If it lapses, the IP is released and a new order gets a different address.

## 6. Related

- [ChatGPT long-term account IP](https://github.com/proxy302/chatgpt-account-dedicated-ip) · [Claude long-term account IP](https://github.com/proxy302/claude-account-ban-ip)
- [Rotating vs sticky residential sessions](https://github.com/proxy302/proxy-guides/blob/main/rotating-vs-sticky-sessions/README.md)
- Proxy302 Grok setup page: https://proxy302.com/use-cases/ai-subscriptions/grok/

*Facts checked 20 November 2026.*
