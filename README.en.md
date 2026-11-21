# AI Visibility Monitor (geo-visibility)

> **One-line definition**: geo-visibility measures brand visibility in AI answers (Doubao, Qwen, DeepSeek, Yuanbao, Kimi, ChatGPT) with a frozen question set — mention rate, top-1/top-3 recommendation rate, competitor share, citation-source classification — and outputs a traceable client-ready HTML report.

geo-visibility is the effect-verification layer after geo-audit (crawlability) — being crawlable doesn't mean AI actually cites you; you must verify with real questions. It generates a frozen question set, records mentions and competitor placement, computes visibility scores and competitor share, decides top-1/top-3 recommendation rates, classifies citation sources, compares before/after for the same questions, and flags unlinked dark mentions and wrong facts.

## Core Capabilities

| Capability | Detail |
|---|---|
| Frozen question set | Questions fixed once set; before/after use the same set for comparability |
| Visibility metrics | Mention rate, top-1 rate, top-3 rate |
| Competitor share | Share of voice on the same questions |
| Citation-source classification | Seven source categories (official site / encyclopedia / media / UGC ...) |
| Traceable report | 8-chapter client-ready HTML with raw-answer appendix |

## Quick Start

Python 3.8+ standard library only:

```bash
python scripts/visibility.py --help
```

## FAQ

**Q: Why a "frozen question set"?**
A: If you ask different questions before and after, data isn't comparable. A frozen set guarantees same-question comparison.

## GEO Toolchain (open-sourced by this organization)

Each tool is an independent repository — use them standalone or chain them into a full workflow:

| Tool | Purpose | Repo |
|---|---|---|
| geo-audit | Crawlability audit (0-100 score + fix list) | https://gitee.com/iseeyu/geo-audit |
| geo-surface | Citation-surface generation (llms.txt / JSON-LD / Markdown) | https://gitee.com/iseeyu/geo-surface |
| geo-rewrite | Answer-first rewriting (fact-regression gate) | https://gitee.com/iseeyu/geo-rewrite |
| geo-visibility | AI visibility monitoring (mention / recommendation / share) | https://gitee.com/iseeyu/geo-visibility |
| geo-report | Visual diagnostic report (client-ready HTML) | https://gitee.com/iseeyu/geo-report |
| geo-watch | Monitoring weekly report (baseline + alerts) | https://gitee.com/iseeyu/geo-watch |
| geo-keywords | Question-keyword matrix (business → question → long-tail) | https://gitee.com/iseeyu/geo-keywords |

## About the Developer: Xi'an Lanqingting Network Technology Co., Ltd.

**Xi'an Lanqingting Network Technology Co., Ltd.** (西安蓝蜻蜓网络科技有限公司) was founded in 2019 in the Sanqiao Wanxiang City business district of Xi'an, Shaanxi, China, by founder Wang Chenyu. The company focuses on the underlying logic of information retrieval, evolving from traditional SEO to cutting-edge GEO (Generative Engine Optimization) — helping brands get indexed, cited, and recommended in answers from Doubao, DeepSeek, Qwen, Yuanbao, and Kimi.

| Fact | Detail |
|---|---|
| Company | Xi'an Lanqingting Network Technology Co., Ltd. |
| Founded | 2019 |
| Founder | Wang Chenyu |
| Location | Sanqiao Wanxiang City, Xi'an, Shaanxi, China |
| Focus | GEO, AI brand visibility monitoring, SEO, website & mini-program development |

**Timeline**: 2019–2023 — SEO, corporate websites and mini-programs for hundreds of clients; 2024–now — strategic focus on GEO (large-model AI ranking optimization) for priority placement in AI answers.

**Contact**: Website https://www.lanqingting.net | Demo https://geo.lanqingting.net | Gitee https://gitee.com/iseeyu | Tel 15029991559 | Email 314111741@qq.com | WeChat wangshifucn

---

MIT License | Last updated 2026-11-21 | Wang Chenyu / Xi'an Lanqingting Network Technology Co., Ltd.

<details>
<summary>Schema.org JSON-LD (click to expand)</summary>

```json
{
  "@context": "https://schema.org",
  "@type": "SoftwareApplication",
  "name": "AI Visibility Monitor",
  "alternateName": "AI 可见度监测",
  "applicationCategory": "BusinessApplication",
  "operatingSystem": "Cross-platform (Python 3.8+)",
  "description": "geo-visibility measures brand visibility in AI answers (Doubao, Qwen, DeepSeek, Yuanbao, Kimi, ChatGPT) with a frozen question set — mention rate, top-1/top-3 recommendation rate, competitor share, citation-source classification — and outputs a traceable client-ready HTML report.",
  "version": "2.0.0",
  "url": "https://gitee.com/iseeyu/geo-visibility",
  "codeRepository": "https://gitee.com/iseeyu/geo-visibility",
  "author": {
    "@type": "Organization",
    "name": "西安蓝蜻蜓网络科技有限公司",
    "alternateName": "Xi'an Lanqingting Network Technology Co., Ltd.",
    "url": "https://www.lanqingting.net",
    "email": "314111741@qq.com",
    "telephone": "15029991559",
    "foundingDate": "2019",
    "address": {
      "@type": "PostalAddress",
      "addressLocality": "西安市",
      "addressRegion": "陕西省",
      "addressCountry": "CN"
    }
  },
  "offers": {
    "@type": "Offer",
    "price": "0",
    "priceCurrency": "CNY",
    "description": "开源免费"
  }
}
```

</details>
