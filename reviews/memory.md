# 🗂️ Memory reviews · Best of Open-Source AI

Long-term memory engines that store and retrieve facts for agents across sessions. Back to the [leaderboard](../README.md#%EF%B8%8F-memory).

<sub>🌐 Also on the web: [Memory on archestack.com](https://archestack.com/best-of-ai/memory/), each project on its own page.</sub>

<a name="hindsight"></a>
### 🥇 [hindsight](https://github.com/vectorize-io/hindsight) <sub>score [97](../README.md#-how-we-rank "Score 97/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 64k · MIT · Nov 2026</sub>

**Agent memory server with retain, recall and reflect operations.**

Hindsight is a long-term memory system for agents. It uses an LLM to extract facts, entities and time data on retain, then recalls them with semantic, BM25, graph and temporal search, merged by reciprocal rank fusion and a cross-encoder rerank. It also consolidates facts into observations and mental models, and ships Python, TypeScript and Go clients, a CLI and a per-bank MCP endpoint.

- **+** Four parallel retrieval strategies (semantic, BM25, graph, temporal) with cross-encoder reranking
- **+** Works with 25+ LLM providers, including local ones: ollama, lmstudio, llamacpp
- **+** Python, Node.js and Go clients, CLI, REST API and a built-in MCP endpoint per bank
- **+** Embedded pg0 database by default; external PostgreSQL and Helm chart also supported
- **−** Retain depends on an LLM call for fact extraction, adding provider cost and latency
- **−** Dashboard, backups and uptime SLA are described only for the hosted Hindsight Cloud
- **−** Benchmark claims are partly vendor-reported; only some were independently reproduced
- **−** Intel Macs need the hindsight-all-slim package instead of the default

<sub>Docker · Needs LLM provider (API or local), PostgreSQL (embedded pg0 by default) · Models: openai, anthropic, gemini, groq, bedrock · port 9999 · [Repo](https://github.com/vectorize-io/hindsight) · [📖 Docs ↗](https://hindsight.vectorize.io) · [🌐 Site ↗](https://hindsight.vectorize.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hindsight/)</sub>

<a name="gbrain"></a>
### 🥈 [gbrain](https://github.com/garrytan/gbrain) <sub>score [94](../README.md#-how-we-rank "Score 94/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · MIT · Nov 2026</sub>

**Memory store with sources and a knowledge graph for coding agents.**

GBrain stores facts and markdown pages with their sources and exposes them over MCP to agents such as Claude Code, Codex, Cursor and ChatGPT. It starts keyless with keyword search on embedded PGLite, and optionally adds embeddings, reranking, a typed link graph, and `gbrain think`, which writes cited answers with gap notes. Postgres and a paid hosted option at gbrain.io are also available.

- **+** Keyless start: embedded PGLite and keyword search, no server or API keys needed
- **+** MCP access via local stdio, Tailscale tailnet exposure, or remote URL with token
- **+** `gbrain think` answers carry citations and note stale or missing knowledge
- **+** Swappable schema packs and a typed link graph; MIT license
- **−** Not on npm; install from GitHub with Bun 1.4.4 or newer
- **−** Semantic search, synthesis and enrichment need separately configured, paid model providers
- **−** Shared brains are not isolated against local file or shared DB credential access
- **−** Always-on enrichment suggests a server with 8GB+ RAM plus its own API usage

<sub>RAM ≥ 8 GB · no GPU · Compose · Needs Bun 1.4.4+, PGLite or Postgres, Tailscale (optional, remote MCP), Embedding and chat provider API (optional) · [Repo](https://github.com/garrytan/gbrain) · [🌐 Site ↗](https://gbrain.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gbrain/)</sub>

<a name="mempalace"></a>
### 🥉 [MemPalace](https://github.com/mempalace/mempalace) <sub>score [91](../README.md#-how-we-rank "Score 91/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 61k · MIT · Nov 2026</sub>

**Local verbatim memory store for AI agents with semantic search and MCP.**

MemPalace stores conversation history and project files as verbatim text, without summarizing, and retrieves it by semantic search scoped into wings (people, projects), rooms (topics) and drawers (original content). It defaults to ChromaDB with a pluggable backend interface, and exposes 47 MCP tools plus a SQLite temporal knowledge graph. The README reports 96.6% R@5 on LongMemEval in raw mode with no LLM.

- **+** Stores original text verbatim; raw mode needs no LLM or API key
- **+** Pluggable backends: Chroma, SQLite exact, Rust exact, Milvus, Qdrant, pgvector
- **+** Benchmarks reproducible from the repo with committed per-question results
- **+** Auto-save hooks for Claude Code, Codex CLI and Cursor; 47 MCP tools
- **−** Native Termux install unsupported; Android needs a Debian PRoot container
- **−** Claude Code sessions expire in 30 days unless auto-save hooks are wired
- **−** First embedding call downloads a model of about 80-300 MB

<sub>GPU optional · Docker + Compose · Needs Python 3.10+, ChromaDB (default), Milvus (optional), Qdrant (optional), Postgres pgvector (optional) · Models: minilm, embeddinggemma, OpenAI-compatible embeddings endpoints · [Repo](https://github.com/mempalace/mempalace) · [📖 Docs ↗](https://mempalaceofficial.com/guide/getting-started.html) · [🌐 Site ↗](https://mempalaceofficial.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mempalace/)</sub>

<a name="supermemory"></a>
### #&#8288;4 [Supermemory](https://github.com/supermemoryai/supermemory) <sub>score [91](../README.md#-how-we-rank "Score 91/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · MIT · Nov 2026</sub>

**Memory and context engine for AI agents, with user profiles and hybrid search.**

Supermemory extracts facts from conversations, tracks updates and contradictions, expires stale information, and returns a per-user profile plus relevant memories through one API. It also covers RAG, connectors (Google Drive, Gmail, Notion, OneDrive, GitHub) and file extraction. It can be used via the hosted API, an MCP server and editor plugins, or a local server on port 6767.

- **+** Hybrid search returns RAG documents and user memories in a single query
- **+** Handles knowledge updates and contradictions, and auto-forgets expired facts
- **+** Local server keeps data in ~/.supermemory and can use Ollama with local embeddings
- **+** Plugins for Claude Code, Cursor, Codex, OpenCode, plus Vercel AI SDK, LangChain, Mastra wrappers
- **−** Benchmark #1 claims are self-reported in the README, with details on a separate research page
- **−** Hosted MCP server and plugins point at supermemory.ai cloud by default
- **−** Local mode URL ingestion depends on a hosted reader service
- **−** Local-versus-Enterprise feature differences are only documented on a separate page

<sub>GPU optional · Needs LLM provider (OpenAI, Anthropic, Gemini, Groq, or Ollama), Docker (optional) · Models: OpenAI, Anthropic, Gemini, Groq, Ollama · port 6767 · [Repo](https://github.com/supermemoryai/supermemory) · [📖 Docs ↗](https://supermemory.ai/docs) · [🌐 Site ↗](https://supermemory.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/supermemory/)</sub>

<a name="mem0"></a>
### #&#8288;5 [Mem0](https://github.com/mem0ai/mem0) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: fair (71) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 70k · Apache-2.0 · Nov 2026</sub>

**Long-term memory layer that stores and retrieves user facts for LLM agents.**

Mem0 extracts facts from conversations with an LLM, stores them per user, session or agent, and retrieves them with combined semantic, BM25 keyword and entity matching. It ships as a Python and npm library, a self-hosted server with a dashboard and API keys, a CLI, and a managed cloud platform. The published benchmark numbers come from the managed platform, not the open-source SDK.

- **+** Python (pip) and npm SDKs plus a CLI, so it embeds in existing agents
- **+** Hybrid retrieval: semantic, BM25 keyword and entity linking fused in one search
- **+** Evaluation framework is open-sourced so benchmark numbers can be reproduced
- **+** Supports several LLMs and embedders; defaults are configurable
- **−** Benchmarks reflect the managed platform; OSS results may differ
- **−** Needs an LLM; default is OpenAI gpt-5-mini and text-embedding-3-small
- **−** BM25 and entity features need the optional mem0ai[nlp] extra and a spaCy model
- **−** Self-hosted dashboard is listed as limited; advanced features are cloud-only

<sub>GPU optional · Needs LLM provider (default OpenAI), Embedding model (default OpenAI text-embedding-3-small), Docker Compose (self-hosted server), spaCy en_core_web_sm (optional NLP extra) · Models: OpenAI gpt-5-mini (default), text-embedding-3-small (default), other LLMs and embedders via configuration · port 3000 · [Repo](https://github.com/mem0ai/mem0) · [▶️ Demo ↗](https://mem0.dev/demo) · [📖 Docs ↗](https://docs.mem0.ai) · [🌐 Site ↗](https://mem0.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mem0/)</sub>

<a name="cognee"></a>
### #&#8288;6 [Cognee](https://github.com/topoteretes/cognee) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · Apache-2.0 · Nov 2026</sub>

**Long-term memory engine that builds a knowledge graph from documents, code and sessions.**

Cognee is a Python library, CLI and REST API that stores content through remember, recall, improve and forget operations. It builds entities, relationships and vector chunks from text and code, and runs without an LLM key using local GLiNER extraction and a local embedding model. Plugins exist for Claude Code, Codex and OpenClaw, plus an MCP server for other clients.

- **+** Keyless local mode: GLiNER extraction and local embeddings, no LLM API key required
- **+** Four-call API (remember, recall, improve, forget) in Python, CLI, REST, TypeScript and Rust
- **+** Plugins for Claude Code, Codex and OpenClaw, plus an MCP server
- **+** Imports memory from Mem0, Letta, Zep or Graphiti via the COGX exchange format
- **−** Postgres-only graph store is labelled a demo; production version is a licensed product
- **−** Bundled GLiNER extractor is a demo; the more accurate version requires contacting the vendor
- **−** Generated answers and media processing need a configured LLM, vision or transcription model
- **−** Docker defaults to multi-tenant auth; single-user use needs ENABLE_BACKEND_ACCESS_CONTROL=false

<sub>GPU optional · Docker + Compose · Needs Python 3.10-3.14, Node.js/npm (UI launcher), Docker (MCP service, optional), Postgres (optional) · Models: OpenAI, Ollama, GLiNER (local) · port 8000 · [Repo](https://github.com/topoteretes/cognee) · [▶️ Demo ↗](https://www.youtube.com/watch?v=8hmqS2Y5RVQ&t=13s) · [📖 Docs ↗](https://docs.cognee.ai/) · [🌐 Site ↗](https://cognee.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cognee/)</sub>

<a name="graphiti"></a>
### #&#8288;7 [Graphiti](https://github.com/getzep/graphiti) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · Apache-2.0 · Nov 2026</sub>

**Python framework for building temporal knowledge graphs for agent memory.**

Graphiti is a Python library (graphiti-core) that ingests text and JSON episodes into a graph of entities and facts, each with a validity window. Superseded facts are invalidated rather than deleted, so you can query current or past state. Retrieval combines embeddings, BM25 and graph traversal. You supply the graph database (Neo4j, FalkorDB, Neptune), the LLM and the embedder.

- **+** Facts carry validity windows; old facts are invalidated, not deleted, enabling point-in-time queries
- **+** Incremental ingestion with no full graph recompute; every fact traces to its source episode
- **+** Custom entity and edge types defined as Pydantic models, or learned from data
- **+** Multiple graph backends: Neo4j 5.26, FalkorDB 1.1.2, Amazon Neptune
- **−** Needs a separately run graph database; no built-in storage
- **−** Defaults to OpenAI; needs structured-output LLMs, and smaller models can fail ingestion
- **−** Reference MCP and REST servers have no authentication and are not for production
- **−** Kuzu backend is deprecated; auth, tenancy and ingestion service are left to you

<sub>no GPU · Docker + Compose · Needs Neo4j 5.26, FalkorDB 1.1.2, Amazon Neptune + OpenSearch Serverless, OpenAI API key · Models: OpenAI, Anthropic, Google Gemini, Groq, OpenAI-compatible endpoints (Ollama, vLLM, llama.cpp, LM Studio) · [Repo](https://github.com/getzep/graphiti) · [🌐 Site ↗](https://www.getzep.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/graphiti/)</sub>

<a name="agentmemory"></a>
### #&#8288;8 [agentmemory](https://github.com/rohitg00/agentmemory) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · Apache-2.0 · Nov 2026</sub>

**Shared persistent memory server for coding agents, exposed via MCP, hooks and REST.**

AgentMemory captures coding-session events through agent hooks and plugins, scrubs secrets, and stores decisions and fixes for later recall by any connected agent. Recall uses BM25 keyword search without an API key, with optional local or remote embeddings for semantic search. It exposes 54 MCP tools, a REST API on port 3111 and a live viewer on port 3113 for browsing, editing and forgetting memories.

- **+** Keyless BM25 recall works with no API key; README reports 84.7% recall-all@5 on LongMemEval-S
- **+** One memory store shared across Claude Code, Codex CLI, Cursor, Gemini CLI and others via hooks, MCP or REST
- **+** No external database required; data stays local, with Redis backend migration documented
- **+** Live viewer to browse, edit, export and forget memories
- **−** Keyless mode has no vector embeddings, so purely semantic queries can return nothing
- **−** Hook-based capture depth varies by agent; several are MCP-only with no automatic capture
- **−** Published benchmark covers retrieval only, not full-system answer quality or competitor comparison
- **−** Requires Node.js 20+; native Windows setup is separate from the default path

<sub>no GPU · Docker + Compose · Needs Node.js 20+, curl, sh and tar on macOS/Linux for runtime setup · Models: BM25 keyword search (no model), Local embeddings (Xenova/all-MiniLM-L6-v2), Remote embedding and LLM providers (optional) · port 3113 · [Repo](https://github.com/rohitg00/agentmemory) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agentmemory/)</sub>

<a name="everos"></a>
### #&#8288;9 [everos](https://github.com/evermind-ai/everos) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Nov 2026</sub>

**Agent memory runtime that keeps memories as Markdown, indexed in SQLite and LanceDB.**

EverOS is a Python library and HTTP server that stores conversations, files and agent trajectories as editable Markdown, then indexes them in SQLite and LanceDB for keyword, vector and hybrid search. It keeps user memory (episodes, profile) separate from agent memory (cases, skills) and runs a reflection step that consolidates memories between sessions. A single OpenRouter key enables the core add, flush and keyword-search flow; embedding and rerank providers unlock the rest.

- **+** Markdown is the source of truth: editable, diffable, Git-versionable, with a watcher that re-syncs
- **+** No MongoDB, Elasticsearch or Redis needed; storage is Markdown, SQLite and LanceDB
- **+** Scopes search by user_id, agent_id, app_id, project_id and session_id
- **+** Reports LoCoMo 94.61% and LongMemEval 94.00% with reproduction steps in benchmarks/
- **−** Default hybrid search needs an embedding provider; one-key setup is limited to keyword search
- **−** Needs an external LLM API for extraction; OpenRouter or any OpenAI-compatible endpoint
- **−** Office file ingestion requires LibreOffice and a multimodal model
- **−** /api/v1 is a legacy alias that may be removed in a future major release

<sub>no GPU · Needs OpenRouter or OpenAI-compatible LLM API, Embedding provider (for hybrid search), Rerank provider (for agentic search and Knowledge Wiki), LibreOffice (office documents), SQLite, LanceDB · Models: openai/gpt-4.1-mini, Qwen/Qwen3-Embedding-4B, Qwen/Qwen3-Reranker-4B, google/gemini-3.8-flash, any OpenAI-compatible model · port 8000 · [Repo](https://github.com/evermind-ai/everos) · [📖 Docs ↗](https://docs.evermind.ai) · [🌐 Site ↗](https://evermind.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/everos/)</sub>

<a name="memos"></a>
### #&#8288;10 [MemOS](https://github.com/memtensor/memos) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Nov 2026</sub>

**Graph-structured long-term memory API and local plugins for LLM agents.**

MemOS is a memory layer for LLM agents with add, search, edit and delete operations over a graph-structured store, organized into memory cubes per user or project. It runs as a REST API on port 8000 backed by Neo4j and Qdrant, or as local SQLite-based plugins for OpenClaw, Hermes Agent and DeepSeek Harness. A hosted Cloud API is also offered.

- **+** Self-host REST API plus local SQLite plugins with no cloud dependency
- **+** Memory cubes isolate or share knowledge bases across users, projects and agents
- **+** Plugins use hybrid retrieval (FTS5 + vector) and include a local Memory Viewer
- **+** Reports LoCoMo 88.83 and LongMemEval 89.20 on its own OmniMemEval suite
- **−** Self-hosted server needs Neo4j and Qdrant running alongside the API
- **−** Cloud API and Cloud plugins send data to MemOS Cloud and need an API key
- **−** Benchmark figures come from the authors' own evaluation suite
- **−** Ready-made plugins cover only OpenClaw, Hermes and DeepSeek Harness

<sub>Docker + Compose · Needs Neo4j, Qdrant, Node.js (local plugin), LLM provider API key · port 8000 · [Repo](https://github.com/memtensor/memos) · [🌐 Site ↗](https://memos.openmem.net/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/memos/)</sub>

<a name="openviking"></a>
### #&#8288;11 [OpenViking](https://github.com/volcengine/openviking) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 43k · AGPL-3.0 · Nov 2026</sub>

**Filesystem-style context database for agent memory, resources and skills.**

OpenViking stores agent knowledge, memories and skills as a virtual filesystem under viking:// URIs, which agents browse with ls, tree, read, write and grep. Directories carry generated L0 abstracts and L1 overviews so agents read summaries before full content, and committed sessions become editable Markdown memories. It ships a Python server, an ov CLI, Python/Go/TypeScript SDKs, an HTTP API and memory plugins for Claude Code, Codex, Cursor and others.

- **+** Stored memories are plain Markdown under viking:// paths that you can inspect and edit
- **+** Semantic search can be scoped to a directory subtree instead of a flat vector pool
- **+** Plugin installer covers Claude Code, Codex, Cursor, TRAE, OpenCode and more
- **+** Python, Go and TypeScript SDKs, HTTP API, multi-tenant accounts and opt-in ACLs
- **−** Needs a model provider with both an embedding model and a VLM
- **−** AGPL-3.0 license restricts use in closed-source network services
- **−** Memory extraction runs in the background, so new memories are not instantly retrievable
- **−** Desktop app is beta; the plugin installer supports only macOS and Linux

<sub>no GPU · Docker + Compose · Needs uv, Python 3.10+, embedding model provider, VLM provider, Node.js 18+ (plugin installer) · Models: Volcengine, OpenAI, Codex OAuth, Kimi, GLM · [Repo](https://github.com/volcengine/openviking) · [▶️ Demo ↗](https://openviking.ai/studio) · [📖 Docs ↗](https://docs.openviking.ai/) · [🌐 Site ↗](https://www.openviking.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openviking/)</sub>

<a name="claude-obsidian"></a>
### #&#8288;12 [claude-obsidian](https://github.com/agricidaniel/claude-obsidian) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · MIT · Oct 2026</sub>

**Claude Code plugin that builds a linked Markdown wiki in an Obsidian vault.**

A Claude Code plugin and set of 15 Agent Skills that ingest sources from an inbox/ folder into cited, interlinked Markdown notes. It answers questions read-only from the vault, runs a lint for dead links and orphans, and applies all writes as journaled transactions with SHA-256 conflict checks. The same skills can be linked into Codex, OpenCode, Gemini, ZCode, Cursor and Windsurf via a setup script.

- **+** Writes are transactional, with hash conflict detection and journal rollback after interrupted writes
- **+** Output is plain Markdown that works in Obsidian or any editor, with originals kept untouched
- **+** Same skills run in Codex, OpenCode, Gemini, ZCode, Cursor and Windsurf via a setup script
- **+** Offers filing modes: Generic, LYT, PARA and Zettelkasten, without moving existing notes
- **−** No built-in text extraction for PDF and EPUB; only metadata, hash and size
- **−** Web pages and YouTube need a separate runner; OCR needs an external tool
- **−** Notes Claude reads are sent to Anthropic's model; it is not fully offline
- **−** Native Windows cannot write to the vault; WSL is required

<sub>no GPU · Needs Claude Code, Python 3.11+, Obsidian (optional, for visual side), Bash · Models: Claude (via Claude Code), Codex, OpenCode, Gemini, ZCode · [Repo](https://github.com/agricidaniel/claude-obsidian) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/claude-obsidian/)</sub>

<a name="engram"></a>
### #&#8288;13 [Engram](https://github.com/gentleman-programming/engram) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.3k · MIT · Nov 2026</sub>

**Persistent memory store for AI coding agents, exposed over MCP.**

Engram is a single Go binary that stores coding-agent memory in a local SQLite file with FTS5 search. It exposes the memory through MCP stdio, an HTTP API, a CLI and a terminal UI, and `engram setup` configures 14 agents including Claude Code, OpenCode, Gemini CLI, Codex and Cursor. Memory can be shared via Git Sync chunks or optional project-scoped Engram Cloud replication.

- **+** Single Go binary with one SQLite file; no Node, Python or Docker required
- **+** One-command setup for 14 agents, plus manual MCP config for any other client
- **+** Memory is project-aware, resolved from explicit project, env var or cwd
- **+** Local-first, with Git Sync export and optional cloud replication for sharing
- **−** Search is SQLite FTS5 full-text; README mentions no embedding or vector retrieval
- **−** Aimed at coding agents; not a general-purpose memory layer for other apps
- **−** Codex integration needs a matching, manually restarted core; hooks never restart it
- **−** README is dense with edge-case migration and compatibility detail

<sub>no GPU · Docker + Compose · Needs SQLite (bundled) · Models: Any MCP-compatible agent · [Repo](https://github.com/gentleman-programming/engram) · [📖 Docs ↗](https://github.com/Gentleman-Programming/engram/blob/main/DOCS.md) · [🌐 Site ↗](https://engram.gentlemanprogramming.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/engram/)</sub>

<a name="basic-memory"></a>
### #&#8288;14 [basic-memory](https://github.com/basicmachines-co/basic-memory) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: known (50) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.7k · AGPL-3.0 · Nov 2026</sub>

**MCP server that stores AI memory as Markdown notes with a knowledge graph.**

Basic Memory is a Python MCP server that lets Claude, Codex, Cursor, ChatGPT and other MCP clients read and write structured Markdown notes on your disk. Notes use observations and wikilink relations that form a traversable graph, indexed in local SQLite (or Postgres) with hybrid full-text and vector search. A hosted cloud edition is sold separately; the local version is free.

- **+** Notes are plain Markdown files, editable in Obsidian or any editor, with two-way sync
- **+** Hybrid full-text and vector search via FastEmbed, with optional cross-encoder reranking
- **+** MCP tools carry read-only/destructive/idempotent hints; works with Claude, Codex, Cursor, VS Code
- **+** Ships Claude Code, Hermes and OpenClaw plugins plus shared skills from the same repo
- **−** AGPL-3.0 license may be a problem for embedding in proprietary products
- **−** Install needs uv and the --prerelease=allow flag due to a FastMCP 4 pre-release dependency
- **−** Built-in cross-device sync and mobile access are in the paid cloud; local needs Git or Syncthing
- **−** Reranking is off by default and adds latency plus a first-run model download

<sub>no GPU · Docker + Compose · Needs Python 3.12+, uv, SQLite (default) or Postgres, Milvus (optional), LiteLLM (optional) · Models: Any MCP client (Claude, Codex, Cursor, VS Code, ChatGPT), FastEmbed embeddings, jinaai/jina-reranker-v1-tiny-en reranker · [Repo](https://github.com/basicmachines-co/basic-memory) · [📖 Docs ↗](https://docs.basicmemory.com) · [🌐 Site ↗](https://basicmemory.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/basic-memory/)</sub>

<a name="semantica"></a>
### #&#8288;15 [semantica](https://github.com/semantica-agi/semantica) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Nov 2026</sub>

**Python library for building context graphs and knowledge graphs with decision provenance.**

Semantica is a Python library that ingests documents, databases and enterprise sources, extracts entities and relations, and builds a knowledge graph governed by OWL, SHACL and SKOS ontologies. It records agent decisions as graph nodes with causal links and W3C PROV-O provenance, and runs deterministic reasoning (Rete, Datalog, SPARQL). It stores to RDF or property-graph backends and is exposed through REST, an MCP server and a CLI.

- **+** Graph construction, reasoning and provenance need no LLM; LLM providers are optional
- **+** Swappable storage: Oxigraph, Jena, RDF4J, Blazegraph, Neo4j, FalkorDB, AGE, Neptune
- **+** Decisions are queryable nodes with causal chains, precedent search and PROV-O export
- **+** Connectors for Databricks, Snowflake, SAP, Kafka and Kinesis, plus MCP server and CLI
- **−** Broad scope (ontology, reasoning, decisions, analytics) means a steep learning curve
- **−** Explains only context and decisions outside the model, not the LLM's internal reasoning
- **−** Requires Python 3.11.5 or newer
- **−** Many optional backends mean extra services to run for production use

<sub>no GPU · Docker + Compose · Needs Python 3.11.5+, Optional graph stores: Oxigraph, Blazegraph, Jena, RDF4J, Neo4j, FalkorDB, AGE, Neptune, Optional vector store (e.g. FAISS) · Models: OpenAI, Anthropic, Gemini · [Repo](https://github.com/semantica-agi/semantica) · [▶️ Demo ↗](https://www.youtube.com/watch?v=QfnNZg4-dZA) · [📖 Docs ↗](https://docs.getsemantica.ai/) · [🌐 Site ↗](https://getsemantica.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/semantica/)</sub>

<a name="obsidian-second-brain"></a>
### #&#8288;16 [obsidian-second-brain](https://github.com/eugeniughelbur/obsidian-second-brain) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.5k · MIT · Nov 2026</sub>

**Claude Code plugin that saves chats into a linked Obsidian vault and recalls them.**

A Claude Code plugin, also usable from Codex, Gemini CLI, OpenCode and others, that gives agents persistent memory in an Obsidian vault of plain Markdown. Slash commands save conversations as linked notes, ingest URLs, PDFs, Word files, audio and screenshots, and answer questions from the vault. Optional scheduled agents reconcile contradictions and write a morning brief. A separate Crew feature shares a job log across agents without Obsidian.

- **+** Notes stay as local Markdown files; core commands need no API keys
- **+** Ingest rewrites existing pages rather than only appending new notes
- **+** Runs in Claude Code, Codex, Gemini CLI, OpenCode and Grok Bot
- **+** MIT licensed, with a changelog and recent releases
- **−** Large surface of about 48 commands; README suggests starting with three
- **−** Research commands depend on external services such as Perplexity, Grok and Gemini
- **−** Word and OpenDocument ingest needs a separate LibreOffice 26.2+ install
- **−** Presentation and spreadsheet formats are out of scope for ingest

<sub>Needs Obsidian, Claude Code (or Codex, Gemini CLI, OpenCode), Python 3.10+, LibreOffice 26.2+ (Word/ODT ingest), Local Whisper (audio ingest), ffmpeg (YouTube --visual), Perplexity, Grok, Gemini (optional research) · Models: Claude Code, Codex, Gemini CLI, OpenCode, Grok Bot · [Repo](https://github.com/eugeniughelbur/obsidian-second-brain) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/obsidian-second-brain/)</sub>

<a name="tencentdb-agent-memory"></a>
### #&#8288;17 [tencentdb-agent-memory](https://github.com/tencentcloud/tencentdb-agent-memory) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · custom license · Nov 2026</sub>

**Team memory layer for coding agents: chat memory, skills, wiki, code graph.**

Runs a memory core, a web panel (Memory Hub) and an LLM proxy between agents such as Claude Code, Codex, OpenClaw, Hermes and OpenCode and their model. It distills conversations into four layers (L0 to L3), extracts reusable skills, and indexes documents and code into a wiki and a call graph. Assets carry owner, version and private/team/ACL visibility, and can be bound to specific agents.

- **+** Proxy integration: most agents only need a changed base URL and user key
- **+** Retrieval combines BM25, vectors and RRF, capped by item count, characters and timeout
- **+** Per-asset owner, version and private/team/restricted ACLs, with per-agent binding
- **+** Imports codebases, documents and past sessions to cold-start new agents
- **−** Three services to run, plus two separate sets of LLM parameters to configure
- **−** MongoDB storage backend is experimental and off by default
- **−** License detected as NOASSERTION, while the README badge says MIT
- **−** Only one benchmark reported: PersonaMem, 48% to 76%

<sub>Docker · Needs Docker, LLM API (memory and proxy parameter groups), MongoDB (optional, experimental) · Models: OpenAI Chat Completions-compatible endpoints · port 8125 · [Repo](https://github.com/tencentcloud/tencentdb-agent-memory) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tencentdb-agent-memory/)</sub>

<a name="obsidian-wiki"></a>
### #&#8288;18 [obsidian-wiki](https://github.com/ar9av/obsidian-wiki) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: known (39) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.8k · MIT · Nov 2026</sub>

**Markdown skills that let coding agents compile notes into an Obsidian wiki.**

obsidian-wiki is a set of 39 markdown skills, plus an optional Python CLI and library, that has agents such as Claude Code, Cursor and Codex ingest docs, chats and URLs into linked markdown pages in an Obsidian vault. It follows Karpathy's LLM Wiki pattern: merge knowledge into existing pages, tag claims as extracted or inferred, and answer queries with wikilink citations. Session hooks inject a recap at start and suggest a capture at end.

- **+** Knowledge is plain markdown on disk, readable, greppable and diffable; no vector store or API key
- **+** Manifest tracks ingested sources, so repeat runs process only changed files
- **+** Works across many agents from one skills directory, including Claude Code, Cursor, Codex and Gemini CLI
- **+** Lint, dedup and cross-linking skills flag contradictions, orphans and speculative pages
- **−** Quality depends on the host agent and model; the project ships no model of its own
- **−** Audio and video are skipped, and Office file handling depends on the agent
- **−** Benchmark is small: n=2 per cell on one 38-page vault
- **−** Claude Code plugin install omits the session hooks and the CLI

<sub>no GPU · Docker + Compose · Needs Obsidian (optional viewer), An AI coding agent such as Claude Code, Cursor or Codex · Models: Any model via the host agent · [Repo](https://github.com/ar9av/obsidian-wiki) · [📖 Docs ↗](https://github.com/Ar9av/obsidian-wiki/blob/main/docs/installation.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/obsidian-wiki/)</sub>

<a name="honcho"></a>
### #&#8288;19 [Honcho](https://github.com/plastic-labs/honcho) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.3k · AGPL-3.0 · Nov 2026</sub>

**Memory service that builds per-peer representations from stored agent conversations.**

Honcho is a FastAPI server with Python and TypeScript SDKs that stores messages on sessions, reasons over them in the background, and returns peer representations, session context, hybrid search results, or natural-language answers. Users, agents, groups and ideas are modeled as peers inside workspaces. It runs managed at api.honcho.dev or self-hosted, and has plugins for Claude Code, Codex, Cursor, OpenCode, Kilo Code, OpenClaw and MCP clients.

- **+** Peer model covers humans and agents, with optional modeling of what one peer knows about another
- **+** Hybrid BM25 plus vector search; context output formats for OpenAI and Anthropic messages
- **+** First-party plugins for Claude Code, Codex, Cursor, OpenCode, Kilo Code and OpenClaw share one config file
- **+** Python and TypeScript SDKs in the repo; honcho-cli starts a local stack
- **−** Background reasoning is asynchronous, so new messages may not appear in chat responses right away
- **−** Self-hosting needs an LLM provider key and Postgres with pgvector
- **−** AGPL-3.0 license may constrain use inside proprietary network services
- **−** Benchmark claims point to the project's own evals page; the README gives no figures

<sub>no GPU · Docker · Needs PostgreSQL with pgvector, LLM provider API key (e.g. OpenAI, OpenRouter), Redis (optional), Docker (optional) · Models: OpenAI, OpenRouter · port 8000 · [Repo](https://github.com/plastic-labs/honcho) · [▶️ Demo ↗](https://app.honcho.dev) · [📖 Docs ↗](https://honcho.dev/docs/v3/documentation/reference/sdk) · [🌐 Site ↗](https://honcho.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/honcho/)</sub>

<a name="reme"></a>
### #&#8288;20 [reme](https://github.com/agentscope-ai/reme) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: known (40) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.8k · Apache-2.0 · Nov 2026</sub>

**File-based Markdown memory store for AI agents with BM25 search.**

ReMe stores agent memory as plain Markdown files with frontmatter and wikilinks, organized into session, daily and digest layers. It runs as a local service (CLI, HTTP, MCP or embedded Python API) that indexes files with BM25 and optional embeddings, and uses an LLM to consolidate conversations and resources into long-term notes. Plugins exist for Claude Code, Codex, Qoder, OpenClaw, Hermes and DeepSeek Harness.

- **+** Memory is ordinary Markdown; indexes under metadata/ are rebuildable from the files
- **+** File operations, BM25 search and wikilink traversal work without LLM credentials
- **+** Integrations for Claude Code, Codex, Qoder, OpenClaw, Hermes, plus CLI, HTTP, MCP and Python
- **+** Embeddings are off by default, so no embedding model or key is needed to start
- **−** auto_memory, auto_resource, auto_dream and proactive refresh require an external LLM API key
- **−** Semantic search requires editing default.yaml to enable embedding components
- **−** Requires running a separate long-lived service (reme start) alongside the agent
- **−** Source install needs Node.js 22.13+ to build the Studio static assets

<sub>no GPU · Docker + Compose · Needs Python 3.11+, OpenAI-compatible LLM API (for auto features), Optional embedding API, Docker Compose 2.24.0+ (Docker path) · Models: OpenAI-compatible LLM endpoints (e.g. DashScope), Optional OpenAI-compatible embeddings · port 2333 · [Repo](https://github.com/agentscope-ai/reme) · [▶️ Demo ↗](https://reme.agentscope.io/studio/?lang=en) · [📖 Docs ↗](https://reme.agentscope.io/en/configuration) · [🌐 Site ↗](https://reme.agentscope.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/reme/)</sub>

<a name="letta"></a>
### #&#8288;21 [letta-ai/letta-code](https://github.com/letta-ai/letta-code) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (43) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.9k · Apache-2.0 · Nov 2026</sub>

**Stateful CLI agent harness with self-editing memory, skills and chat integrations.**

Letta Code is a TypeScript CLI for running long-lived agents that keep memory, skills and prompts across sessions and rewrite them over time. Agents can be driven from the terminal, from chat.letta.com (including mobile), or through Telegram, Slack, Discord and custom channels. Memory is tracked in git (MemFS), and agents can use subagents, hooks, crons and permission modes.

- **+** Memory blocks and skills are tracked in git and can sync to your own GitHub repo
- **+** Reaches the same agent from CLI, browser, Telegram, Slack and Discord
- **+** Supports hooks, crons, heartbeats, subagents and configurable permission modes
- **+** Installs skills from GitHub, ClawHub and Hermes Skills Hub
- **−** Letta Cloud is the default backend; local mode must be chosen at setup
- **−** Remote computers and secrets require signing in with Letta
- **−** AgentFile export and import have been removed
- **−** Automatic dreaming is off by default on native Windows

<sub>no GPU · Docker · Needs Node.js or Python 3.9+ (uv/pipx), Letta Cloud (default backend), LLM API keys via /connect · Models: OpenAI / ChatGPT, Anthropic, Z.ai coding plan · [Repo](https://github.com/letta-ai/letta-code) · [▶️ Demo ↗](https://chat.letta.com) · [📖 Docs ↗](https://docs.letta.com/letta-code/cli) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/letta/)</sub>

<a name="lossless-claw"></a>
### #&#8288;22 [lossless-claw](https://github.com/martian-engineering/lossless-claw) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: fair (80) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.9k · MIT · Nov 2026</sub>

**OpenClaw plugin that replaces sliding-window compaction with a summary DAG over SQLite.**

Lossless-claw is a context-engine plugin for OpenClaw. It stores every message in SQLite, summarizes older chunks with a configured LLM, and condenses those summaries into a DAG. Each turn it assembles context from summaries plus recent raw messages, and exposes lcm_grep, lcm_describe and lcm_expand tools so agents can recover original detail. It also ships an lcm CLI, /lossless slash commands and a session migration tool.

- **+** Keeps every raw message in SQLite; summaries link back to source messages
- **+** Agent tools (lcm_grep, lcm_describe, lcm_expand) recover details from compacted history
- **+** Summary and expansion models configurable separately, with per-session spend guard
- **+** Includes read-only lcm CLI, backup and doctor commands, and JSONL session backfill tool
- **−** Works only with OpenClaw 2026.9.2 or newer
- **−** Summarization consumes LLM calls, adding provider cost and quota use
- **−** Many tuning options (thresholds, fanout, deferred debt) make configuration involved
- **−** Programmatic control API unavailable until the host supports the required endpoints

<sub>no GPU · Docker · Needs OpenClaw 2026.9.2+, Node.js 22+, SQLite, LLM provider configured in OpenClaw · Models: Any provider configured in OpenClaw (e.g. openai/gpt-5.4-mini) · [Repo](https://github.com/martian-engineering/lossless-claw) · [▶️ Demo ↗](https://losslesscontext.ai) · [🌐 Site ↗](https://martian.engineering/?utm_source=github&utm_medium=readme&utm_campaign=lossless-claw) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lossless-claw/)</sub>

<a name="letta-ai-letta"></a>
### #&#8288;23 [letta-ai/letta](https://github.com/letta-ai/letta) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: widely used (82) · Freshness: active (99) · Maintenance: patchy (48) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · Apache-2.0 · Oct 2026</sub>

**Stateful agents with persistent memory, run from a terminal UI or App Server.**

Letta (formerly MemGPT) builds agents that keep memory and improve over time. This repository now only points to letta-ai/letta-code, which holds the agent harness, terminal UI, App Server and channel integrations. The original V1 API server is retired and kept on the archive branch.

- **+** Installs from npm and runs as a terminal UI with `letta`
- **+** `letta server` runs the App Server for local or self-hosted agents
- **+** Reachable through Slack, Telegram, Discord and custom channels
- **+** TypeScript Agent SDK for embedding agents in applications
- **−** This repo holds no active source; development moved to letta-code
- **−** Original V1 API server is retired and only on the archive branch
- **−** Cross-computer memory and identity depend on Letta Cloud
- **−** Agent SDK is TypeScript only according to the README

<sub>Needs Node.js (npm) · [Repo](https://github.com/letta-ai/letta) · [▶️ Demo ↗](https://chat.letta.com) · [📖 Docs ↗](https://docs.letta.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/letta-ai-letta/)</sub>

<a name="vestige"></a>
### #&#8288;24 [vestige](https://github.com/samvallad33/vestige) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 664 · AGPL-3.0 · Nov 2026</sub>

**Append-only, hash-chained memory store for agents, exposed over MCP.**

Vestige is a Rust memory kernel for AI agents that records facts in an append-only, hash-chained, signed log with bi-temporal validity and FSRS-6 decay. Retrieval uses deterministic rules and retroactive salience backfill instead of embeddings or LLM calls. It connects to agents as an MCP server (`vestige-mcp`) and runs on CPU.

- **+** No embeddings, LLM, GPU or API keys needed; benchmarked on an i5-2520M with 8 GB RAM
- **+** Append-only signed log keeps superseded facts and returns receipts for admitted writes
- **+** Reproducible retrieval benchmarks on LoCoMo, LongMemEval-S, BEAM and MemoryAgentBench
- **+** Optional Operator gate with 15-minute one-use owner permits for write control
- **−** Benchmarks measure top-k retrieval only, not answer accuracy
- **−** LoCoMo turn-level exact R@1 is 47.92%, so top-slot misses are common
- **−** AGPL-3.0 license restricts use in closed-source network services
- **−** Install goes through an npx initializer; no standalone setup steps in the README

<sub>no GPU · Docker · Needs Node.js (npx installer) · [Repo](https://github.com/samvallad33/vestige) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vestige/)</sub>

<a name="memanto"></a>
### #&#8288;25 [memanto](https://github.com/moorcheh-ai/memanto) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (23) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · MIT · Nov 2026</sub>

**Memory layer for coding agents that supersedes stale facts and flags conflicts.**

Memanto stores agent memory without calling an LLM on write, and recalls it through the Moorcheh search engine, run as a local Docker container or a cloud service. New facts supersede old ones with history kept, conflicts between agents are flagged, and expiry follows user-written policies. It connects through a CLI, MCP server, REST API and Python, TypeScript and Go SDKs.

- **+** No LLM call on write, so memories are recallable immediately
- **+** Supersedes outdated facts, keeps dated history, and supports as-of recall
- **+** Fully local mode with Docker and Ollama; exports to plain Markdown (OKF)
- **+** Imports from Mem0, Letta, Supermemory, Zep and Hindsight with one command
- **−** Recall depends on Moorcheh, run as a Docker container or via a cloud key
- **−** Own adversarial benchmark shows more stale and injected records in top results than Mem0
- **−** Default setup is Memanto Cloud; fully local mode needs Docker and Ollama

<sub>Docker + Compose · Needs Docker, Ollama, Moorcheh (local container or cloud API key) · Models: Ollama (local) · [Repo](https://github.com/moorcheh-ai/memanto) · [📖 Docs ↗](https://docs.memanto.ai) · [🌐 Site ↗](https://memanto.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/memanto/)</sub>

<a name="memmy-agent"></a>
### #&#8288;26 [memmy-agent](https://github.com/memtensor/memmy-agent) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · MIT · Nov 2026</sub>

**Local memory service and agent that shares context across coding agents.**

Memmy runs a local memory service (default http://127.0.0.1:18960) that records your AI collaboration history as structured memory. It exposes that memory to agents such as Claude Code, Codex, Cursor and OpenCode through a Skill and hooks. It also ships its own agent runtime, as a desktop app and a CLI/TUI, with an OpenAI-compatible API on port 18990.

- **+** Memory is shared across Claude Code, Codex, Cursor, OpenCode and others via Skill and hooks
- **+** Memory service can run alone, with a memmy-memory CLI for search, add and get
- **+** BYOK config in ~/.memmy/config.yaml; serves an OpenAI-compatible API on :18990
- **+** Install does not modify existing agents until you run memmy-memory init
- **−** Linux installer requires a systemd user session and specific Node.js 22, 24 or 26 versions
- **−** No Docker or compose files provided
- **−** Desktop trial runs on hosted credits and needs sign-up before switching to BYOK
- **−** Team sharing and non-conversation memory sources are only roadmap items

<sub>Needs Node.js 22+, systemd user session (Linux CLI installer), LLM provider API key (BYOK) · Models: OpenAI (e.g. openai/gpt-4.1), Other providers via config.yaml · port 18990 · [Repo](https://github.com/memtensor/memmy-agent) · [📖 Docs ↗](https://memmy.bot/docs/) · [🌐 Site ↗](https://memmy.bot/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/memmy-agent/)</sub>

<a name="ob1"></a>
### #&#8288;27 [ob1](https://github.com/natebjones-projects/ob1) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: patchy (33) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.8k · custom license · Sep 2026</sub>

**Shared Postgres vector memory exposed to any AI client over MCP.**

Open Brain is a guide and contribution repo for building a personal memory store: a Supabase Postgres database with vector search, an MCP server deployed as an edge function, and Slack or Discord capture. Claude, ChatGPT, Cursor and Claude Code connect to the same database. The repo adds extensions, import recipes (ChatGPT, Obsidian, Gmail, X), agent skills, schemas, dashboards and a Kubernetes option.

- **+** One MCP-exposed database shared across Claude, ChatGPT, Cursor and Claude Code
- **+** Many import recipes: ChatGPT, Perplexity, Obsidian, Gmail, X, Instagram, Google Takeout
- **+** Kubernetes option runs on plain PostgreSQL with pgvector, no Supabase required
- **+** Community contributions go through automated PR review, each with its own README
- **−** Default setup depends on Supabase, Slack and an AI gateway, not one self-contained binary
- **−** Repo of guides, SQL and edge functions, not an installable package
- **−** License is detected as NOASSERTION, so reuse terms need checking
- **−** Setup takes about 45 minutes and several hosted accounts

<sub>no GPU · Needs Supabase, PostgreSQL with pgvector, Slack or Discord, AI gateway · Models: MCP clients: Claude, ChatGPT, Cursor, Claude Code · [Repo](https://github.com/natebjones-projects/ob1) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ob1/)</sub>

<a name="m-flow"></a>
### #&#8288;28 [m_flow](https://github.com/flowelement-xinliuyuansu/m_flow) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: known (48) · Freshness: active (90) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.5k · Apache-2.0 · Aug 2026</sub>

**Graph-based memory engine that scores retrieval by evidence paths.**

M-flow is a Python memory layer for AI agents that ingests text and files into a four-level graph (Episode, Facet, FacetPoint, Entity). Queries are anchored by vector search at the matching granularity, then scored by graph path cost, and whole Episode bundles are returned. It ships a Python API, a CLI, a FastAPI backend, a Next.js console and an MCP server.

- **+** Multi-granularity graph retrieval; reports 81.8% on LoCoMo-10 and 89% on LongMemEval
- **+** Resolves pronouns to named entities before indexing, so later turns stay retrievable
- **+** Supports LanceDB, Neo4j, pgvector, ChromaDB, KùzuDB and Pinecone backends
- **+** Includes MCP server, CLI, web console and 50+ file format ingestion
- **−** Benchmark figures are self-reported and compared against vendor cloud products
- **−** Graph building runs through an LLM at ingestion, so it needs an API key or local model
- **−** Summaries keep all details, so retrieved context is longer than with compressed approaches
- **−** Face-aware playground needs a separate companion service and a camera

<sub>Docker + Compose · Needs LLM API key, LanceDB, Neo4j, PostgreSQL/pgvector, ChromaDB, KùzuDB or Pinecone · Models: OpenAI, Anthropic, Mistral, Groq, Ollama · [Repo](https://github.com/flowelement-xinliuyuansu/m_flow) · [🌐 Site ↗](https://m-flow.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/m-flow/)</sub>

<a name="agentic-context-engine"></a>
### #&#8288;29 [agentic-context-engine](https://github.com/kayba-ai/agentic-context-engine) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: patchy (48) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.6k · Apache-2.0 · Sep 2026</sub>

**Python library that lets agents learn strategies from past runs.**

ACE adds a learning loop to LLM agents. A Reflector analyzes execution traces, and a SkillManager adds, refines or removes strategies in a persistent Skillbook that is fed back to the agent on later tasks. The Reflector writes and runs Python in a sandbox to search traces. Runners cover LiteLLM models, browser-use, LangChain and Claude Code. It needs no fine-tuning or vector database.

- **+** Learns from pre-recorded traces via TraceAnalyser, without re-running tasks
- **+** Runners for LiteLLM (100+ providers), browser-use, LangChain and Claude Code
- **+** No fine-tuning, training data or vector database required
- **+** Composable pipeline steps with requires/provides contracts; ships CLI and MCP server
- **−** Benchmarks are self-reported: one Tau2 airline run and one Claude Code translation
- **−** Every learning step makes LLM calls, which adds API cost
- **−** Managed trace upload and fixes shipped as PRs belong to the hosted Kayba service
- **−** Skillbook quality depends on supplied feedback or traces; no safeguards against bad strategies stated

<sub>no GPU · Needs LLM provider API key (OpenAI, Anthropic, or others via LiteLLM), PydanticAI · Models: OpenAI, Anthropic, Google, Bedrock, Groq · [Repo](https://github.com/kayba-ai/agentic-context-engine) · [📖 Docs ↗](https://kayba-ai.github.io/agentic-context-engine/latest/) · [🌐 Site ↗](https://kayba.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agentic-context-engine/)</sub>

<a name="tradememory-protocol"></a>
### #&#8288;30 [tradememory-protocol](https://github.com/mnemox-ai/tradememory-protocol) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · MIT · Oct 2026</sub>

**Local trade memory and pre-order policy brake for AI trading agents.**

TradeMemory is an MCP server that syncs your fills (Hyperliquid, Alpaca, MT5, Binance spot) into local SQLite and reports where your own history loses money. Agents recall losing trades before proposing an order through 20 MCP tools and a REST API. A preview proxy extra sits in front of Alpaca's MCP server and refuses orders that break a policy you set. Decisions are SHA-256 hash-chained.

- **+** Local SQLite storage; the memory server never places orders or asks for broker keys
- **+** Syncs Hyperliquid fills without a key and Alpaca with read-only keys
- **+** Proxy refuses unclassified tools, entries without a stop, and orders it cannot evaluate
- **+** Hash-chained decision log with daily Merkle roots and RFC 3161 timestamping
- **−** Broker brake is a preview and supports only Alpaca; options and trailing orders are refused
- **−** Empirical validation is n=14 trades; README says that is too few to conclude anything
- **−** Proxy extra needs Python 3.12+ and installs Mnemox Control, which is AGPL-3.0
- **−** Audit log is tamper-evident, not tamper-proof; no record signing or public-log anchoring

<sub>no GPU · Docker + Compose · Needs SQLite, Alpaca MCP server (proxy), Mnemox Control (proxy extra), RFC 3161 timestamp authority · Models: Claude Desktop, Claude Code, Cursor, Anthropic API (evolution), DeepSeek (replay) · [Repo](https://github.com/mnemox-ai/tradememory-protocol) · [🌐 Site ↗](https://mnemox.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tradememory-protocol/)</sub>

<a name="nautilus-compass"></a>
### #&#8288;31 [nautilus-compass](https://github.com/chunxiaoxx/nautilus-compass) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (3) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.3k · custom license · Nov 2026</sub>

**Local long-term memory and drift detection for MCP clients.**

Stores raw text locally, embeds it with BGE-m3 and retrieves it with hybrid BM25 plus dense search. It exposes 17 MCP tools and installs as hooks for Claude Code, with config patching for Cursor, Cline, Continue.dev and Zed. It also scores each prompt against failure-pattern anchors to flag drift. The README reports LongMemEval-S P@5 of 0.978 against mem0's 0.916, from its own reproduction.

- **+** No extraction LLM at ingest; BGE-m3 embeddings run locally, so data stays on your machine
- **+** Reproduction script and evidence JSON published, including failed experiments like cross-encoder reranking
- **+** Drift check reports p95 latency under 50 ms, so it can run on every prompt
- **+** Installer patches Claude Desktop, Cursor, Cline, Continue.dev and Zed MCP configs
- **−** mem0 comparison is the authors' own reproduction, each side on its own embedder
- **−** License detected as NOASSERTION; README badge says Modified MIT, so read the terms
- **−** Needs a BGE-m3 daemon; first recall after idle can take up to 90 s
- **−** README mixes memory with judging, leaderboards and several packages, which blurs scope

<sub>GPU optional · Docker + Compose · Needs BGE-m3 embedding model, Python · Models: BGE-m3 · [Repo](https://github.com/chunxiaoxx/nautilus-compass) · [▶️ Demo ↗](https://huggingface.co/spaces/chunxiaox/nautilus-compass) · [🌐 Site ↗](https://nautilus.social) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nautilus-compass/)</sub>

<a name="memmachine"></a>
### #&#8288;32 [memmachine](https://github.com/memmachine/memmachine) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: known (34) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.1k · Apache-2.0 · Nov 2026</sub>

**Long-term memory server for AI agents with episodic and profile memory.**

MemMachine stores and retrieves agent memory across sessions through a REST API, Python and TypeScript SDKs, and an MCP server. It keeps episodic memory in a Neo4j graph database and user profile facts in SQL, alongside short-term working memory. Integrations are listed for LangChain, LangGraph, CrewAI, LlamaIndex, AWS Strands, n8n, Dify and FastGPT.

- **+** Separate working, episodic (graph) and profile (SQL) memory types
- **+** Python SDK, REST API, TypeScript SDK and stdio/HTTP MCP server
- **+** Integrations for LangChain, LangGraph, CrewAI, LlamaIndex, n8n, Dify, FastGPT
- **+** Works with OpenAI, Anthropic, Bedrock, Ollama and other LLM providers
- **−** Requires running a separate server plus Neo4j and SQL storage
- **−** Quick Start snippet has a typo: duplicated 'import import'
- **−** README gives no benchmarks or memory retrieval accuracy numbers
- **−** Managed platform exists, so some convenience pushes toward the hosted service

<sub>Docker + Compose · Needs Neo4j, SQL database · Models: OpenAI, Anthropic, Bedrock, Ollama · port 8080 · [Repo](https://github.com/memmachine/memmachine) · [📖 Docs ↗](https://docs.memmachine.ai) · [🌐 Site ↗](https://memmachine.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/memmachine/)</sub>

<a name="voicemem"></a>
### #&#8288;33 [voicemem](https://github.com/xzf-thu/voicemem) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: known (30) · Freshness: active (100) · Maintenance: fair (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · Apache-2.0 · Sep 2026</sub>

**Memory engine for voice agents that retrieves while the user is still speaking.**

VoiceMem is a Python library that gives real-time voice agents long-term memory. It ingests audio or text, runs ASR, speaker ID, emotion and embedding extraction, and keeps facts and emotion/persona data in separate stores. Retrieval starts speculatively mid-utterance. The repo also ships a web demo, memory-reading Qwen and Step-Audio models, the ChatMem-400K dataset, and finetuning and evaluation scripts.

- **+** Streaming search starts mid-utterance, so memory is ready when VAD ends the turn
- **+** Separate factual and emotion/persona stores, plus a text-only leftbrain_only mode
- **+** LoCoMo evaluation script is included, with an --inspect dry run that makes no API calls
- **+** Reply model is swappable through a callback; the memory side stays unchanged
- **−** Writing memories needs an OpenAI API key for fact extraction
- **−** Local ASR, speaker and embedding models must be downloaded separately from Hugging Face
- **−** Early releases (v0.0.1, v0.0.2); API stability unknown
- **−** No Docker or compose files; the web demo requires cloning the repo

<sub>GPU optional · Needs OpenAI API (fact extraction on write, chat, TTS, Realtime), Hugging Face model download (VoiceMem_Default_Models_Env), mem0, FunASR, sherpa-onnx · Models: Qwen2.5-Omni, Qwen3-Omni, Step-Audio2-Mini, OpenAI API, multilingual-e5-small · port 8787 · [Repo](https://github.com/xzf-thu/voicemem) · [🌐 Site ↗](https://xzf-thu.github.io/VoiceMem/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/voicemem/)</sub>

<a name="memori"></a>
### #&#8288;34 [memori](https://github.com/memorilabs/memori) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · custom license · Sep 2026</sub>

**Long-term memory layer for LLM agents, with Python and TypeScript SDKs.**

Memori wraps an LLM client (OpenAI, Anthropic, Gemini, Bedrock, DeepSeek, Grok) and records conversations per entity, process and session. It extracts structured memories such as facts, preferences, rules, skills and relationships, and recalls them on later calls. It also ships plugins for OpenClaw and Hermes Agent and a hosted MCP endpoint. The default path uses Memori Cloud with an API key; self-hosting is via a separate BYODB mode.

- **+** Registers on an existing LLM client; sync, async and streamed calls are covered
- **+** Extracts typed memories: facts, preferences, rules, skills, relationships, events
- **+** Integrations for OpenClaw, Hermes Agent, LangChain, Agno, Pydantic AI and MCP clients
- **+** Reports 87% on LoCoMo at about 721 tokens per query, per its own paper
- **−** Quickstart depends on the hosted Memori Cloud and an API key
- **−** Advanced Augmentation is a hosted service, rate-limited without an account
- **−** No memories are created unless entity and process attribution is set
- **−** Benchmark figures are vendor-reported, not independently verified

<sub>no GPU · Docker + Compose · Needs Memori Cloud API key (or BYODB database), LLM provider API key · Models: OpenAI, Anthropic, Bedrock, DeepSeek, Gemini · [Repo](https://github.com/memorilabs/memori) · [📖 Docs ↗](https://memorilabs.ai/docs/memori-cloud/) · [🌐 Site ↗](https://memorilabs.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/memori/)</sub>

<a name="memvid"></a>
### #&#8288;35 [memvid](https://github.com/memvid/memvid) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: popular (77) · Freshness: active (88) · Maintenance: weak (6) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Jul 2026</sub>

**Single-file memory store for AI agents, with search built in.**

Memvid packs documents, embeddings, a Tantivy full-text index, an HNSW vector index and a time index into one append-only .mv2 file, so no database server is needed. It is a Rust library (memvid-core) with a CLI and Node.js and Python SDKs. Optional features cover local ONNX text embeddings, OpenAI embeddings, CLIP image search, Whisper transcription and encrypted capsules.

- **+** One .mv2 file holds data and indexes; no .wal, .lock or sidecar files
- **+** Append-only frames with embedded WAL give crash recovery and queries over past states
- **+** Runs offline with local ONNX embeddings (BGE, Nomic, GTE) and Whisper models
- **+** SDKs for Rust, Node.js and Python plus a CLI; Apache-2.0 licensed
- **−** Local embedding ONNX models must be downloaded manually with curl before use
- **−** Benchmark claims (+35% on LoCoMo, 0.025ms P50) come from the project itself
- **−** README gives no multi-user or concurrent-writer details for the single file
- **−** Features like predictive caching and branching are not shown in README examples

<sub>GPU optional · Docker + Compose · Needs Rust 1.85.0+, ONNX embedding model files (for vec), OpenAI API key (for api_embed only) · Models: bge-small-en-v1.5, bge-base-en-v1.5, nomic-embed-text-v1.5, gte-large, OpenAI text-embedding-3 · [Repo](https://github.com/memvid/memvid) · [▶️ Demo ↗](https://sandbox.memvid.com) · [📖 Docs ↗](https://docs.memvid.com) · [🌐 Site ↗](https://www.memvid.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/memvid/)</sub>

<a name="skillclaw"></a>
### #&#8288;36 [skillclaw](https://github.com/amap-ml/skillclaw) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: patchy (46) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.8k · MIT · Oct 2026</sub>

**Local proxy that evolves reusable agent skills from recorded sessions.**

SkillClaw runs a local proxy exposing /v1/chat/completions and /v1/messages between an agent and its LLM. It records sessions and manages a local SKILL.md library. An optional evolve server reads sessions from shared storage (local, Alibaba OSS or S3), then deduplicates and rewrites skills with a workflow or OpenClaw-driven engine. It integrates with Hermes, Codex, Claude Code and OpenClaw.

- **+** Works with Hermes, Codex, Claude Code, OpenClaw, QwenPaw and any OpenAI-compatible API
- **+** Client-only install works alone; the evolve server is optional and can be added later
- **+** Shared storage backends: local filesystem, Alibaba OSS, S3, with optional Nacos for skills
- **+** Ships doctor/restore commands and a local dashboard for skills, sessions and version history
- **−** Automatic evolution needs a separate evolve server process plus an upstream LLM endpoint
- **−** No Docker or compose files; install is from a git clone with a shell script
- **−** Windows install is manual; no native PowerShell installer
- **−** No tagged releases; Hermes session boundaries fall back to proxy heuristics without session headers

<sub>no GPU · Needs Python 3.10+, OpenAI-compatible API or AWS Bedrock, OpenClaw (only for agent engine), Alibaba OSS or S3 (optional, for sharing) · Models: OpenAI-compatible APIs, AWS Bedrock · port 30000 · [Repo](https://github.com/amap-ml/skillclaw) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/skillclaw/)</sub>

<a name="memory-lancedb-pro"></a>
### #&#8288;37 [memory-lancedb-pro](https://github.com/cortexreach/memory-lancedb-pro) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: known (46) · Freshness: active (94) · Maintenance: patchy (48) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 4.4k · no license · Nov 2026</sub>

**LanceDB-backed long-term memory plugin for OpenClaw agents.**

OpenClaw plugin that stores preferences, decisions and project context in LanceDB and injects relevant memories before each reply. It auto-captures with LLM-based extraction into 6 categories, retrieves with vector plus BM25 search and cross-encoder reranking, and applies Weibull decay to fade low-value memories. Embeddings come from OpenAI, Jina, Gemini, Ollama or any OpenAI-compatible API.

- **+** Hybrid retrieval: vector plus BM25, fused and reranked with a cross-encoder
- **+** Per-agent, per-user and per-project scope isolation
- **+** Works with any OpenAI-compatible embedding API, including local Ollama
- **+** CLI covers export, import, upgrade, reembed and migration from built-in memory-lancedb
- **−** Tied to OpenClaw 2026.3+ plugin hooks; not usable with other agent hosts
- **−** Requires AVX CPU; AVX2 builds can crash with SIGILL unless native cosine is disabled
- **−** Changing embedding model or dimensions requires re-embedding into a fresh database
- **−** Only 4 core tools exposed by default; full toolset needs enableManagementTools

<sub>no GPU · Needs OpenClaw 2026.3+, LanceDB, Embedding provider API (OpenAI, Jina, Gemini, Ollama or compatible), AVX-capable CPU · Models: OpenAI, Jina, Gemini, Ollama, OpenAI-compatible APIs · [Repo](https://github.com/cortexreach/memory-lancedb-pro) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/memory-lancedb-pro/)</sub>

<a name="simplemem"></a>
### #&#8288;38 [simplemem](https://github.com/aiming-lab/simplemem) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: known (41) · Freshness: active (90) · Maintenance: weak (8) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.9k · MIT · Jul 2026</sub>

**Long-term memory for LLM agents, with text and multimodal backends.**

SimpleMem is a Python package that compresses dialogue into atomic, timestamped memory units and retrieves them by inferred query intent. One `simplemem` import routes to a text backend or an Omni backend (image, audio, video; FAISS plus BM25), and an EvolveMem step tunes retrieval settings on a dev set. It can run as an MCP server, either cloud-hosted or self-hosted via Docker Compose with a web UI on port 8000.

- **+** Auto-routes between text and multimodal backends from the first method called
- **+** Works with MCP clients such as Claude Desktop, Cursor, LM Studio and Cherry Studio
- **+** Offline retrieval-config tuning against your own dev questions via simplemem.optimize
- **+** Self-hostable with docker compose; data persists in ./data (LanceDB)
- **−** Needs an OpenAI-compatible API key for memory construction and retrieval
- **−** Cloud MCP endpoint is the default path; self-hosting needs JWT and encryption keys
- **−** Full multimodal use requires the Python API; MCP covers text memory only
- **−** Benchmark gains (LoCoMo F1, 30x token cut) are self-reported from the authors' papers

<sub>Docker + Compose · Needs OpenAI-compatible LLM API, LanceDB, FAISS, Docker (optional) · Models: OpenAI, Qwen, Azure OpenAI, Ollama, Requesty · port 8000 · [Repo](https://github.com/aiming-lab/simplemem) · [▶️ Demo ↗](https://aiming-lab.github.io/SimpleMem-Page) · [📖 Docs ↗](https://github.com/aiming-lab/SimpleMem/blob/main/MCP/README.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/simplemem/)</sub>

<a name="langmem"></a>
### #&#8288;39 [langmem](https://github.com/langchain-ai/langmem) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: weak (26) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · MIT · Nov 2026</sub>

**Python library giving LangGraph agents long-term memory tools and background extraction.**

LangMem is a Python library that lets agents store, search and consolidate long-term memories. It provides tools an agent calls during a conversation to write and search memories, a background manager that extracts and updates memories, and prompt refinement helpers. Persistence goes through LangGraph's BaseStore, or any storage you wire to its functional core API.

- **+** Hot-path memory tools plus a background manager cover both write patterns
- **+** Core API is storage-agnostic; LangGraph BaseStore integration is built in
- **+** Works with DB-backed LangGraph stores such as AsyncPostgresStore for persistence
- **+** Installs with one pip command and a few lines of setup
- **−** Examples and native integration assume LangGraph; other stacks must use the functional core
- **−** Quickstart InMemoryStore loses memories on restart
- **−** Needs an external LLM provider API key and an embedding model
- **−** Library only: no standalone server or UI

<sub>no GPU · Needs LangGraph, LLM provider API key (e.g. Anthropic), Embedding model (e.g. OpenAI text-embedding-3-small), Postgres (optional, for persistent store) · Models: Anthropic, OpenAI · [Repo](https://github.com/langchain-ai/langmem) · [📖 Docs ↗](https://langchain-ai.github.io/langmem/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/langmem/)</sub>

<a name="memory-os"></a>
### #&#8288;40 [memory-os](https://github.com/claudiodrews/memory-os) <sub>score [23](../README.md#-how-we-rank "Score 23/100. Adoption: niche (6) · Freshness: recent (71) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.4k · MIT · Jun 2026</sub>

**Seven-layer long-term memory for Hermes Agent, backed by Qdrant and SQLite.**

Memory OS adds persistent memory to Hermes Agent through seven layers: workspace markdown files, SQLite session search with FTS5, a trust-scored fact store, a forked Icarus plugin, Qdrant hybrid vector search, an auto-curated wiki, and a ground-truth prompt layer. Context is injected before each LLM call and learnings are extracted afterward. Memory runs locally and the LLM provider is configurable.

- **+** Retrieval falls back from hybrid to dense to lexical to SQLite if needed
- **+** Gated injection with per-session dedup and a social-closer filter limits token use
- **+** Trust-scored facts, weekly decay scanner and cosine >0.92 semantic dedup
- **+** Memory data stays local; works with OpenRouter, OpenAI, Anthropic or Ollama
- **−** Tied to Hermes Agent; not usable as a standalone memory library
- **−** Needs Qdrant, Redis and an ARQ worker running in Docker
- **−** Bundled Icarus fork is not upstream-compatible, so upstream changes need manual merging
- **−** Installs via curl-pipe-to-bash script; no tagged releases

<sub>Docker + Compose · Needs Hermes Agent, Docker, Qdrant, Redis, ARQ Worker, Python 3.11+, SQLite · Models: OpenRouter, OpenAI, Anthropic, Ollama · [Repo](https://github.com/claudiodrews/memory-os) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/memory-os/)</sub>

<a name="memoryos"></a>
### #&#8288;41 [memoryos](https://github.com/bai-lab/memoryos) <sub>score [22](../README.md#-how-we-rank "Score 22/100. Adoption: niche (12) · Freshness: recent (60) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · Apache-2.0 · Jul 2026</sub>

**Tiered short, mid and long-term memory for LLM agents, with MCP server.**

MemoryOS is a Python library that stores agent conversations in short-term, mid-term and long-term persona tiers. It promotes content between tiers by a heat threshold, retrieves context across them and builds a user profile. It ships as a PyPI package (memoryos-pro), an MCP server with add_memory, retrieve_memory and get_user_profile tools, a ChromaDB variant, and a playground app.

- **+** Three memory tiers with heat-based promotion and automatic user profile and knowledge updates
- **+** MCP server with three tools, documented for Claude Desktop, Cline and Cursor
- **+** Uses any OpenAI-style endpoint, including vLLM; embeddings BGE-M3, Qwen3-Embedding or MiniLM
- **+** LoCoMo evaluation scripts included, plus an EMNLP 2025 paper
- **−** Last tagged release is July 2025, though commits continue
- **−** Summarizing and profiling need LLM calls, so an API or local LLM is required
- **−** PyPI, MCP and ChromaDB variants sit in separate folders with separate requirements
- **−** README says detailed documentation is still coming soon

<sub>GPU optional · Docker · Needs OpenAI-compatible LLM API, ChromaDB (optional variant) · Models: OpenAI, Anthropic, Deepseek-R1, Qwen3, vLLM · [Repo](https://github.com/bai-lab/memoryos) · [▶️ Demo ↗](https://baijia.online/memoryos/) · [📖 Docs ↗](https://bai-lab.github.io/MemoryOS/docs) · [🌐 Site ↗](https://baijia.online/memoryos/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/memoryos/)</sub>

<a name="memobase"></a>
### #&#8288;42 [memobase](https://github.com/memodb-io/memobase) <sub>score [15](../README.md#-how-we-rank "Score 15/100. Adoption: known (32) · Freshness: quiet (17) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.0k · Apache-2.0 · Jan 2026</sub>

**User-profile memory backend for LLM apps with event timeline.**

Memobase is a FastAPI server backed by Postgres and Redis that builds a structured per-user profile (topic, sub_topic, content) and an event timeline from chat blobs. Chats go into a per-user buffer and are batch-processed on flush, using a fixed 3 LLM calls per run since 0.0.40. A context API packs profile and recent events into a prompt string. Python, Node and Go SDKs and an MCP server are provided.

- **+** Configurable profile schema controls which user attributes are captured
- **+** Buffered batch processing keeps LLM calls fixed at 3 per run
- **+** Event timeline supports time-related queries alongside profiles
- **+** SDKs for Python, Node and Go, plus MCP server and HTTP API
- **−** Memory is per-user profile based, not built as a general RAG or search engine
- **−** Self-hosting needs Postgres, Redis and an external LLM and embedding API
- **−** Memory updates lag until the buffer flushes (about 1024 tokens or 1 hour idle)
- **−** No tagged release is listed for the repository

<sub>no GPU · Needs PostgreSQL, Redis, LLM API, Embedding API · Models: OpenAI-compatible APIs, Ollama · port 8019 · [Repo](https://github.com/memodb-io/memobase) · [▶️ Demo ↗](https://app.memobase.io/playground) · [📖 Docs ↗](https://docs.memobase.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/memobase/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
