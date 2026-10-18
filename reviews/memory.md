# 🗂️ Memory reviews · Best of Open-Source AI

Long-term memory engines that store and retrieve facts for agents across sessions. Back to the [leaderboard](../README.md#%EF%B8%8F-memory).

<sub>🌐 Also on the web: [Memory on archestack.com](https://archestack.com/best-of-ai/memory/), each project on its own page.</sub>

<a name="gbrain"></a>
### 🥇 [gbrain](https://github.com/garrytan/gbrain) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: healthy (97) · Easy to run: very easy (83) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · MIT · Oct 2026</sub>

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

<a name="hindsight"></a>
### 🥈 [hindsight](https://github.com/vectorize-io/hindsight) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: healthy (95) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 51k · MIT · Oct 2026</sub>

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

<a name="cognee"></a>
### 🥉 [Cognee](https://github.com/topoteretes/cognee) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: fair (79) · Easy to run: easy (67) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · Apache-2.0 · Oct 2026</sub>

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

<a name="mempalace"></a>
### #&#8288;4 [MemPalace](https://github.com/mempalace/mempalace) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 60k · MIT · Oct 2026</sub>

**Local long-term memory store for agents with verbatim storage and semantic search.**

MemPalace stores conversation history as verbatim text and retrieves it with semantic search, organized into wings (people, projects), rooms (topics) and drawers (original content). It ships a CLI, 47 MCP tools, a SQLite temporal knowledge graph, and auto-save hooks for Claude Code, Codex CLI and Cursor. ChromaDB is the default backend; sqlite_exact, rust_exact, Milvus, Qdrant and pgvector are selectable.

- **+** Raw retrieval scores 96.6% R@5 on LongMemEval with no LLM or API key
- **+** Pluggable backends: Chroma, SQLite exact, Rust, Milvus, Qdrant, pgvector
- **+** Benchmark results and reproduction commands are committed in the repository
- **+** Optional OpenAI-compatible embedding endpoint, including local LM Studio, llama.cpp or Ollama
- **−** Native Termux install unsupported; Android needs a Debian PRoot container
- **−** Stores verbatim text only; no summarization or fact extraction
- **−** First embedding call downloads a model of about 80 to 300 MB
- **−** GPU Docker image is not published and is x86_64-only

<sub>GPU optional · Docker + Compose · Needs ChromaDB (default backend), ONNX Runtime, Optional: Milvus, Qdrant, PostgreSQL with pgvector · Models: all-MiniLM-L6-v2, embeddinggemma-300m, OpenAI-compatible /v1/embeddings endpoints · [Repo](https://github.com/mempalace/mempalace) · [📖 Docs ↗](https://mempalaceofficial.com/guide/getting-started.html) · [🌐 Site ↗](https://mempalaceofficial.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mempalace/)</sub>

<a name="agentmemory"></a>
### #&#8288;5 [agentmemory](https://github.com/rohitg00/agentmemory) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: healthy (81) · Easy to run: very easy (83) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Oct 2026</sub>

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

<a name="openviking"></a>
### #&#8288;6 [OpenViking](https://github.com/volcengine/openviking) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: healthy (87) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · AGPL-3.0 · Oct 2026</sub>

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

<a name="mem0"></a>
### #&#8288;7 [Mem0](https://github.com/mem0ai/mem0) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: healthy (80) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 67k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;8 [Graphiti](https://github.com/getzep/graphiti) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;9 [Supermemory](https://github.com/supermemoryai/supermemory) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: healthy (92) · Easy to run: easy (50) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · MIT · Oct 2026</sub>

**Memory and context API that extracts user facts and serves profiles to agents.**

Supermemory extracts facts from conversations, tracks updates and contradictions, expires stale facts, and returns a per-user profile plus hybrid RAG and memory search through one API. It ships TypeScript and Python SDKs, an MCP server, plugins for Claude Code, Cursor, Codex and OpenCode, and connectors for Google Drive, Gmail, Notion, OneDrive and GitHub. A local server (default port 6767) runs against any OpenAI-compatible, Anthropic, Gemini or Ollama model.

- **+** Single call returns user profile (static and dynamic facts) plus search results, claimed ~50ms
- **+** Local server exposes the same API as the hosted platform; switch by changing baseURL
- **+** Handles contradictions and expiry of temporary facts instead of only appending
- **+** Wrappers for Vercel AI SDK, LangChain, LangGraph, Mastra, OpenAI Agents SDK, n8n
- **−** Benchmark claims (#1 on LongMemEval, LoCoMo, ConvoMem) are self-reported
- **−** URL ingestion in local mode relies on a hosted reader service
- **−** MCP server and plugins default to the hosted service at mcp.supermemory.ai
- **−** Local edition differs from Enterprise; README defers details to a separate docs page

<sub>GPU optional · Needs LLM provider key (OpenAI, Anthropic, Gemini, Groq or Ollama), Docker (optional) · Models: OpenAI, Anthropic, Gemini, Groq, Ollama · port 6767 · [Repo](https://github.com/supermemoryai/supermemory) · [📖 Docs ↗](https://supermemory.ai/docs) · [🌐 Site ↗](https://supermemory.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/supermemory/)</sub>

<a name="memos"></a>
### #&#8288;10 [MemOS](https://github.com/memtensor/memos) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: healthy (87) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Sep 2026</sub>

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

<a name="semantica"></a>
### #&#8288;11 [semantica](https://github.com/semantica-agi/semantica) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (25) · Freshness: active (100) · Maintenance: healthy (94) · Easy to run: easy (50) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Oct 2026</sub>

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

<a name="engram"></a>
### #&#8288;12 [Engram](https://github.com/gentleman-programming/engram) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: healthy (96) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.4k · MIT · Oct 2026</sub>

**Persistent memory store for AI coding agents, exposed over MCP.**

Engram is a single Go binary that stores coding-agent memory in a local SQLite database with FTS5 search. It exposes save, search, timeline and session tools over MCP stdio, plus a CLI, local HTTP API and terminal UI. `engram setup <agent>` configures 14 targets including Claude Code, OpenCode, Gemini CLI, Codex, Cursor and Windsurf. Git Sync and an optional Engram Cloud handle sharing across machines.

- **+** Single Go binary with one SQLite file; no Node, Python or Docker required
- **+** One setup command per agent, 14 targets plus any MCP-compatible client
- **+** Project-aware: resolves project from explicit flag, ENGRAM_PROJECT or cwd
- **+** Local database is authoritative; Git Sync exports compressed chunks for sharing
- **−** Aimed at coding agents; not a general-purpose memory layer for other assistants
- **−** Search is SQLite FTS5 full-text; README mentions no embedding or vector search
- **−** Cloud replication is a separate optional component with its own upgrade steps
- **−** Codex integration needs a compatible running core and manual restart after upgrades

<sub>no GPU · Docker + Compose · Models: Any MCP-compatible agent · [Repo](https://github.com/gentleman-programming/engram) · [📖 Docs ↗](https://github.com/Gentleman-Programming/engram/blob/main/DOCS.md) · [🌐 Site ↗](https://engram.gentlemanprogramming.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/engram/)</sub>

<a name="tencentdb-agent-memory"></a>
### #&#8288;13 [tencentdb-agent-memory](https://github.com/tencentcloud/tencentdb-agent-memory) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: fair (76) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · custom license · Oct 2026</sub>

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

<a name="everos"></a>
### #&#8288;14 [everos](https://github.com/evermind-ai/everos) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: healthy (89) · Easy to run: some setup (33) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Oct 2026</sub>

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

<a name="honcho"></a>
### #&#8288;15 [Honcho](https://github.com/plastic-labs/honcho) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: healthy (85) · Easy to run: some setup (33) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.7k · AGPL-3.0 · Oct 2026</sub>

**Memory server that builds per-peer representations from agent conversations.**

Honcho is a FastAPI memory service that stores messages on sessions, reasons over them in a background queue, and returns peer representations, session context, hybrid BM25 plus vector search, or natural-language answers. It ships Python and TypeScript SDKs, a CLI, and plugins for Claude Code, Codex, Cursor, OpenCode, Kilo Code and OpenClaw. It runs as a managed service at api.honcho.dev or self-hosted with API, deriver, Postgres and Redis.

- **+** Peer model covers users, agents, groups and projects, including what one peer knows about another
- **+** Python and TypeScript SDKs; context exports directly to OpenAI or Anthropic message formats
- **+** First-party plugins for Claude Code, Codex, Cursor, OpenCode, Kilo Code and OpenClaw share one config file
- **+** Hybrid BM25 plus vector search and a low-latency representation endpoint alongside the chat endpoint
- **−** Reasoning runs asynchronously, so new messages may not appear in chat results immediately
- **−** Self-hosting needs an LLM provider key (Gemini, Anthropic or OpenAI) for the background deriver
- **−** AGPL-3.0 license may restrict use in closed-source network services
- **−** Self-hosted stack requires Postgres and Redis alongside the API and deriver processes

<sub>no GPU · Docker · Needs Postgres, Redis, LLM provider API key (Gemini, Anthropic or OpenAI), Docker (for honcho start) · Models: Gemini, Anthropic, OpenAI · port 8000 · [Repo](https://github.com/plastic-labs/honcho) · [▶️ Demo ↗](https://app.honcho.dev) · [📖 Docs ↗](https://honcho.dev/docs/v3/documentation/reference/sdk) · [🌐 Site ↗](https://honcho.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/honcho/)</sub>

<a name="letta"></a>
### #&#8288;16 [Letta](https://github.com/letta-ai/letta-code) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (2) · Freshness: active (100) · Maintenance: healthy (84) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.6k · Apache-2.0 · Oct 2026</sub>

**Stateful agent harness with git-tracked memory, channels and remote computers.**

Letta Code is an npm-installed agent harness whose agents keep memory blocks, skills and prompts in a git-tracked MemFS and rewrite them over time. Agents run from a CLI, desktop app, browser (chat.letta.com) or Telegram, Slack and Discord channels, use subagents, hooks and cron schedules, and can run on remote machines via letta server. Letta Cloud is the default backend; local is available.

- **+** All agent context including memory blocks is versioned in git (MemFS)
- **+** Same agent reachable from CLI, desktop, browser, Telegram, Slack and Discord
- **+** Skills installable from GitHub, ClawHub or the Hermes Skills Hub
- **+** Apache-2.0; Nix flake and AUR packages available
- **−** Letta Cloud is the default; remote computers and secrets require signing in
- **−** Self-hosted app server setup is not described in the README; local backend only mentioned
- **−** AgentFile export/import removed; agent registry imports no longer supported
- **−** Automatic dreaming is disabled on native Windows by default

<sub>no GPU · Docker · Models: OpenAI / ChatGPT, Anthropic, Z.ai coding plan · [Repo](https://github.com/letta-ai/letta-code) · [▶️ Demo ↗](https://chat.letta.com) · [📖 Docs ↗](https://docs.letta.com/letta-code/cli) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/letta/)</sub>

<a name="letta-ai-letta"></a>
### #&#8288;17 [letta](https://github.com/letta-ai/letta) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: known (46) · Freshness: active (100) · Maintenance: fair (54) · Easy to run: hard (0) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · Apache-2.0 · Sep 2026</sub>

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

<a name="memvid"></a>
### #&#8288;18 [memvid](https://github.com/memvid/memvid) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: known (33) · Freshness: active (98) · Maintenance: weak (4) · Easy to run: some setup (33) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Jul 2026</sub>

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
