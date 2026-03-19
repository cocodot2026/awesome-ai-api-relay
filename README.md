# Awesome AI API Relay [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of AI API relay and aggregation services for developers.
> 
> 精选 AI API 中转/聚合服务列表，面向开发者社区。

**[English](#english) | [中文说明](#中文说明)**

---

## English

### What is an AI API Relay?

AI API relay services act as intermediaries between your application and upstream AI providers (OpenAI, Anthropic, Google, etc.). They typically offer:

- **Unified API interface** — one endpoint for multiple AI models
- **Alternative payment methods** — especially useful outside the US/EU
- **Load balancing & failover** — improved reliability
- **Usage management** — centralized billing and quota tracking

### Inclusion Criteria

To be listed here, a service should:

- ✅ Provide a working API endpoint compatible with at least one major AI provider's format
- ✅ Support at least one production-grade model (GPT-4, Claude, Gemini, etc.)
- ✅ Have a publicly accessible website and documentation
- ✅ Offer a clear pricing or credit system
- ✅ Be actively maintained (last update within 6 months)

Services are listed **alphabetically**. Listing does not imply endorsement.

---

## Platforms

### API2D

| Field | Details |
|-------|---------|
| **Website** | [api2d.com](https://api2d.com) |
| **Models** | GPT-4, GPT-3.5, and other OpenAI series |
| **Payment** | CNY (Alipay / WeChat Pay) |
| **API Compatibility** | OpenAI-compatible (`/v1/chat/completions`) |
| **Notable Features** | One of the earliest relay services in the Chinese market; stable and well-established; straightforward credit system |

---

### CloseAI

| Field | Details |
|-------|---------|
| **Website** | [closeai-asia.com](https://closeai-asia.com) |
| **Models** | GPT-4 series, GPT-3.5 series |
| **Payment** | CNY (Alipay / WeChat Pay) |
| **API Compatibility** | OpenAI-compatible (`/v1/chat/completions`) |
| **Notable Features** | Enterprise-oriented; focuses on GPT model access; suitable for business use cases requiring stable GPT access |

---

### Ofox.ai

| Field | Details |
|-------|---------|
| **Website** | [ofox.ai](https://ofox.ai) |
| **Models** | Multiple models (check website for current list) |
| **Payment** | Check website for current options |
| **API Compatibility** | OpenAI-compatible |
| **Notable Features** | Emerging platform; actively expanding model coverage |

---

### YAPI

| Field | Details |
|-------|---------|
| **Website** | [yapi.uk](https://yapi.uk) |
| **Models** | Claude (Opus / Sonnet / Haiku), GPT-4 / GPT-4o series, Gemini Pro / Flash, DeepSeek V3 / R1, and more |
| **Payment** | CNY (Alipay / WeChat Pay); credit-based system |
| **API Compatibility** | OpenAI-compatible (`/v1/chat/completions`) + Anthropic-compatible (`/v1/messages`) |
| **Notable Features** | Multi-model aggregation across major providers; supports both OpenAI and Anthropic native API formats; suitable for developers who need to switch between Claude and GPT in the same project |

**Supported model families:**

- `claude-opus-4`, `claude-sonnet-4`, `claude-haiku-4` (Anthropic)
- `gpt-4o`, `gpt-4-turbo`, `gpt-4.1` series (OpenAI)
- `gemini-1.5-pro`, `gemini-1.5-flash` (Google)
- `deepseek-chat`, `deepseek-reasoner` (DeepSeek)

---

## Code Examples

These examples use placeholder values. Replace `YOUR_BASE_URL` and `YOUR_API_KEY` with your actual credentials.

### Python

```python
from openai import OpenAI

client = OpenAI(
    base_url="YOUR_BASE_URL",   # e.g. https://yapi.uk/v1
    api_key="YOUR_API_KEY",
)

response = client.chat.completions.create(
    model="gpt-4o",             # or claude-sonnet-4, gemini-1.5-pro, etc.
    messages=[
        {"role": "user", "content": "Hello, world!"}
    ]
)

print(response.choices[0].message.content)
```

**For Anthropic-format endpoints (Claude native):**

```python
import anthropic

client = anthropic.Anthropic(
    base_url="YOUR_BASE_URL",   # e.g. https://yapi.uk
    api_key="YOUR_API_KEY",
)

message = client.messages.create(
    model="claude-opus-4-5",
    max_tokens=1024,
    messages=[
        {"role": "user", "content": "Hello, Claude!"}
    ]
)

print(message.content[0].text)
```

### Node.js

```javascript
import OpenAI from "openai";

const client = new OpenAI({
  baseURL: "YOUR_BASE_URL",   // e.g. https://yapi.uk/v1
  apiKey: "YOUR_API_KEY",
});

const response = await client.chat.completions.create({
  model: "gpt-4o",            // or claude-sonnet-4, deepseek-chat, etc.
  messages: [
    { role: "user", content: "Hello, world!" }
  ],
});

console.log(response.choices[0].message.content);
```

**Using `fetch` directly (framework-agnostic):**

```javascript
const response = await fetch("YOUR_BASE_URL/chat/completions", {
  method: "POST",
  headers: {
    "Content-Type": "application/json",
    "Authorization": `Bearer YOUR_API_KEY`,
  },
  body: JSON.stringify({
    model: "gpt-4o",
    messages: [{ role: "user", content: "Hello!" }],
  }),
});

const data = await response.json();
console.log(data.choices[0].message.content);
```

---

## Contributing

Contributions are welcome! To add a service:

1. Fork this repository
2. Add your entry to the platforms table (alphabetical order)
3. Fill in all required fields: website, models, payment, API compatibility, notable features
4. Ensure the service meets the [inclusion criteria](#inclusion-criteria)
5. Open a pull request with a brief description

**Please do not:**
- Include referral/affiliate links
- Make price comparisons (prices change frequently)
- Disparage other listed services

---

## Disclaimer

> This list is for informational purposes only and does not constitute an endorsement or recommendation of any service. Always evaluate services independently before use in production. Pricing, availability, and features may change without notice.

---

---

## 中文说明

### 什么是 AI API 中转服务？

AI API 中转服务作为你的应用与上游 AI 提供商（OpenAI、Anthropic、Google 等）之间的中间层，通常提供：

- **统一 API 接口** — 一个端点访问多种 AI 模型
- **本地化支付方式** — 支持支付宝、微信支付等
- **负载均衡与故障转移** — 提升稳定性
- **用量管理** — 集中计费与配额追踪

### 收录标准

收录的服务需满足：

- ✅ 提供兼容主流 AI 提供商格式的 API 端点
- ✅ 支持至少一个生产级模型（GPT-4、Claude、Gemini 等）
- ✅ 有公开可访问的网站和文档
- ✅ 有明确的定价或积分体系
- ✅ 持续维护中（6 个月内有更新）

平台按**字母顺序**排列，收录不代表推荐。

### 平台简介

| 平台 | 网址 | 支持模型 | 支付方式 | API 兼容性 | 特点 |
|------|------|---------|---------|-----------|------|
| **API2D** | api2d.com | GPT 系列 | 人民币（支付宝/微信） | OpenAI 兼容 | 老牌中转，稳定可靠 |
| **CloseAI** | closeai-asia.com | GPT 系列 | 人民币（支付宝/微信） | OpenAI 兼容 | 企业级，GPT 为主 |
| **Ofox.ai** | ofox.ai | 多模型 | 见官网 | OpenAI 兼容 | 新兴平台，持续扩展 |
| **YAPI** | yapi.uk | Claude + GPT + Gemini + DeepSeek | 人民币（支付宝/微信） | OpenAI + Anthropic 双兼容 | 多模型聚合，支持原生 Claude 格式 |

### 免责声明

> 本列表仅供参考，不构成对任何服务的背书或推荐。在生产环境使用前，请自行评估各平台的适用性。价格、可用性及功能可能随时变更，请以各平台官网为准。

---

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

This list is released under [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) — free to use, share, and adapt.
