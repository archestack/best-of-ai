# 📚 RAG and knowledge reviews · Best of Open-Source AI

Document Q&A, knowledge bases and enterprise search over your own files and data. Back to the [leaderboard](../README.md#-rag-and-knowledge).

<a name="lightrag"></a>
### 🥇 [LightRAG](https://github.com/hkuds/lightrag) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (80) · Freshness: active (100) · Maintenance: healthy (89) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · MIT · Sep 2026</sub>

**Graph-plus-vector RAG server with web UI and Ollama-compatible API.**

LightRAG indexes documents into a knowledge graph plus vector store and queries both layers, as a lighter alternative to Microsoft GraphRAG. The server package ships a REST API, a web UI for inserting and visualizing the graph, and Ollama-compatible /api routes for chat frontends. Parsing runs via MinerU, Docling or a native engine; production storage goes to PostgreSQL, Neo4j, MongoDB, Milvus or OpenSearch.

- **+** Dual-level graph and vector retrieval with fewer LLM calls than community-report GraphRAG
- **+** Incremental updates and document deletion with graph regeneration from the LLM cache
- **+** Three parsing engines and four chunking strategies, including paragraph-semantic
- **+** Separate LLM settings per role: extract, query, keywords and VLM
- **−** Default KV, vector and graph stores are in-memory with file persistence, not for production
- **−** Server binds 0.0.0.0 with every endpoint public until auth is configured
- **−** Ollama-compatible /api routes stay open even with auth unless WHITELIST_PATHS is set
- **−** docx smart headings and SVG rendering need extra spaCy models and libcairo

<sub>no GPU · Docker + Compose · Needs PostgreSQL (recommended for production), Neo4j (optional), MongoDB (optional), Milvus (optional), OpenSearch (optional) · Models: LLM and embedding providers configured in .env, tested with open models such as Qwen3-30B-A3B · [Repo](https://github.com/hkuds/lightrag)</sub>

<a name="open-notebook"></a>
### 🥈 [Open Notebook](https://github.com/lfnovo/open-notebook) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: healthy (86) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · MIT · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · Needs SurrealDB · Models: OpenAI, Anthropic, Google, Mistral, Groq, DeepSeek, xAI, OpenRouter, Cohere, Ollama, LM Studio, oMLX and any OpenAI-compatible endpoint · port 8502 · README: alternative to NotebookLM · [Repo](https://github.com/lfnovo/open-notebook) · [🌐 Site ↗](https://www.open-notebook.ai)</sub>

<a name="ragflow"></a>
### 🥉 [RAGFlow](https://github.com/infiniflow/ragflow) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: healthy (94) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 92k · Apache-2.0 · Oct 2026</sub>

**RAG engine with document parsing, agentic retrieval and citations.**

RAGFlow parses documents (Word, slides, Excel, TXT, images, scans, web pages) with template-based chunking, then retrieves with multiple recall and fused re-ranking to produce answers with traceable citations. Recent releases add agentic multi-step retrieval with four thinking modes and Knowledge Compilation into wikis, graphs, trees and mind maps. Models are configured by name, address and API key for the LLM, embedding and reranker.

- **+** Chunk visualization lets you inspect and correct parsing before retrieval
- **+** Citations link answers back to source chunks
- **+** Ingests sitemaps and Google BigQuery with incremental sync
- **+** Apache-2.0 with prebuilt Docker Compose deployment
- **−** Stack needs MySQL, MinIO, NATS, Kvrocks, ClickHouse and a document engine
- **−** Go backend not supported on macOS; Linux x86_64 host required
- **−** DeepDoc OCR and layout analysis run on CPU only in 1.0
- **−** Current release is 1.0.0-rc1, a release candidate

<sub>RAM ≥ 16 GB · no GPU · Docker + Compose · Needs Elasticsearch or Infinity, MySQL, MinIO, NATS JetStream, Kvrocks, ClickHouse · Models: configurable LLM, embedding, reranker · port 80 · [Repo](https://github.com/infiniflow/ragflow) · [▶️ Demo ↗](https://cloud.ragflow.io) · [📖 Docs ↗](https://ragflow.io/docs/dev/) · [🌐 Site ↗](https://ragflow.io/)</sub>

<a name="weknora"></a>
### #&#8288;4 [WeKnora](https://github.com/tencent/weknora) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: healthy (89) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · custom license · Oct 2026</sub>

**Enterprise knowledge base combining RAG Q&A, agents and generated wikis.**

WeKnora turns team documents into knowledge bases with three modes: cited RAG answers, an agent that runs multi-step tasks with skills in Docker, E2B or Cube sandboxes, and auto-generated wiki pages with a knowledge graph. It syncs from Feishu, Confluence, GitLab, Notion and RSS, answers in WeCom, Slack and Telegram, and exposes an MCP server. Deploy with Docker Compose, Helm or one Lite binary on SQLite.

- **+** 29 built-in model vendors including OpenAI, DeepSeek, Qwen, Gemini, LiteLLM and Ollama
- **+** Lite single binary with SQLite and in-memory queue for low-resource hosts
- **+** Workspace RBAC with four roles, per-resource ownership and audit log
- **+** Per-workspace MCP endpoints with own token, scope and rate limit
- **−** Many integrations target the Chinese ecosystem (WeChat, Feishu, DingTalk, Yuque)
- **−** Sandbox commands run as root since v0.8.2
- **−** Maintainers advise against exposing it to the public internet
- **−** Desktop app has no published installer; hardware requirements live in external docs

<sub>no GPU · Docker + Compose · Needs Neo4j (optional profile), MinIO (optional profile), Langfuse (optional profile) · Models: OpenAI, DeepSeek, Qwen, Zhipu, Hunyuan, Gemini, MiniMax, NVIDIA, LiteLLM, Ollama · port 80 · [Repo](https://github.com/tencent/weknora) · [📖 Docs ↗](https://weknora.weixin.qq.com/docs/) · [🌐 Site ↗](https://weknora.weixin.qq.com)</sub>

<a name="surfsense"></a>
### #&#8288;5 [SurfSense](https://github.com/modsetter/surfsense) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (41) · Freshness: active (100) · Maintenance: healthy (91) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · custom license · Oct 2026</sub>

**Offline NotebookLM alternative that turns documents into decks, reports and podcasts.**

SurfSense indexes local PDFs, Office files and images into SQLite, answers with citations and turns sources into summaries, flashcards, quizzes, mind maps, editable pptx/docx/xlsx and offline podcasts (Kokoro-82M). It runs a local Qwen3 (six sizes from 0.5 GB) or any OpenAI-compatible API, egress off by default. The supported path is a desktop installer; the Docker stack is community-supported.

- **+** Parser, retrieval model and podcast voice ship in the installer; works with networking off
- **+** Egress panel off by default, no telemetry or crash reporting
- **+** Produces editable pptx, docx and xlsx files rather than chat only
- **+** No account required; keys stored in the OS keychain
- **−** Primary product is a desktop app, not a server
- **−** Self-hosted Docker stack has no SLA and no hosted service behind it
- **−** Hosted web app retired; export window closes 2026-10-18
- **−** Plugins and priority support are behind a paid licence; no video overviews

<sub>no GPU · Docker + Compose · Models: local Qwen3 in six sizes from 0.5 GB, any OpenAI-compatible API · README: alternative to NotebookLM · [Repo](https://github.com/modsetter/surfsense) · [📖 Docs ↗](https://www.surfsense.com/docs) · [🌐 Site ↗](https://www.surfsense.com/)</sub>

<a name="maxkb"></a>
### #&#8288;6 [MaxKB](https://github.com/1panel-dev/maxkb) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: healthy (97) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · GPL-3.0 · Oct 2026</sub>

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

<sub>no GPU · Models: OpenAI, Claude, Gemini, MiniMax, DeepSeek, Llama, Qwen as private models · port 8080 · [Repo](https://github.com/1panel-dev/maxkb)</sub>

<a name="private-gpt"></a>
### #&#8288;7 [PrivateGPT](https://github.com/zylon-ai/private-gpt) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: fair (63) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 58k · Apache-2.0 · Oct 2026</sub>

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

<sub>no GPU · Docker · Needs OpenAI-compatible inference server (Ollama, llama.cpp, vLLM) · Models: any model behind an OpenAI-compatible /v1/chat/completions endpoint · port 8080 · [Repo](https://github.com/zylon-ai/private-gpt) · [📖 Docs ↗](https://docs.privategpt.dev/)</sub>

<a name="pipeshub"></a>
### #&#8288;8 [PipesHub](https://github.com/pipeshub-ai/pipeshub-ai) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: healthy (82) · Easy to run: some setup (33) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.8k · Apache-2.0 · Oct 2026</sub>

**Permission-aware search and agent context over 50+ workplace systems.**

PipesHub indexes Slack, Google Drive, GitHub, Microsoft 365, Notion and 50+ systems into a knowledge graph (Neo4j or ArangoDB), Qdrant and MongoDB, then serves permission-aware search with block-level citations and hands the same context to agents over MCP and SDKs. Access is checked against source permissions at query time. A one-command installer writes Compose files and starts the stack on port 3000.

- **+** Permission filtering resolved against the source system at query time
- **+** 50+ connectors with real-time and scheduled indexing
- **+** MCP server plus Python, TypeScript and Go SDKs
- **+** Kubernetes deployment with HA defaults; slim or full Compose profiles
- **−** Needs Neo4j or ArangoDB, Qdrant, MongoDB, Redis, and Kafka at scale
- **−** Installer is curl piped to bash
- **−** Audio and video are stored but not indexed yet
- **−** Plain-HTTP cloud deployments show a white screen; TLS termination required

<sub>no GPU · Docker + Compose · Needs Neo4j or ArangoDB, Qdrant, MongoDB, Redis, Kafka (larger deployments) · Models: any LLM provider, bring your own model, Ollama, local embedding server by default · port 3000 · [Repo](https://github.com/pipeshub-ai/pipeshub-ai) · [📖 Docs ↗](https://docs.pipeshub.com/) · [🌐 Site ↗](https://www.pipeshub.com/)</sub>

<a name="deepwiki-open"></a>
### #&#8288;9 [DeepWiki-Open](https://github.com/asyncfuncai/deepwiki-open) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: known (45) · Freshness: active (100) · Maintenance: patchy (39) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · MIT · Sep 2026</sub>

**Generates browsable wikis and diagrams for GitHub, GitLab and Bitbucket repos.**

DeepWiki-Open takes a repository URL from GitHub, GitLab or Bitbucket, analyzes the code structure, generates documentation and diagrams, organizes them into a navigable wiki and builds a codemap for guided tours. The repo ships a Dockerfile and compose file. The README now points to a 2.0 release called Grok Wiki distributed as a download from grok-wiki.com and no longer documents configuration.

- **+** Works with GitHub, GitLab and Bitbucket repositories
- **+** Produces diagrams and codemap guided tours, not only prose
- **+** Dockerfile and docker-compose in the repo; MIT license
- **−** README no longer documents setup, ports or supported model providers
- **−** 2.0 is pushed as a separate download at grok-wiki.com
- **−** No hardware guidance; single-maintainer project

<sub>no GPU · Docker + Compose · [Repo](https://github.com/asyncfuncai/deepwiki-open) · [🌐 Site ↗](https://grok-wiki.com)</sub>

<a name="db-gpt"></a>
### #&#8288;10 [DB-GPT](https://github.com/eosphoros-ai/db-gpt) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: popular (50) · Freshness: active (100) · Maintenance: fair (61) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · MIT · Oct 2026</sub>

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

<sub>GPU optional · Docker + Compose · Compose runs MySQL · Models: OpenAI-compatible APIs, DashScope/Tongyi, Moonshot (Kimi), MiniMax, local models via vLLM or llama.cpp: DeepSeek, Qwen, GLM, Llama, Gemma, Yi · port 5670 · [Repo](https://github.com/eosphoros-ai/db-gpt) · [📖 Docs ↗](http://docs.dbgpt.cn/docs/overview/) · [🌐 Site ↗](http://dbgpt.cn/)</sub>

<a name="paperless-gpt"></a>
### #&#8288;11 [paperless-gpt](https://github.com/icereed/paperless-gpt) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: niche (7) · Freshness: active (100) · Maintenance: fair (79) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.7k · MIT · Oct 2026</sub>

**LLM-based OCR, titles, tags and document links for paperless-ngx.**

paperless-gpt is a companion service for paperless-ngx that calls an LLM to generate titles, tags, correspondents, created dates and custom fields, with a web UI for manual review or automatic processing. It can also replace the stock OCR with LLM OCR (OpenAI, Ollama, Mistral, Anthropic), Google Document AI, Azure Document Intelligence or a Docling server, and can produce searchable PDFs. It fills Document Link fields by extracting invoice, contract or case references and doing an exact lookup.

- **+** Supports OpenAI, Mistral, Anthropic, Azure OpenAI and local Ollama models
- **+** Four OCR backends: LLM, Google Document AI, Azure, Docling
- **+** Document linking uses exact whole-word lookup and leaves ambiguous matches unlinked
- **+** Prompts and per-document-type workflows editable in the web UI
- **−** No built-in authentication; needs a reverse proxy or VPN
- **−** Works only with paperless-ngx, tested on 2.20.x and 3.0 beta
- **−** Hosted LLM and OCR options send document content to third parties
- **−** PDF_REPLACE mode deletes the original document after upload

<sub>GPU optional · Docker + Compose · Needs paperless-ngx, LLM provider (OpenAI, Ollama, Mistral, Anthropic or Azure OpenAI) · Models: OpenAI, Azure OpenAI, Mistral, Anthropic, Ollama · port 8080 · [Repo](https://github.com/icereed/paperless-gpt)</sub>

<a name="docling-serve"></a>
### #&#8288;12 [Docling Serve](https://github.com/docling-project/docling-serve) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: niche (2) · Freshness: active (100) · Maintenance: fair (80) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · MIT · Oct 2026</sub>

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

<sub>GPU optional · Docker · Models: bundled Docling parsing models · port 5001 · [Repo](https://github.com/docling-project/docling-serve)</sub>

<a name="kotaemon"></a>
### #&#8288;13 [Kotaemon](https://github.com/cinnamon/kotaemon) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: popular (60) · Freshness: active (89) · Maintenance: weak (3) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · Apache-2.0 · May 2026</sub>

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

<sub>no GPU · Docker · Needs Elasticsearch, LanceDB, ChromaDB, Milvus or Qdrant (optional stores), Unstructured (optional, for .doc/.docx and more) · Models: OpenAI, Azure OpenAI, Cohere, Groq, Ollama · port 7860 · [Repo](https://github.com/cinnamon/kotaemon) · [▶️ Demo ↗](https://huggingface.co/spaces/cin-model/kotaemon-demo) · [📖 Docs ↗](https://cinnamon.github.io/kotaemon/)</sub>

<a name="morphik"></a>
### #&#8288;14 [Morphik](https://github.com/morphik-org/morphik-core) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: weak (22) · Easy to run: easy (50) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · custom license · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · Compose runs Redis, PostgreSQL, Ollama · Models: ColPali multimodal embeddings · [Repo](https://github.com/morphik-org/morphik-core) · [▶️ Demo ↗](https://dev.morphik.ai) · [📖 Docs ↗](https://dev.morphik.ai/docs) · [🌐 Site ↗](https://morphik.ai)</sub>

<a name="paperless-ai"></a>
### #&#8288;15 [Paperless-AI](https://github.com/clusterzx/paperless-ai) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: niche (27) · Freshness: recent (61) · Maintenance: weak (18) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · MIT · Mar 2026</sub>

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

<sub>no GPU · Docker + Compose · Needs Paperless-ngx · Models: Ollama (Mistral, Llama, Phi-3, Gemma-2), OpenAI, DeepSeek, OpenRouter, Perplexity, Together, LiteLLM, vLLM, Fastchat, Gemini · [Repo](https://github.com/clusterzx/paperless-ai) · [📖 Docs ↗](https://github.com/clusterzx/paperless-ai/wiki/2.-Installation)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
