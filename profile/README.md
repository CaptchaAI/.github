<!-- Banner / Logo -->
<p align="center">
 <a href="https://captchaai.com/?utm_source=github&amp;utm_medium=profile&amp;utm_campaign=org-profile"> <img src="https://captchaai.com/logo.png" alt="CaptchaAI Logo" width="300"/> </a>
</p>

<p align="center">
  <strong>AI-powered CAPTCHA solving API, official SDKs, n8n nodes, and browser automation tools.</strong>
</p>

<p align="center">
  <a href="https://captchaai.com/?utm_source=github&amp;utm_medium=profile&amp;utm_campaign=org-profile#pricing"><strong>Get API Key</strong></a> &nbsp;•&nbsp;
  <a href="https://docs.captchaai.com/?utm_source=github&amp;utm_medium=profile&amp;utm_campaign=org-profile"><strong>API Documentation</strong></a> &nbsp;•&nbsp;
  <a href="#-official-sdks--developer-tools"><strong>Official SDKs</strong></a> &nbsp;•&nbsp;
  <a href="https://chromewebstore.google.com/detail/fnnmnnfpdnlkccecmiicejhimhkbolhk?utm_source=item-share-cb"><strong>Chrome Extension</strong></a> &nbsp;•&nbsp;
  <a href="https://captchaai.com/?utm_source=github&amp;utm_medium=profile&amp;utm_campaign=org-profile#pricing"><strong>Pricing</strong></a>
</p>

---

## 🚀 What is CaptchaAI?

CaptchaAI is an AI-powered image and CAPTCHA recognition service. CaptchaAI's main purpose is solving your CAPTCHAs in a quick, reliable, and cost-effective way using Artificial Intelligence.

---

## ✨ Features
- Supports **reCAPTCHA v2 / v3 / Enterprise**, **Cloudflare Turnstile & Challenge**, **GeeTest v3**, and **27,500+ image CAPTCHAs**  
- **Low-latency** responses for real-time automation and scraping  
- **Easy integrations** (REST API + 4 official language SDKs + 2 n8n community nodes + diagnostic CLI)  
- **Secure, reliable infrastructure** with high availability and proxy support

---

## 📦 Official SDKs & Developer Tools

We maintain official, production-ready libraries across 4 languages, 2 n8n community nodes, and an automated workflow diagnostic CLI:

| Tool / Integration | Platform / Language | GitHub Repository | Install / Quick Start |
| :--- | :--- | :--- | :--- |
| **Python SDK** | Python 3.10+ (`httpx`, sync & `asyncio`) | [`CaptchaAI/captchaai-python`](https://github.com/CaptchaAI/captchaai-python) | `pip install captchaai` |
| **Node.js / TypeScript SDK** | Node 18+ & TypeScript (native `fetch`) | [`CaptchaAI/captchaai-javascript`](https://github.com/CaptchaAI/captchaai-javascript) | `npm i captchaai-javascript` |
| **PHP SDK** | PHP 8.2+ (`Guzzle` / PSR-18) | [`CaptchaAI/captchaai-PHP`](https://github.com/CaptchaAI/captchaai-PHP) | `composer require captchaai/captchaai` |
| **Go SDK** | Go 1.22+ (`context.Context`, zero deps) | [`CaptchaAI/captchaai-go`](https://github.com/CaptchaAI/captchaai-go) | `go get github.com/CaptchaAI/captchaai-go` |
| **n8n Solver Node** | n8n Community Package | [`CaptchaAI/n8n-nodes-captchaai`](https://github.com/CaptchaAI/n8n-nodes-captchaai) | Install `n8n-nodes-captchaai` in n8n |
| **n8n Detector Node** | n8n Community Package | [`CaptchaAI/n8n-captchaai-detector`](https://github.com/CaptchaAI/n8n-captchaai-detector) | Install `n8n-nodes-captchaai-detect` in n8n |
| **Workflow Doctor CLI** | Diagnostic CLI (`playwright`) | [`CaptchaAI/captchaai-workflow-doctor`](https://github.com/CaptchaAI/captchaai-workflow-doctor) | E2E failure root-cause analysis |
| **Code Examples** | Multi-language recipes | [`CaptchaAI/CaptchaAI-Examples`](https://github.com/CaptchaAI/CaptchaAI-Examples) | Python, JS, PHP, Go, Java, Selenium |

### Quick Start (Python)
```python
from captchaai import CaptchaAI

client = CaptchaAI(api_key="YOUR_API_KEY")

# Solve Cloudflare Turnstile in seconds
result = client.solve({
    "type": "TurnstileTaskProxyless",
    "websiteURL": "https://example.com/login",
    "websiteKey": "0x4AAAAAAAB..."
})
print("Token:", result.solution.token)
```

### Quick Start (TypeScript / Node.js)
```typescript
import { CaptchaAI } from "captchaai-javascript";

const client = new CaptchaAI({ apiKey: "YOUR_API_KEY" });

// Solve reCAPTCHA v2
const result = await client.solve({
  type: "NoCaptchaTaskProxyless",
  websiteURL: "https://example.com",
  websiteKey: "6Le-wvkSAAAAAPBMRTvw0Q4CeHgBQBp18..."
});
console.log("Token:", result.solution.gRecaptchaResponse);
```

---

## 🧩 Browser Automation Extension

The [CaptchaAI solver extension](https://captchaai.com/lp/captcha-bypass-extension?utm_source=github&amp;utm_medium=profile&amp;utm_campaign=org-profile) allows you to automatically solve CAPTCHAs on any webpage or inside browser automation frameworks (Playwright, Puppeteer, Selenium).

[![Chrome Extension](https://img.shields.io/badge/Chrome-Extension-4285F4?logo=googlechrome&logoColor=white&style=for-the-badge)](https://chromewebstore.google.com/detail/fnnmnnfpdnlkccecmiicejhimhkbolhk?utm_source=item-share-cb)

---

## ✅ Supported Challenges

- **Image/Text CAPTCHAs:** 27,500+ types supported
- **reCAPTCHA:** v2, v2 Invisible, v2 Callback, v2 Enterprise, v3, v3 Enterprise
- **Cloudflare:** Cloudflare Turnstile and Cloudflare Challenge
- **GeeTest:** GeeTest v3
- **Specialized Tasks:** Grid Image and BLS
- **In beta:** CaptchaFox, Friendly Captcha, Lemin
- **Workflows:** Custom workflows via `solve`, `send` / `get_result`, `threads_info`, proxies, and async helpers

---

## 📚 Documentation & Resources

To get started quickly, check the [CaptchaAI Documentation](https://docs.captchaai.com/?utm_source=github&amp;utm_medium=profile&amp;utm_campaign=org-profile).

---

## 📣 Connect with us

[![Telegram](https://img.shields.io/badge/Telegram-Channel-26A5E4?logo=telegram&logoColor=white&style=for-the-badge)](https://t.me/+GOIbbcX6dig3ZDg0) 
[![YouTube](https://img.shields.io/badge/YouTube-Channel-FF0000?logo=youtube&logoColor=white&style=for-the-badge)](https://www.youtube.com/@captchaai) 
[![Facebook](https://img.shields.io/badge/Facebook-Page-1877F2?logo=facebook&logoColor=white&style=for-the-badge)](https://www.facebook.com/CaptchaAI) 
[![Instagram](https://img.shields.io/badge/Instagram-Profile-E4405F?logo=instagram&logoColor=white&style=for-the-badge)](https://www.instagram.com/captchaai/) 

## 💬 Customer Support 
[![Telegram](https://img.shields.io/badge/Contact-us-26A5E4?logo=telegram&logoColor=white&style=for-the-badge)](https://t.me/AskCaptchaAI)

---

## ⚙️ Package Registries & Links

- 🌐 **Website:** [https://captchaai.com/](https://captchaai.com/?utm_source=github&amp;utm_medium=profile&amp;utm_campaign=org-profile)
- 📘 **API Documentation:** [https://docs.captchaai.com/](https://docs.captchaai.com/?utm_source=github&amp;utm_medium=profile&amp;utm_campaign=org-profile)
- 🐍 **PyPI (Python):** [`https://pypi.org/project/captchaai/`](https://pypi.org/project/captchaai/)
- 📦 **npm (Node.js/TS):** [`https://www.npmjs.com/package/captchaai-javascript`](https://www.npmjs.com/package/captchaai-javascript)
- 🐘 **Packagist (PHP):** [`https://packagist.org/packages/captchaai/captchaai`](https://packagist.org/packages/captchaai/captchaai)
- 🐹 **pkg.go.dev (Go):** [`https://pkg.go.dev/github.com/CaptchaAI/captchaai-go`](https://pkg.go.dev/github.com/CaptchaAI/captchaai-go)
- ⚡ **n8n Community Node:** [`https://www.npmjs.com/package/n8n-nodes-captchaai`](https://www.npmjs.com/package/n8n-nodes-captchaai)
