# 📚 RAG, knowledge and search reviews · Best of Open-Source AI

Document Q&A, knowledge bases and private search over your own files and the web, with queries kept on your host. Back to the [leaderboard](../README.md#-rag-knowledge-and-search).

<sub>🌐 Also on the web: [RAG, knowledge and search on archestack.com](https://archestack.com/best-of-ai/rag-knowledge/), each project on its own page.</sub>

<a name="ragflow"></a>
### 🥇 [RAGFlow](https://github.com/infiniflow/ragflow) <sub>score [90](../README.md#-how-we-rank "Score 90/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 93k · Apache-2.0 · Oct 2026</sub>

**RAG engine with deep document parsing, template chunking and agentic retrieval.**

RAGFlow parses complex documents (PDF, Word, Excel, PowerPoint, scans, web pages) with its DeepDoc layout, OCR and table recognition, then chunks them by template and answers with traceable citations. It adds multi-step agentic retrieval with four thinking modes, plus knowledge compilation into wikis, graphs and mind maps. Services are written in Go and deployed with Docker Compose, with a web UI and HTTP API.

- **+** Template-based chunking with a visual view of chunks so humans can correct them
- **+** Answers include traceable citations back to source chunks
- **+** Ingests many formats, plus sitemap crawling and Google BigQuery sync
- **+** Configurable LLM, embedding and reranker models; multiple recall with fused re-ranking
- **−** Heavy stack: MySQL, MinIO, NATS, Kvrocks and a document engine; 16 GB RAM suggested
- **−** macOS is not supported for the Docker deployment
- **−** DeepDoc runs on CPU inference in the 1.0 release, which may slow parsing
- **−** Current release is 1.0.0-rc1, a release candidate rather than a stable 1.0

<sub>RAM ≥ 16 GB · no GPU · Docker + Compose · Needs Docker, Docker Compose, MySQL, Elasticsearch or Infinity, MinIO, NATS, Kvrocks · Models: Configurable LLM, embedding and reranker models via provider page · port 80 · [Repo](https://github.com/infiniflow/ragflow) · [▶️ Demo ↗](https://cloud.ragflow.io) · [📖 Docs ↗](https://ragflow.io/docs/dev/) · [🌐 Site ↗](https://ragflow.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ragflow/)</sub>

<a name="lightrag"></a>
### 🥈 [LightRAG](https://github.com/hkuds/lightrag) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · MIT · Oct 2026</sub>

**Graph-based RAG framework with a REST API server and web UI.**

LightRAG indexes documents into a knowledge graph plus vector embeddings and answers queries with dual-level (entity and concept) retrieval. It ships as a Python library and as lightrag-server, which provides a REST API and a web UI for inserting, querying and visualizing the graph. It supports incremental updates, document deletion with graph rebuild, reranking, and several parsing and chunking options.

- **+** Document deletion rebuilds affected graph entries from the LLM cache; inserts are incremental
- **+** Storage backends include PostgreSQL, Neo4j, MongoDB and OpenSearch, plus local file stores
- **+** Parsers: MinerU, Docling and a native engine; four chunking strategies
- **+** Setup wizard generates .env and compose files; RAGAS evaluation and Langfuse tracing supported
- **−** Default in-memory/file stores are stated as not for production
- **−** Server binds to 0.0.0.0 and endpoints are public until auth is set in .env
- **−** Graph extraction needs LLM calls at index time; RAM and GPU needs are unstated
- **−** Optional features need extra steps: spaCy models for smart_heading, libcairo for SVG

<sub>Docker + Compose · Needs LLM provider, embedding model, PostgreSQL (recommended for production), Neo4j (optional), MongoDB (optional), OpenSearch (optional), MinerU or Docling (optional) · Models: LLMs configured via .env, open-source LLMs such as Qwen3-30B-A3B, rerankers · [Repo](https://github.com/hkuds/lightrag) · [📖 Docs ↗](https://github.com/HKUDS/LightRAG/blob/main/docs/LightRAG-API-Server.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lightrag/)</sub>

<a name="deeptutor"></a>
### 🥉 [deeptutor](https://github.com/hkuds/deeptutor) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 47k · Apache-2.0 · Oct 2026</sub>

**Self-hosted AI tutor with knowledge bases, guided learning, books and quizzes.**

DeepTutor is a Python backend with a Next.js 16 web UI for studying from your own documents. It combines chat over knowledge bases (LightRAG, PageIndex, GraphRAG, LlamaIndex, FAISS) with guided learning, generated books, quizzes, question banks and deep research. It also offers multi-user accounts, IM-connected Partners, MCP services and a CLI.

- **+** Several retrieval engines selectable per knowledge base: LightRAG, PageIndex, GraphRAG, LlamaIndex
- **+** Covers study workflows: guided learning, mastery gates, quizzes, question bank, daily practice
- **+** Multi-user deployment with per-user isolation, admin grants and learner/guardian accounts
- **+** Wide provider and parser coverage, including Codex OAuth, MinerU, Tika and PyMuPDF4LLM
- **−** Fast release cadence with breaking refactors (v1.6.3) makes upgrades risky
- **−** Large surface area: Partners, MCP, CLI apps and plugins add configuration overhead
- **−** RAM, GPU and port requirements are not stated in the visible README
- **−** Aimed at learning and study; less suited to general chat or enterprise search

<sub>Docker + Compose · Needs Python 3.11+, Node.js (Next.js 16), Docker (optional) · Models: OpenAI-compatible providers, Anthropic, Gemini, OpenAI Codex OAuth, Lemonade (local) · [Repo](https://github.com/hkuds/deeptutor) · [📖 Docs ↗](https://deeptutor.info) · [🌐 Site ↗](https://deeptutor.info) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deeptutor/)</sub>

<a name="maxkb"></a>
### #&#8288;4 [MaxKB](https://github.com/1panel-dev/maxkb) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · GPL-3.0 · Oct 2026</sub>

**Enterprise knowledge-base agent platform with RAG, workflows and MCP tools.**

MaxKB runs as one Docker container (port 8080, state in one volume) with a RAG pipeline that uploads or crawls documents, a workflow engine with function library and MCP tool use, and zero-code embedding into other systems. It works with private models (DeepSeek, Llama, Qwen) and public APIs (OpenAI, Claude, Gemini, MiniMax) and handles text, image, audio and video. Built on Django, LangChain and PostgreSQL.

- **+** Single docker run with all data under one mounted volume
- **+** Workflow engine with function library and MCP tool calling
- **+** Crawls online documents into the knowledge base automatically
- **+** Multimodal input and output: text, image, audio, video
- **−** GPL-3.0 limits bundling into proprietary products
- **−** Ships with default admin password MaxKB@123..
- **−** README gives no hardware guidance or provider configuration detail
- **−** Detailed docs are on maxkb.cn, partly in Chinese

<sub>no GPU · Models: OpenAI, Claude, Gemini, MiniMax, DeepSeek, Llama, Qwen as private models · port 8080 · [Repo](https://github.com/1panel-dev/maxkb) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/maxkb/)</sub>

<a name="open-notebook"></a>
### #&#8288;5 [Open Notebook](https://github.com/lfnovo/open-notebook) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · MIT · Oct 2026</sub>

**Self-hosted NotebookLM alternative with podcasts and 20+ model providers.**

Open Notebook collects PDFs, audio, video, web pages and Office files into notebooks and offers cited chat, full-text and vector search, notes and multi-speaker podcast generation. It runs as two containers (SurrealDB plus a FastAPI/Next.js app) and talks to OpenAI, Anthropic, Google, Mistral, Groq, Ollama, LM Studio or any OpenAI-compatible server. A REST API and MCP integration expose the same features.

- **+** 20+ providers, including Ollama and LM Studio for fully local runs
- **+** Podcasts with 1 to 4 speakers and custom episode profiles
- **+** REST API on port 5055 and an MCP server for Claude Desktop or VS Code
- **+** Two-service Docker Compose; keys stored encrypted with OPEN_NOTEBOOK_ENCRYPTION_KEY
- **−** Single-user; multi-user support is only a future direction in VISION.md
- **−** No password by default and ports 8502/5055 bind to all interfaces
- **−** Anthropic and Groq offer no embeddings, so a second provider is needed
- **−** UI in 14 languages but provider setup is manual per model type

<sub>no GPU · Docker + Compose · Needs SurrealDB · Models: OpenAI, Anthropic, Google, Mistral, Groq, DeepSeek, xAI, OpenRouter, Cohere, Ollama, LM Studio, oMLX and any OpenAI-compatible endpoint · port 8502 · README: alternative to NotebookLM · [Repo](https://github.com/lfnovo/open-notebook) · [🌐 Site ↗](https://www.open-notebook.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-notebook/)</sub>

<a name="pageindex"></a>
### #&#8288;6 [pageindex](https://github.com/vectifyai/pageindex) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · MIT · Oct 2026</sub>

**Vectorless RAG that builds a tree index of a document and searches it with an LLM.**

PageIndex builds a hierarchical tree index from each long PDF and has an LLM reason its way through that tree to answer questions, with no vector database and no chunking. The Python SDK runs in local mode with your own LLM API key, or against PageIndex Cloud, which adds OCR, image understanding and an MCP server. Local mode handles text-based PDFs only and cites at page level.

- **+** No vector DB or chunking; retrieval is traceable to tree nodes and page references
- **+** Local indexing costs about $0.001 per page; 9 to 1,098 pages took 13 seconds to 4.5 minutes
- **+** Reports 98.7% on FinanceBench; the repo documents a separate OSS benchmark with a runner
- **+** Same client switches between local and cloud; supports agent SDK integration
- **−** Local mode handles text-based PDFs only; OCR and image understanding require the paid Cloud
- **−** Metadata, folders, MCP server and File System for large corpora are Cloud-only
- **−** Query accuracy depends on a strong chat model, which raises per-question cost
- **−** Needs an external LLM API for indexing and chat; no fully offline setup is described

<sub>no GPU · Needs LLM API key (OpenAI or other supported provider), PageIndex API key (Cloud mode only) · Models: OpenAI models, Claude via Claude Code subscription, PageIndex Cloud compatible models · [Repo](https://github.com/vectifyai/pageindex) · [▶️ Demo ↗](https://app.pageindex.ai) · [📖 Docs ↗](https://docs.pageindex.ai) · [🌐 Site ↗](https://pageindex.ai/developer) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pageindex/)</sub>

<a name="surfsense"></a>
### #&#8288;7 [SurfSense](https://github.com/modsetter/surfsense) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Oct 2026</sub>

**Desktop NotebookLM-style agent that researches and edits local documents.**

SurfSense is a desktop app for Windows, macOS (Apple Silicon) and Linux that answers questions over your files with citations and can also create, edit and convert PDF, Word, Excel and PowerPoint documents. The index stays on disk and there is no account. You choose the model: any OpenAI-compatible API or a local one. Edits always produce a new copy.

- **+** Index stays on your disk; no account required
- **+** Edits PDF, Word and Excel files as copies, never altering originals
- **+** Transcribes audio locally and reads scanned pages via OCR
- **+** Works with any OpenAI-compatible API or a local model
- **−** Built-in plugins (Google Search, Web Crawl, etc.) need a SurfSense license; trial is 30 days
- **−** Word and PowerPoint to PDF needs LibreOffice, not included in the installer
- **−** Image generation needs a model you configure; none is chosen by default
- **−** Hosted web app is being sunset; only the desktop app remains

<sub>GPU optional · Needs LibreOffice (optional, for Office conversion) · Models: OpenAI-compatible APIs, local models · README: alternative to NotebookLM · [Repo](https://github.com/modsetter/surfsense) · [🌐 Site ↗](https://www.surfsense.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/surfsense/)</sub>

<a name="gpt-researcher"></a>
### #&#8288;8 [GPT Researcher](https://github.com/assafelovic/gpt-researcher) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Oct 2026</sub>

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

<a name="weknora"></a>
### #&#8288;9 [WeKnora](https://github.com/tencent/weknora) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · custom license · Oct 2026</sub>

**Knowledge base framework with RAG Q&A, tool-using agents and auto-generated wikis.**

WeKnora is a Go-based knowledge framework from Tencent that parses documents (PDF, Word, Excel, images, XMind and others) into knowledge bases. It then serves hybrid-search RAG with citations, a multi-step agent with sandboxed skills and MCP tools, and an auto-generated wiki with a knowledge graph. It syncs from sources like Feishu, Confluence, Notion and GitLab, answers in IM apps such as WeCom, Slack and Telegram, and can also run as a built-in MCP server.

- **+** Many data source connectors: Feishu, Confluence, Notion, GitLab, Yuque, DingTalk, Seafile, RSS
- **+** Multi-workspace RBAC with four roles, audit log and scoped API keys
- **+** Swappable LLMs, vector databases and storage; 29 built-in model vendors including Ollama
- **+** Lite single-binary mode (SQLite, in-memory queue) alongside Docker Compose and Helm chart
- **−** License reported as NOASSERTION by detection, while the README badge says MIT
- **−** Full feature set needs several services (Neo4j, MinIO, Langfuse via profiles)
- **−** Desktop app has no published installer; must be built from source
- **−** Frequent breaking changes between releases, such as sandbox commands running as root in v0.8.2

<sub>GPU optional · Docker + Compose · Needs Docker, Docker Compose, Neo4j (optional), MinIO (optional), Langfuse (optional), Ollama (optional) · Models: OpenAI, DeepSeek, Qwen, Zhipu, Hunyuan · port 80 · [Repo](https://github.com/tencent/weknora) · [📖 Docs ↗](https://weknora.weixin.qq.com/docs/) · [🌐 Site ↗](https://weknora.weixin.qq.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/weknora/)</sub>

<a name="graphrag"></a>
### #&#8288;10 [graphrag](https://github.com/microsoft/graphrag) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · MIT · Oct 2026</sub>

**Pipeline that builds knowledge graphs from text for LLM question answering.**

GraphRAG is a Python data pipeline from Microsoft Research that uses an LLM to extract structured data from unstructured text and form a knowledge graph. That graph is used to build context for question answering over private data. It runs from a command line (`graphrag init`, indexing, querying) with configurable settings and tunable prompts. The project is in maintenance mode: bug fixes and dependency updates only.

- **+** Backed by a published paper (arXiv 2404.16130) and a Microsoft Research blog post
- **+** Prompt tuning guide for adapting extraction to your own data
- **+** Installable from PyPI, with a CLI quickstart and hosted documentation
- **+** MIT license, with a release in September 2026
- **−** Maintenance mode: no new features and no new PRs accepted
- **−** Indexing can be expensive in LLM calls; README advises starting small
- **−** Not an officially supported Microsoft offering; code is a demonstration
- **−** Config format changes between versions require re-running `graphrag init --force`

<sub>Needs LLM provider · [Repo](https://github.com/microsoft/graphrag) · [📖 Docs ↗](https://microsoft.github.io/graphrag) · [🌐 Site ↗](https://www.microsoft.com/en-us/research/blog/graphrag-unlocking-llm-discovery-on-narrative-private-data/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/graphrag/)</sub>

<a name="rag-anything"></a>
### #&#8288;11 [rag-anything](https://github.com/hkuds/rag-anything) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · MIT · Oct 2026</sub>

**Python library for RAG over PDFs, Office files, images, tables and equations.**

RAG-Anything is a Python framework built on LightRAG that parses mixed-content documents with MinerU, Docling or PaddleOCR. It runs separate processors for images, tables and equations, builds a multimodal knowledge graph, and answers queries with combined vector and graph retrieval. LLM, vision and embedding functions are supplied by the caller, with OpenAI-style examples.

- **+** Handles images, tables and LaTeX equations with dedicated processors instead of text-only chunking
- **+** Selectable parsers: MinerU, Docling or PaddleOCR
- **+** Can insert pre-parsed content lists, skipping document parsing
- **+** VLM-enhanced query mode sends document images to a vision model
- **−** Library only; the visible README shows no web UI, server or user accounts
- **−** Office formats require a separate LibreOffice install
- **−** Needs external LLM and vision model functions that you wire up yourself
- **−** RAM and GPU requirements are not stated; MinerU models download on first use

<sub>Needs LightRAG, MinerU, LibreOffice (Office files), Pillow (image extra), ReportLab (text extra) · Models: OpenAI-compatible LLM, vision and embedding functions · [Repo](https://github.com/hkuds/rag-anything) · [🌐 Site ↗](https://github.com/HKUDS/RAG-Anything) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rag-anything/)</sub>

<a name="private-gpt"></a>
### #&#8288;12 [PrivateGPT](https://github.com/zylon-ai/private-gpt) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 58k · Apache-2.0 · Oct 2026</sub>

**Anthropic-style API layer for private RAG on local inference servers.**

PrivateGPT 1.0 is an API server shaped like the Anthropic Messages API, adding file ingestion, retrieval with citations, web search, code execution, MCP and direct database or CSV querying. It runs no models; it calls any OpenAI-compatible server (Ollama, llama.cpp, vLLM) through OPENAI_API_BASE. A workbench UI at /ui on port 8080 exists for testing; the API is the product.

- **+** Anthropic Messages API shape, so Claude Code, Claude Desktop and Office add-ins can target it
- **+** Backend-agnostic: any OpenAI-compatible inference server via OPENAI_API_BASE
- **+** Built-in database and CSV querying, no extra tool server needed
- **+** Installs with brew or uv tool install; Docker also documented
- **−** Runs no models; a separate inference server and embedding server are required
- **−** No prompt caching and no OAuth or organizations
- **−** Skills support is marked basic; structured output depends on the backend
- **−** RBAC, LDAP, connectors and audit logs exist only in the commercial Zylon platform

<sub>no GPU · Docker · Needs OpenAI-compatible inference server (Ollama, llama.cpp, vLLM) · Models: any model behind an OpenAI-compatible /v1/chat/completions endpoint · port 8080 · [Repo](https://github.com/zylon-ai/private-gpt) · [📖 Docs ↗](https://docs.privategpt.dev/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/private-gpt/)</sub>

<a name="quivr"></a>
### #&#8288;13 [quivr](https://github.com/the-vibe-company/quivr) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (85) · Freshness: recent (70) · Maintenance: healthy (82) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · MIT · Oct 2026</sub>

**Go engine that ingests content streams for hybrid search and keyword alerts.**

Quivr V2 is a Go service that durably ingests text and documents, indexes them in Weaviate for lexical, semantic and hybrid search, and runs saved queries as subscriptions that produce matches and signed webhooks. State lives in PostgreSQL and S3-compatible storage, with Temporal for orchestration and plugins for connectors and alert rules. The README marks it as evaluation stage with a v0 API that may change.

- **+** Idempotent writes and immutable Versions; search index can be rebuilt from PostgreSQL and S3
- **+** Hybrid search rehydrates and re-authorizes every hit; outages return errors, not empty results
- **+** Subscriptions with keyword, meaning and described alerts, plus signed webhook delivery
- **+** Prometheus metrics, optional OpenTelemetry tracing, and documented worker autoscaling and upgrades
- **−** README says evaluation stage, API v0 may change, not for production
- **−** Heavy stack: PostgreSQL, Temporal, Weaviate, S3 storage and a TEI embedding server
- **−** No chat or LLM answer generation described; differs from the earlier Quivr assistant
- **−** Described alerts send article text to TypeSafe; last release is February 2025

<sub>no GPU · Docker + Compose · Needs PostgreSQL 17, Temporal, Weaviate, S3-compatible storage (SeaweedFS locally), TEI (multilingual-e5-small), Docker Compose · Models: multilingual-e5-small (384-dim, local TEI), custom embedding model server, hosted embedding API · port 5183 · [Repo](https://github.com/the-vibe-company/quivr) · [📖 Docs ↗](https://docs.quivr.thevibecompany.co/quickstart) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/quivr/)</sub>

<a name="docsgpt"></a>
### #&#8288;14 [docsgpt](https://github.com/arc53/docsgpt) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · MIT · Oct 2026</sub>

**Builds agents and workflows that answer from your documents with citations.**

DocsGPT ingests documents, web pages and synced sources such as Google Drive, Confluence, GitHub and S3, and runs agents that answer with cited sources. Agents can use tools, MCP servers and sandboxed code, and can be chained in a visual workflow builder. It is served through a web app, an embeddable widget, an OpenAI-compatible /v1 API and an MCP server, with OIDC SSO, teams and quotas.

- **+** Connectors sync Google Drive, SharePoint, Confluence, GitHub and S3, with GraphRAG
- **+** Exposes agents via widget, OpenAI-compatible API, webhooks and MCP server
- **+** SSO (OIDC/SCIM), roles, quotas and audit log are all MIT licensed
- **+** Works with OpenAI, Anthropic, Google, Groq, Ollama, vLLM; air-gapped install documented
- **−** Stack needs API, Celery worker, Postgres, Redis and a vector store
- **−** README gives no RAM or GPU sizing for local models
- **−** Wide scope (workflows, guardrails, connectors) means a large surface to operate
- **−** Quick install is a curl-pipe-to-shell script that requires Docker

<sub>GPU optional · Docker + Compose · Needs Docker, PostgreSQL, Redis, Vector store (FAISS, pgvector, Elasticsearch, Qdrant, Milvus or MongoDB) · Models: OpenAI, Anthropic, Google, Groq, OpenRouter · port 7091 · [Repo](https://github.com/arc53/docsgpt) · [▶️ Demo ↗](https://app.docsgpt.cloud/) · [📖 Docs ↗](https://docs.docsgpt.cloud/) · [🌐 Site ↗](https://www.docsgpt.cloud) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/docsgpt/)</sub>

<a name="morphic"></a>
### #&#8288;15 [Morphic](https://github.com/miurla/morphic) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: known (30) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.2k · Apache-2.0 · Oct 2026</sub>

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

<a name="txtai"></a>
### #&#8288;16 [txtai](https://github.com/neuml/txtai) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (46) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Oct 2026</sub>

**Python embeddings database with pipelines, workflows and agents for search and RAG.**

txtai is a Python library built around an embeddings database that combines sparse and dense vector indexes, graph networks and relational storage. On top of it sit LLM pipelines, workflows, RAG and agents (built on smolagents), exposed through a FastAPI web API and an MCP API. LLMs can come from Hugging Face, llama.cpp or LiteLLM.

- **+** Embeddings database combines vector indexes, graph analysis and SQL queries in one library
- **+** Pipelines for transcription, translation, summarization and labeling, not only LLM prompts
- **+** Web API from a YAML config via uvicorn; bindings for JavaScript, Java, Rust and Go
- **+** Over 70 example notebooks plus quickstart scripts for search, RAG, agents and workflows
- **−** Code-first library with no built-in chat UI or visual workflow builder
- **−** No Docker or compose files detected in the repo; container docs are linked separately
- **−** Hardware requirements are not stated; the recommended LLM in the model guide is 31B
- **−** Agent layer is built on smolagents, so its behavior follows that upstream project

<sub>GPU optional · Docker · Needs Python 3.11+, Hugging Face Transformers, Sentence Transformers, FastAPI · Models: Hugging Face models, llama.cpp, LiteLLM (OpenAI, Claude, AWS Bedrock) · port 8000 · [Repo](https://github.com/neuml/txtai) · [📖 Docs ↗](https://neuml.github.io/txtai/) · [🌐 Site ↗](https://neuml.github.io/txtai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/txtai/)</sub>

<a name="db-gpt"></a>
### #&#8288;17 [DB-GPT](https://github.com/eosphoros-ai/db-gpt) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · MIT · Oct 2026</sub>

**Agentic data assistant that writes SQL and code over your databases.**

DB-GPT connects to databases, CSV and Excel files, warehouses and knowledge bases, then plans tasks, writes SQL and Python, runs them in sandboxes and produces charts, dashboards and HTML reports. It installs with pip install dbgpt-app (Python 3.10+) plus a setup wizard and serves a web UI on port 5670, with OpenAI-compatible, DashScope, Moonshot and MiniMax profiles and local models via vLLM or llama.cpp.

- **+** NL-to-SQL plus Python analysis with sandboxed execution
- **+** Outputs charts, dashboards and HTML reports, not only answers
- **+** Skills importable from GitHub for repeatable analysis workflows
- **+** Local serving via vLLM or llama.cpp and a Text2SQL fine-tuning hub
- **−** Recommended install pipes a remote script into bash
- **−** Docs and community largely on dbgpt.cn; Docker and GPU setup only there
- **−** Text2SQL fine-tune list stops at older models such as LLaMA-2 and ChatGLM2
- **−** Default pip install bundles ChromaDB only; other vector stores need extras

<sub>GPU optional · Docker + Compose · Compose runs MySQL · Models: OpenAI-compatible APIs, DashScope/Tongyi, Moonshot (Kimi), MiniMax, local models via vLLM or llama.cpp: DeepSeek, Qwen, GLM, Llama, Gemma, Yi · port 5670 · [Repo](https://github.com/eosphoros-ai/db-gpt) · [📖 Docs ↗](http://docs.dbgpt.cn/docs/overview/) · [🌐 Site ↗](http://dbgpt.cn/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/db-gpt/)</sub>

<a name="utopia"></a>
### #&#8288;18 [utopia](https://github.com/deeplethe/utopia) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (25) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.6k · Apache-2.0 · Oct 2026</sub>

**Bitemporal knowledge graph with ontology, review queue and MCP access.**

Utopia ingests documents and database tables into a bitemporal knowledge graph, tracking when each fact held and when the system learned it. It adds an editable ontology, entity resolution, conflict detection and a human review queue. Search and chat use Tantivy full-text and pgvector with citations, and each knowledge base is exposed over MCP. It runs as one Rust binary plus Postgres.

- **+** Bitemporal facts: corrections close old versions instead of overwriting, so past beliefs stay queryable
- **+** Only a Rust binary and Postgres with pgvector; full-text search is embedded
- **+** Any OpenAI-compatible endpoint (Ollama, vLLM, DeepSeek, Qwen) works, so it can run air-gapped
- **+** Per-knowledge-base MCP server with scoped permissions; agent writes go to human review
- **−** Version 0.1: schema changes between versions, migrations only roll forward
- **−** Chat and embedding models must be configured before extraction works
- **−** Decision reasoning, execution gate, OIDC SSO and backup commands are still roadmap items
- **−** Scanned documents need a MinerU service or a Volcengine Ark vision model

<sub>no GPU · Docker + Compose · Needs Postgres with pgvector, OpenAI-compatible chat model endpoint, OpenAI-compatible embedding endpoint, MinerU or Volcengine Ark (optional, for scans) · Models: OpenAI-compatible endpoints, DeepSeek, Qwen, GLM, Ollama · port 1516 · [Repo](https://github.com/deeplethe/utopia) · [🌐 Site ↗](https://utopia.bi) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/utopia/)</sub>

<a name="pipeshub"></a>
### #&#8288;19 [PipesHub](https://github.com/pipeshub-ai/pipeshub-ai) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.9k · Apache-2.0 · Oct 2026</sub>

**Permission-aware search and cited answers across Slack, Drive, GitHub and 50+ systems.**

PipesHub indexes content from 50+ business systems such as Slack, Google Drive, GitHub, Microsoft 365 and Notion. It answers questions with block-level citations, filtered by each user's source-system permissions. The same context is exposed to your own agents through an MCP server, Python, TypeScript and Go SDKs, and a no-code agent builder.

- **+** Answers carry block-level citations to the original documents
- **+** Access checks follow source-system permissions per user, resolved at query time
- **+** 50+ connectors with real-time and scheduled indexing
- **+** MCP server plus Python, TypeScript and Go SDKs; any LLM provider or Ollama
- **−** Stack needs Neo4j or ArangoDB, Qdrant, MongoDB and Redis, plus Kafka at larger scale
- **−** Audio and video can be stored but are not indexed yet
- **−** Hosted PipesHub Cloud is only a waitlist
- **−** README does not list supported LLM providers, only 'any provider'

<sub>GPU optional · Docker + Compose · Needs Docker Compose v2, Neo4j or ArangoDB, Qdrant, MongoDB, Redis, Kafka (larger deployments) · Models: any LLM provider, Ollama, local embedding server, multimodal LLM for scanned PDF OCR · port 3000 · [Repo](https://github.com/pipeshub-ai/pipeshub-ai) · [▶️ Demo ↗](https://youtu.be/VgyND38QZ7w) · [📖 Docs ↗](https://docs.pipeshub.com/) · [🌐 Site ↗](https://www.pipeshub.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pipeshub/)</sub>

<a name="local-deep-research"></a>
### #&#8288;20 [Local Deep Research](https://github.com/learningcircuit/local-deep-research) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: known (33) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.4k · MIT · Oct 2026</sub>

**Agentic research tool that searches web, papers and your files, writes cited reports.**

Local Deep Research runs multi-step research on a question using an LLM (Ollama or any OpenAI-compatible endpoint) and search engines such as SearXNG, arXiv and PubMed, then writes a report with citations. Sources can be saved to a per-user SQLCipher-encrypted library that is indexed and searched in later runs. The web UI listens on port 5000 and offers several strategies, including a LangGraph agent mode, plus egress scopes that limit where a run may connect.

- **+** Per-user AES-256 SQLCipher databases, including per-user LLM API keys
- **+** Egress scopes (Adaptive, Public only, Private only, Strict) restrict search and model traffic
- **+** README reports ~95% SimpleQA (n=500) with Qwen3.6-27B on one RTX 3090
- **+** Researched sources can be downloaded, indexed and searched alongside the live web
- **−** Needs a separate LLM backend and SearXNG; pip install does not include them
- **−** Egress guard is a partial safeguard, not an air gap; relays to hosted models go undetected
- **−** Self-hosted SearXNG still forwards queries to upstream internet engines
- **−** Private SearXNG URLs are blocked by default since v1.10.3 without an operator opt-in

<sub>GPU optional · Docker + Compose · Needs Ollama or OpenAI-compatible LLM endpoint, SearXNG, Docker (optional) · Models: Ollama, OpenAI-compatible endpoints · port 5000 · [Repo](https://github.com/learningcircuit/local-deep-research) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/local-deep-research/)</sub>

<a name="paperless-gpt"></a>
### #&#8288;21 [paperless-gpt](https://github.com/icereed/paperless-gpt) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (3) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.8k · MIT · Oct 2026</sub>

**LLM-based OCR, titles, tags and document linking for paperless-ngx.**

paperless-gpt is a Go service that sits next to paperless-ngx and uses an LLM to generate titles, tags, correspondents, created dates and custom fields. It also re-runs OCR through a vision LLM, Google Document AI, Azure Document Intelligence or a Docling server, and can produce searchable PDFs. Suggestions can be reviewed in a web UI or applied automatically via trigger tags.

- **+** Supports OpenAI, Azure OpenAI, Mistral, Anthropic and Ollama, so it can run fully local
- **+** Four OCR backends: vision LLM, Google Document AI, Azure Document Intelligence, Docling
- **+** Links related documents via exact reference lookup and leaves ambiguous matches unlinked
- **+** Editable prompts and per-document-type AI workflows, with manual review or auto processing
- **−** No built-in authentication; needs a reverse proxy or VPN in front
- **−** Only works with paperless-ngx; tested against 2.20.x and a 3.0 beta
- **−** Version-mode PDF upload requires paperless-ngx 3.0 or later
- **−** Local OCR quality and speed depend on the Ollama model and hardware; sizing unknown

<sub>GPU optional · Docker + Compose · Needs paperless-ngx, OpenAI, Anthropic, Mistral or Ollama LLM provider, Docker · Models: OpenAI, Azure OpenAI, Mistral, Anthropic, Ollama · port 8080 · [Repo](https://github.com/icereed/paperless-gpt) · [📖 Docs ↗](https://github.com/icereed/paperless-gpt/blob/main/docs/workflows.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paperless-gpt/)</sub>

<a name="niubigeo"></a>
### #&#8288;22 [niubigeo](https://github.com/albert-weasker/niubigeo) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: fair (79) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.9k · Apache-2.0 · Oct 2026</sub>

**Self-hosted tool for tracking how AI models mention your brand and competitors.**

NiubiGEO runs a domain or keyword through several models via OpenRouter, direct provider APIs or custom OpenAI-compatible endpoints, and stores the original answers, mentions, competitors and citations. Runs can be repeated or scheduled, and v0.3 adds a beta keyword monitoring module with a Diff View between stored runs. It is a Node.js app on port 8787 with a Docker option.

- **+** Stores original answers and citations behind each observation, with no opaque score
- **+** Mixes OpenRouter, direct provider and custom OpenAI-compatible endpoints in one test
- **+** Per-model web search setting; results record the actual execution conditions
- **+** Keyword monitoring with hourly, daily or weekly schedules and a Diff View between runs
- **−** Keyword monitoring is labeled BETA in v0.3
- **−** No separate competitor detection dashboard in v0.3
- **−** Scheduled runs need a separate monitoring worker running
- **−** Model API and search costs are charged to your own keys

<sub>no GPU · Docker + Compose · Needs Node.js 22.13+, OpenRouter API key or other OpenAI-compatible model API · Models: OpenRouter, direct provider APIs, custom OpenAI-compatible endpoints · port 8787 · [Repo](https://github.com/albert-weasker/niubigeo) · [📖 Docs ↗](https://github.com/Albert-Weasker/niubigeo/blob/main/docs/PRODUCT-GUIDE.md) · [🌐 Site ↗](https://niubigeo.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/niubigeo/)</sub>

<a name="pixelrag"></a>
### #&#8288;23 [pixelrag](https://github.com/startrail-org/pixelrag) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: known (39) · Freshness: active (100) · Maintenance: patchy (47) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Oct 2026</sub>

**Visual RAG that renders pages and PDFs to screenshots and searches the images.**

PixelRAG renders web pages, PDFs and images to screenshot tiles with Playwright/CDP, embeds them with a LoRA-fine-tuned Qwen3-VL-Embedding-2B, and serves FAISS (or Qdrant) search through a FastAPI endpoint. Tables, charts and layout are kept because nothing is parsed to text. It also ships a pixelbrowse plugin for Claude Code and opencode, and a hosted index of 8.28M Wikipedia pages.

- **+** Retrieves over screenshots, so tables, charts and layout survive indexing
- **+** Hosted API over 8.28M Wikipedia pages, no setup or API key
- **+** Stages run standalone: pixelshot, chunk, embed, build-index, serve
- **+** Runs on Linux CUDA and Apple Silicon MPS; FAISS default, optional Qdrant backend
- **−** Pre-built base Wikipedia index is about 217G to download
- **−** Docker image is not built in CI and runs Chrome without its sandbox
- **−** Training is a separate uv project with pinned torch 2.9.1+cu129
- **−** Bundled turbo headless_shell auto-installs on linux-x64 only

<sub>GPU optional · Docker + Compose · Needs Chromium/Chrome (Playwright), FAISS, poppler (PDF), Qdrant (optional) · Models: Qwen3-VL-Embedding-2B, LoRA adapters on Hugging Face · port 30001 · [Repo](https://github.com/startrail-org/pixelrag) · [▶️ Demo ↗](https://pixelrag.ai) · [📖 Docs ↗](https://pixelrag.ai/docs) · [🌐 Site ↗](https://pixelrag.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pixelrag/)</sub>

<a name="localgpt"></a>
### #&#8288;24 [localgpt](https://github.com/promtengineer/localgpt) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: popular (65) · Freshness: active (100) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Aug 2026</sub>

**Private document Q&A with hybrid search and reranking over Ollama models.**

LocalGPT indexes PDF, DOCX, HTML, Markdown and TXT files with Docling and answers questions over them using LanceDB hybrid search (dense vectors plus full-text, fused with RRF) and a Qwen3 cross-encoder reranker. A router chooses between RAG and a direct LLM answer, and generation runs through Ollama. It ships a Next.js UI, a REST backend on port 8000 and a RAG API on port 8001.

- **+** Hybrid retrieval: LanceDB vector plus full-text, RRF fusion, reranking on by default
- **+** Defaults chosen from documented ablations in eval/decisions; late chunking and verification are optional
- **+** Every UI action is an HTTP call; CLI and scripts can also build indexes
- **+** Embedding and reranking pick CUDA, then Apple MPS, then CPU automatically
- **−** Needs Python, Node.js 20+ and Ollama, running four separate services
- **−** Reranker is about 7.5 GB and downloads on the first reranked query
- **−** Changing the embedding model invalidates existing indexes; they must be rebuilt
- **−** Vision and multimodal models are not integrated; scanned PDFs rely on OCR engines

<sub>RAM ≥ 8 GB · GPU optional · Docker + Compose · Needs Ollama, Python 3.10+, Node.js 20+, LanceDB, Docling, SQLite · Models: Ollama models (qwen3.5:9b default), HuggingFace embedding models, Qwen3-Reranker, watsonx · port 3000 · [Repo](https://github.com/promtengineer/localgpt) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/localgpt/)</sub>

<a name="vane"></a>
### #&#8288;25 [Vane](https://github.com/itzcrazykns/vane) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: widely used (81) · Freshness: active (98) · Maintenance: weak (10) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · MIT · Sep 2026</sub>

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

<a name="llmware"></a>
### #&#8288;26 [llmware](https://github.com/llmware-ai/llmware) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: known (50) · Freshness: active (100) · Maintenance: patchy (40) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · Apache-2.0 · Oct 2026</sub>

**Python framework for RAG pipelines with a catalog of 300+ local models.**

llmware is a Python library that combines a model catalog (300+ models in GGUF, OpenVINO, ONNXRuntime, PyTorch and Hugging Face formats, plus OpenAI, Anthropic and Google APIs) with a RAG pipeline. The pipeline parses mixed document types into libraries, embeds them into a chosen vector DB, and runs text, semantic or hybrid queries. It also ships its own 1-7B BLING, DRAGON and SLIM models for laptop-scale inference.

- **+** One ModelCatalog interface across GGUF, OpenVINO, ONNXRuntime, PyTorch and cloud APIs
- **+** Ingests pdf, docx, pptx, xlsx, csv, html, wav and images through one add_files call
- **+** Mix and match embedding models and vector DBs per library, such as Milvus or ChromaDB
- **+** Includes post-inference evidence checks against the attached source material
- **−** Library only; no web UI or server is described in the README
- **−** Needs a text-collection database and vector DB; setup details are not in the excerpt
- **−** RAG examples lean on llmware's own finetuned 1-7B models, so quality on other models is unknown
- **−** No Docker or compose files detected in the repository

<sub>GPU optional · Needs Milvus, ChromaDB · Models: GGUF, OpenVINO, ONNXRuntime, ONNXRuntime-QNN, PyTorch · [Repo](https://github.com/llmware-ai/llmware) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llmware/)</sub>

<a name="deepwiki-open"></a>
### #&#8288;27 [DeepWiki-Open](https://github.com/asyncfuncai/deepwiki-open) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: weak (29) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · MIT · Oct 2026</sub>

**Generates browsable wikis and diagrams for GitHub, GitLab and Bitbucket repos.**

DeepWiki-Open takes a repository URL from GitHub, GitLab or Bitbucket, analyzes the code structure, generates documentation and diagrams, organizes them into a navigable wiki and builds a codemap for guided tours. The repo ships a Dockerfile and compose file. The README now points to a 2.0 release called Grok Wiki distributed as a download from grok-wiki.com and no longer documents configuration.

- **+** Works with GitHub, GitLab and Bitbucket repositories
- **+** Produces diagrams and codemap guided tours, not only prose
- **+** Dockerfile and docker-compose in the repo; MIT license
- **−** README no longer documents setup, ports or supported model providers
- **−** 2.0 is pushed as a separate download at grok-wiki.com
- **−** No hardware guidance; single-maintainer project

<sub>no GPU · Docker + Compose · [Repo](https://github.com/asyncfuncai/deepwiki-open) · [🌐 Site ↗](https://grok-wiki.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepwiki-open/)</sub>

<a name="docling-serve"></a>
### #&#8288;28 [Docling Serve](https://github.com/docling-project/docling-serve) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (2) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · MIT · Oct 2026</sub>

**Docling document conversion as an HTTP API with playground UI.**

Docling Serve wraps the Docling document converter in a FastAPI service: POST a URL or file to /v1/convert/source and get structured text back, with OpenAPI docs at /docs and a playground UI at /ui on port 5001. Container images cover CPU (4.4 GB), CUDA 12.8 (11.4 GB) and CUDA 13.0 on amd64 and arm64; a ROCm image builds locally. Suited to RAG pipelines that need a document-to-text service.

- **+** Single container with API, OpenAPI docs and a playground UI
- **+** Stable v1 API after migration
- **+** CPU and CUDA 12.8/13.0 images for amd64 and arm64
- **+** Converts from HTTP sources or uploads in one call
- **−** Images are large: 4.4 GB CPU, 8.7 GB base amd64, 11.4 GB CUDA
- **−** CUDA images carry no latest tag; pin explicit versions
- **−** ROCm image is not published; build it yourself
- **−** Slim images without bundled weights are only announced

<sub>GPU optional · Docker · Models: bundled Docling parsing models · port 5001 · [Repo](https://github.com/docling-project/docling-serve) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/docling-serve/)</sub>

<a name="paper-qa"></a>
### #&#8288;29 [paper-qa](https://github.com/future-house/paper-qa) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: known (35) · Freshness: active (100) · Maintenance: patchy (30) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.5k · Apache-2.0 · Oct 2026</sub>

**Python RAG library and CLI for answering questions over scientific PDFs with citations.**

PaperQA2 indexes local PDFs, text, Office documents and source files, fetches paper metadata from Crossref and Semantic Scholar, and answers questions with in-text citations. An LLM agent runs paper search, evidence gathering and answer generation, using LLM re-ranking and contextual summarization. It ships a `pqa` CLI and a Python API, and works with any LiteLLM-supported model.

- **+** Answers carry in-text citations to specific papers and page ranges
- **+** Pulls citation counts and retraction checks from Crossref and Semantic Scholar
- **+** Any LiteLLM provider works, including local servers and Sentence Transformers embeddings
- **+** Bundled settings (fast, high_quality, wikicrow, contracrow) and a CLI with persistent index
- **−** Defaults to OpenAI embeddings and models, so an API key is needed out of the box
- **−** CalVer since December 2025 drops backwards-compatibility guarantees between releases
- **−** Library and CLI only, with no web UI or multi-user features
- **−** Indexing 100+ papers needs Crossref and Semantic Scholar keys to avoid rate limits

<sub>GPU optional · Needs LLM provider API key or local LLM server, Crossref API, Semantic Scholar API · Models: LiteLLM providers, OpenAI, llamafile, Sentence Transformers embeddings · [Repo](https://github.com/future-house/paper-qa) · [🌐 Site ↗](https://paper.wikicrow.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paper-qa/)</sub>

<a name="kotaemon"></a>
### #&#8288;30 [Kotaemon](https://github.com/cinnamon/kotaemon) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: popular (71) · Freshness: active (84) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · Apache-2.0 · May 2026</sub>

**Gradio RAG UI with hybrid retrieval, citations and multi-user login.**

Kotaemon is a Gradio web app for question answering over uploaded documents, with hybrid full-text plus vector retrieval, reranking, citations shown in an in-browser PDF viewer and ReAct or ReWOO agents. It supports OpenAI, Azure, Cohere, Groq, Ollama and GGUF via llama-cpp-python, with Elasticsearch, LanceDB, ChromaDB, Milvus or Qdrant storage. Docker images come in lite, full and ollama variants on port 7860.

- **+** Hybrid retriever plus reranking by default, with low-relevance warnings
- **+** Citations open in a PDF viewer with highlights and relevance scores
- **+** Multi-user login with private and public collections
- **+** GraphRAG options: nano-graphrag, LightRAG or Microsoft GraphRAG
- **−** Default login is admin/admin
- **−** GraphRAG extras cause hnswlib version conflicts that need manual pip fixes
- **−** Only PDF, HTML, MHTML and XLSX without the larger full image
- **−** Last commit 2026-05-30; MS GraphRAG indexing works only with OpenAI or Ollama

<sub>no GPU · Docker · Needs Elasticsearch, LanceDB, ChromaDB, Milvus or Qdrant (optional stores), Unstructured (optional, for .doc/.docx and more) · Models: OpenAI, Azure OpenAI, Cohere, Groq, Ollama · port 7860 · [Repo](https://github.com/cinnamon/kotaemon) · [▶️ Demo ↗](https://huggingface.co/spaces/cin-model/kotaemon-demo) · [📖 Docs ↗](https://cinnamon.github.io/kotaemon/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kotaemon/)</sub>

<a name="scira"></a>
### #&#8288;31 [scira](https://github.com/zaidmukaddam/scira) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: known (42) · Freshness: active (100) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · AGPL-3.0 · Aug 2026</sub>

**AI search engine that plans multi-step research and answers with inline citations.**

Scira is a Next.js app that takes a question, uploaded file or URL, breaks it into sub-tasks, searches live sources and returns an answer with clickable citations. It has 17 search modes (web, academic, Reddit, X, YouTube, stocks, crypto and others) and 28 tools, and it routes to hosted models from xAI, OpenAI, Anthropic, Google and others through the Vercel AI SDK. Self-hosting needs API keys for many third-party services.

- **+** 17 search modes, including academic, Reddit, YouTube, stocks and prediction markets
- **+** Every answer carries inline citations linked to the retrieved sources
- **+** Many hosted model families via one SDK, including Claude, GPT, Gemini, Qwen and DeepSeek
- **+** Scheduled recurring research agents (Lookouts) email updates on tracked topics
- **−** Depends on many third-party APIs (Exa, Firecrawl, Tavily, Valyu, Supadata, Daytona)
- **−** README lists no local model support such as Ollama or GGUF
- **−** Connectors, Memory, Voice and XQL modes are marked Pro
- **−** README is inconsistent on which API keys are required to run it

<sub>no GPU · Docker + Compose · Needs Exa, Firecrawl, Tavily, Parallel, Valyu, Supadata, Daytona, Upstash Redis, Cloudflare R2, Supermemory, Cohere, ElevenLabs, Database (DATABASE_URL), Better Auth · Models: xAI Grok, OpenAI GPT, Anthropic Claude, Google Gemini, Qwen · port 3000 · [Repo](https://github.com/zaidmukaddam/scira) · [▶️ Demo ↗](https://scira.ai) · [🌐 Site ↗](https://scira.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/scira/)</sub>

<a name="morphik"></a>
### #&#8288;32 [Morphik](https://github.com/morphik-org/morphik-core) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: niche (5) · Freshness: active (100) · Maintenance: weak (29) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · custom license · Oct 2026</sub>

**Multimodal retrieval engine for visually rich PDFs, images and video.**

Morphik Core is a retrieval engine for visually rich documents: it embeds page images with ColPali so charts, tables and diagrams are searchable through one endpoint covering PDFs, images and video, and extracts metadata such as bounding boxes and labels by rules. It is used via a Python SDK, REST API, MCP or the Console web UI. Self-hosting is documented separately and offered with limited support.

- **+** ColPali retrieval over page images instead of extracted text
- **+** One search endpoint for images, PDFs and video
- **+** Rule-based metadata extraction with bounding boxes and classification
- **+** Python SDK, REST API and MCP access
- **−** BSL 1.1: commercial use above US $2,000 per month revenue needs a paid key
- **−** Self-hosted deployments get no full support from the maintainers
- **−** README centers on the hosted dev.morphik.ai service, not self-hosting
- **−** Parent company now focuses on back-office AI workers; Core is a side product

<sub>no GPU · Docker + Compose · Compose runs Redis, PostgreSQL, Ollama · Models: ColPali multimodal embeddings · [Repo](https://github.com/morphik-org/morphik-core) · [▶️ Demo ↗](https://dev.morphik.ai) · [📖 Docs ↗](https://dev.morphik.ai/docs) · [🌐 Site ↗](https://morphik.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/morphik/)</sub>

<a name="local-deep-researcher"></a>
### #&#8288;33 [local-deep-researcher](https://github.com/langchain-ai/local-deep-researcher) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: known (32) · Freshness: active (100) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.4k · MIT · Oct 2026</sub>

**Iterative web research agent that runs on Ollama or LM Studio models.**

Takes a topic, has a local LLM write a search query, summarizes the results, reflects on knowledge gaps and searches again for a configurable number of loops (default 3). The output is a markdown summary with cited sources, stored in LangGraph state. It runs as a LangGraph graph that you inspect through LangGraph Studio.

- **+** DuckDuckGo search by default, so no API key is needed to start
- **+** Supports Ollama and LM Studio, with SearXNG, Tavily and Perplexity as search options
- **+** Final markdown report cites all sources gathered during the loops
- **+** Fallback handling for models that fail structured JSON output
- **−** No standalone UI; interaction goes through LangGraph Studio, opened via smith.langchain.com
- **−** Small models such as DeepSeek R1 1.5B and 7B struggle with required JSON output
- **−** Docker image does not include Ollama; it must be run and configured separately
- **−** Safari shows mixed-content warnings with Studio; Firefox is recommended

<sub>GPU optional · Docker · Needs Ollama or LM Studio, LangGraph CLI, uv, DuckDuckGo, SearXNG, Tavily or Perplexity for search · Models: Ollama models (default llama3.2), LM Studio OpenAI-compatible server, DeepSeek R1 distills, qwen_qwq-32b · port 2024 · [Repo](https://github.com/langchain-ai/local-deep-researcher) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/local-deep-researcher/)</sub>

<a name="deep-searcher"></a>
### #&#8288;34 [deep-searcher](https://github.com/zilliztech/deep-searcher) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: niche (23) · Freshness: active (100) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.4k · Apache-2.0 · Sep 2026</sub>

**Python library for multi-step research reports over private documents in Milvus.**

DeepSearcher is a Python package that loads local files (and web pages via Firecrawl) into a Milvus vector database, then answers questions by running iterative search and reasoning steps with an LLM to produce a written report. LLM, embedding model and vector store are chosen through set_provider_config calls, with many hosted providers and Ollama supported.

- **+** Many LLM providers: OpenAI, DeepSeek, Anthropic, Gemini, Grok, Bedrock, watsonx, Ollama
- **+** Local embedding options via Ollama, FastEmbed and Pymilvus models
- **+** Installs with pip; optional extras such as deepsearcher[ollama]
- **+** Produces long-form reports rather than single-shot answers
- **−** Milvus is the only vector database; other backends are marked under development
- **−** Web crawling needs a Firecrawl API key and is described as under development
- **−** Quick start defaults to OpenAI and requires OPENAI_API_KEY
- **−** Python API only; no bundled web UI documented in the visible README

<sub>GPU optional · Docker · Needs Milvus or Zilliz Cloud, LLM API key or local Ollama, Firecrawl (optional, web crawling) · Models: OpenAI, DeepSeek, Anthropic, Gemini, xAI Grok · [Repo](https://github.com/zilliztech/deep-searcher) · [📖 Docs ↗](https://deepwiki.com/zilliztech/deep-searcher) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deep-searcher/)</sub>

<a name="deep-research"></a>
### #&#8288;35 [deep-research](https://github.com/dzhng/deep-research) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: popular (60) · Freshness: recent (60) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · MIT · Apr 2026</sub>

**Iterative deep-research agent that searches, reads and writes a markdown report.**

A TypeScript CLI that takes a query, asks follow-up questions, then runs recursive search rounds through Firecrawl and an LLM, controlled by breadth and depth parameters. Each round extracts learnings and new research directions, and the result is written to report.md or answer.md. The code is kept deliberately small (target under 500 lines) so it can be read and extended.

- **+** Small codebase, targeted at under 500 lines, easy to read and fork
- **+** Breadth and depth parameters give direct control over research scope
- **+** Works with OpenAI-compatible endpoints, local servers, or Fireworks DeepSeek R1
- **+** Supports self-hosted Firecrawl via FIRECRAWL_BASE_URL
- **−** Requires a Firecrawl key or self-hosted Firecrawl for search and scraping
- **−** CLI only; no web UI or API server described
- **−** Free Firecrawl tier can hit rate limits, forcing concurrency down to 1
- **−** No tagged releases; Docker setup steps are manual

<sub>no GPU · Docker + Compose · Needs Firecrawl API or self-hosted Firecrawl, OpenAI API key or OpenAI-compatible endpoint, Node.js · Models: OpenAI o3-mini, DeepSeek R1 via Fireworks, OpenAI-compatible endpoints (OpenRouter, Gemini, local servers) · [Repo](https://github.com/dzhng/deep-research) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deep-research/)</sub>

<a name="bertopic"></a>
### #&#8288;36 [bertopic](https://github.com/maartengr/bertopic) <sub>score [34](../README.md#-how-we-rank "Score 34/100. Adoption: niche (19) · Freshness: active (88) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.9k · MIT · Aug 2026</sub>

**Python topic modeling library using transformer embeddings and c-TF-IDF.**

BERTopic is a Python library that groups documents into topics. By default it embeds text with sentence-transformers, reduces dimensions with UMAP, clusters with HDBSCAN, and extracts topic words with c-TF-IDF. Each step can be swapped. It also covers guided, supervised, dynamic, hierarchical, online, multimodal and zero-shot variants, plus optional LLM-generated topic labels.

- **+** Each pipeline stage (embedding, UMAP, HDBSCAN, vectorizer, representation) can be replaced or removed
- **+** Many variants in one API: guided, supervised, online, dynamic, hierarchical, multimodal, zero-shot
- **+** Built-in visualizations: topic map, hierarchy, heatmap, topics over time
- **+** Representation models include KeyBERTInspired and OpenAI-based topic labeling
- **−** Library only: no web UI or server, so you write Python
- **−** Default HDBSCAN puts many documents in outlier topic -1 that need extra handling
- **−** Default install pulls in transformers, UMAP and HDBSCAN; lightweight setup is separate
- **−** RAM and GPU requirements are not stated in the README

<sub>GPU optional · Needs sentence-transformers, UMAP, HDBSCAN, scikit-learn · Models: sentence-transformers, Flair, Gensim, spaCy, Universal Sentence Encoder · [Repo](https://github.com/maartengr/bertopic) · [📖 Docs ↗](https://maartengr.github.io/BERTopic/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/bertopic/)</sub>

<a name="langchain-chatchat"></a>
### #&#8288;37 [langchain-chatchat](https://github.com/chatchat-space/langchain-chatchat) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: widely used (83) · Freshness: quiet (3) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · Apache-2.0 · Nov 2025</sub>

**Local knowledge-base Q&A and agent app built on LangChain.**

Chatchat answers questions over your own files by splitting, embedding and retrieving text, then passing the top-k matches to an LLM. It does not load models itself: it connects to Xinference, Ollama, LocalAI, FastChat or One API through OpenAI-compatible endpoints. It ships a FastAPI backend and a Streamlit WebUI, and installs with pip install langchain-chatchat.

- **+** Connects to Xinference, Ollama, LocalAI, FastChat and One API via OpenAI-compatible endpoints
- **+** FAISS by default, other vector stores selectable in kb_settings.yaml
- **+** YAML config reloads without restart (0.3.1+)
- **+** Also has agent tools, search-engine chat, database chat and image chat with qwen-vl-chat
- **−** Needs a separate model server running before the knowledge base can be built
- **−** Last release 2024-07-12; README Docker image tag is dated 2024-08-29
- **−** Default bind is 127.0.0.1; remote access requires editing basic_settings.yaml
- **−** 0.3.x differs a lot from 0.2.x; migration is not guaranteed to work

<sub>GPU optional · Docker + Compose · Needs Xinference, Ollama, LocalAI, FastChat or One API, FAISS (default vector store), SQLite (default database) · Models: GLM-4-Chat, Qwen2-Instruct, Llama3, bge-large-zh-v1.5, qwen-vl-chat · [Repo](https://github.com/chatchat-space/langchain-chatchat) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/langchain-chatchat/)</sub>

<a name="paperless-ai"></a>
### #&#8288;38 [Paperless-AI](https://github.com/clusterzx/paperless-ai) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: niche (9) · Freshness: recent (54) · Maintenance: weak (18) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · MIT · Mar 2026</sub>

**Auto-tags Paperless-ngx documents and adds RAG chat over the archive.**

Paperless-AI watches a Paperless-ngx instance, sends new documents to OpenAI, Ollama, DeepSeek, OpenRouter, Gemini or other OpenAI-compatible backends and writes back title, tags, document type and correspondent. It adds RAG chat over the whole archive and a manual review page at /manual. The maintainer has declared the repo unmaintained pending a rewrite.

- **+** Assigns title, tags, document type and correspondent on new documents automatically
- **+** RAG chat answers questions across the full Paperless archive
- **+** Rules limit which documents get processed; manual mode for sensitive files
- **+** Ollama support keeps processing local
- **−** Repo marked not maintained; rewrite and future uncertain
- **−** Container must be restarted after first setup to build the RAG index
- **−** No port, hardware or env var details in the README; see the wiki
- **−** Paperless-ngx is adding native AI, which may supersede it

<sub>no GPU · Docker + Compose · Needs Paperless-ngx · Models: Ollama (Mistral, Llama, Phi-3, Gemma-2), OpenAI, DeepSeek, OpenRouter, Perplexity, Together, LiteLLM, vLLM, Fastchat, Gemini · [Repo](https://github.com/clusterzx/paperless-ai) · [📖 Docs ↗](https://github.com/clusterzx/paperless-ai/wiki/2.-Installation) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paperless-ai/)</sub>

<a name="kag"></a>
### #&#8288;39 [kag](https://github.com/openspg/kag) <sub>score [19](../README.md#-how-we-rank "Score 19/100. Adoption: niche (29) · Freshness: quiet (28) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.1k · Apache-2.0 · Jan 2026</sub>

**Knowledge-graph Q&A framework with logic-form reasoning, built on OpenSPG.**

KAG builds a knowledge graph from structured and unstructured data on the OpenSPG engine, then answers multi-hop questions with planning, retrieval and reasoning steps guided by logical forms. Graph entities and source text chunks are indexed against each other. Version 0.8.0 adds MCP integration and several built-in index types. It ships as a web product and as a Python toolkit.

- **+** Graph and text chunks are mutually indexed, so answers can link back to source passages
- **+** Schema-constrained extraction supports domain-specific entity and event types
- **+** Solver combines retrieval, graph reasoning, language reasoning and numeric calculation
- **+** MCP support for public data sources and for use inside agent workflows
- **−** Requires the OpenSPG engine and its Docker Compose stack before any use
- **−** The kag-model component is not yet open-sourced
- **−** Detailed usage guides are hosted on Yuque, not in the repo
- **−** Last release was 2025-06-28; RAM and GPU needs are not stated

<sub>Needs OpenSPG engine, Docker, Docker Compose, LLM provider · Models: KAG-Thinker · port 8887 · [Repo](https://github.com/openspg/kag) · [📖 Docs ↗](https://openspg.yuque.com/ndx6g9/docs_en) · [🌐 Site ↗](https://openspg.github.io/v2/docs_en) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kag/)</sub>

<a name="maestro"></a>
### #&#8288;40 [MAESTRO](https://github.com/murtaza-nasir/maestro) <sub>score [17](../README.md#-how-we-rank "Score 17/100. Adoption: niche (0) · Freshness: recent (57) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · AGPL-3.0 · Apr 2026</sub>

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

<a name="r2r"></a>
### #&#8288;41 [r2r](https://github.com/sciphi-ai/r2r) <sub>score [9](../README.md#-how-we-rank "Score 9/100. Adoption: niche (20) · Freshness: quiet (5) · Maintenance: weak (0) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.0k · MIT · Nov 2025</sub>

**RAG server with REST API, hybrid search, knowledge graphs and a research agent.**

R2R is a retrieval-augmented generation server built around a RESTful API, with Python and JavaScript SDKs. It ingests documents (txt, pdf, json, png, mp3), runs hybrid semantic and keyword search with reciprocal rank fusion, and extracts entities and relationships into knowledge graphs. A Deep Research agent does multi-step reasoning over your knowledge base and optionally the web.

- **+** Hybrid search combines semantic and keyword results with reciprocal rank fusion
- **+** Python and JavaScript SDKs over one REST API (examples use port 7272)
- **+** Includes user auth, collections and document management
- **+** Light mode runs from pip install; full mode uses Docker Compose with Postgres
- **−** Last release was 2025-06-06; later commits are unreleased
- **−** README gives no RAM or hardware requirements
- **−** Examples assume hosted LLMs (OpenAI, Anthropic); local model setup not shown
- **−** No bundled chat UI described in the README

<sub>Compose · Needs OpenAI API key (default in quick start), Postgres (full mode via Docker Compose) · Models: OpenAI, Anthropic · port 7272 · [Repo](https://github.com/sciphi-ai/r2r) · [📖 Docs ↗](https://r2r-docs.sciphi.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/r2r/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
