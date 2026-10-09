# 🔎 Search — reviews

Private search engines and AI answer engines that keep queries on your host. Back to the [leaderboard](../README.md#-search).

<a name="crawl4ai"></a>
### 🥇 82 [Crawl4AI](https://github.com/unclecode/crawl4ai) <sub>⭐ 85k · Apache-2.0 · Oct 2026</sub>

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

<a name="gpt-researcher"></a>
### 🥈 73 [GPT Researcher](https://github.com/assafelovic/gpt-researcher) <sub>⭐ 30k · Apache-2.0 · Sep 2026</sub>

**Research agent that writes cited reports from web and local documents.**

Planner and execution agents generate research questions, scrape 20+ sources, filter passages (Jev by default, BM25 fallback with no key) and write cited reports over 2,000 words, exportable to PDF and Word. Runs as a FastAPI server on port 8000 with a static or Next.js frontend, or as a pip package; local PDF, Office, CSV and Markdown files can be sources. For analysts automating long-form research.

- **+** Deep Research mode: tree-like exploration, about 5 minutes and $0.40 per run on o3-mini
- **+** Hybrid retrievers: Tavily plus MCP servers such as GitHub as research sources
- **+** Works with any OpenAI-compatible endpoint via OPENAI_BASE_URL
- **+** Multi-agent LangGraph and AG2 variants produce 5-6 page PDF, DOCX and Markdown reports
- **−** Default setup needs OpenAI and Tavily API keys
- **−** Jev context filtering needs a TYPESAFE_API_KEY; the fallback is keyword BM25
- **−** Python 3.12 or later required
- **−** Disclaimer labels the project experimental and for academic purposes

<sub>no GPU · Docker + Compose · Needs OpenAI or OpenAI-compatible LLM API, Tavily API key (default retriever), TypeSafe API key (optional Jev filter) · Models: OpenAI models, any OpenAI-compatible endpoint via OPENAI_BASE_URL, Gemini 2.5 Flash Image (inline images) · port 8000 · [Repo](https://github.com/assafelovic/gpt-researcher) · [📖 Docs ↗](https://docs.gptr.dev) · [🌐 Site ↗](https://gptr.dev)</sub>

<a name="morphic"></a>
### 🥈 69 [Morphic](https://github.com/miurla/morphic) <sub>⭐ 9.2k · Apache-2.0 · Oct 2026</sub>

**AI search engine with generative UI and bundled SearXNG.**

Next.js search app that answers with cited sources and renders results as streamed UI components rather than plain markdown. Works with OpenAI, Anthropic, Google, Ollama, Vercel AI Gateway or OpenAI-compatible providers and Tavily, SearXNG, Brave or Exa search. Docker Compose starts PostgreSQL, Redis, SearXNG and Morphic on port 3000, so no search API key is needed.

- **+** Compose stack includes SearXNG, so no paid search key is needed
- **+** Dynamic provider detection; Ollama works for fully local models
- **+** Chat history in PostgreSQL, shareable result URLs, file uploads
- **+** Supabase Auth with guest mode for anonymous use
- **−** Authentication depends on Supabase; no built-in local auth
- **−** Needs PostgreSQL and Redis even for a single user
- **−** At least one AI provider API key or an Ollama endpoint is required
- **−** Feature configuration lives in a separate CONFIGURATION.md, not the README

<sub>no GPU · Docker + Compose · Needs PostgreSQL, Redis, SearXNG (bundled) or Tavily, Brave, Exa API, Supabase (auth) · Models: OpenAI, Anthropic, Google, Ollama, Vercel AI Gateway · port 3000 · [Repo](https://github.com/miurla/morphic)</sub>

<a name="local-deep-research"></a>
### 🥈 67 [Local Deep Research](https://github.com/LearningCircuit/local-deep-research) <sub>⭐ 9.2k · MIT · Oct 2026</sub>

**Agentic research assistant with local LLMs, SearXNG and encrypted libraries.**

Runs multi-step research across the web, academic engines and your own documents using Ollama or any OpenAI-compatible endpoint, with a LangGraph agent that picks engines adaptively and writes cited reports. Each user gets an AES-256 SQLCipher database, and egress scopes limit which engines and providers a run may use. Web UI on port 5000 via Docker, Compose or pip, for privacy-focused researchers.

- **+** Reports about 95% SimpleQA fully local on one RTX 3090 with Qwen3.6-27B
- **+** Per-user SQLCipher databases; keys derived from the password, never stored
- **+** No telemetry; Docker images signed with Cosign, with SLSA provenance and SBOMs
- **+** Downloaded sources build a searchable, embedded personal library
- **−** Needs Ollama (or an LLM endpoint) and SearXNG running separately
- **−** Private or localhost engine URLs are blocked unless an operator env var allows them
- **−** Requires an AVX-capable x86-64 CPU; older CPUs crash with Illegal instruction
- **−** docker run --network host only works on native Linux; Docker Desktop needs Compose

<sub>GPU optional · Docker + Compose · Needs Ollama or OpenAI-compatible LLM endpoint, SearXNG, SQLCipher (bundled wheels) · Models: Ollama models (e.g. gpt-oss:20b, Qwen3.6-27B), any OpenAI-compatible endpoint · port 5000 · [Repo](https://github.com/LearningCircuit/local-deep-research)</sub>

<a name="firecrawl"></a>
### 🥈 66 [Firecrawl](https://github.com/firecrawl/firecrawl) <sub>⭐ 190k · AGPL-3.0 · Oct 2026</sub>

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

<a name="vane"></a>
### 🥉 57 [Vane](https://github.com/ItzCrazyKns/Vane) <sub>⭐ 37k · MIT · Sep 2026</sub>

**Self-hosted answer engine with cited sources over SearXNG.**

Next.js answer engine (formerly Perplexica) that runs searches through a bundled SearXNG instance, then answers with citations using Ollama, OpenAI-compatible servers, OpenAI, Anthropic, Gemini or Groq models. Offers Speed, Balanced and Quality modes, web, discussion and academic sources, image and video search, file uploads and a search API. One container on port 3000; a slim image uses your own SearXNG.

- **+** Single Docker image bundles SearXNG; no search API key needed
- **+** Local models via Ollama or any OpenAI-compatible server, plus cloud providers
- **+** Browser search-engine shortcut via /?q=%s and a REST search API
- **+** Slim image works with an existing SearXNG (JSON format and Wolfram Alpha enabled)
- **−** No authentication yet; listed as an upcoming feature
- **−** Own-SearXNG setups must enable JSON output and Wolfram Alpha or searches fail
- **−** Tavily and Exa search backends are marked coming soon
- **−** Ollama on Linux must listen on 0.0.0.0 for the container to reach it

<sub>no GPU · Docker + Compose · Needs SearXNG (bundled in the default image), LLM provider (Ollama, OpenAI-compatible server or cloud API) · Models: Ollama, OpenAI, Anthropic Claude, Google Gemini, Groq · port 3000 · [Repo](https://github.com/ItzCrazyKns/Vane)</sub>

<a name="jina-reader"></a>
### 52 [Jina Reader](https://github.com/jina-ai/reader) <sub>⭐ 12k · Apache-2.0 · May 2026</sub>

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

<a name="maestro"></a>
### 25 [MAESTRO](https://github.com/murtaza-nasir/maestro) <sub>⭐ 1.5k · AGPL-3.0 · Apr 2026</sub>

**Multi-agent research platform that writes long reports from documents and web.**

Planning, Research, Reflection and Writing agents run research missions over uploaded PDF, Word and Markdown documents and web search, producing long reports with visible agent steps. Retrieval uses BGE-M3 embeddings in PostgreSQL with pgvector; any OpenAI-compatible API, including Azure OpenAI, can serve the models. Docker Compose stack on http://localhost with CPU and NVIDIA variants.

- **+** Mission checkpoints allow pause, resume and writing-phase recovery
- **+** Local embeddings (BGE-M3) and pgvector; local LLMs via OpenAI-compatible API
- **+** Search providers: Tavily, LinkUp, Jina and SearXNG
- **+** CPU-only compose file plus automatic NVIDIA GPU detection
- **−** 16 GB RAM minimum (32 GB recommended) and 30 GB disk
- **−** Alpha (v0.1.10-alpha); last commit April 2026
- **−** Dual-licensed AGPLv3 or commercial; proprietary use needs a paid license
- **−** First startup takes 5 to 10 minutes while models download

<sub>RAM ≥ 16 GB · GPU optional · Compose · Needs Docker Compose v2+, API key for an AI provider or an OpenAI-compatible endpoint, PostgreSQL with pgvector (in compose) · Models: OpenAI-compatible APIs, Azure OpenAI (GPT-5), BGE-M3 embeddings · port 80 · [Repo](https://github.com/murtaza-nasir/maestro) · [📖 Docs ↗](https://murtaza-nasir.github.io/maestro/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-selfhosted-ai/issues/new/choose).</sub>
