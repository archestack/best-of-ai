# 🗂️ Memory reviews · Best of Open-Source AI

Long-term memory engines that store and retrieve facts for agents across sessions. Back to the [leaderboard](../README.md#%EF%B8%8F-memory).

<sub>🌐 Also on the web: [Memory on archestack.com](https://archestack.com/best-of-ai/memory/), each project on its own page.</sub>

<a name="hindsight"></a>
### 🥇 [hindsight](https://github.com/vectorize-io/hindsight) <sub>score [95](../README.md#-how-we-rank "Score 95/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 61k · MIT · Nov 2026</sub>

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
### 🥈 [gbrain](https://github.com/garrytan/gbrain) <sub>score [91](../README.md#-how-we-rank "Score 91/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · MIT · Nov 2026</sub>

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
### 🥉 [MemPalace](https://github.com/mempalace/mempalace) <sub>score [90](../README.md#-how-we-rank "Score 90/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 61k · MIT · Nov 2026</sub>

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
### #&#8288;4 [Supermemory](https://github.com/supermemoryai/supermemory) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · MIT · Nov 2026</sub>

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
### #&#8288;5 [Mem0](https://github.com/mem0ai/mem0) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 69k · Apache-2.0 · Nov 2026</sub>

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

<a name="graphiti"></a>
### #&#8288;6 [Graphiti](https://github.com/getzep/graphiti) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · Apache-2.0 · Nov 2026</sub>

**Python framework for temporal knowledge graphs that track how facts change.**

Graphiti ingests text and JSON episodes into a knowledge graph of entities and facts, each with a validity window. Changed facts are invalidated rather than deleted, and every fact traces back to its source episode. Retrieval combines embeddings, BM25 and graph traversal. It runs on Neo4j, FalkorDB or Amazon Neptune, and ships an MCP server and a FastAPI service.

- **+** Facts carry validity windows; old facts are invalidated, so past state stays queryable
- **+** Every derived fact traces to its source episode
- **+** Custom entity and edge types defined with Pydantic models
- **+** Includes an MCP server and a FastAPI REST service in the repo
- **−** Needs a separate graph database: Neo4j, FalkorDB or Neptune plus OpenSearch
- **−** Defaults to OpenAI; README warns other LLMs may break structured output
- **−** Kuzu driver is deprecated and will be removed
- **−** Users, threads and retrieval tuning are left to you; Zep covers them as a hosted product

<sub>no GPU · Docker + Compose · Needs Neo4j 5.26, FalkorDB 1.1.2, or Amazon Neptune + OpenSearch Serverless, OpenAI API key (default LLM and embedder) · Models: OpenAI, Azure OpenAI, Anthropic, Google Gemini, Groq · [Repo](https://github.com/getzep/graphiti) · [🌐 Site ↗](https://www.getzep.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/graphiti/)</sub>

<a name="cognee"></a>
### #&#8288;7 [Cognee](https://github.com/topoteretes/cognee) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · Apache-2.0 · Nov 2026</sub>

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

<a name="openviking"></a>
### #&#8288;8 [OpenViking](https://github.com/volcengine/openviking) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 42k · AGPL-3.0 · Nov 2026</sub>

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

<a name="agentmemory"></a>
### #&#8288;9 [agentmemory](https://github.com/rohitg00/agentmemory) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Nov 2026</sub>

**Persistent cross-session memory for coding agents via hooks, MCP and REST.**

agentmemory captures what coding agents do through hooks, compresses it into searchable memory, and injects relevant context at the start of later sessions. It runs a local server on a pinned iii engine with no external database, exposes 54 MCP tools plus a REST API, and shares one store across Claude Code, Cursor, Codex CLI, Gemini CLI and others. Keyless mode uses BM25; embeddings are optional.

- **+** No external database; state lives in a local data directory
- **+** One server shared by 20 listed agents via hooks, MCP or REST
- **+** Keyless BM25 mode works offline; local embeddings use Xenova/all-MiniLM-L6-v2
- **+** Reports 95.2% R@5 on LongMemEval-S (README benchmark)
- **−** Keyless mode has no vector embeddings, so semantic queries can return nothing
- **−** Pins iii-engine v0.22.1 and will not attach to a different engine version
- **−** Native Windows needs a manual iii.exe install; WSL2 or Docker is the easier path
- **−** Uses four local ports (3111, 3112, 3113, 49134)

<sub>no GPU · Docker + Compose · Needs Node.js 20+, iii engine v0.22.1 · Models: Xenova/all-MiniLM-L6-v2 (local embeddings), optional LLM provider for compression · port 3113 · [Repo](https://github.com/rohitg00/agentmemory) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agentmemory/)</sub>

<a name="everos"></a>
### #&#8288;10 [everos](https://github.com/evermind-ai/everos) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Nov 2026</sub>

**Local-first agent memory runtime that stores memories as Markdown files.**

EverOS is a Python library and HTTP server that stores agent conversations, files and trajectories as Markdown, then indexes them in SQLite and LanceDB for retrieval. It separates user memory (episodes, profile) from agent memory (cases, skills) and searches by user, agent, app, project and session IDs. A single OpenRouter key enables core add, flush and keyword search; embeddings and rerank unlock hybrid search, reflection and a Knowledge Wiki.

- **+** Canonical Markdown files are editable and Git-versionable; a watcher re-syncs indexes after edits
- **+** No MongoDB, Elasticsearch or Redis needed; storage is Markdown, SQLite and LanceDB
- **+** Search can be scoped by user_id, agent_id, app_id, project_id and session_id
- **+** Offline reflection merges episode clusters and refines profiles and skills between sessions
- **−** Needs an LLM provider (OpenRouter in the quick start); no fully offline setup is described
- **−** Hybrid search, reflection and skill extraction require a separate embedding provider
- **−** Knowledge Wiki and agentic search also need a rerank provider
- **−** Office file ingestion needs LibreOffice installed on the host; no Docker setup is listed

<sub>no GPU · Needs Python 3.12+, OpenRouter API key (or other LLM provider), LibreOffice (office documents only) · Models: OpenRouter-hosted LLMs (default openai/gpt-4.1-mini), Optional embedding and rerank providers, Optional multimodal model (default google/gemini-3.8-flash) · port 8000 · [Repo](https://github.com/evermind-ai/everos) · [📖 Docs ↗](https://docs.evermind.ai) · [🌐 Site ↗](https://evermind.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/everos/)</sub>

<a name="claude-obsidian"></a>
### #&#8288;11 [claude-obsidian](https://github.com/agricidaniel/claude-obsidian) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (60) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · MIT · Oct 2026</sub>

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

<a name="memos"></a>
### #&#8288;12 [MemOS](https://github.com/memtensor/memos) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (50) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Nov 2026</sub>

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

<sub>Docker + Compose · Needs Neo4j, Qdrant, Node.js (local plugin), LLM provider API key · port 8000 · [Repo](https://github.com/memtensor/memos) · [📖 Docs ↗](https://memos-docs.openmem.net/home/overview/) · [🌐 Site ↗](https://memos.openmem.net/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/memos/)</sub>

<a name="semantica"></a>
### #&#8288;13 [semantica](https://github.com/semantica-agi/semantica) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Nov 2026</sub>

**Python library for building context graphs with decision provenance and reasoning.**

Semantica is a Python library that ingests data from files, databases, Databricks, Snowflake and SAP, extracts entities and relations, and builds a knowledge graph with W3C PROV-O provenance. It records agent decisions as graph nodes with causal links, and runs rule-based reasoning (Rete, Datalog, SPARQL) and SHACL/OWL governance. It stores graphs in RDF or property-graph backends and exposes a CLI, REST API and MCP server.

- **+** Graph construction, reasoning and provenance are deterministic; no LLM required
- **+** Swappable storage: Oxigraph, Blazegraph, Jena, RDF4J, Neo4j, FalkorDB, AGE, Neptune
- **+** Decisions stored as graph nodes with causal tracing, precedent search and PROV-O export
- **+** Connectors for Databricks, Snowflake, SAP OData, Kafka, Kinesis, plus CrewAI, LangChain, Agno integrations
- **−** Broad scope (ontology, reasoning, ingestion, analytics) means a large surface to learn
- **−** Explains context and decisions outside the LLM only, not the model's internal reasoning
- **−** Aimed at regulated enterprise use; heavy for simple agent memory needs

<sub>no GPU · Docker + Compose · Needs Optional graph stores: Neo4j, FalkorDB, Apache AGE, AWS Neptune, Blazegraph, Jena, RDF4J, Optional vector store: FAISS, Optional LLM provider: OpenAI, Anthropic, Gemini · Models: OpenAI, Anthropic, Gemini · [Repo](https://github.com/semantica-agi/semantica) · [📖 Docs ↗](https://docs.getsemantica.ai/) · [🌐 Site ↗](https://getsemantica.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/semantica/)</sub>

<a name="tencentdb-agent-memory"></a>
### #&#8288;14 [tencentdb-agent-memory](https://github.com/tencentcloud/tencentdb-agent-memory) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (77) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · custom license · Nov 2026</sub>

**Shared memory server for coding agents: chat memory, skills, wiki, code graph.**

Memory service behind a proxy: point an agent's base URL at it and it extracts layered chat memory (L0 to L3), reusable Skills, a document Wiki and a CodeGraph of repositories. Memory Hub is a web panel for teams, ownership, private/team/ACL visibility and binding assets to specific agents. Listed clients include Claude Code, Codex, CodeBuddy, Hermes and OpenClaw.

- **+** Proxy integration needs no plugin, hook or MCP server in the agent
- **+** Layered L0-L3 memory with BM25, vector and RRF retrieval, capped by budget
- **+** Per-asset ownership, versions and private/team/restricted ACL visibility
- **+** Cold-start import of codebases, documents and past conversation sessions
- **−** Setup runs three services and needs two sets of LLM parameters in .env
- **−** CodeGraph mainly supports public HTTPS repositories; private repos still being refined
- **−** Agent binding is manual; automated memory routing is still under iteration
- **−** License detected as NOASSERTION while the README badge says MIT

<sub>Docker · Needs Node.js >=22.16, LLM API (memory and proxy parameter sets), MongoDB (experimental, optional) · Models: Configurable LLM via .env (providers unknown) · port 8125 · [Repo](https://github.com/tencentcloud/tencentdb-agent-memory) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tencentdb-agent-memory/)</sub>

<a name="engram"></a>
### #&#8288;15 [Engram](https://github.com/gentleman-programming/engram) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (37) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.0k · MIT · Nov 2026</sub>

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

<a name="honcho"></a>
### #&#8288;16 [Honcho](https://github.com/plastic-labs/honcho) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: known (40) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.1k · AGPL-3.0 · Nov 2026</sub>

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

<a name="obsidian-second-brain"></a>
### #&#8288;17 [obsidian-second-brain](https://github.com/eugeniughelbur/obsidian-second-brain) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.3k · MIT · Nov 2026</sub>

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

<a name="letta-ai-letta"></a>
### #&#8288;18 [letta](https://github.com/letta-ai/letta) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: fair (52) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · Apache-2.0 · Oct 2026</sub>

**Stateful agents with persistent memory, run from a terminal UI or App Server.**

Letta (formerly MemGPT) builds agents that keep memory and learn across sessions. This repository now only points to letta-ai/letta-code, which holds the agent harness, terminal UI, App Server, channels and desktop/web runtime; the old V1 API server is archived on a branch. It installs through npm and also offers a TypeScript Agent SDK and a hosted Letta Cloud.

- **+** Installs with one npm command; `letta` starts a terminal UI, `letta server` an App Server
- **+** Reachable from desktop app, browser, Slack, Telegram, Discord and custom channels
- **+** TypeScript Agent SDK for embedding agents in applications
- **+** Apache-2.0 licensed, with old releases and tags kept for reproducibility
- **−** This repo holds no active source; code lives in letta-ai/letta-code
- **−** V1 API server is retired and only on the archive branch
- **−** Cross-device memory and identity depend on Letta Cloud
- **−** README gives no hardware, model provider or port details

<sub>Needs Node.js (npm) · [Repo](https://github.com/letta-ai/letta) · [▶️ Demo ↗](https://chat.letta.com) · [📖 Docs ↗](https://docs.letta.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/letta-ai-letta/)</sub>

<a name="obsidian-wiki"></a>
### #&#8288;19 [obsidian-wiki](https://github.com/ar9av/obsidian-wiki) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · MIT · Nov 2026</sub>

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

<a name="lossless-claw"></a>
### #&#8288;20 [lossless-claw](https://github.com/martian-engineering/lossless-claw) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.9k · MIT · Nov 2026</sub>

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

<a name="letta"></a>
### #&#8288;21 [Letta](https://github.com/letta-ai/letta-code) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.8k · Apache-2.0 · Nov 2026</sub>

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

<a name="basic-memory"></a>
### #&#8288;22 [basic-memory](https://github.com/basicmachines-co/basic-memory) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (14) · Freshness: active (100) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.5k · AGPL-3.0 · Nov 2026</sub>

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

<a name="memori"></a>
### #&#8288;23 [memori](https://github.com/memorilabs/memori) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: popular (65) · Freshness: active (100) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · custom license · Sep 2026</sub>

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

<a name="ob1"></a>
### #&#8288;24 [ob1](https://github.com/natebjones-projects/ob1) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (19) · Freshness: active (100) · Maintenance: patchy (35) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.8k · custom license · Sep 2026</sub>

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

<a name="memvid"></a>
### #&#8288;25 [memvid](https://github.com/memvid/memvid) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: popular (63) · Freshness: active (92) · Maintenance: weak (5) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Jul 2026</sub>

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

<a name="m-flow"></a>
### #&#8288;26 [m_flow](https://github.com/flowelement-xinliuyuansu/m_flow) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: niche (16) · Freshness: active (94) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.5k · Apache-2.0 · Aug 2026</sub>

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

<sub>Docker + Compose · Needs LLM API key, LanceDB, Neo4j, PostgreSQL/pgvector, ChromaDB, KùzuDB or Pinecone · Models: OpenAI, Anthropic, Mistral, Groq, Ollama · [Repo](https://github.com/flowelement-xinliuyuansu/m_flow) · [📖 Docs ↗](https://github.com/flowelement-xinliuyuansu/m_flow/blob/main/docs/RETRIEVAL_ARCHITECTURE.md) · [🌐 Site ↗](https://m-flow.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/m-flow/)</sub>

<a name="memory-lancedb-pro"></a>
### #&#8288;27 [memory-lancedb-pro](https://github.com/cortexreach/memory-lancedb-pro) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: niche (12) · Freshness: active (96) · Maintenance: patchy (44) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 4.5k · no license · Nov 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
