# 📚 RAG, knowledge and search reviews · Best of Open-Source AI

Document Q&A, knowledge bases and private search over your own files and the web, with queries kept on your host. Back to the [leaderboard](../README.md#-rag-knowledge-and-search).

<sub>🌐 Also on the web: [RAG, knowledge and search on archestack.com](https://archestack.com/best-of-ai/rag-knowledge/), each project on its own page.</sub>

<a name="open-notebook"></a>
### 🥇 [Open Notebook](https://github.com/lfnovo/open-notebook) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 42k · MIT · Nov 2026</sub>

**Self-hosted NotebookLM alternative for research notebooks, chat, and podcasts.**

Open Notebook organizes PDFs, videos, audio, web pages and Office docs into notebooks, with full-text and vector search, cited chat, notes and custom transformations. It also generates podcasts with 1-4 speakers. It runs as a Next.js UI plus FastAPI backend on SurrealDB, and connects to 20+ providers or local servers such as Ollama and LM Studio.

- **+** 20+ providers plus Ollama and OpenAI-compatible servers, configured in the UI
- **+** Podcast generation with 1-4 speakers and custom episode profiles
- **+** Full REST API on port 5055 and MCP integration docs
- **+** Answers cite the sources, notes and insights they used
- **−** No password by default; UI and API bind to all interfaces
- **−** Multi-user support is only a direction under consideration, not shipped
- **−** Needs a separate SurrealDB container alongside the app
- **−** Anthropic and Groq lack embedding models, so a second provider is required

<sub>GPU optional · Docker + Compose · Needs SurrealDB, Docker Compose, LLM provider API key or Ollama · Models: OpenAI, Anthropic, Google, Mistral, Groq · port 8502 · README: alternative to NotebookLM · [Repo](https://github.com/lfnovo/open-notebook) · [🌐 Site ↗](https://www.open-notebook.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-notebook/)</sub>

<a name="lightrag"></a>
### 🥈 [LightRAG](https://github.com/hkuds/lightrag) <sub>score [91](../README.md#-how-we-rank "Score 91/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · MIT · Nov 2026</sub>

**Graph-based RAG framework with a REST server and WebUI.**

LightRAG indexes documents into both a knowledge graph and vector embeddings, then answers queries with dual-level retrieval over entities and concepts. It ships as a Python library and as lightrag-server, which provides a REST API and a WebUI for inserting, querying and visualizing the graph. Storage defaults to local files, with PostgreSQL, Neo4j, MongoDB and OpenSearch as options.

- **+** Runs with local file storage by default; no database required
- **+** Pluggable backends: PostgreSQL, Neo4j, MongoDB, OpenSearch, any OpenAI-compatible LLM
- **+** Optional reranker, citations, document deletion with KG regeneration, RAGAS and Langfuse
- **+** Separate LLM settings for extraction, query, keywords and VLM roles
- **−** Entity extraction makes one LLM call per chunk, raising indexing time and cost
- **−** Server binds 0.0.0.0 with authentication off by default
- **−** Changing the embedding model requires re-indexing every document
- **−** Source install needs bun to build the WebUI; PyPI package avoids this

<sub>no GPU · Docker + Compose · Needs OpenAI-compatible LLM and embedding API, Optional: PostgreSQL, Neo4j, MongoDB, OpenSearch, Milvus, Optional: MinerU or Docling for multimodal parsing · Models: OpenAI-compatible APIs, Open-source LLMs such as Qwen3-30B-A3B · port 9621 · [Repo](https://github.com/hkuds/lightrag) · [📖 Docs ↗](https://github.com/HKUDS/LightRAG/blob/main/docs/ExploreLightRAG.md) · [🌐 Site ↗](https://github.com/HKUDS/LightRAG) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lightrag/)</sub>

<a name="ragflow"></a>
### 🥉 [RAGFlow](https://github.com/infiniflow/ragflow) <sub>score [90](../README.md#-how-we-rank "Score 90/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 94k · Apache-2.0 · Nov 2026</sub>

**RAG engine with document parsing, agentic retrieval and citations.**

RAGFlow ingests Word, PowerPoint, Excel, PDFs, scans, images and web pages, chunks them with selectable templates, and answers questions with traceable citations. It adds multi-step agentic retrieval with Low to Ultra thinking modes and knowledge compilation into wikis, graphs and mind maps. It runs as Go services (Admin, Ingestor, Syncer, API) with a React web UI, deployed through Docker Compose.

- **+** Template-based chunking with visualization so humans can inspect and edit chunks
- **+** Citations trace answers back to source chunks
- **+** Agentic retrieval with four thinking modes for multi-step questions
- **+** Handles scanned files, Office formats and PDFs; DeepDoc runs on CPU
- **−** Many services to run: MySQL, MinIO, NATS, Kvrocks and a document engine
- **−** Recommended start is 4 cores, 16 GB RAM and 50 GB disk
- **−** macOS is not currently supported for the Docker image
- **−** Source build needs Go 1.27, Clang 20, CMake 4 and native libraries

<sub>RAM ≥ 16 GB · no GPU · Docker + Compose · Needs Docker, MySQL, MinIO, NATS, Kvrocks, Elasticsearch or Infinity · Models: Configurable LLM, embedding and reranker models via provider page · port 80 · [Repo](https://github.com/infiniflow/ragflow) · [▶️ Demo ↗](https://cloud.ragflow.io) · [📖 Docs ↗](https://ragflow.io/docs/dev/) · [🌐 Site ↗](https://ragflow.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ragflow/)</sub>

<a name="deeptutor"></a>
### #&#8288;4 [deeptutor](https://github.com/hkuds/deeptutor) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 59k · Apache-2.0 · Nov 2026</sub>

**Tutoring workspace with knowledge bases, guided learning, memory and quizzes.**

DeepTutor is a Python tutoring application that builds a learning workspace around your documents. It offers knowledge bases with several retrieval engines (LightRAG, PageIndex, GraphRAG, FAISS), guided learning with mastery gates, quizzes, generated books and deep research. It also has layered memory, Partner agents reachable over IM channels, MCP services and a CLI. It runs from source, Docker Compose, or desktop installers for macOS and Windows.

- **+** Multiple retrieval backends (LightRAG, PageIndex, GraphRAG, FAISS) and several document parsing engines
- **+** Learning features beyond chat: mastery paths, question bank, quizzes, Anki and calendar export
- **+** Multi-user accounts with per-user isolation; Docker Compose and desktop installers available
- **+** Active releases, latest v1.7.2 on 2026-11-06
- **−** Very large feature surface; many settings to configure before it is useful
- **−** Fast release cadence, including a breaking front/back-end refactor in v1.6.3
- **−** Needs an external LLM and embedding provider; hardware sizing is not documented
- **−** Recent release notes describe desktop builds as previews

<sub>Docker + Compose · Needs LLM provider or local model endpoint, Embedding model provider · Models: OpenAI-compatible providers, Anthropic, Gemini, OpenAI Codex OAuth, NVIDIA NIM · [Repo](https://github.com/hkuds/deeptutor) · [📖 Docs ↗](https://deeptutor.info) · [🌐 Site ↗](https://deeptutor.info) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deeptutor/)</sub>

<a name="maxkb"></a>
### #&#8288;5 [MaxKB](https://github.com/1panel-dev/maxkb) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: popular (80) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · GPL-3.0 · Nov 2026</sub>

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

<a name="surfsense"></a>
### #&#8288;6 [SurfSense](https://github.com/modsetter/surfsense) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Nov 2026</sub>

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

<sub>GPU optional · Docker + Compose · Needs LibreOffice (optional, for Office conversion) · Models: OpenAI-compatible APIs, local models · README: alternative to NotebookLM · [Repo](https://github.com/modsetter/surfsense) · [🌐 Site ↗](https://www.surfsense.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/surfsense/)</sub>

<a name="quivr"></a>
### #&#8288;7 [quivr](https://github.com/the-vibe-company/quivr) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · MIT · Nov 2026</sub>

**Headless engine that stores, searches and alerts on incoming documents.**

Quivr 2 is a Go service that ingests documents (articles, emails, posts, PDFs) sent to its HTTP API or pulled from RSS, Microsoft 365 mailboxes and X lists. It keeps every version in PostgreSQL and object storage, offers keyword and semantic search with passage-level citations, and matches new documents against saved alerts, delivered by read API or signed webhooks. It has no UI of its own; `quivr mcp` exposes search to agents.

- **+** Keeps every document version; withdrawn documents leave search at once and alerts are told
- **+** Results cite the exact passage, document and version
- **+** Formats, sources, embeddings, ranking and alerts are HTTP plugins in any language
- **+** /v0 API stays compatible across 2.x releases
- **−** No user interface; the web demo is a separate app on the public API
- **−** Local setup needs Docker Compose v2, Go, Python 3.12, jq and about 1 GB download
- **−** Not a document chat tool; the application layer is yours to build
- **−** Local dev stack supports only Linux x86_64 and Apple Silicon Macs

<sub>Docker + Compose · Needs PostgreSQL, Object storage, Docker Compose · Models: Pluggable embedding models · [Repo](https://github.com/the-vibe-company/quivr) · [📖 Docs ↗](https://docs.quivr.thevibecompany.co) · [🌐 Site ↗](https://www.thevibecompany.co) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/quivr/)</sub>

<a name="gpt-researcher"></a>
### #&#8288;8 [GPT Researcher](https://github.com/assafelovic/gpt-researcher) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · Apache-2.0 · Nov 2026</sub>

**Research agent that writes cited reports from web and local documents.**

GPT Researcher uses a planner agent to split a query into research questions, then execution agents scrape sources in parallel and a publisher assembles a cited report. It runs as a FastAPI server with a static or Next.js frontend, as a pip package, or as a LangGraph/AG2 multi-agent workflow. It can also research local files and connect to MCP data sources.

- **+** Works on web sources and local PDF, Word, Excel, CSV, PowerPoint and Markdown files
- **+** Usable as a web app, a pip package, or a Claude skill
- **+** Recursive deep research mode with configurable depth and breadth, about $0.4 per run
- **+** Context filter falls back to local BM25 keyword ranking when no key is set
- **−** Needs an LLM API key and a search key such as Tavily; no offline setup documented
- **−** Default context filter (Jev) is a hosted service requiring TYPESAFE_API_KEY
- **−** Deep research takes about 5 minutes per run
- **−** Non-Docker install requires Python 3.12 or later

<sub>no GPU · Docker + Compose · Needs OpenAI API key, Tavily API key, TypeSafe API key (optional, Jev filter), Google API key (optional, image generation), LangSmith (optional) · Models: OpenAI, OpenAI-compatible APIs via OPENAI_BASE_URL, Google Gemini · port 8000 · [Repo](https://github.com/assafelovic/gpt-researcher) · [📖 Docs ↗](https://docs.gptr.dev) · [🌐 Site ↗](https://gptr.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gpt-researcher/)</sub>

<a name="pageindex"></a>
### #&#8288;9 [pageindex](https://github.com/vectifyai/pageindex) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · MIT · Nov 2026</sub>

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

<a name="wrenai"></a>
### #&#8288;10 [wrenai](https://github.com/canner/wrenai) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · custom license · Nov 2026</sub>

**Semantic layer and context engine that lets agents write governed SQL.**

WrenAI is a CLI and Python SDK (pip install wrenai) that gives agents such as Claude Code, Cursor and LangChain a semantic layer written in MDL, plus Git-versioned YAML and Markdown context. Agents generate SQL planned against that layer, validated by dry-plan, and run on an Apache DataFusion engine across 22+ data sources. The earlier Docker chat-style GenBI app is archived on a legacy branch.

- **+** Business definitions are YAML and Markdown in Git, reviewable as pull-request diffs
- **+** Dry-plan validation, row limits and structured errors constrain agent-written SQL
- **+** Connects 22+ sources, including BigQuery, Snowflake, PostgreSQL, ClickHouse and DuckDB
- **+** Ships LangChain and Pydantic AI SDKs, an MCP server and agent skills
- **−** GenBI UI, dashboards, row/column security and user groups are commercial only
- **−** Docker chat BI app moved to legacy/v1 with no new features or security fixes
- **−** Needs an external agent or LLM client; it is not a standalone chat UI
- **−** Detected license is NOASSERTION, though the README states Apache 2.0

<sub>Needs Python (pip), A supported data source such as Postgres, BigQuery or Snowflake, An AI agent such as Claude Code or Cursor · Models: Agent-agnostic: Claude Code, Cursor, Cline, Codex, MCP clients, LangChain · [Repo](https://github.com/canner/wrenai) · [📖 Docs ↗](https://docs.getwren.ai) · [🌐 Site ↗](https://getwren.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/wrenai/)</sub>

<a name="morphic"></a>
### #&#8288;11 [Morphic](https://github.com/miurla/morphic) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.3k · Apache-2.0 · Nov 2026</sub>

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

<a name="weknora"></a>
### #&#8288;12 [WeKnora](https://github.com/tencent/weknora) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · custom license · Nov 2026</sub>

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

<a name="rag-anything"></a>
### #&#8288;13 [rag-anything](https://github.com/hkuds/rag-anything) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · MIT · Nov 2026</sub>

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
### #&#8288;14 [docsgpt](https://github.com/arc53/docsgpt) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · MIT · Nov 2026</sub>

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

<a name="txtai"></a>
### #&#8288;15 [txtai](https://github.com/neuml/txtai) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Nov 2026</sub>

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

<a name="graphrag"></a>
### #&#8288;16 [graphrag](https://github.com/microsoft/graphrag) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · MIT · Nov 2026</sub>

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

<a name="local-deep-research"></a>
### #&#8288;17 [Local Deep Research](https://github.com/learningcircuit/local-deep-research) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.6k · MIT · Nov 2026</sub>

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

<a name="private-gpt"></a>
### #&#8288;18 [PrivateGPT](https://github.com/zylon-ai/private-gpt) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 58k · Apache-2.0 · Nov 2026</sub>

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

<a name="niubigeo"></a>
### #&#8288;19 [niubigeo](https://github.com/albert-weasker/niubigeo) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Nov 2026</sub>

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

<a name="aihot"></a>
### #&#8288;20 [aihot](https://github.com/kkkkhazix/aihot) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (60) · Freshness: active (100) · Maintenance: fair (66) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Nov 2026</sub>

**Self-hosted site that scores, clusters and summarizes news feeds into daily digests.**

Engine behind aihot.news. It ingests RSS, web lists, JSON APIs, X accounts and WeChat accounts, pre-filters with an LLM, scores each item twice, and writes Chinese titles and summaries. Reports of the same event are clustered and ranked by heat, and daily, weekly and monthly editions are compiled. Prompts and thresholds are editable files, so the site can be retargeted to another industry.

- **+** Selection and writing prompts and admission thresholds are published and editable without code changes
- **+** Event clustering with per-source heat scoring, so repeated coverage from one outlet counts once
- **+** Exposes RSS, public API, MCP, llms.txt and an /agent page for agent consumers
- **+** Admin panel with source test-fetch, per-step model choice, budget cutoff and a calibration script
- **−** Synced from the live site, not a polished generic framework; upstream sync not guaranteed
- **−** Needs an OpenAI-compatible LLM API key, so token costs recur
- **−** Ships only 18 demo overseas AI sources; you must build your own source list
- **−** Default output and docs are Chinese-oriented; AI-specific features stay on aihot.news only

<sub>no GPU · Docker + Compose · Needs PostgreSQL 17, Node.js 24, Docker Compose, OpenAI-compatible LLM API · Models: OpenAI-compatible APIs (DeepSeek, Qwen, Zhipu) · port 3000 · [Repo](https://github.com/kkkkhazix/aihot) · [🌐 Site ↗](https://aihot.news) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/aihot/)</sub>

<a name="pandawiki"></a>
### #&#8288;21 [pandawiki](https://github.com/chaitin/pandawiki) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · AGPL-3.0 · Nov 2026</sub>

**Knowledge base and docs site builder with AI writing, Q&A and search.**

PandaWiki builds documentation sites, FAQs and blogs from an admin console, and adds AI-assisted writing, question answering and search over the stored documents. Content can be imported from a URL, sitemap, RSS or offline files, and a published site can be embedded as a web widget or connected to DingTalk, Feishu and WeCom bots. It installs on Linux through a shell script and needs an LLM configured before the AI features work.

- **+** Imports from web URL, sitemap, RSS and offline files
- **+** Exports to Word, PDF and Markdown; editor accepts Markdown and HTML
- **+** Creates a separate wiki site for each knowledge base
- **+** Web widget and DingTalk, Feishu, WeCom bot integrations
- **−** AI writing, Q&A and search do not work until a model is configured
- **−** Install is a curl-piped root shell script; no compose file is documented
- **−** README is Chinese only; English docs availability is unknown
- **−** AGPL-3.0 requires publishing source of modified network-served versions

<sub>no GPU · Needs Docker 20.x or newer, Linux server with root access, LLM provider (Baizhi Cloud model square suggested) · Models: unknown · port 2443 · [Repo](https://github.com/chaitin/pandawiki) · [📖 Docs ↗](https://pandawiki.docs.baizhi.cloud/node/01971602-bb4e-7c90-99df-6d3c38cfd6d5) · [🌐 Site ↗](https://ly.safepoint.cloud/Br48PoX) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pandawiki/)</sub>

<a name="utopia"></a>
### #&#8288;22 [utopia](https://github.com/deeplethe/utopia) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (50) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.7k · Apache-2.0 · Nov 2026</sub>

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

<a name="autorag"></a>
### #&#8288;23 [autorag](https://github.com/marker-inc-korea/autorag) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: known (37) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.7k · Apache-2.0 · Nov 2026</sub>

**Librarian agent that searches local files, mail and chats in place.**

AutoRAG Agent (@autorag/librarian, TypeScript, Node 24+ or Bun) is a single-model agent built on the Pi framework. It searches local files, mail, Slack, Telegram, Discord and KakaoTalk without copying them into a central vector database. It combines SPLADE sparse, local vector and hybrid retrieval through MinSync with direct file reads via bash, and returns answers with numbered citations. It ships a CLI, TUI, MCP server and TypeScript API; the original Python RAG AutoML tool now lives in legacy/.

- **+** Searches data in place across files, mail and chat apps, keeping source-native identities
- **+** Local embeddings (Qwen3-Embedding-0.6B via MinSync); no remote embedder unless configured
- **+** Surfaces: CLI, Pi-based TUI, MCP server, TypeScript API, Telegram/Discord/WhatsApp
- **+** Parses HWP/HWPX, PDF, DOCX and XLSX in-process, no Java needed
- **−** Desktop app is a separate repo under Fair Source FSL-1.1-MIT, not Apache-2.0
- **−** Needs a configured model provider or hosted plan; no bundled LLM
- **−** Downloads MinSync and filee-cli (~85 MB) on first run
- **−** SPLADE ranks exact identifiers among look-alike files less reliably than BM25

<sub>Needs Node.js >= 24 or Bun >= 1.2, MinSync, Pi coding agent, filee-cli, Jikji (optional, Rust), fsearch-cli (optional) · Models: Provider-configured LLMs via Pi, Qwen3-Embedding-0.6B (local embeddings), KURE-Sparse-nano (SPLADE) · [Repo](https://github.com/marker-inc-korea/autorag) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/autorag/)</sub>

<a name="db-gpt"></a>
### #&#8288;24 [DB-GPT](https://github.com/eosphoros-ai/db-gpt) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: fair (57) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · MIT · Nov 2026</sub>

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

<a name="ultrarag"></a>
### #&#8288;25 [ultrarag](https://github.com/openbmb/ultrarag) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (37) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.7k · Apache-2.0 · Nov 2026</sub>

**MCP-based RAG framework with YAML pipelines and a visual pipeline builder.**

UltraRAG splits RAG components such as retriever and generation into independent MCP servers, and an MCP client orchestrates them from YAML files with sequence, loop and conditional-branch control. It includes a web UI for building pipelines on a canvas or in code, managing knowledge bases, and turning a pipeline into a chat interface, plus built-in evaluation workflows and benchmark datasets for research.

- **+** Loops and conditional branches in RAG pipelines are defined in YAML, not Python
- **+** Each component is an MCP server, so new tools register at function level
- **+** Built-in evaluation workflows and public benchmark datasets for reproducible RAG experiments
- **+** Pipeline Builder syncs canvas and code editing, and exports a pipeline as a chat UI
- **−** Aimed at research and prototyping; production hardening is not documented in the README
- **−** Full install pins Linux GPU dependencies to CUDA 12.9 with vLLM
- **−** Docker latest tags are moving nightly builds; pinning a digest is needed for reproducibility
- **−** Some docs, such as the debugging guide, are Chinese-only

<sub>GPU optional · Docker · Needs uv, Milvus, Docker, NVIDIA Container Toolkit · Models: vLLM, AgentCPM-Report, MiniCPM-Embedding-Light · port 5050 · [Repo](https://github.com/openbmb/ultrarag) · [📖 Docs ↗](https://ultrarag.openbmb.cn/pages/en/getting_started/introduction) · [🌐 Site ↗](https://ultrarag.github.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ultrarag/)</sub>

<a name="pipeshub"></a>
### #&#8288;26 [PipesHub](https://github.com/pipeshub-ai/pipeshub-ai) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.1k · Apache-2.0 · Nov 2026</sub>

**Permission-aware search and cited answers across Slack, Drive, GitHub and 50+ systems.**

PipesHub indexes content from 50+ business systems such as Slack, Google Drive, GitHub, Microsoft 365 and Notion. It answers questions with block-level citations, filtered by each user's source-system permissions. The same context is exposed to your own agents through an MCP server, Python, TypeScript and Go SDKs, and a no-code agent builder.

- **+** Answers carry block-level citations to the original documents
- **+** Access checks follow source-system permissions per user, resolved at query time
- **+** 50+ connectors with real-time and scheduled indexing
- **+** MCP server plus Python, TypeScript and Go SDKs; any LLM provider or Ollama
- **−** Stack needs Neo4j or ArangoDB, Qdrant, MongoDB and Redis, plus Kafka at larger scale
- **−** Audio and video can be stored but are not indexed yet
- **−** Hosted PipesHub Cloud is only a waitlist

<sub>GPU optional · Docker + Compose · Needs Docker Compose v2, Neo4j or ArangoDB, Qdrant, MongoDB, Redis, Kafka (larger deployments) · Models: any LLM provider, Ollama, local embedding server, multimodal LLM for scanned PDF OCR · port 3000 · [Repo](https://github.com/pipeshub-ai/pipeshub-ai) · [▶️ Demo ↗](https://youtu.be/VgyND38QZ7w) · [📖 Docs ↗](https://docs.pipeshub.com/) · [🌐 Site ↗](https://www.pipeshub.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pipeshub/)</sub>

<a name="horizon"></a>
### #&#8288;27 [horizon](https://github.com/thysrael/horizon) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: fair (64) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Nov 2026</sub>

**Daily AI-curated news briefings from RSS, Hacker News, Reddit and more.**

Horizon pulls items from RSS, Hacker News, Reddit, Telegram, X, GitHub and other sources, then scores, deduplicates and summarizes them with an LLM using configurable profiles. It writes English and Chinese Markdown briefings and publishes them to GitHub Pages or sends them by email, webhook or WeChat. It runs as a Python CLI, with an MCP server and an agent skill for driving it from an assistant.

- **+** Profiles set per-source scoring rubrics, thresholds and output format, usually without code changes
- **+** Ten source types, including HN, Reddit, Telegram, GitHub, GDELT and Google News
- **+** Delivers via Markdown, GitHub Pages, email, webhooks (Feishu, Slack, Discord) and WeChat
- **+** Exposes pipeline stages through an MCP server and an installable agent skill
- **−** Needs an LLM provider key or ChatGPT sign-in; Ollama appears only as a badge
- **−** Twitter/X source depends on Apify and a Playwright setup the Dockerfile lacks
- **−** Batch CLI run on a schedule, not a persistent app with search over past items
- **−** No tagged releases

<sub>no GPU · Docker + Compose · Needs LLM provider API key (OpenAI, Gemini, etc.), uv or pip, SMTP/IMAP for email delivery (optional), Apify for X source (optional) · Models: OpenAI, Gemini, Claude, DeepSeek, Doubao · [Repo](https://github.com/thysrael/horizon) · [▶️ Demo ↗](https://thysrael.github.io/Horizon/) · [📖 Docs ↗](https://thysrael.github.io/Horizon/configuration) · [🌐 Site ↗](https://www.horizon1123.top/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/horizon/)</sub>

<a name="pixelrag"></a>
### #&#8288;28 [pixelrag](https://github.com/startrail-org/pixelrag) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: fair (54) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Nov 2026</sub>

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

<a name="hyper-extract"></a>
### #&#8288;29 [hyper-extract](https://github.com/yifanfeng97/hyper-extract) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.2k · custom license · Nov 2026</sub>

**CLI that extracts knowledge graphs from documents using LLMs and YAML templates.**

Hyper-Extract is a Python CLI (`he`) and library that parses documents such as PDF, Word, HTML and Markdown into structured knowledge: lists, graphs, hypergraphs and temporal or spatial graphs. It ships 80+ YAML templates and several extraction methods, including GraphRAG, LightRAG and KG-Gen. Results can be searched, visualized, exported to Obsidian, or exposed over an MCP server.

- **+** 80+ YAML templates across finance, legal, medical and general domains need no code
- **+** Incremental feed with per-source provenance, rollback and re-feed of updated documents
- **+** Works with OpenAI, Anthropic, Gemini, DeepSeek, Bailian or local vLLM endpoints
- **+** Exports to Obsidian, GraphML, CSV, JSON-LD and Cypher; includes an MCP server
- **−** Requires a model with tool/function calling; extraction quality depends on that model
- **−** Anthropic, Gemini and DeepSeek have no embeddings path, so a second embedder is needed
- **−** PDF, Word and other non-text formats need the optional ingest extra
- **−** Hosted APIs bill per page extracted; local vLLM use needs a GPU

<sub>GPU optional · Needs LLM provider API or local vLLM, OpenAI-compatible embedding endpoint, uv or pipx · Models: OpenAI, Anthropic, Google Gemini, DeepSeek, Alibaba Bailian · [Repo](https://github.com/yifanfeng97/hyper-extract) · [📖 Docs ↗](https://yifanfeng97.github.io/Hyper-Extract/latest/) · [🌐 Site ↗](https://yifanfeng97.github.io/Hyper-Extract/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hyper-extract/)</sub>

<a name="opendeepwiki"></a>
### #&#8288;30 [opendeepwiki](https://github.com/aidotnet/opendeepwiki) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · MIT · Oct 2026</sub>

**Generates wiki-style docs and chat for Git repos, with per-repo MCP endpoints.**

OpenDeepWiki ingests Git URLs, ZIP archives or local directories and uses configured LLMs to generate READMEs, wiki catalogs, document pages, translations and mind maps. The ASP.NET Core (.NET 10) backend and Next.js 16 frontend publish the result as a public site and reuse it for a chat assistant, embedded chat and repository-scoped MCP endpoints. An admin console manages users, roles, API keys and AI providers.

- **+** Accepts Git URLs, ZIP uploads and approved local directories as sources
- **+** Per-repo MCP endpoints at /api/mcp/{owner}/{repo}
- **+** Separate model bindings for catalog, content and translation; translation falls back to content model
- **+** SQLite by default, PostgreSQL supported via compose.pgsql.yaml
- **−** Needs an external LLM API key; local model setup is not documented beyond optional Graphify Ollama
- **−** Seeded default admin credentials must be changed manually before real use
- **−** Several moving parts: .NET backend, Next.js web app, background workers
- **−** Enterprise support and pricing exist; the split with the MIT edition is unclear

<sub>no GPU · Compose · Needs LLM API (OpenAI-compatible endpoint), SQLite or PostgreSQL, Docker Compose · Models: OpenAI-compatible APIs, Ollama (Graphify only) · port 3000 · [Repo](https://github.com/aidotnet/opendeepwiki) · [🌐 Site ↗](https://docs.opendeep.wiki/pricing) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/opendeepwiki/)</sub>

<a name="paperless-gpt"></a>
### #&#8288;31 [paperless-gpt](https://github.com/icereed/paperless-gpt) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.8k · MIT · Oct 2026</sub>

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

<a name="deepwiki-open"></a>
### #&#8288;32 [DeepWiki-Open](https://github.com/asyncfuncai/deepwiki-open) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: patchy (34) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · MIT · Nov 2026</sub>

**Generates browsable wikis with diagrams from Git repositories.**

DeepWiki-Open takes a GitHub, GitLab or Bitbucket repository, analyzes the code structure, and generates documentation, diagrams and a navigable wiki, plus a codemap for guided tours. The README documents a Helm chart that runs the published ghcr.io image, reads provider keys (Google, OpenAI) from a Secret and keeps ~/.adalflow on a PVC.

- **+** Accepts GitHub, GitLab and Bitbucket repositories as input
- **+** Produces diagrams and a codemap, not only text documentation
- **+** Helm chart and published container image for Kubernetes
- **+** MIT licensed, with Docker and Compose files included
- **−** README gives no local setup steps beyond the Helm chart
- **−** Helm example needs external provider API keys (Google, OpenAI)
- **−** README lists no supported models or hardware requirements
- **−** README points to a separate 2.0 version at grok-wiki.com

<sub>Docker + Compose · Needs GOOGLE_API_KEY, OPENAI_API_KEY, Kubernetes (optional, Helm) · Models: Google, OpenAI · port 3000 · [Repo](https://github.com/asyncfuncai/deepwiki-open) · [🌐 Site ↗](https://grok-wiki.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepwiki-open/)</sub>

<a name="llmware"></a>
### #&#8288;33 [llmware](https://github.com/llmware-ai/llmware) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: patchy (40) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · Apache-2.0 · Oct 2026</sub>

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

<a name="audiomuse-ai"></a>
### #&#8288;34 [audiomuse-ai](https://github.com/neptunehub/audiomuse-ai) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · AGPL-3.0 · Nov 2026</sub>

**Self-hosted sonic analysis and playlist generation for Navidrome, Jellyfin and Plex.**

AudioMuse-AI analyzes the audio in your music library on your own server and uses the results for clustering, similarity playlists, a 2D music map, and text, lyrics and 20-second recording search. It connects to Navidrome, Jellyfin, LMS, Lyrion, Emby and Plex, including several at once with cross-server duplicate detection. It runs as Flask and worker containers on PostgreSQL 15, or as native packages for macOS, Linux and Windows.

- **+** Supports Navidrome, Jellyfin, LMS, Lyrion, Emby and Plex, several servers in one deployment
- **+** Analysis runs locally without metadata or external APIs; no ads or paywalls
- **+** Native packages bundle embedded PostgreSQL, web UI and workers; no Docker needed
- **+** Swagger API docs at /apidocs/ and AMD64/ARM64 images, with NVIDIA GPU variants
- **−** Requires PostgreSQL v15; other versions may cause errors
- **−** Needs AVX2 CPU; VMs must pass through host CPU, noavx2 images are experimental
- **−** Native apps are unsigned; macOS build is Apple Silicon only, Windows x86_64 only
- **−** Major or minor releases can require re-running the full library analysis

<sub>RAM ≥ 8 GB · GPU optional · Docker + Compose · Needs PostgreSQL 15, Navidrome, Jellyfin, LMS, Lyrion, Emby or Plex server · port 8000 · [Repo](https://github.com/neptunehub/audiomuse-ai) · [📖 Docs ↗](https://github.com/NeptuneHub/AudioMuse-AI/tree/main/docs) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/audiomuse-ai/)</sub>

<a name="knowhere"></a>
### #&#8288;35 [knowhere](https://github.com/ontos-ai/knowhere) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.0k · Apache-2.0 · Nov 2026</sub>

**Document parsing and retrieval backend that builds navigable memory for agents.**

Knowhere ingests PDFs, slides, Office files, images and audio, then builds hierarchy-aware chunks, a cross-document entity graph and page-grounded citations. PDF and PowerPoint go through vision-model parsing, other formats are parsed natively, and agents query the result through built-in retrieval, MCP or a REST tools endpoint. It is a Python API plus worker that needs Postgres, Redis and S3-compatible storage.

- **+** Progressive ingestion makes documents searchable before background enrichment finishes
- **+** Citations keep source document, section path, page number and rendered page image
- **+** External agents can call the same corpus tools via MCP or POST /v2/retrieval/tools/invoke
- **+** Model-agnostic: DeepSeek, OpenAI, Qwen, GLM or any compatible provider
- **−** Setup needs Postgres, Redis, S3-compatible storage and several external API keys
- **−** PDF and PowerPoint parsing depends on a vision-capable model provider
- **−** Anonymous PostHog telemetry is on by default in self-hosted installs
- **−** Benchmark figures come from an internal evaluation, not independent runs

<sub>Docker + Compose · Needs PostgreSQL, Redis, S3-compatible storage, LLM provider API key, Vision-capable model provider, VERCEL_KEY for embeddings, uv · Models: DeepSeek, OpenAI, Qwen, GLM, Volcengine · port 5005 · [Repo](https://github.com/ontos-ai/knowhere) · [📖 Docs ↗](https://docs.knowhereto.ai/) · [🌐 Site ↗](https://knowhereto.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/knowhere/)</sub>

<a name="localgpt"></a>
### #&#8288;36 [localgpt](https://github.com/promtengineer/localgpt) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: weak (26) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Aug 2026</sub>

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

<a name="paperless-ai"></a>
### #&#8288;37 [Paperless-AI](https://github.com/clusterzx/paperless-ai) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: known (39) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · MIT · Nov 2026</sub>

**AI metadata tagging and archive Q&A extension for Paperless-ngx.**

Paperless-AI is a Node.js (TypeScript) service that connects to Paperless-ngx 2.x and 3.x and fills in title, tags, correspondent, document type, date and custom fields using an LLM. It also provides "Ask your archive", a hybrid BM25 plus vector search with streamed, cited answers. Providers include OpenAI, Anthropic, Ollama, Azure OpenAI and OpenAI-compatible APIs.

- **+** Runs as one Node.js process; README cites ~135 MB image and 80–150 MB idle RAM
- **+** Works fully local with Ollama and a built-in offline CPU embedding model
- **+** History with undo restores original values in Paperless; settings apply without restart
- **+** Webhook from a Paperless workflow triggers processing on document add
- **−** Only works with Paperless-ngx; not a general document search tool
- **−** Versions before 4.0 had an unauthenticated setup wizard that is being exploited
- **−** Local embedding model needs ~0.5 GB RAM while indexing and a ~120 MB first download
- **−** Upgrading from 3.x on an exposed instance may require a fresh data volume

<sub>GPU optional · Docker + Compose · Needs Paperless-ngx, Docker, Ollama or a cloud LLM API · Models: OpenAI, Anthropic, Ollama, Azure OpenAI, OpenAI-compatible APIs · port 3000 · [Repo](https://github.com/clusterzx/paperless-ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paperless-ai/)</sub>

<a name="flashrag"></a>
### #&#8288;38 [flashrag](https://github.com/ruc-nlpir/flashrag) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.6k · MIT · Oct 2026</sub>

**Python toolkit for reproducing and building RAG pipelines on benchmarks.**

FlashRAG is a Python library for RAG research. It provides retrievers, rerankers, generators and compressors that can be assembled into pipelines, with 36 pre-processed benchmark datasets and 23 implemented RAG algorithms, 7 of them reasoning-based. It includes index-building scripts for Faiss, BM25s, Pyserini and SPLADE (Seismic), plus a UI for configuring and evaluating methods.

- **+** 36 pre-processed RAG benchmark datasets and 23 algorithms with reported results
- **+** Dense (Faiss), BM25 (bm25s or Pyserini) and SPLADE retrieval via Seismic
- **+** Custom pipelines by subclassing BasicPipeline, configured through YAML or dict
- **+** Optional vLLM for faster generation; multimodal RAG and OpenAI generators supported
- **−** Research-oriented; not a ready-made document Q&A app for end users
- **−** Faiss has to be installed through conda because the pip package is incompatible
- **−** faiss-gpu is Linux x86_64 only; latest Faiss unavailable on some systems
- **−** Roadmap still lists API-based retriever (vLLM server) support as not done

<sub>GPU optional · Needs Faiss, PyTorch, vLLM (optional), Pyserini or bm25s, sentence-transformers (optional), Serper API key (web search retriever) · Models: OpenAI models, vLLM, FastChat, Hugging Face embedding models (E5, BGE), Llava, Qwen, InternVL (multimodal) · [Repo](https://github.com/ruc-nlpir/flashrag) · [📖 Docs ↗](https://ruc-nlpir.github.io/FlashRAG/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/flashrag/)</sub>

<a name="vane"></a>
### #&#8288;39 [Vane](https://github.com/itzcrazykns/vane) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: widely used (89) · Freshness: active (97) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · MIT · Sep 2026</sub>

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

<a name="llm-for-zotero"></a>
### #&#8288;40 [llm-for-zotero](https://github.com/yilewang/llm-for-zotero) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (14) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.6k · AGPL-3.0 · Nov 2026</sub>

**Zotero plugin for chatting with papers and running an agent over your library.**

A Zotero add-on (.xpi) that adds an LLM sidebar to the PDF reader for Q&A with citations that jump to the source passage, figure screenshots, and multi-paper comparison. An optional Agent Mode searches and edits the library (tags, metadata, imports, notes) with confirmation and undo. Backends include API providers, local OpenAI-compatible models, ChatGPT WebChat, Codex App Server and Claude Code.

- **+** Citations in answers jump to the matching passage in the Zotero PDF reader
- **+** Agent write actions use confirmation cards and can be undone from the conversation
- **+** Saves notes to Zotero or local Markdown folders such as Obsidian and Logseq
- **+** Supports responses_api, openai_chat_compat, anthropic_messages and gemini_native protocols
- **−** Agent Mode is labelled beta and is disabled by default
- **−** Web search requires a separate Tavily key
- **−** Works only inside Zotero; no standalone web or server deployment
- **−** AGPL-3.0 license may limit use in proprietary products

<sub>no GPU · Needs Zotero, LLM provider API key or local OpenAI-compatible server, Tavily API key (optional, web search), MinerU (optional, PDF parsing) · Models: OpenAI Responses API, OpenAI-compatible chat, Anthropic Messages, Gemini native, Codex App Server · [Repo](https://github.com/yilewang/llm-for-zotero) · [📖 Docs ↗](https://yilewang.github.io/llm-for-zotero) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llm-for-zotero/)</sub>

<a name="docling-serve"></a>
### #&#8288;41 [Docling Serve](https://github.com/docling-project/docling-serve) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (4) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · MIT · Oct 2026</sub>

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

<a name="morphik"></a>
### #&#8288;42 [Morphik](https://github.com/morphik-org/morphik-core) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: patchy (44) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · custom license · Oct 2026</sub>

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

<a name="papersgpt-for-zotero"></a>
### #&#8288;43 [papersgpt-for-zotero](https://github.com/papersgpt/papersgpt-for-zotero) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (9) · Freshness: active (100) · Maintenance: fair (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.7k · AGPL-3.0 · Nov 2026</sub>

**Zotero plugin for chatting with PDFs and searching your whole library.**

PapersGPT is a Zotero plugin (.xpi) that indexes PDFs locally and answers questions over a single paper, a selection, or the entire library, with click-to-jump citations. It adds Literature Radar for daily digests from arXiv, PubMed and other sources, AutoPilot for batch-reading collections into Zotero Notes, and an MCP server. Models can be 30+ cloud LLMs, built-in local models, Ollama, or any OpenAI-compatible endpoint.

- **+** Parsing, indexing and search run locally; local LLMs work fully offline
- **+** Benchmark: 10,000 PDFs indexed in about 7 minutes, 19.5 ms average query
- **+** Works with Ollama, custom OpenAI-compatible endpoints, or built-in Hugging Face local models
- **+** Exposes the Zotero library to Claude Desktop, Cursor and other clients via MCP
- **−** Tied to Zotero 7 to 10; unusable outside Zotero
- **−** README points to 'Professional' capabilities on the website, so free versus paid scope is unclear
- **−** Indexing 10,000 PDFs used 2.21 GB RSS and 901 MB of index
- **−** Download links in the README point to different versions (v2.1.0 and v2.2.0)

<sub>GPU optional · Needs Zotero 7+, Ollama (optional) · Models: OpenAI, Claude, Gemini, DeepSeek, Grok · [Repo](https://github.com/papersgpt/papersgpt-for-zotero) · [📖 Docs ↗](https://www.papersgpt.com/quickstart) · [🌐 Site ↗](https://www.papersgpt.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/papersgpt-for-zotero/)</sub>

<a name="pyserini"></a>
### #&#8288;44 [pyserini](https://github.com/castorini/pyserini) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: fair (71) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · Apache-2.0 · Nov 2026</sub>

**Python toolkit for reproducible sparse and dense retrieval research.**

Pyserini is a Python toolkit for first-stage retrieval in IR research. It wraps Anserini (Lucene) for BM25 and learned sparse models such as uniCOIL and SPLADE, and Faiss for dense models such as DPR, Contriever and BGE, with hybrid fusion. It ships prebuilt indexes, queries, relevance judgments and evaluation scripts for MS MARCO, BEIR and other collections, and offers a REST API and an MCP server.

- **+** Prebuilt indexes and two-click reproductions for MS MARCO, BEIR, BRIGHT, MIRACL and more
- **+** BM25, learned sparse, dense and hybrid retrieval behind one Python API
- **+** Can index your own corpus as BM25, sparse vector or dense vector indexes
- **+** Ships a REST API and MCP server, plus Index Reader, Analyzer and Query Builder APIs
- **−** Needs Java 21 and Python 3.12, with PyTorch and Faiss installed separately
- **−** Research-oriented first-stage retrieval; no built-in answer generation or chat UI
- **−** README notes dependency version mismatches as a source of install problems
- **−** Some prebuilt corpora are large, up to 72 GB for MS MARCO V2 doc uniCOIL

<sub>GPU optional · Needs Java 21, Anserini (Lucene 10.5.0), Faiss, PyTorch · Models: BM25, uniCOIL, SPLADE, DPR, Contriever · [Repo](https://github.com/castorini/pyserini) · [📖 Docs ↗](https://castorini.github.io/pyserini/2cr/beir.html) · [🌐 Site ↗](http://anserini.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pyserini/)</sub>

<a name="llm-wiki-agent"></a>
### #&#8288;45 [llm-wiki-agent](https://github.com/samuraigpt/llm-wiki-agent) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: patchy (32) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · MIT · Nov 2026</sub>

**Coding-agent skill that builds an interlinked markdown wiki from ingested documents.**

A set of schema files (CLAUDE.md, AGENTS.md, GEMINI.md) and Claude Code slash commands that make a coding agent ingest documents from raw/ into a markdown wiki with source, entity, concept and synthesis pages. It also lints for orphans and contradictions, and builds a vis.js graph.html from wikilinks plus agent-inferred edges. Non-markdown files are converted with markitdown.

- **+** Output is plain markdown in a git repo, browsable in Obsidian
- **+** Works with Claude Code, Codex, OpenCode and Gemini CLI via per-agent schema files
- **+** Flags contradictions at ingest and lints for orphans and broken links
- **+** Graph build is SHA256-cached and outputs a self-contained graph.html, no server
- **−** Requires a separate coding agent; the skill does nothing on its own
- **−** Standalone tools/ scripts need ANTHROPIC_API_KEY; no other provider is documented
- **−** Wiki quality depends on the agent's reading; no accuracy figures given
- **−** No published release and no multi-user or web UI

<sub>no GPU · Needs Claude Code, Codex, OpenCode or Gemini CLI, markitdown, NetworkX, ANTHROPIC_API_KEY (standalone tools/ scripts) · Models: Claude, Codex, Gemini CLI · [Repo](https://github.com/samuraigpt/llm-wiki-agent) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llm-wiki-agent/)</sub>

<a name="obsidian-smart-connections"></a>
### #&#8288;46 [obsidian-smart-connections](https://github.com/brianpetro/obsidian-smart-connections) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: known (35) · Freshness: active (100) · Maintenance: patchy (36) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · custom license · Oct 2026</sub>

**Obsidian plugin that finds related notes using local embeddings.**

Smart Connections is an Obsidian community plugin that indexes a vault with a bundled local embedding model and lists notes semantically related to the current one. It also has a Lookup view for semantic search, drag-to-link results, and a Send to Smart Context action that copies connected note content for use in any AI chat. Inline connections, configurable ranking and Bases integration are in paid Pro plugins.

- **+** Bundled local embedding model; no API key, extra app or CLI required
- **+** Embeddings are created locally by default, and it works offline
- **+** Works on Obsidian mobile as well as desktop
- **+** Connections view supports pinning, hiding and dragging results in as links
- **−** Inline and footer connections, ranking algorithms and Bases integration require paid Pro
- **−** Core is source-available, not a standard open-source license
- **−** Runs only inside Obsidian; not a standalone search tool
- **−** Semantic matching can omit notes that contain the exact query text

<sub>no GPU · Needs Obsidian · Models: bundled local embedding model · [Repo](https://github.com/brianpetro/obsidian-smart-connections) · [📖 Docs ↗](https://smartconnections.app/smart-connections/) · [🌐 Site ↗](https://smartconnections.app/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/obsidian-smart-connections/)</sub>

<a name="sentrysearch"></a>
### #&#8288;47 [sentrysearch](https://github.com/ssrajadh/sentrysearch) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: patchy (43) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.6k · Apache-2.0 · Oct 2026</sub>

**Semantic search over video footage that returns trimmed clips from text or image queries.**

SentrySearch splits videos into overlapping chunks, embeds them with Gemini, Alibaba DashScope, LiteLLM or a local Qwen3-VL-Embedding model, and stores vectors in a local ChromaDB. Text or image queries are matched against the chunks, and the top match is trimmed from the source file with ffmpeg. It also offers anomaly-based highlights, VLM reranking, and MLX support on Apple Silicon.

- **+** Several backends: Gemini, qwen-cloud, LiteLLM, local PyTorch, and MLX for Apple Silicon
- **+** Fully local option keeps footage on your machine; vectors stored in local ChromaDB
- **+** Auto-trims matching clips; supports image queries, reranking and anomaly highlights
- **+** Backend and model auto-detected from the index; separate indexes avoid mixing embeddings
- **−** Default Gemini backend sends video chunks to a cloud API and costs money
- **−** Requires Python 3.11 or 3.12; PyTorch wheels block 3.13+
- **−** Local backend is impractical on CPU-only or Intel Macs
- **−** MLX backend does not support --rerank; LiteLLM backend also lacks it

<sub>GPU optional · Needs ffmpeg, ChromaDB, uv, Gemini API (default backend) · Models: Gemini Embedding, Qwen3-VL-Embedding 2B/8B, qwen3-vl-embedding (DashScope), LiteLLM gateways, MLX 4-bit · [Repo](https://github.com/ssrajadh/sentrysearch) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sentrysearch/)</sub>

<a name="paper-qa"></a>
### #&#8288;48 [paper-qa](https://github.com/future-house/paper-qa) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.6k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;49 [Kotaemon](https://github.com/cinnamon/kotaemon) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: widely used (82) · Freshness: active (80) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · Apache-2.0 · May 2026</sub>

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
### #&#8288;50 [scira](https://github.com/zaidmukaddam/scira) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: popular (63) · Freshness: active (99) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · AGPL-3.0 · Aug 2026</sub>

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

<a name="ragent"></a>
### #&#8288;51 [ragent](https://github.com/nageoffer/ragent) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: patchy (36) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.5k · Apache-2.0 · Nov 2026</sub>

**Java Agentic RAG platform with hybrid retrieval, MCP tools and admin console.**

Ragent is a Spring Boot 4 and React 18 application for document ingestion and question answering, built as seven Maven modules. It has two paths: a fixed workflow (query rewrite, intent tree, multi-channel retrieval) and an AgentScope ReAct agent that uses retrieval, MCP tools and skills. It adds model failover, Redis request queuing, Langfuse tracing, and user and admin UIs, and is positioned as a source-level reference for Java developers.

- **+** Vector, keyword, graph and web retrieval run in parallel, merged with RRF and rerank
- **+** Model tiers with first-packet probing, three-state circuit breaker and candidate failover
- **+** Agent write actions can require user confirmation; tools discovered via MCP servers
- **+** Includes user chat UI, admin console, trace viewer and Langfuse integration
- **−** README is in Chinese and much of it targets interview and résumé preparation
- **−** No Docker or compose files detected; setup follows a separate local-dev guide
- **−** Needs several services (Redis, RocketMQ, vector store); versions not listed in README
- **−** Two parallel pipelines (v1 workflow, v2 agent) add code to learn

<sub>Needs Redis, RocketMQ, Langfuse, MCP servers, vector database, object storage · Models: Chat, Embedding, Rerank, VLM, MCP tools · [Repo](https://github.com/nageoffer/ragent) · [▶️ Demo ↗](https://nageoffer.com/ragent/demo/) · [📖 Docs ↗](https://nageoffer.com/ragent/local-dev/) · [🌐 Site ↗](https://nageoffer.com/ragent) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ragent/)</sub>

<a name="local-deep-researcher"></a>
### #&#8288;52 [local-deep-researcher](https://github.com/langchain-ai/local-deep-researcher) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.4k · MIT · Oct 2026</sub>

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
### #&#8288;53 [deep-searcher](https://github.com/zilliztech/deep-searcher) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: known (49) · Freshness: active (100) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.4k · Apache-2.0 · Sep 2026</sub>

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

<a name="bertopic"></a>
### #&#8288;54 [bertopic](https://github.com/maartengr/bertopic) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: known (46) · Freshness: active (86) · Maintenance: weak (23) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.0k · MIT · Aug 2026</sub>

**Python topic modeling library using transformer embeddings and c-TF-IDF.**

BERTopic is a Python library that groups documents into topics. By default it embeds text with sentence-transformers, reduces dimensions with UMAP, clusters with HDBSCAN, and extracts topic words with c-TF-IDF. Each step can be swapped. It also covers guided, supervised, dynamic, hierarchical, online, multimodal and zero-shot variants, plus optional LLM-generated topic labels.

- **+** Each pipeline stage (embedding, UMAP, HDBSCAN, vectorizer, representation) can be replaced or removed
- **+** Many variants in one API: guided, supervised, online, dynamic, hierarchical, multimodal, zero-shot
- **+** Built-in visualizations: topic map, hierarchy, heatmap, topics over time
- **+** Representation models include KeyBERTInspired and OpenAI-based topic labeling
- **−** Library only: no web UI or server, so you write Python
- **−** Default HDBSCAN puts many documents in outlier topic -1 that need extra handling
- **−** Default install pulls in transformers, UMAP and HDBSCAN; lightweight setup is separate

<sub>GPU optional · Needs sentence-transformers, UMAP, HDBSCAN, scikit-learn · Models: sentence-transformers, Flair, Gensim, spaCy, Universal Sentence Encoder · [Repo](https://github.com/maartengr/bertopic) · [📖 Docs ↗](https://maartengr.github.io/BERTopic/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/bertopic/)</sub>

<a name="trace-moe"></a>
### #&#8288;55 [trace.moe](https://github.com/soruly/trace.moe) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: known (31) · Freshness: active (100) · Maintenance: weak (20) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.0k · MIT · Sep 2026</sub>

**Reverse image search that identifies the anime, episode and timestamp of a screenshot.**

Index repo for the trace.moe system, which matches an anime screenshot to its title, episode and the moment it appears. Self-hosting uses a compose.yml that runs the web server and API server, with Postgres and Milvus storing hashes of your own video files. The repo itself is mostly a pointer to sub-repos (API, www, Telegram bot, MCP server, browser extension, image-vector library).

- **+** Returns anime, episode and exact timestamp for a screenshot
- **+** Compose file brings up web and API; scans VIDEO_PATH every minute for new files
- **+** Pre-hashed database dump available on Hugging Face to skip indexing
- **+** Separate API, Telegram bot and MCP server repos for integrations
- **−** This repo is an index page; code lives in separate repositories
- **−** Full pre-hashed dataset needs about 140GB RAM to load into memory
- **−** Loading hashes into Milvus may take 24 hours, optimization days more
- **−** Only .mp4, .mkv and .webm files indexed, organized by anilist ID folders

<sub>Compose · Needs Docker Compose, PostgreSQL, Milvus, zstd (for database dump) · Models: .mp4, .mkv, .webm · port 3000 · [Repo](https://github.com/soruly/trace.moe) · [▶️ Demo ↗](https://trace.moe) · [📖 Docs ↗](https://soruly.github.io/trace.moe-api/) · [🌐 Site ↗](https://trace.moe) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/trace-moe/)</sub>

<a name="deep-research"></a>
### #&#8288;56 [deep-research](https://github.com/dzhng/deep-research) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: popular (76) · Freshness: recent (54) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · MIT · Apr 2026</sub>

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

<a name="llm-graph-builder"></a>
### #&#8288;57 [llm-graph-builder](https://github.com/neo4j-labs/llm-graph-builder) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: known (34) · Freshness: active (100) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.3k · Apache-2.0 · Oct 2026</sub>

**Turns PDFs, web pages and videos into a Neo4j knowledge graph.**

A FastAPI backend and React frontend that ingest local files, S3 or GCS objects, YouTube, Wikipedia and web pages. An LLM called through LangChain extracts entities and relationships, which are written to Neo4j. It previews graphs in Bloom and offers chat over the graph with several retrieval modes. It is an experimental Neo4j Labs project, not a supported Neo4j product.

- **+** Ingests local files, S3, GCS, YouTube, Wikipedia and web pages into one graph
- **+** Chat modes include vector, graph, fulltext, entity_vector and global_vector, with source metadata
- **+** Custom node and relationship schema can be set before extraction
- **+** Extraction works with OpenAI, Gemini, Diffbot, Anthropic, Bedrock, Groq and Ollama
- **−** Experimental Neo4j Labs project, not part of Neo4j's supported products
- **−** Requires Neo4j 5.23+ with APOC; no other graph store
- **−** Docker Compose not supported with Neo4j Desktop; run backend and frontend separately
- **−** Most non-OpenAI providers are labelled dev deployed version

<sub>GPU optional · Compose · Needs Neo4j 5.23+ with APOC, LLM API key (OpenAI, Diffbot, etc.) or Ollama, YouTube transcript proxy key · Models: OpenAI, Gemini, Diffbot, Anthropic, Azure OpenAI · [Repo](https://github.com/neo4j-labs/llm-graph-builder) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llm-graph-builder/)</sub>

<a name="daily-arxiv-ai-enhanced"></a>
### #&#8288;58 [daily-arxiv-ai-enhanced](https://github.com/dw-dengwei/daily-arxiv-ai-enhanced) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.0k · custom license · Sep 2026</sub>

**Daily arXiv crawler that adds LLM-written summaries, hosted on GitHub Pages.**

A GitHub Actions workflow crawls arXiv daily (cs.CV, cs.GR, cs.CL, cs.AI, cs.CE, cs.GT, cs.IT, cs.LG by default) and summarizes each paper with DeepSeek in Chinese. Results are published as a static GitHub Pages site with keyword and author highlighting, date filtering, and preferences stored locally in the browser. Forks can change categories, model and language through repository variables.

- **+** Runs on GitHub Actions and Pages, so no server to host
- **+** Categories, model name and language set via repository variables
- **+** README states cost of about 0.2 CNY per day with DeepSeek
- **+** Optional ACCESS_PASSWORD secret to restrict who can view the page
- **−** Needs an OpenAI-compatible API key and base URL as repository secrets
- **−** Full workflow run can take about one hour
- **−** License is not a recognized SPDX type (NOASSERTION)
- **−** Default hosted site summarizes in Chinese only; other languages require a fork

<sub>no GPU · Needs GitHub Actions, GitHub Pages, OpenAI-compatible LLM API (e.g. DeepSeek), arXiv · Models: DeepSeek, OpenAI-compatible APIs · [Repo](https://github.com/dw-dengwei/daily-arxiv-ai-enhanced) · [▶️ Demo ↗](https://dw-dengwei.github.io/daily-arXiv-ai-enhanced/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/daily-arxiv-ai-enhanced/)</sub>

<a name="jamaibase"></a>
### #&#8288;59 [jamaibase](https://github.com/embeddedllm/jamaibase) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: niche (0) · Freshness: recent (70) · Maintenance: patchy (34) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.1k · Apache-2.0 · Oct 2026</sub>

**RAG backend with spreadsheet-style tables over SQLite and LanceDB.**

JamAI Base is a RAG backend that stores data in embedded SQLite and LanceDB and exposes it as spreadsheet-like tables, where columns can be filled by LLM prompts. It provides Generative, Action, Knowledge and Chat tables, with built-in embedding, reranking, query rewriting and hybrid search, reachable through a web UI and a REST API. It can be used on the hosted cloud or self-hosted.

- **+** Embedded SQLite and LanceDB, so no separate database server is listed
- **+** Built-in hybrid search, reranking and query rewriting without assembling a RAG pipeline
- **+** Spreadsheet-style UI plus a REST API
- **+** Supports multiple LLM providers, including OpenAI, Anthropic and Llama models
- **−** Self-hosting steps live in external docs; README has no Docker or compose instructions
- **−** Last release is 2025-02-13, while commits continue into 2026-10
- **−** Existing v1 installs need a migration to v2
- **−** Contributing guide link in the README is a placeholder

<sub>Docker + Compose · Needs SQLite, LanceDB · Models: OpenAI GPT-4, Anthropic Claude 3, Meta Llama 3, BGE M3 embeddings · [Repo](https://github.com/embeddedllm/jamaibase) · [▶️ Demo ↗](https://cloud.jamaibase.com/) · [📖 Docs ↗](https://docs.jamaibase.com) · [🌐 Site ↗](https://cloud.jamaibase.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/jamaibase/)</sub>

<a name="langchain-chatchat"></a>
### #&#8288;60 [langchain-chatchat](https://github.com/chatchat-space/langchain-chatchat) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: widely used (90) · Freshness: quiet (0) · Maintenance: weak (28) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · Apache-2.0 · Nov 2025</sub>

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

<a name="node-deepresearch"></a>
### #&#8288;61 [node-deepresearch](https://github.com/jina-ai/node-deepresearch) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: known (33) · Freshness: recent (70) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.2k · Apache-2.0 · Nov 2026</sub>

**Iterative web search, read and reason loop that returns short, cited answers.**

A TypeScript agent that loops through search, page reading and reasoning until it finds an answer or exhausts a token budget. It runs as a CLI or as an OpenAI-compatible server exposing /v1/chat/completions on port 3000, with streamed <think> blocks. Reasoning uses Gemini, OpenAI or a local OpenAI-style endpoint, and search and page reading go through Jina Reader.

- **+** OpenAI-compatible server works with clients such as CherryStudio and Chatbox
- **+** Supports Gemini, OpenAI and local endpoints such as Ollama or LMStudio
- **+** Token budget caps the loop, with a final-answer fallback called Beast Mode
- **+** Hosted UI and API run the same codebase, so you can test before installing
- **−** Search and page reading depend on the Jina Reader API and a Jina key
- **−** Local LLMs must handle structured output well; not every model works
- **−** Built for short answers, not long-form research reports
- **−** Last release was 2025-02-12, and the npm package is not recommended

<sub>no GPU · Docker + Compose · Needs Jina Reader API key, Gemini or OpenAI API key, or a local OpenAI-compatible LLM endpoint, Node.js · Models: Gemini (gemini-2.0-flash), OpenAI, Ollama / LMStudio via OpenAI-compatible endpoint (e.g. qwen2.5-7b) · port 3000 · [Repo](https://github.com/jina-ai/node-deepresearch) · [▶️ Demo ↗](https://search.jina.ai) · [📖 Docs ↗](https://jina.ai/news/a-practical-guide-to-implementing-deepsearch-deepresearch) · [🌐 Site ↗](https://jina.ai/deepsearch) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/node-deepresearch/)</sub>

<a name="u14app-deep-research"></a>
### #&#8288;62 [deep-research](https://github.com/u14app/deep-research) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: niche (29) · Freshness: recent (77) · Maintenance: weak (0) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.7k · MIT · Jun 2026</sub>

**Next.js app that runs multi-step web research and writes a Markdown report.**

Deep Research takes a topic, asks clarifying questions, drafts a research plan, then runs rounds of search queries and compiles a Markdown report using separate thinking and task models. It works with many LLM providers (Gemini, OpenAI, Anthropic, Ollama, OpenRouter and others) and search backends (Searxng, Tavily, Firecrawl, Exa, Brave). It also exposes an SSE API and an MCP server.

- **+** Supports many LLM providers, including Ollama and any OpenAI-compatible endpoint
- **+** Pluggable search: Searxng, Tavily, Firecrawl, Exa, Bocha, or the model's own search
- **+** Exposes /api/sse and an MCP server (streamable-http and SSE) for use from other tools
- **+** Research history and local knowledge base from uploaded files, stored in the browser in local mode
- **−** Calling Ollama or Searxng from the browser can hit CORS errors; server proxy mode needed
- **−** Custom model list works only in proxy mode
- **−** MCP clients need long timeouts (README example uses 600) because runs are slow
- **−** Docker image can lag the latest release by one to two days

<sub>no GPU · Docker + Compose · Needs LLM API key or Ollama, Search provider (Searxng, Tavily, Firecrawl, Exa, Brave, or model search), Node.js 18.18+ for development · Models: Gemini, OpenAI, Anthropic, DeepSeek, Grok · port 3000 · [Repo](https://github.com/u14app/deep-research) · [▶️ Demo ↗](https://research.u14.app/) · [📖 Docs ↗](https://github.com/u14app/deep-research/blob/main/docs/deep-research-api-doc.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/u14app-deep-research/)</sub>

<a name="kag"></a>
### #&#8288;63 [kag](https://github.com/openspg/kag) <sub>score [25](../README.md#-how-we-rank "Score 25/100. Adoption: popular (52) · Freshness: quiet (22) · Maintenance: weak (9) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.2k · Apache-2.0 · Jan 2026</sub>

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

<a name="videorag"></a>
### #&#8288;64 [videorag](https://github.com/hkuds/videorag) <sub>score [23](../README.md#-how-we-rank "Score 23/100. Adoption: niche (13) · Freshness: slowing (45) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.5k · custom license · Mar 2026</sub>

**Desktop app and algorithm for question answering over very long videos.**

Vimo is an Electron desktop app backed by a Python VideoRAG server. It indexes videos into a multi-modal knowledge graph and answers natural-language questions about them. The VideoRAG algorithm (arXiv 2502.01549) builds on nano-graphrag, LightRAG and ImageBind, and the repo includes the LongerVideos benchmark and evaluation scripts. Prebuilt app releases are not available yet, so setup is from source.

- **+** Targets videos of hundreds of hours on a single RTX 3090 (24GB)
- **+** Includes LongerVideos benchmark (164 videos, ~134.6 hours) with reproduction scripts
- **+** Reports 60.2% on Video-MME long track versus 51.8% to 56.3% for MiniCPM baselines
- **+** Supports queries across multiple videos
- **−** No downloadable release yet; macOS Apple Silicon beta is only announced
- **−** Must run a Python backend and Electron frontend from source
- **−** License is not detected (NOASSERTION), so reuse terms are unclear
- **−** Main README gives no model provider list; setup details live in subfolders

<sub>GPU required · Needs Python, Electron, Conda, ImageBind, nano-graphrag, LightRAG · Models: MiniCPM-o, MiniCPM-V, ImageBind · [Repo](https://github.com/hkuds/videorag) · [▶️ Demo ↗](https://www.youtube.com/watch?v=D5vsxcp4QZI) · [🌐 Site ↗](https://arxiv.org/abs/2502.01549) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/videorag/)</sub>

<a name="r2r"></a>
### #&#8288;65 [r2r](https://github.com/sciphi-ai/r2r) <sub>score [16](../README.md#-how-we-rank "Score 16/100. Adoption: known (47) · Freshness: quiet (1) · Maintenance: weak (0) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.1k · MIT · Nov 2025</sub>

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

<a name="unblink"></a>
### #&#8288;66 [unblink](https://github.com/zapdos-labs/unblink) <sub>score [16](../README.md#-how-we-rank "Score 16/100. Adoption: niche (3) · Freshness: slowing (42) · Maintenance: weak (0) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · AGPL-3.0 · Mar 2026</sub>

**Camera monitoring with VLM frame summaries, chat and video search.**

Unblink is a camera monitoring app written in Go. A node on your local network proxies RTSP and MJPEG cameras to a publicly reachable server, which handles auth and stores config in PostgreSQL. Qwen3-VL summarizes frames, and a SolidJS frontend lets you chat with your feeds or search recorded frames in plain language.

- **+** Node proxies cameras from a private network, so camera ports stay unexposed
- **+** Prebuilt node binaries for Linux and Windows on x86_64 and ARM64
- **+** Handles RTSP, MJPEG and WebRTC streams through go2rtc
- **+** Natural-language search over recorded frames and chat with camera feeds
- **−** Needs a publicly reachable server plus PostgreSQL, so setup is more than one binary
- **−** No tagged release; README installs the node from the main branch
- **−** AGPL-3.0 license restricts use in closed-source hosted services

<sub>Docker + Compose · Needs PostgreSQL, go2rtc · Models: Qwen3-VL · [Repo](https://github.com/zapdos-labs/unblink) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/unblink/)</sub>

<a name="maestro"></a>
### #&#8288;67 [MAESTRO](https://github.com/murtaza-nasir/maestro) <sub>score [16](../README.md#-how-we-rank "Score 16/100. Adoption: niche (2) · Freshness: recent (51) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · AGPL-3.0 · Apr 2026</sub>

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
