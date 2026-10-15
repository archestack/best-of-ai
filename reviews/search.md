# 🔎 Search reviews · Best of Open-Source AI

Private search engines and AI answer engines that keep queries on your host. Back to the [leaderboard](../README.md#-search).

<sub>🌐 Also on the web: [Search on archestack.com](https://archestack.com/best-of-ai/search/), each project on its own page.</sub>

<a name="morphic"></a>
### 🥇 [Morphic](https://github.com/miurla/morphic) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: healthy (97) · Easy to run: very easy (83) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.2k · Apache-2.0 · Oct 2026</sub>

**AI answer engine with cited search results and generative UI components.**

Morphic is a Next.js (TypeScript) AI search app that answers queries with cited sources and renders results as inline components streamed from a JSON spec. It supports OpenAI, Anthropic, Google, Ollama, Vercel AI Gateway and OpenAI-compatible models, with Tavily, SearXNG, Brave or Exa for search. Chat history lives in PostgreSQL, and Docker Compose bundles Postgres, Redis and SearXNG.

- **+** Docker Compose bundles SearXNG, so no search API key is required
- **+** Many model providers, including local Ollama and OpenAI-compatible endpoints
- **+** Four search backends: Tavily, SearXNG, Brave, Exa
- **+** Built-in accounts via Better Auth or Supabase Auth, plus guest mode and shareable result URLs
- **−** Compose stack needs PostgreSQL, Redis and SearXNG alongside the app
- **−** Needs at least one model provider API key or a local Ollama setup
- **−** Local development requires Bun; RAM and GPU requirements are not stated
- **−** Chat history, auth and file upload need extra configuration beyond the quick start

<sub>no GPU · Docker + Compose · Needs PostgreSQL, Redis, SearXNG, Tavily, Brave, Exa, Supabase · Models: OpenAI, Anthropic, Google, Ollama, Vercel AI Gateway · port 3000 · [Repo](https://github.com/miurla/morphic) · [📖 Docs ↗](https://github.com/miurla/morphic/blob/main/docs/CONFIGURATION.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/morphic/)</sub>

<a name="gpt-researcher"></a>
### 🥈 [GPT Researcher](https://github.com/assafelovic/gpt-researcher) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: healthy (97) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Oct 2026</sub>

**Research agent that writes cited reports from web and local documents.**

GPT Researcher splits a query into research questions with a planner agent, scrapes sources in parallel, filters the context and writes a cited report. It works over web search (Tavily by default) and local files such as PDF, CSV, Excel, Markdown, PowerPoint and Word. It runs as a FastAPI server with a static or NextJS frontend, or as the gpt-researcher pip package.

- **+** Covers both web research and local documents (PDF, CSV, Excel, Markdown, PowerPoint, Word)
- **+** Usable as a pip package, a FastAPI server with two frontends, or via Docker Compose
- **+** Supports MCP data sources, recursive deep research, and LangGraph or AG2 multi-agent workflows
- **+** Context filter falls back to local BM25 keyword ranking when no TypeSafe key is set
- **−** Needs an LLM API key and a search API key (OpenAI and Tavily in the README examples)
- **−** Default Jev context filter requires a TypeSafe API key and a hosted call
- **−** Deep research is quoted at about 5 minutes and $0.4 per run with o3-mini
- **−** README calls it experimental and provided as-is, with no warranty

<sub>no GPU · Docker + Compose · Needs OpenAI API key, Tavily API key, Python 3.12+, TypeSafe API key (optional, Jev filter), Google API key (optional, image generation) · Models: OpenAI, OpenAI-compatible APIs via OPENAI_BASE_URL, Google Gemini (inline images) · port 8000 · [Repo](https://github.com/assafelovic/gpt-researcher) · [📖 Docs ↗](https://docs.gptr.dev) · [🌐 Site ↗](https://gptr.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gpt-researcher/)</sub>

<a name="local-deep-research"></a>
### 🥉 [Local Deep Research](https://github.com/learningcircuit/local-deep-research) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: known (31) · Freshness: active (100) · Maintenance: fair (76) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.2k · MIT · Oct 2026</sub>

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

<sub>GPU optional · Docker + Compose · Needs Ollama or OpenAI-compatible LLM endpoint, SearXNG, SQLCipher (bundled wheels) · Models: Ollama models (e.g. gpt-oss:20b, Qwen3.6-27B), any OpenAI-compatible endpoint · port 5000 · [Repo](https://github.com/learningcircuit/local-deep-research) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/local-deep-research/)</sub>

<a name="vane"></a>
### #&#8288;4 [Vane](https://github.com/itzcrazykns/vane) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: widely used (86) · Freshness: active (99) · Maintenance: weak (10) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · MIT · Sep 2026</sub>

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

<sub>no GPU · Docker + Compose · Needs SearXNG (bundled in the default image), LLM provider (Ollama, OpenAI-compatible server or cloud API) · Models: Ollama, OpenAI, Anthropic Claude, Google Gemini, Groq · port 3000 · [Repo](https://github.com/itzcrazykns/vane) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vane/)</sub>

<a name="maestro"></a>
### #&#8288;5 [MAESTRO](https://github.com/murtaza-nasir/maestro) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: niche (0) · Freshness: recent (61) · Maintenance: weak (0) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · AGPL-3.0 · Apr 2026</sub>

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

<sub>RAM ≥ 16 GB · GPU optional · Compose · Needs Docker Compose v2+, API key for an AI provider or an OpenAI-compatible endpoint, PostgreSQL with pgvector (in compose) · Models: OpenAI-compatible APIs, Azure OpenAI (GPT-5), BGE-M3 embeddings · port 80 · [Repo](https://github.com/murtaza-nasir/maestro) · [📖 Docs ↗](https://murtaza-nasir.github.io/maestro/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/maestro/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
