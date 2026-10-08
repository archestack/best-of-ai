# 📚 RAG and knowledge — reviews

Document Q&A, knowledge bases and enterprise search over your own files and data. Back to the [leaderboard](../README.md#-rag-and-knowledge).

<a name="open-notebook"></a>
### 🥇 91 [Open Notebook](https://github.com/lfnovo/open-notebook) <sub>⭐ 40k · MIT · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · Needs SurrealDB · Models: OpenAI, Anthropic, Google, Mistral, Groq, DeepSeek, xAI, OpenRouter, Cohere, Ollama, LM Studio, oMLX and any OpenAI-compatible endpoint · port 8502 · [Repo](https://github.com/lfnovo/open-notebook) · [🌐 Site](https://www.open-notebook.ai)</sub>

<a name="lightrag"></a>
### 🥇 87 [LightRAG](https://github.com/HKUDS/LightRAG) <sub>⭐ 40k · MIT · Sep 2026</sub>

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

<sub>no GPU · Docker + Compose · Needs PostgreSQL (recommended for production), Neo4j (optional), MongoDB (optional), Milvus (optional), OpenSearch (optional) · Models: LLM and embedding providers configured in .env, tested with open models such as Qwen3-30B-A3B · [Repo](https://github.com/HKUDS/LightRAG)</sub>

<a name="ragflow"></a>
### 🥈 75 [RAGFlow](https://github.com/infiniflow/ragflow) <sub>⭐ 92k · Apache-2.0 · Oct 2026</sub>

**RAG engine with deep document parsing, agentic retrieval and knowledge compilation.**

RAGFlow parses Word, slides, Excel, scans and web pages with in-process layout analysis, OCR and table recognition, chunks by template and answers with traceable citations. Version 1.0 runs as one Go service deployed with Docker Compose beside MySQL, Elasticsearch or Infinity, MinIO, NATS and Kvrocks. For teams building document Q&A and agent workflows over complex enterprise files.

- **+** DeepDoc layout, OCR and table parsing run in-process on CPU
- **+** Chunk visualization and traceable citations let humans check retrieval
- **+** Agentic retrieval with Low to Ultra thinking modes for multi-step questions
- **+** Knowledge Compilation builds wikis, graphs, mind maps and timelines from datasets
- **−** Needs 6 backing services (MySQL, Elasticsearch/Infinity, MinIO, NATS, Kvrocks, ClickHouse)
- **−** Recommended 4 cores, 16 GB RAM and 50 GB disk before any local models
- **−** 1.0 Go rewrite is still rc1 as of 2026-09-29
- **−** Elasticsearch path requires vm.max_map_count >= 262144 on the host

<sub>RAM ≥ 16 GB · no GPU · Docker · Needs MySQL, Elasticsearch or Infinity, MinIO, NATS JetStream, Kvrocks, ClickHouse · Models: external LLM, embedding and reranker providers set by URL and API key · port 80 · [Repo](https://github.com/infiniflow/ragflow) · [🧪 Demo](https://cloud.ragflow.io) · [📖 Docs](https://ragflow.io/docs/dev/) · [🌐 Site](https://ragflow.io/)</sub>

<a name="deepwiki-open"></a>
### 🥈 75 [DeepWiki-Open](https://github.com/AsyncFuncAI/deepwiki-open) <sub>⭐ 18k · MIT · Sep 2026</sub>

**Generates browsable wikis and diagrams for GitHub, GitLab and Bitbucket repos.**

DeepWiki-Open takes a repository URL from GitHub, GitLab or Bitbucket, analyzes the code structure, generates documentation and diagrams, organizes them into a navigable wiki and builds a codemap for guided tours. The repo ships a Dockerfile and compose file. The README now points to a 2.0 release called Grok Wiki distributed as a download from grok-wiki.com and no longer documents configuration.

- **+** Works with GitHub, GitLab and Bitbucket repositories
- **+** Produces diagrams and codemap guided tours, not only prose
- **+** Dockerfile and docker-compose in the repo; MIT license
- **−** README no longer documents setup, ports or supported model providers
- **−** 2.0 is pushed as a separate download at grok-wiki.com
- **−** No hardware guidance; single-maintainer project

<sub>no GPU · Docker + Compose · [Repo](https://github.com/AsyncFuncAI/deepwiki-open) · [🌐 Site](https://grok-wiki.com)</sub>

<a name="private-gpt"></a>
### 🥈 71 [PrivateGPT](https://github.com/zylon-ai/private-gpt) <sub>⭐ 58k · Apache-2.0 · Oct 2026</sub>

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

<sub>no GPU · Docker · Needs OpenAI-compatible inference server (Ollama, llama.cpp, vLLM) · Models: any model behind an OpenAI-compatible /v1/chat/completions endpoint · port 8080 · [Repo](https://github.com/zylon-ai/private-gpt) · [📖 Docs](https://docs.privategpt.dev/)</sub>

<a name="paperless-gpt"></a>
### 🥈 66 [paperless-gpt](https://github.com/icereed/paperless-gpt) <sub>⭐ 2.7k · MIT · Oct 2026</sub>

**LLM-powered OCR, titles, tags and document links for Paperless-ngx.**

paperless-gpt attaches to Paperless-ngx and uses OpenAI, Ollama, Mistral, Azure or Anthropic models to generate titles, tags, correspondents and custom fields, link related documents by reference number, and run OCR via vision models, Google Document AI, Azure Document Intelligence or Docling. OCR output can be written back as searchable PDFs. One container on port 8080; prompts editable in the web UI.

- **+** LLM or VLM OCR produces searchable PDFs with positioned text layers
- **+** Links invoices, amendments and letters via exact reference-number lookup
- **+** Per-document-type AI workflows with trigger tags, testable before saving
- **+** Four OCR providers including a self-hosted Docling server
- **−** No built-in authentication; listens on all interfaces by default
- **−** OCR limited to 5 pages per document unless OCR_LIMIT_PAGES is raised
- **−** PDF_REPLACE deletes the original document; flagged dangerous by the maintainer
- **−** Requires a running Paperless-ngx 2.20.x or 3.0 beta

<sub>no GPU · Docker + Compose · Needs Paperless-ngx, optional OCR: Google Document AI, Azure Document Intelligence, Docling · Models: OpenAI (gpt-4o), Ollama (qwen3:8b, minicpm-v), Mistral, Azure OpenAI, Anthropic · port 8080 · [Repo](https://github.com/icereed/paperless-gpt)</sub>

<a name="weknora"></a>
### 🥈 65 [WeKnora](https://github.com/Tencent/WeKnora) <sub>⭐ 33k · NOASSERTION · Oct 2026</sub>

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

<sub>no GPU · Compose · Needs Neo4j (optional profile), MinIO (optional profile), Langfuse (optional profile) · Models: OpenAI, DeepSeek, Qwen, Zhipu, Hunyuan, Gemini, MiniMax, NVIDIA, LiteLLM, Ollama · port 80 · [Repo](https://github.com/Tencent/WeKnora) · [📖 Docs](https://weknora.weixin.qq.com/docs/) · [🌐 Site](https://weknora.weixin.qq.com)</sub>

<a name="paperless-ai"></a>
### 🥉 61 [Paperless-AI](https://github.com/clusterzx/paperless-ai) <sub>⭐ 6.0k · MIT · Mar 2026</sub>

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

<sub>no GPU · Docker + Compose · Needs Paperless-ngx · Models: Ollama (Mistral, Llama, Phi-3, Gemma-2), OpenAI, DeepSeek, OpenRouter, Perplexity, Together, LiteLLM, vLLM, Fastchat, Gemini · [Repo](https://github.com/clusterzx/paperless-ai) · [📖 Docs](https://github.com/clusterzx/paperless-ai/wiki/2.-Installation)</sub>

<a name="kotaemon"></a>
### 🥉 59 [Kotaemon](https://github.com/Cinnamon/kotaemon) <sub>⭐ 26k · Apache-2.0 · May 2026</sub>

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

<sub>no GPU · Docker · Needs Elasticsearch, LanceDB, ChromaDB, Milvus or Qdrant (optional stores), Unstructured (optional, for .doc/.docx and more) · Models: OpenAI, Azure OpenAI, Cohere, Groq, Ollama · port 7860 · [Repo](https://github.com/Cinnamon/kotaemon) · [🧪 Demo](https://huggingface.co/spaces/cin-model/kotaemon-demo) · [📖 Docs](https://cinnamon.github.io/kotaemon/)</sub>

<a name="db-gpt"></a>
### 🥉 59 [DB-GPT](https://github.com/eosphoros-ai/DB-GPT) <sub>⭐ 20k · MIT · Oct 2026</sub>

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

<sub>GPU optional · Compose · Models: OpenAI-compatible APIs, DashScope/Tongyi, Moonshot (Kimi), MiniMax, local models via vLLM or llama.cpp: DeepSeek, Qwen, GLM, Llama, Gemma, Yi · port 5670 · [Repo](https://github.com/eosphoros-ai/DB-GPT) · [📖 Docs](http://docs.dbgpt.cn/docs/overview/) · [🌐 Site](http://dbgpt.cn/)</sub>

<a name="pipeshub"></a>
### 🥉 58 [PipesHub](https://github.com/pipeshub-ai/pipeshub-ai) <sub>⭐ 3.8k · Apache-2.0 · Oct 2026</sub>

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

<sub>no GPU · Docker · Needs Neo4j or ArangoDB, Qdrant, MongoDB, Redis, Kafka (larger deployments) · Models: any LLM provider, bring your own model, Ollama, local embedding server by default · port 3000 · [Repo](https://github.com/pipeshub-ai/pipeshub-ai) · [📖 Docs](https://docs.pipeshub.com/) · [🌐 Site](https://www.pipeshub.com/)</sub>

<a name="morphik"></a>
### 49 [Morphik](https://github.com/morphik-org/morphik-core) <sub>⭐ 3.7k · NOASSERTION · Oct 2026</sub>

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

<sub>no GPU · Compose · Models: ColPali multimodal embeddings · [Repo](https://github.com/morphik-org/morphik-core) · [🧪 Demo](https://dev.morphik.ai) · [📖 Docs](https://dev.morphik.ai/docs) · [🌐 Site](https://morphik.ai)</sub>

<a name="maxkb"></a>
### 43 [MaxKB](https://github.com/1Panel-dev/MaxKB) <sub>⭐ 23k · GPL-3.0 · Oct 2026</sub>

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

<sub>no GPU · Models: OpenAI, Claude, Gemini, MiniMax, DeepSeek, Llama, Qwen as private models · port 8080 · [Repo](https://github.com/1Panel-dev/MaxKB)</sub>

<a name="surfsense"></a>
### 37 [SurfSense](https://github.com/MODSetter/SurfSense) <sub>⭐ 16k · NOASSERTION · Oct 2026</sub>

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

<sub>no GPU · Models: local Qwen3 in six sizes from 0.5 GB, any OpenAI-compatible API · [Repo](https://github.com/MODSetter/SurfSense) · [📖 Docs](https://www.surfsense.com/docs) · [🌐 Site](https://www.surfsense.com/)</sub>

<a name="docling-serve"></a>
### 27 [Docling Serve](https://github.com/docling-project/docling-serve) <sub>⭐ 1.8k · MIT · Oct 2026</sub>

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

<sub>GPU optional · Models: bundled Docling parsing models · port 5001 · [Repo](https://github.com/docling-project/docling-serve)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-selfhosted-ai/issues/new/choose).</sub>
