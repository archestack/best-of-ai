# 🕸️ Data and scraping for AI reviews · Best of Open-Source AI

Tools that turn web pages, PDFs and documents into clean text or structured data that models can use. Back to the [leaderboard](../README.md#%EF%B8%8F-data-and-scraping-for-ai).

<sub>🌐 Also on the web: [Data and scraping for AI on archestack.github.io](https://archestack.github.io/best-of-ai/data-tools/), each project on its own page.</sub>

<a name="crawl4ai"></a>
### 🥇 [Crawl4AI](https://github.com/unclecode/crawl4ai) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: healthy (82) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 85k · Apache-2.0 · Oct 2026</sub>

**Python crawler that turns pages into LLM-ready markdown, with a Docker API.**

Async Playwright crawler (pip install crawl4ai) that renders pages in Chromium, Firefox or WebKit and emits clean or filtered markdown, with CSS, XPath and regex extraction needing no LLM, or LLM extraction via any LiteLLM provider. Deep crawling (BFS, DFS, priority-scored) and adaptive crawling are built in. A Docker server on port 11235 exposes /md, /html, /crawl, /screenshot, /pdf and MCP behind an API token.

- **+** Structured extraction with CSS, XPath or regex schemas needs no LLM or API key
- **+** Docker server with REST, streaming crawl, MCP, dashboard and playground; amd64 and arm64
- **+** Deep crawl strategies with crash recovery via resume_state
- **+** Persistent browser profiles, CDP remote browsers and an undetected-browser adapter
- **−** Apache-2.0 but requires attribution (badge or text) in your project
- **−** Docker server answers only inside the container until CRAWL4AI_API_TOKEN is set
- **−** Web search and answer endpoints exist only in the paid cloud
- **−** Runs full browsers; the docker run example allocates 1 GB shared memory

<sub>no GPU · Docker + Compose · Needs Playwright Chromium (installed by crawl4ai-setup) · Models: any LiteLLM provider for LLM extraction (OpenAI, Ollama and others) · port 11235 · [Repo](https://github.com/unclecode/crawl4ai) · [📖 Docs ↗](https://docs.crawl4ai.com/)</sub>

<a name="firecrawl"></a>
### 🥈 [Firecrawl](https://github.com/firecrawl/firecrawl) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: patchy (45) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 190k · AGPL-3.0 · Oct 2026</sub>

**Web scraping and crawling API that returns LLM-ready markdown.**

API that turns URLs into markdown, HTML, screenshots or schema-based JSON, with endpoints for search, scrape, crawl, map, batch scrape, page interaction and a prompt-driven agent. Handles JS-rendered pages and parses hosted PDFs and DOCX. SDKs for Python, Node, Go, Java, Elixir, Rust and Ruby plus an MCP server and CLI, for teams feeding web content to RAG pipelines and agents.

- **+** Seven SDKs plus CLI and MCP server; SDKs poll async crawl jobs automatically
- **+** Crawl, map and batch-scrape endpoints return job IDs for large sites
- **+** Scrape supports actions (click, scroll, write, wait) before extraction
- **+** Compose file at the repo root for self-hosting
- **−** README is written around the hosted API and keys; self-hosting lives in separate docs
- **−** AGPL-3.0 license; network use of a modified version triggers source obligations
- **−** Agent endpoint runs the hosted spark-2 model, not a local LLM
- **−** Proxy rotation and anti-bot handling are hosted-service features

<sub>no GPU · Compose · [Repo](https://github.com/firecrawl/firecrawl) · [▶️ Demo ↗](https://firecrawl.dev/playground) · [📖 Docs ↗](https://docs.firecrawl.dev) · [🌐 Site ↗](https://firecrawl.dev)</sub>

<a name="jina-reader"></a>
### 🥉 [Jina Reader](https://github.com/jina-ai/reader) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: niche (20) · Freshness: active (81) · Maintenance: weak (15) · Easy to run: easy (50) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · May 2026</sub>

**Converts any URL or search query into LLM-friendly markdown.**

Open-source branch of the service behind r.jina.ai and s.jina.ai: fetches a page with headless Chrome or curl-impersonate, parses PDFs and Office files, and returns markdown, text, HTML, screenshots or JSON controlled by request headers (engine, timeout, token limits). The ghcr.io image bundles Chrome, LibreOffice and CJK fonts, serves HTTP/1.1 on 8081 and h2c on 8080, and runs stateless or with S3-compatible caching.

- **+** Prebuilt image with Chrome, LibreOffice and CJK fonts; stateless by default
- **+** Fine-grained headers: x-respond-timing, x-max-tokens, x-token-budget, x-target-selector
- **+** Optional VLM captions for images without alt text
- **+** Semantic markdown chunking by heading or block level
- **−** Hosted proxy pool, rate limiting and MongoDB storage layer are not in the OSS branch
- **−** Needs non-redistributable assets (MaxMind GeoLite2, Source Han Sans) fetched at build
- **−** Last commit May 2026; the SaaS resync was April 2026
- **−** Default h2c port 8080 needs --http2-prior-knowledge from curl; use 8081 otherwise

<sub>no GPU · Docker + Compose · Needs Headless Chrome and LibreOffice (bundled in image), S3-compatible bucket (optional cache), VLM endpoint for image captions (optional) · port 8081 · [Repo](https://github.com/jina-ai/reader) · [▶️ Demo ↗](https://jina.ai/reader#demo) · [📖 Docs ↗](https://r.jina.ai/docs) · [🌐 Site ↗](https://jina.ai/reader)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
