# 🔎 Search reviews · Best of Open-Source AI

Private search engines and AI answer engines that keep queries on your host. Back to the [leaderboard](../README.md#-search).

<a name="morphic"></a>
### 🥇 [Morphic](https://github.com/miurla/morphic) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: niche (29) · Freshness: active (100) · Maintenance: healthy (96) · Easy to run: easy (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.2k · Apache-2.0 · Oct 2026</sub>

**Search engine that answers with citations and renders rich inline components.**

Morphic runs web searches and returns cited answers, rendering inline components such as images, grids and headings from a streamed JSON spec instead of plain markdown. It offers Quick and Adaptive search modes and works with OpenAI, Anthropic, Google, Ollama, Vercel AI Gateway and OpenAI-compatible models. Docker Compose brings up PostgreSQL, Redis, SearXNG and the app, with chat history stored in PostgreSQL.

- **+** Compose file bundles PostgreSQL, Redis and SearXNG, so no search API key is required
- **+** Supports Tavily, SearXNG, Brave and Exa as search providers
- **+** Model selector detects providers, including local Ollama and OpenAI-compatible endpoints
- **+** Auth is switchable between Supabase, better-auth and none
- **−** Full stack needs four containers: PostgreSQL, Redis, SearXNG and the app
- **−** Supabase is the default auth provider unless ENABLE_AUTH=false or AUTH_PROVIDER is set
- **−** Needs at least one AI provider API key or a local Ollama setup
- **−** README gives no RAM or hardware requirements

<sub>Docker + Compose · Needs PostgreSQL, Redis, SearXNG, Supabase Auth (optional) · Models: OpenAI, Anthropic, Google, Ollama, Vercel AI Gateway · port 3000 · [Repo](https://github.com/miurla/morphic)</sub>

<a name="local-deep-research"></a>
### 🥈 [Local Deep Research](https://github.com/learningcircuit/local-deep-research) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: known (42) · Freshness: active (100) · Maintenance: fair (75) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.2k · MIT · Oct 2026</sub>

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

<sub>GPU optional · Docker + Compose · Needs Ollama or OpenAI-compatible LLM endpoint, SearXNG, SQLCipher (bundled wheels) · Models: Ollama models (e.g. gpt-oss:20b, Qwen3.6-27B), any OpenAI-compatible endpoint · port 5000 · [Repo](https://github.com/learningcircuit/local-deep-research)</sub>

<a name="gpt-researcher"></a>
### 🥉 [GPT Researcher](https://github.com/assafelovic/gpt-researcher) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: healthy (99) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Sep 2026</sub>

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

<a name="vane"></a>
### #&#8288;4 [Vane](https://github.com/itzcrazykns/vane) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: weak (9) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · MIT · Sep 2026</sub>

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

<sub>no GPU · Docker + Compose · Needs SearXNG (bundled in the default image), LLM provider (Ollama, OpenAI-compatible server or cloud API) · Models: Ollama, OpenAI, Anthropic Claude, Google Gemini, Groq · port 3000 · [Repo](https://github.com/itzcrazykns/vane)</sub>

<a name="maestro"></a>
### #&#8288;5 [MAESTRO](https://github.com/murtaza-nasir/maestro) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: niche (1) · Freshness: recent (63) · Maintenance: weak (0) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · AGPL-3.0 · Apr 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
