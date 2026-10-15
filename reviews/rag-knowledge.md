# 📚 RAG and knowledge reviews · Best of Open-Source AI

Document Q&A, knowledge bases and enterprise search over your own files and data. Back to the [leaderboard](../README.md#-rag-and-knowledge).

<sub>🌐 Also on the web: [RAG and knowledge on archestack.com](https://archestack.com/best-of-ai/rag-knowledge/), each project on its own page.</sub>

<a name="deeptutor"></a>
### 🥇 [deeptutor](https://github.com/hkuds/deeptutor) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: healthy (92) · Easy to run: easy (67) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · Apache-2.0 · Oct 2026</sub>

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

<a name="open-notebook"></a>
### 🥈 [Open Notebook](https://github.com/lfnovo/open-notebook) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (80) · Freshness: active (100) · Maintenance: healthy (84) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · MIT · Oct 2026</sub>

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

<a name="lightrag"></a>
### 🥉 [LightRAG](https://github.com/hkuds/lightrag) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: healthy (86) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · MIT · Oct 2026</sub>

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

<a name="ragflow"></a>
### #&#8288;4 [RAGFlow](https://github.com/infiniflow/ragflow) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: healthy (93) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 92k · Apache-2.0 · Oct 2026</sub>

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

<a name="maxkb"></a>
### #&#8288;5 [MaxKB](https://github.com/1panel-dev/maxkb) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: known (48) · Freshness: active (100) · Maintenance: healthy (96) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · GPL-3.0 · Oct 2026</sub>

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

<a name="weknora"></a>
### #&#8288;6 [WeKnora](https://github.com/tencent/weknora) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: healthy (89) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · custom license · Oct 2026</sub>

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

<a name="surfsense"></a>
### #&#8288;7 [SurfSense](https://github.com/modsetter/surfsense) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (29) · Freshness: active (100) · Maintenance: healthy (92) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · custom license · Oct 2026</sub>

**Desktop agent that researches and edits your local documents with cited answers.**

SurfSense is a desktop app, a NotebookLM-style agent that indexes your files on local disk and answers with citations. It can also create and edit PDF, Word, Excel and PowerPoint files, always writing a new copy, and generate podcasts, mind maps, flashcards and quizzes. It works with any OpenAI-compatible API or a local model and needs no account.

- **+** Index stays on local disk; no account needed
- **+** Edits PDF, Word, Excel and PowerPoint as new copies, originals untouched
- **+** Works with any OpenAI-compatible API or a local model
- **+** Installers for Windows x64, macOS Apple Silicon and Linux (AppImage, deb)
- **−** Hosted web app is being sunset; export workspaces before 18 October 2026
- **−** Word and PowerPoint to PDF needs LibreOffice, enabled in Settings
- **−** Image generation needs an image model; none is chosen by default
- **−** OCR covers only Latin, Chinese and Japanese script

<sub>GPU optional · Docker + Compose · Needs LibreOffice (optional, for Office to PDF) · Models: OpenAI-compatible APIs, local models · README: alternative to NotebookLM · [Repo](https://github.com/modsetter/surfsense) · [🌐 Site ↗](https://www.surfsense.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/surfsense/)</sub>

<a name="quivr"></a>
### #&#8288;8 [quivr](https://github.com/the-vibe-company/quivr) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (75) · Freshness: recent (70) · Maintenance: healthy (81) · Easy to run: easy (50) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · MIT · Oct 2026</sub>

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

<a name="pageindex"></a>
### #&#8288;9 [pageindex](https://github.com/vectifyai/pageindex) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: healthy (90) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · MIT · Oct 2026</sub>

**Vectorless RAG that builds a tree index of a PDF and lets an LLM search it.**

PageIndex builds a hierarchical tree index from each PDF, then has an LLM reason through that tree to find the relevant sections, with no vector database or chunking. The Python SDK (pip install pageindex) runs locally with your own LLM key for text-based PDFs, or points at PageIndex Cloud for OCR, scanned documents and block-level citations. The README reports 98.7% on FinanceBench and about $0.001 per page to index locally.

- **+** No vector DB or chunking; retrieval is traceable to page-level references
- **+** Local mode indexes a 1,000-page PDF for roughly a dollar, per README benchmarks
- **+** Same client switches between local and Cloud by changing the index argument
- **+** Documents integration with OpenAI Agents SDK and Claude Agent SDK
- **−** Local mode handles text-based PDFs only; no OCR or image understanding
- **−** MCP server, metadata, folders and File System for large corpora are Cloud-only
- **−** Each query needs LLM reasoning calls, so accuracy and cost depend on the chat model
- **−** Needs an external LLM API key; local-model support is not stated in the README

<sub>no GPU · Needs LLM API key (e.g. OpenAI), PageIndex API key (Cloud mode only) · Models: OpenAI models (gpt series), other providers configurable per docs · [Repo](https://github.com/vectifyai/pageindex) · [▶️ Demo ↗](https://app.pageindex.ai) · [📖 Docs ↗](https://docs.pageindex.ai) · [🌐 Site ↗](https://pageindex.ai/developer) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pageindex/)</sub>

<a name="private-gpt"></a>
### #&#8288;10 [PrivateGPT](https://github.com/zylon-ai/private-gpt) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: fair (64) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 58k · Apache-2.0 · Oct 2026</sub>

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

<a name="graphrag"></a>
### #&#8288;11 [graphrag](https://github.com/microsoft/graphrag) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: healthy (85) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · MIT · Oct 2026</sub>

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
### #&#8288;12 [rag-anything](https://github.com/hkuds/rag-anything) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (50) · Freshness: active (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · MIT · Oct 2026</sub>

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

<a name="docsgpt"></a>
### #&#8288;13 [docsgpt](https://github.com/arc53/docsgpt) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: known (36) · Freshness: active (100) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · MIT · Oct 2026</sub>

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

<a name="localgpt"></a>
### #&#8288;14 [localgpt](https://github.com/promtengineer/localgpt) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: known (45) · Freshness: active (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Aug 2026</sub>

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

<a name="pipeshub"></a>
### #&#8288;15 [PipesHub](https://github.com/pipeshub-ai/pipeshub-ai) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.8k · Apache-2.0 · Oct 2026</sub>

**Permission-aware search and agent context over Slack, Drive, GitHub and more.**

PipesHub indexes content from 50+ business systems such as Slack, Google Drive, GitHub, Microsoft 365 and Notion, then answers questions with block-level citations filtered by each user's source-system permissions. It stores data in a Neo4j or ArangoDB graph, Qdrant vectors and MongoDB, and exposes the same context to agents through a no-code builder, an MCP server and Python, TypeScript and Go SDKs. Any LLM provider works, including local models via Ollama.

- **+** Answers cite specific blocks in source documents and respect per-user source permissions
- **+** 50+ connectors with real-time and scheduled indexing
- **+** Exposes context via an MCP server and Python, TypeScript and Go SDKs
- **+** Interactive installer generates secrets and .env; Kubernetes with HA defaults supported
- **−** Multi-service stack: Neo4j or ArangoDB, Qdrant, MongoDB, Redis, optionally Kafka
- **−** Audio and video are stored but not indexed yet
- **−** Hosted PipesHub Cloud is only a waitlist; self-hosting is the only option today
- **−** Personalized search and PageRank-augmented relevance are not yet shipped

<sub>GPU optional · Docker + Compose · Needs Docker Compose v2, Neo4j or ArangoDB, Qdrant, MongoDB, Redis, Kafka (larger deployments) · Models: Any LLM provider, Ollama local models, Local embedding server by default · port 3000 · [Repo](https://github.com/pipeshub-ai/pipeshub-ai) · [▶️ Demo ↗](https://youtu.be/VgyND38QZ7w) · [📖 Docs ↗](https://docs.pipeshub.com/) · [🌐 Site ↗](https://www.pipeshub.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pipeshub/)</sub>

<a name="paperless-gpt"></a>
### #&#8288;16 [paperless-gpt](https://github.com/icereed/paperless-gpt) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (3) · Freshness: active (100) · Maintenance: healthy (82) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.8k · MIT · Oct 2026</sub>

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

<a name="serviette"></a>
### #&#8288;17 [serviette](https://github.com/pathwaycom/serviette) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: widely used (91) · Freshness: active (96) · Maintenance: patchy (33) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 59k · MIT · Jul 2026</sub>

**RAG and enterprise search app templates built on the Pathway live data framework.**

A set of Python templates for RAG and document search that stay in sync with sources such as local files, Google Drive, SharePoint, S3, Kafka and PostgreSQL. Indexing is built in (usearch for vectors, Tantivy for full-text), so no separate vector database, cache or API framework is needed. Templates include basic Q&A, multimodal GPT-4o parsing, unstructured-to-SQL, Adaptive RAG, a private Mistral/Ollama variant and video RAG, each exposing an HTTP API.

- **+** Index updates on additions, deletions and edits in connected sources
- **+** Built-in vector, hybrid and full-text indexes, no external vector DB
- **+** Private template runs locally with Mistral and Ollama
- **+** Optional Streamlit UI for quick demos
- **−** Tied to the Pathway framework, so pipeline code is not portable
- **−** Several templates call hosted APIs (GPT-4o, TwelveLabs)
- **−** No tagged releases
- **−** README gives no RAM or hardware requirements

<sub>Needs Pathway, usearch, Tantivy, PostgreSQL (SQL template), Ollama (private template), TwelveLabs (video template), Streamlit (optional UI) · Models: OpenAI GPT-4o, Mistral via Ollama, TwelveLabs Pegasus and Marengo · [Repo](https://github.com/pathwaycom/serviette) · [▶️ Demo ↗](https://pathway.com/solutions/rag-pipelines#try-it-out) · [📖 Docs ↗](https://pathway.com/developers/templates/) · [🌐 Site ↗](https://pathway.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/serviette/)</sub>

<a name="llmware"></a>
### #&#8288;18 [llmware](https://github.com/llmware-ai/llmware) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (24) · Freshness: active (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · Apache-2.0 · Oct 2026</sub>

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

<a name="docling-serve"></a>
### #&#8288;19 [Docling Serve](https://github.com/docling-project/docling-serve) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: healthy (82) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · MIT · Oct 2026</sub>

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

<a name="db-gpt"></a>
### #&#8288;20 [DB-GPT](https://github.com/eosphoros-ai/db-gpt) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: known (40) · Freshness: active (100) · Maintenance: fair (60) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · MIT · Oct 2026</sub>

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

<a name="deepwiki-open"></a>
### #&#8288;21 [DeepWiki-Open](https://github.com/asyncfuncai/deepwiki-open) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: known (34) · Freshness: active (100) · Maintenance: patchy (40) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · MIT · Sep 2026</sub>

**Generates browsable wikis and diagrams for GitHub, GitLab and Bitbucket repos.**

DeepWiki-Open takes a repository URL from GitHub, GitLab or Bitbucket, analyzes the code structure, generates documentation and diagrams, organizes them into a navigable wiki and builds a codemap for guided tours. The repo ships a Dockerfile and compose file. The README now points to a 2.0 release called Grok Wiki distributed as a download from grok-wiki.com and no longer documents configuration.

- **+** Works with GitHub, GitLab and Bitbucket repositories
- **+** Produces diagrams and codemap guided tours, not only prose
- **+** Dockerfile and docker-compose in the repo; MIT license
- **−** README no longer documents setup, ports or supported model providers
- **−** 2.0 is pushed as a separate download at grok-wiki.com
- **−** No hardware guidance; single-maintainer project

<sub>no GPU · Docker + Compose · [Repo](https://github.com/asyncfuncai/deepwiki-open) · [🌐 Site ↗](https://grok-wiki.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepwiki-open/)</sub>

<a name="txtai"></a>
### #&#8288;22 [txtai](https://github.com/neuml/txtai) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: niche (18) · Freshness: active (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Oct 2026</sub>

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

<sub>GPU optional · Needs Python 3.11+, Hugging Face Transformers, Sentence Transformers, FastAPI · Models: Hugging Face models, llama.cpp, LiteLLM (OpenAI, Claude, AWS Bedrock) · port 8000 · [Repo](https://github.com/neuml/txtai) · [📖 Docs ↗](https://neuml.github.io/txtai/) · [🌐 Site ↗](https://neuml.github.io/txtai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/txtai/)</sub>

<a name="morphik"></a>
### #&#8288;23 [Morphik](https://github.com/morphik-org/morphik-core) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: weak (26) · Easy to run: easy (50) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · custom license · Oct 2026</sub>

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

<a name="kotaemon"></a>
### #&#8288;24 [Kotaemon](https://github.com/cinnamon/kotaemon) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: popular (55) · Freshness: active (88) · Maintenance: weak (3) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · Apache-2.0 · May 2026</sub>

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

<a name="langchain-chatchat"></a>
### #&#8288;25 [langchain-chatchat](https://github.com/chatchat-space/langchain-chatchat) <sub>score [34](../README.md#-how-we-rank "Score 34/100. Adoption: popular (71) · Freshness: quiet (7) · Maintenance: weak (15) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · Apache-2.0 · Nov 2025</sub>

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
### #&#8288;26 [Paperless-AI](https://github.com/clusterzx/paperless-ai) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: niche (12) · Freshness: recent (59) · Maintenance: weak (18) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · MIT · Mar 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
