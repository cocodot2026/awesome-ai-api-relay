# Awesome AI API Relay [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of AI API relay and aggregation services for developers.
>
> 精选 AI API 中转 / 聚合服务列表，面向开发者社区。

![Last Updated](https://img.shields.io/badge/updated-2026--07-blue) ![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen) ![License CC0](https://img.shields.io/badge/license-CC0-lightgrey)

**[English](#english) · [中文说明](#中文说明) · [FAQ](#faq) · [How to Choose](#how-to-choose-a-relay-service)**

---

## English

### What is an AI API Relay?

AI API relay services act as intermediaries between your application and upstream AI providers (OpenAI, Anthropic, Google, DeepSeek, etc.). They typically offer:

- **Unified API interface** — one endpoint for multiple AI models
- **Alternative payment methods** — Alipay / WeChat Pay / CNY credit, useful outside the US/EU
- **Load balancing & failover** — improved reliability across upstream providers
- **Usage management** — centralized billing, quota tracking, and audit logs

They are commonly used by developers in regions where direct access to official AI APIs is restricted by network, payment, or account-verification barriers.

### Inclusion Criteria

To be listed here, a service should:

- ✅ Provide a working API endpoint compatible with at least one major AI provider's format
- ✅ Support at least one production-grade model (GPT-4/5 series, Claude, Gemini, DeepSeek, etc.)
- ✅ Have a publicly accessible website and documentation
- ✅ Offer a clear pricing or credit system
- ✅ Be actively maintained (last observed update within 6 months)

Services are listed **alphabetically**. Listing does **not** imply endorsement. Always evaluate a service independently before production use.

---

## Platforms

### AiHubMix

| Field | Details |
|-------|---------|
| **Website** | [aihubmix.com](https://aihubmix.com) |
| **Models** | Multi-model aggregation (Claude, GPT, Gemini, and others) |
| **Payment** | CNY / credit-based |
| **API Compatibility** | OpenAI-compatible |
| **Notable Features** | Well-known aggregation platform; broad model coverage |

---

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

### DMXAPI

| Field | Details |
|-------|---------|
| **Website** | [dmxapi.cn](https://dmxapi.cn) |
| **Models** | Multi-model aggregation |
| **Payment** | CNY / credit-based |
| **API Compatibility** | OpenAI-compatible |
| **Notable Features** | Multi-provider aggregation; commonly referenced in Chinese developer communities |

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

### OpenRouter

| Field | Details |
|-------|---------|
| **Website** | [openrouter.ai](https://openrouter.ai) |
| **Models** | Very broad multi-provider catalog (hundreds of models) |
| **Payment** | Credit-based (international cards, crypto) |
| **API Compatibility** | OpenAI-compatible (`/v1/chat/completions`) |
| **Notable Features** | International aggregator; unified access to many providers; transparent per-model pricing |

---

### SiliconFlow

| Field | Details |
|-------|---------|
| **Website** | [siliconflow.cn](https://siliconflow.cn) |
| **Models** | Open-source and multimodal models (DeepSeek, Qwen, and others) |
| **Payment** | CNY / credit-based |
| **API Compatibility** | OpenAI-compatible |
| **Notable Features** | Strong focus on open-source model hosting; company-operated |

---

### YAPI

| Field | Details |
|-------|---------|
| **Website** | [yapi.uk](https://yapi.uk) |
| **Models** | Claude (Opus / Sonnet / Haiku), GPT-4 / GPT-4o / GPT-5 series, Gemini Pro / Flash, DeepSeek V3 / R1, and more |
| **Payment** | CNY (Alipay / WeChat Pay); credit-based system |
| **API Compatibility** | OpenAI-compatible (`/v1/chat/completions`) + Anthropic-compatible (`/v1/messages`) |
| **Notable Features** | Multi-model aggregation across major providers; supports both OpenAI and Anthropic native API formats in one endpoint; itemized billing; suitable for developers who need to switch between Claude and GPT in the same project |

**Supported model families:**

- `claude-opus-4`, `claude-sonnet-4`, `claude-haiku-4` (Anthropic)
- `gpt-4o`, `gpt-4-turbo`, `gpt-4.1` / `gpt-5` series (OpenAI)
- `gemini-1.5-pro`, `gemini-1.5-flash` (Google)
- `deepseek-chat`, `deepseek-reasoner` (DeepSeek)

---

## How to Choose a Relay Service

Picking a relay is mostly about risk management. Six practical criteria:

1. **Stability & uptime** — a relay that frequently goes down costs you more time than it saves. Prefer services with a track record and a support channel.
2. **Latency** — slow response times make interactive use painful. Test round-trip latency from your own network before committing.
3. **Model coverage** — a good relay gives one-stop access to top models and adds new official models quickly.
4. **Billing transparency** — watch for hidden token-counting tricks or inflated rates. Clear, itemized billing lets you audit anomalies later.
5. **Provider trust** — every relay carries shutdown risk. Prefer company-operated services; top up small amounts, use as you go.
6. **Model authenticity** — suspiciously cheap "flagship" models are sometimes silently swapped for cheaper ones. Verify with your own prompts.

> **Rule of thumb:** the industry is volatile. Never prepay large amounts — top up what you need, when you need it.

---

## FAQ

**Q: What is an AI API relay / proxy service?**
A: It is an intermediary endpoint that forwards your requests to upstream AI providers (OpenAI, Anthropic, Google, DeepSeek). It gives you a single unified API, local payment options, and centralized billing without needing a foreign card or unrestricted network access.

**Q: Are relay services legal / safe to use?**
A: Using a relay is a common practice, but each carries operational risk (downtime, billing disputes, provider ToS considerations). Evaluate reliability, security, and compliance yourself before production use. This list does not endorse any service.

**Q: How do I call a relay from Python or Node.js?**
A: Most relays are OpenAI-compatible — point the official OpenAI SDK's `base_url` at the relay endpoint and use your relay API key. Anthropic-compatible relays additionally expose `/v1/messages` for native Claude calls. See the [Code Examples](#code-examples) below.

**Q: Which relays support native Anthropic (Claude) format?**
A: Some relays expose only the OpenAI-compatible `/v1/chat/completions` route, while others also provide Anthropic's native `/v1/messages`. If you use the Anthropic SDK directly, choose a relay that lists Anthropic compatibility (e.g. YAPI).

**Q: How do I avoid getting scammed by a cheap relay?**
A: Top up small amounts first, run your own benchmark prompts to verify model authenticity and latency, and prefer services with itemized billing you can audit. See [How to Choose](#how-to-choose-a-relay-service).

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
2. Add your entry to the platforms section (alphabetical order)
3. Fill in all required fields: website, models, payment, API compatibility, notable features
4. Ensure the service meets the [inclusion criteria](#inclusion-criteria)
5. Open a pull request with a brief description

**Please do not:**
- Include referral/affiliate links
- Make price comparisons (prices change frequently)
- Disparage other listed services

---

## Disclaimer

> This list is for informational purposes only and does not constitute an endorsement or recommendation of any service. Always evaluate services independently before use in production. Pricing, availability, and features may change without notice. Using any third-party API relay carries risk, including data exposure, service interruption, and provider ToS considerations — you assume that risk.

---

---

## 中文说明

### 什么是 AI API 中转服务？

AI API 中转服务作为你的应用与上游 AI 提供商（OpenAI、Anthropic、Google、DeepSeek 等）之间的中间层，通常提供：

- **统一 API 接口** — 一个端点访问多种 AI 模型
- **本地化支付方式** — 支持支付宝、微信支付、人民币额度
- **负载均衡与故障转移** — 提升跨上游的稳定性
- **用量管理** — 集中计费、配额追踪、调用记录

常见使用场景：受网络、支付或账号验证门槛限制、难以直接访问官方 AI API 的开发者。

### 收录标准

收录的服务需满足：

- ✅ 提供兼容主流 AI 提供商格式的 API 端点
- ✅ 支持至少一个生产级模型（GPT-4/5、Claude、Gemini、DeepSeek 等）
- ✅ 有公开可访问的网站和文档
- ✅ 有明确的定价或积分体系
- ✅ 持续维护中（6 个月内有观察到更新）

平台按**字母顺序**排列，收录**不代表推荐**。生产使用前请自行评估。

### 平台简介

| 平台 | 网址 | 支持模型 | 支付方式 | API 兼容性 | 特点 |
|------|------|---------|---------|-----------|------|
| **AiHubMix** | aihubmix.com | 多模型聚合 | 人民币 / 额度 | OpenAI 兼容 | 知名聚合平台，模型覆盖广 |
| **API2D** | api2d.com | GPT 系列 | 人民币（支付宝/微信） | OpenAI 兼容 | 老牌中转，稳定可靠 |
| **CloseAI** | closeai-asia.com | GPT 系列 | 人民币（支付宝/微信） | OpenAI 兼容 | 企业级，GPT 为主 |
| **DMXAPI** | dmxapi.cn | 多模型聚合 | 人民币 / 额度 | OpenAI 兼容 | 多上游聚合，社区常见 |
| **Ofox.ai** | ofox.ai | 多模型 | 见官网 | OpenAI 兼容 | 新兴平台，持续扩展 |
| **OpenRouter** | openrouter.ai | 数百款模型 | 额度（国际卡/加密货币） | OpenAI 兼容 | 国际聚合器，按模型透明计价 |
| **SiliconFlow 硅基流动** | siliconflow.cn | 开源 / 多模态模型 | 人民币 / 额度 | OpenAI 兼容 | 专注开源模型托管，公司运营 |
| **YAPI** | yapi.uk | Claude + GPT + Gemini + DeepSeek | 人民币（支付宝/微信） | OpenAI + Anthropic 双兼容 | 多模型聚合，同端点支持原生 Claude 格式，账单可追溯 |

### 如何挑选中转服务（6 个硬指标）

1. **稳定性** — 经常宕机的站反而耽误事，优先选有口碑、有支持渠道的。
2. **速度** — 返回过慢的接口用起来很难受，先从自己的网络测延迟。
3. **模型覆盖** — 好的站能一站式调用顶尖模型，并尽快上官方新模型。
4. **账单透明** — 警惕隐形的 token 计数或费率把戏，清晰账单才能事后核查异常。
5. **运营方可信度** — 每个站都有跑路风险，优先公司运营，少充勤充。
6. **模型真实性** — 异常便宜的"旗舰"模型可能被悄悄换成廉价模型，用自己的 prompt 验证。

> **经验法则：** 行业不稳定，切勿大额充值——用多少充多少。

### 免责声明

> 本列表仅供参考，不构成对任何服务的背书或推荐。在生产环境使用前，请自行评估各平台的适用性、安全性与合规性。价格、可用性及功能可能随时变更，请以各平台官网为准。使用任何第三方 API 中转服务均存在风险（数据泄露、服务中断、厂商 ToS 等），使用者需自行承担。

---

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

This list is released under [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) — free to use, share, and adapt.
