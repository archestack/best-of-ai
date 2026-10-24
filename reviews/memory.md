# 🗂️ Memory reviews · Best of Open-Source AI

Long-term memory engines that store and retrieve facts for agents across sessions. Back to the [leaderboard](../README.md#%EF%B8%8F-memory).

<sub>🌐 Also on the web: [Memory on archestack.com](https://archestack.com/best-of-ai/memory/), each project on its own page.</sub>

<a name="hindsight"></a>
### 🥇 [hindsight](https://github.com/vectorize-io/hindsight) <sub>score [94](../README.md#-how-we-rank "Score 94/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 53k · MIT · Oct 2026</sub>

**Agent memory server with retain, recall and reflect operations.**

Hindsight stores agent memories in banks and extracts facts, entities and timestamps from retained text using an LLM. Recall runs semantic, BM25, graph and temporal retrieval in parallel, then reranks the merged results. Background jobs consolidate facts into observations and mental models. It exposes a REST API, Python, Node.js and Go clients, a CLI, and a per-bank MCP endpoint.

- **+** Four parallel retrieval strategies merged with reciprocal rank fusion and cross-encoder reranking
- **+** Works with 25+ LLM providers, including local ollama, lmstudio and llamacpp
- **+** Built-in MCP endpoint per bank, plus 60+ listed integrations
- **+** Embedded mode runs in-process via pip with a bundled pg0 database
- **−** Every retain call requires an LLM, adding cost and latency
- **−** Accuracy claims are the vendor's own benchmarks; independent reproduction is partial
- **−** Managed Cloud and Enterprise tiers exist; feature differences from self-hosted are unclear
- **−** Minimum RAM and GPU needs are not stated in the README

<sub>Docker · Needs LLM provider (hosted or local), PostgreSQL (embedded pg0 by default), Oracle AI Database (optional) · Models: openai, anthropic, gemini, groq, bedrock · port 9999 · [Repo](https://github.com/vectorize-io/hindsight) · [📖 Docs ↗](https://hindsight.vectorize.io) · [🌐 Site ↗](https://hindsight.vectorize.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hindsight/)</sub>

<a name="mempalace"></a>
### 🥈 [MemPalace](https://github.com/mempalace/mempalace) <sub>score [90](../README.md#-how-we-rank "Score 90/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 60k · MIT · Oct 2026</sub>

**Local verbatim memory store for AI agents with semantic search and MCP.**

MemPalace stores conversation history and project files as verbatim text, without summarizing, and retrieves it by semantic search scoped into wings (people, projects), rooms (topics) and drawers (original content). It defaults to ChromaDB with a pluggable backend interface, and exposes 47 MCP tools plus a SQLite temporal knowledge graph. The README reports 96.6% R@5 on LongMemEval in raw mode with no LLM.

- **+** Stores original text verbatim; raw mode needs no LLM or API key
- **+** Pluggable backends: Chroma, SQLite exact, Rust exact, Milvus, Qdrant, pgvector
- **+** Benchmarks reproducible from the repo with committed per-question results
- **+** Auto-save hooks for Claude Code, Codex CLI and Cursor; 47 MCP tools
- **−** Native Termux install unsupported; Android needs a Debian PRoot container
- **−** GPU Docker image is not published and fails to build on ARM hosts
- **−** Claude Code sessions expire in 30 days unless auto-save hooks are wired
- **−** First embedding call downloads a model of about 80-300 MB

<sub>GPU optional · Docker + Compose · Needs Python 3.10+, ChromaDB (default), Milvus (optional), Qdrant (optional), Postgres pgvector (optional) · Models: minilm, embeddinggemma, OpenAI-compatible embeddings endpoints · [Repo](https://github.com/mempalace/mempalace) · [📖 Docs ↗](https://mempalaceofficial.com/guide/getting-started.html) · [🌐 Site ↗](https://mempalaceofficial.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mempalace/)</sub>

<a name="mem0"></a>
### 🥉 [Mem0](https://github.com/mem0ai/mem0) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 68k · Apache-2.0 · Oct 2026</sub>

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

<a name="gbrain"></a>
### #&#8288;4 [gbrain](https://github.com/garrytan/gbrain) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · MIT · Oct 2026</sub>

**Long-term memory store for coding agents, with sources and corrections.**

GBrain keeps explicit facts and their sources in a local PGLite or Postgres brain and exposes them to agents such as Claude Code, Codex, Cursor and Hermes over stdio or HTTP MCP. It starts keyless with keyword search; semantic search, cited synthesis, a typed knowledge graph and an overnight enrichment cycle are optional. It is installed with Bun from GitHub, not npm.

- **+** Keyless start: PGLite brain with keyword search, no server or Docker needed
- **+** One brain shared across agents via stdio MCP or HTTP MCP with scoped OAuth tokens
- **+** One-command setup for Claude Code and Codex, with dry-run and remove options
- **+** Optional cited synthesis that notes gaps, plus a typed graph for relationship queries
- **−** Not on npm; the unrelated npm package named gbrain can shadow the real binary
- **−** Always-on OpenClaw/Hermes setup needs a server with 8GB+ RAM plus paid API usage
- **−** Local files and shared database credentials are not isolated by sources
- **−** Remote put_page does not extract graph edges inline; HTTP needs explicit maintenance

<sub>RAM ≥ 8 GB · no GPU · Compose · Needs Bun 1.4.0+, PGLite or Postgres, Tailscale (optional, for remote MCP) · Models: Optional cloud embedding, reranking, extraction and synthesis providers (unspecified) · [Repo](https://github.com/garrytan/gbrain) · [🌐 Site ↗](https://gbrain.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gbrain/)</sub>

<a name="cognee"></a>
### #&#8288;5 [Cognee](https://github.com/topoteretes/cognee) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · Apache-2.0 · Oct 2026</sub>

**Memory engine that turns documents and code into a knowledge graph.**

Cognee builds persistent agent memory by extracting entities, relationships and chunks from text, code and sessions into a graph and vector index with hybrid recall. Without an LLM key it uses local GLiNER extraction and embeddings; adding a key enables generated answers via OpenAI, Ollama or other providers. It runs as a library, CLI, REST API (port 8000), UI (3000) and MCP server (8001).

- **+** Keyless mode: local GLiNER extraction and embeddings, no cloud LLM required
- **+** Claude Code and Codex plugins, OpenClaw plugin, MCP server, Python, TypeScript and Rust SDKs
- **+** Imports memory from Mem0, Letta, Zep or Graphiti via the COGX format
- **+** Apache-2.0; research paper and BEAM evaluation published
- **−** Single-Postgres graph store is a demo; production version is a licensed product
- **−** API defaults to multi-tenant mode; local use needs ENABLE_BACKEND_ACCESS_CONTROL=false
- **−** Bundled GLiNER extractor is a demo; higher-accuracy version requires contacting the vendor
- **−** UI launcher needs Node.js/npm and Docker for its MCP service

<sub>no GPU · Docker + Compose · Compose runs Neo4j, PostgreSQL, Redis · Models: local GLiNER + embeddings (keyless), OpenAI, Ollama, other providers per docs · port 8000 · [Repo](https://github.com/topoteretes/cognee) · [📖 Docs ↗](https://docs.cognee.ai/) · [🌐 Site ↗](https://cognee.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cognee/)</sub>

<a name="graphiti"></a>
### #&#8288;6 [Graphiti](https://github.com/getzep/graphiti) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · Apache-2.0 · Oct 2026</sub>

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

<a name="supermemory"></a>
### #&#8288;7 [Supermemory](https://github.com/supermemoryai/supermemory) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · MIT · Oct 2026</sub>

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

<a name="openviking"></a>
### #&#8288;8 [OpenViking](https://github.com/volcengine/openviking) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · AGPL-3.0 · Oct 2026</sub>

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
### #&#8288;9 [agentmemory](https://github.com/rohitg00/agentmemory) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;10 [everos](https://github.com/evermind-ai/everos) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (36) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · Apache-2.0 · Oct 2026</sub>

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

<a name="tencentdb-agent-memory"></a>
### #&#8288;11 [tencentdb-agent-memory](https://github.com/tencentcloud/tencentdb-agent-memory) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · custom license · Oct 2026</sub>

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

<a name="semantica"></a>
### #&#8288;12 [semantica](https://github.com/semantica-agi/semantica) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: known (40) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Oct 2026</sub>

**Python library for building context graphs with decision provenance and reasoning.**

Semantica is a Python library that ingests data from files, databases, Databricks, Snowflake and SAP, extracts entities and relations, and builds a knowledge graph with W3C PROV-O provenance. It records agent decisions as graph nodes with causal links, and runs rule-based reasoning (Rete, Datalog, SPARQL) and SHACL/OWL governance. It stores graphs in RDF or property-graph backends and exposes a CLI, REST API and MCP server.

- **+** Graph construction, reasoning and provenance are deterministic; no LLM required
- **+** Swappable storage: Oxigraph, Blazegraph, Jena, RDF4J, Neo4j, FalkorDB, AGE, Neptune
- **+** Decisions stored as graph nodes with causal tracing, precedent search and PROV-O export
- **+** Connectors for Databricks, Snowflake, SAP OData, Kafka, Kinesis, plus CrewAI, LangChain, Agno integrations
- **−** Broad scope (ontology, reasoning, ingestion, analytics) means a large surface to learn
- **−** Explains context and decisions outside the LLM only, not the model's internal reasoning
- **−** Resource requirements and benchmark figures not stated in the visible README
- **−** Aimed at regulated enterprise use; heavy for simple agent memory needs

<sub>no GPU · Docker + Compose · Needs Optional graph stores: Neo4j, FalkorDB, Apache AGE, AWS Neptune, Blazegraph, Jena, RDF4J, Optional vector store: FAISS, Optional LLM provider: OpenAI, Anthropic, Gemini · Models: OpenAI, Anthropic, Gemini · [Repo](https://github.com/semantica-agi/semantica) · [📖 Docs ↗](https://docs.getsemantica.ai/) · [🌐 Site ↗](https://getsemantica.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/semantica/)</sub>

<a name="memos"></a>
### #&#8288;13 [MemOS](https://github.com/memtensor/memos) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: known (30) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Oct 2026</sub>

**Memory operating system for agents with cubes, scheduler and hybrid retrieval.**

MemOS gives LLM apps and agents long-term memory via one API over graph-structured memories, grouped into memory cubes per user, project or agent. Self-hosting runs docker compose for the REST API on port 8000 with Neo4j and Qdrant; a local plugin for OpenClaw, Hermes and DeepSeek Harness instead keeps everything in SQLite with FTS5 and vector search.

- **+** Memory cubes isolate or share knowledge across users, projects and agents
- **+** MemScheduler ingests asynchronously for high-concurrency workloads
- **+** Local plugin for OpenClaw, Hermes and DeepSeek Harness is 100% on-device SQLite
- **+** Apache-2.0; two arXiv papers and OmniMemEval benchmark published
- **−** Self-hosted service requires Neo4j and Qdrant
- **−** Local plugin docs are partly in Chinese; cloud dashboard links go to a cn locale
- **−** LLM, embedder and vector DB keys must be filled in .env before start
- **−** Benchmark table lists scores without comparison baselines in the README

<sub>no GPU · Docker + Compose · Needs Neo4j, Qdrant · port 8000 · [Repo](https://github.com/memtensor/memos) · [📖 Docs ↗](https://memos-docs.openmem.net/home/overview/) · [🌐 Site ↗](https://memos.openmem.net/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/memos/)</sub>

<a name="letta-ai-letta"></a>
### #&#8288;14 [letta](https://github.com/letta-ai/letta) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: fair (56) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · Apache-2.0 · Oct 2026</sub>

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

<a name="honcho"></a>
### #&#8288;15 [Honcho](https://github.com/plastic-labs/honcho) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.8k · AGPL-3.0 · Oct 2026</sub>

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

<a name="engram"></a>
### #&#8288;16 [Engram](https://github.com/gentleman-programming/engram) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · MIT · Oct 2026</sub>

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

<a name="letta"></a>
### #&#8288;17 [Letta](https://github.com/letta-ai/letta-code) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · Apache-2.0 · Oct 2026</sub>

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

<a name="memvid"></a>
### #&#8288;18 [memvid](https://github.com/memvid/memvid) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: known (46) · Freshness: active (97) · Maintenance: weak (6) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Jul 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
