# Web Search & Extract Providers — the honest comparison

Built for **Web Search Plus** users configuring `web_search_plus` and `web_extract_plus`. WSP is capability-based: configure **one search-capable provider** and search works; extraction is additive. Pick providers by what their **free tier**, **pricing**, and **capabilities** actually are — not by landing-page glitter.

**Verified 2026-06-30** against live provider pricing/billing/docs where possible. Prices and free tiers change often; re-confirm at signup before relying on a provider for production.

## Quick picks

- **Best no-card starter:** Tavily.
- **Best extraction/scrape fallback:** Firecrawl.
- **Best generous one-time starter credit:** You.com.
- **Best cheap Google-style SERP:** Serper or SerpBase.
- **Best semantic discovery:** Exa, but only with the credit caveat.
- **Best no-key experiment:** Keenable public tier, opt-in.
- **Best privacy/self-host path:** SearXNG.

## Free-tier types

- 🟢 **Forever / recurring** — recurring allowance, currently-free API, self-hosted, or keyless public tier.
- 🟡 **One-time / trial** — signup credits you burn once, then pay.
- 🔴 **None** — paid from request one / no durable free API tier found.
- ⚪ **Depends** — gated behind another account or billing system.

---

## 🟢 Forever / recurring

Recurring allowance, self-hosted, or currently free/keyless. Still read the caveats: Brave needs a card; Keenable can change; SearXNG needs an instance.

### Tavily — *search + extract + research*
- **🟢 forever** — 1,000 API credits / month, recurring, no credit card.
- **Pricing:** Pay-as-you-go $0.008 / credit; Project about $30/mo for 4,000 credits; higher plans reduce unit cost.
- **Best for:** Best honest default for WSP users who want search + extract without payment-card friction.
- **Watch out:** Credits are not always equal to calls; deeper research-style features can consume more credits.
- **Key:** `TAVILY_API_KEY` · **Source:** https://docs.tavily.com/documentation/api-credits, https://docs.tavily.com/documentation/keyless

### Firecrawl — *search + extract + JS/crawl*
- **🟢 forever** — 1,000 credits / month, recurring — no cost, no card, no hassle.
- **Pricing:** Hobby $16–19/mo for 5k credits; Standard about $83–99/mo for 100k; Growth about $333–399/mo for 500k. Search costs 2 credits / 10 results; scrape/crawl/map are commonly 1 credit per page/call.
- **Best for:** Best extraction/scraping fallback, especially JS-heavy pages and crawl workflows.
- **Watch out:** Excellent for extraction; less ideal as the main cheap search backend because search burns credits quickly.
- **Key:** `FIRECRAWL_API_KEY` · **Source:** https://www.firecrawl.dev/pricing.md, https://docs.firecrawl.dev/features/scrape

### Brave Search — *search + news + local*
- **🟢 forever / card caveat** — $5 in free credits every month, recurring.
- **Pricing:** Search $5 / 1k requests; Answers $4 / 1k queries plus token charges; autosuggest/spellcheck priced separately.
- **Best for:** Independent broad web index, news/images/videos, privacy-friendly search.
- **Watch out:** Brave docs require a payment card because API usage can generate costs. Treat as recurring free credits, not no-payment onboarding.
- **Key:** `BRAVE_API_KEY` · **Source:** https://api-dashboard.search.brave.com/documentation/pricing, https://brave.com/search/api/

### Querit — *search (multilingual, real-time)*
- **🟢 forever** — 1,000 API requests / calendar month on the Free tier.
- **Pricing:** Pay-as-you-go US$4 / 1,000 API requests; Enterprise custom. Paid activation requires valid payment info.
- **Best for:** Multilingual / real-time search candidate.
- **Watch out:** WSP exposes it as search-only; arbitrary URL extraction is not published/clear.
- **Key:** `QUERIT_API_KEY` · **Source:** https://www.querit.ai/en/subscription, https://www.querit.ai

### SearXNG — *search (meta, self-hosted)*
- **🟢 self-hosted** — Free if you self-host; no vendor API bill.
- **Pricing:** Open-source/self-hosted. Your cost is the server, maintenance and upstream engine reliability.
- **Best for:** Privacy, no vendor lock-in, metasearch across multiple engines.
- **Watch out:** Not a beginner-friendly hosted API key; public instances are fragile and not production-grade.
- **Key:** `SEARXNG_INSTANCE_URL` · **Source:** https://docs.searxng.org/admin/installation.html, https://github.com/searxng/searxng

### Keenable — *search + extract*
- **🟢 currently free / keyless** — Keyless public tier plus optional API key; docs say API usage is currently free.
- **Pricing:** Unauthenticated: 1,000 requests/hour, max 10 rps per IP. Authenticated removes hourly cap but keeps 10 rps/org. No public paid price list yet.
- **Best for:** Zero-setup WSP fallback and independent search/fetch endpoint.
- **Watch out:** “Currently free” can change. Keep public/keyless mode opt-in for privacy and reliability.
- **Key:** `KEENABLE_API_KEY` · **Source:** https://docs.keenable.ai/rate-limits, https://docs.keenable.ai/authentication.md

### Linkup — *search + fetch/extract + citations*
- **🟢 recurring credits / eligible accounts** — Professional-email signups receive $20 credit; eligible accounts are topped back up to $20 each month.
- **Pricing:** Search $0.005–$0.006 / request for standard/fast; deep $0.05–$0.055. Fetch $0.001 without JS, $0.005 with JS. Research $0.25–$2.50 / request.
- **Best for:** Clean cited extraction, sourced answers, low-cost fetch.
- **Watch out:** Eligibility matters: this is not “everyone forever no questions asked”; confirm account eligibility at signup.
- **Key:** `LINKUP_API_KEY` · **Source:** https://docs.linkup.so/pages/documentation/platform/pricing, https://docs.linkup.so/pages/changelog/usd-pricing

---

## 🟡 One-time / trial credits

Good for trying WSP quickly. You burn the credit, then pricing matters.

### You.com — *search + extract + research*
- **🟡 one-time** — $100 free API credit to get started.
- **Pricing:** Search $5 / 1k calls; Contents $1 / 1k pages; Research Lite $12 / 1k calls.
- **Best for:** Generous starter key with search, contents/extract and research-style endpoints.
- **Watch out:** One-time credit, not a permanent monthly free tier.
- **Key:** `YOU_API_KEY` · **Source:** https://you.com/pricing, https://you.com/docs/administration/billing.md

### Parallel — *search + extract + citations*
- **🟡 one-time** — “Run up to 16,000 requests for free.”
- **Pricing:** Search $5 / 1k requests with 10 results; +$1 / 1k additional page results/excerpts. Extract $1 / 1k URLs. Chat $5 / 1k; Task API ranges from $5 to $2,400 / 1k runs.
- **Best for:** Ranked URLs, compressed excerpts, direct page extraction and agent-friendly citations.
- **Watch out:** Free allowance is broad across Parallel APIs. Confirm account eligibility and exact credit accounting at signup.
- **Key:** `PARALLEL_API_KEY` · **Source:** https://www.parallel.ai/pricing, https://docs.parallel.ai/getting-started/pricing.md

### Serper — *search + maps/news/shopping/scholar*
- **🟡 one-time** — 2,500 free credits, no credit card.
- **Pricing:** Volume packs: $1.00 / 1k at 50k credits down to $0.30 / 1k at 12.5M credits; credits valid 6 months.
- **Best for:** Cheap, fast Google-like SERP with rich verticals.
- **Watch out:** Search-only in WSP; pair with an extract provider if you need page contents.
- **Key:** `SERPER_API_KEY` · **Source:** https://serper.dev/

### Exa — *search + extract (semantic)*
- **🟡 credit-based / caveated** — $10 one-time onboarding credit; +$7/month only when a payment method is on file.
- **Pricing:** Search $7 / 1k requests; Contents $1 / 1k pages; Deep Search $12 / 1k; Answer $5 / 1k.
- **Best for:** Neural/semantic discovery, similar pages, AI-optimized contents.
- **Watch out:** Pricing page markets “20,000 requests/month for free”, but billing docs show the real usable model is credits. Treat billing docs as truth.
- **Key:** `EXA_API_KEY` · **Source:** https://exa.ai/pricing, https://exa.ai/docs/reference/billing.md

### SerpBase — *search + images/news/maps*
- **🟡 one-time** — 100 free searches to start, no card; no-key preview capped to 5 organic links.
- **Pricing:** Starter Boost $3 / 10k expires after one month. Standard prepaid packs run about $0.50–$0.30 / 1k and do not expire.
- **Best for:** Very cheap Google-like SERP fallback.
- **Watch out:** Search-only in WSP; explicit/fallback-only rather than a complete search+extract stack.
- **Key:** `SERPBASE_API_KEY` · **Source:** https://serpbase.dev/, https://serpbase.dev/docs

---

## 🔴 No durable free API tier

Useful provider, but not a zero-cost onboarding path.

### Perplexity Sonar API — *search + cited answers*
- **🔴 none** — No durable free API tier found.
- **Pricing:** Search/Sonar request fees roughly $5–$22 / 1k depending context/model, plus token pricing.
- **Best for:** Search-grounded answers with Perplexity synthesis and citations.
- **Watch out:** Not a $0 setup recommendation and not an arbitrary URL extract provider in WSP.
- **Key:** `PERPLEXITY_API_KEY` · **Source:** https://docs.perplexity.ai/docs/getting-started/pricing, https://docs.perplexity.ai/docs/sonar/models/sonar

---

## ⚪ Depends on another account

Not an independent provider free tier; billing happens elsewhere.

### Kilo Code — Perplexity bridge — *search + answers*
- **⚪ depends** — Depends on your Kilo account and billing.
- **Pricing:** Usage is billed through the configured Kilo/provider account; no standalone WSP free tier.
- **Best for:** Convenience if you already use Kilo Code and want Perplexity-style answers through that account.
- **Watch out:** Do not present as a free-tier provider; it inherits another account’s billing rules.
- **Key:** `KILOCODE_API_KEY` · **Source:** https://kilo.ai/docs/ai-providers/kilocode, https://kilo.ai/

---

## Capability & free-tier matrix

| Provider | Search | Extract | Free tier | Headline free | Starting price |
|---|:--:|:--:|---|---|---|
| Tavily | ✅ | ✅ | 🟢 forever | 1,000 API credits / month, recurring, no credit card. | Pay-as-you-go $0.008 / credit |
| Firecrawl | ✅ | ✅ | 🟢 forever | 1,000 credits / month, recurring — no cost, no card, no hassle. | Hobby $16–19/mo for 5k credits |
| Brave Search | ✅ | — | 🟢 forever / card caveat | $5 in free credits every month, recurring. | Search $5 / 1k requests |
| Querit | ✅ | — | 🟢 forever | 1,000 API requests / calendar month on the Free tier. | Pay-as-you-go US$4 / 1,000 API requests |
| SearXNG | ✅ | — | 🟢 self-hosted | Free if you self-host; no vendor API bill. | Open-source/self-hosted. Your cost is the server, maintenance and upstream engine reliability. |
| Keenable | ✅ | ✅ | 🟢 currently free / keyless | Keyless public tier plus optional API key; docs say API usage is currently free. | Unauthenticated: 1,000 requests/hour, max 10 rps per IP. Authenticated removes hourly cap but keeps 10 rps/org. No public paid price list yet. |
| You.com | ✅ | ✅ | 🟡 one-time | $100 free API credit to get started. | Search $5 / 1k calls |
| Parallel | ✅ | ✅ | 🟡 one-time | “Run up to 16,000 requests for free.” | Search $5 / 1k requests with 10 results |
| Serper | ✅ | — | 🟡 one-time | 2,500 free credits, no credit card. | Volume packs: $1.00 / 1k at 50k credits down to $0.30 / 1k at 12.5M credits |
| Exa | ✅ | ✅ | 🟡 credit-based / caveated | $10 one-time onboarding credit; +$7/month only when a payment method is on file. | Search $7 / 1k requests |
| SerpBase | ✅ | — | 🟡 one-time | 100 free searches to start, no card; no-key preview capped to 5 organic links. | Starter Boost $3 / 10k expires after one month. Standard prepaid packs run about $0.50–$0.30 / 1k and do not expire. |
| Linkup | ✅ | ✅ | 🟢 recurring credits / eligible accounts | Professional-email signups receive $20 credit; eligible accounts are topped back up to $20 each month. | Search $0.005–$0.006 / request for standard/fast |
| Perplexity Sonar API | ✅ | — | 🔴 none | No durable free API tier found. | Search/Sonar request fees roughly $5–$22 / 1k depending context/model, plus token pricing. |
| Kilo Code — Perplexity bridge | ✅ | — | ⚪ depends | Depends on your Kilo account and billing. | Usage is billed through the configured Kilo/provider account |

*Compiled for Web Search Plus · 14 search providers / 7 extract providers · verified snapshot 2026-06-30. This is a starting map, not a contract.*
