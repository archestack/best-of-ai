# 🗂️ Memory reviews · Best of Open-Source AI

Long-term memory engines that store and retrieve facts for agents across sessions. Back to the [leaderboard](../README.md#%EF%B8%8F-memory).

<sub>🌐 Also on the web: [Memory on archestack.com](https://archestack.com/best-of-ai/memory/), each project on its own page.</sub>

<a name="hindsight"></a>
### 🥇 [hindsight](https://github.com/vectorize-io/hindsight) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: healthy (94) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 50k · MIT · Oct 2026</sub>

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
### 🥈 [MemPalace](https://github.com/mempalace/mempalace) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 60k · MIT · Oct 2026</sub>

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

<a name="cognee"></a>
### 🥉 [Cognee](https://github.com/topoteretes/cognee) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (57) · Freshness: active (100) · Maintenance: healthy (81) · Easy to run: easy (67) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · Apache-2.0 · Oct 2026</sub>

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

<a name="openviking"></a>
### #&#8288;4 [OpenViking](https://github.com/volcengine/openviking) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: healthy (88) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · AGPL-3.0 · Oct 2026</sub>

**Context database that stores agent memory, resources and skills as a virtual filesystem.**

OpenViking organizes what an agent knows under a viking:// virtual filesystem, with documents, memories and skills browsable through ls, tree, read, write and grep. Directories carry generated L0 abstracts and L1 overviews so agents read summaries before full content, and committed sessions become editable Markdown memories. It ships a server, an ov CLI, Python, Go and TypeScript SDKs, an HTTP API, and a memory plugin installer for Claude Code, Codex, Cursor and others.

- **+** Memory is stored as inspectable, editable files under viking:// URIs rather than opaque embeddings
- **+** Search can be scoped to a directory subtree; L0/L1 summaries cut full reads
- **+** Plugin installer covers Claude Code, Codex, Cursor, TRAE, OpenCode, with OpenClaw and Hermes integrations
- **+** Python, Go and TypeScript SDKs, HTTP API, CLI, plus accounts, user isolation and opt-in ACLs
- **−** AGPL-3.0 license may constrain embedding in proprietary or networked products
- **−** Needs a model provider with both an embedding model and a VLM
- **−** Memory extraction runs in the background, so new memories are not immediately retrievable
- **−** Published benchmarks use Volcengine Doubao models; results with other providers are not shown

<sub>no GPU · Docker + Compose · Needs uv, Python 3.10+, Embedding model provider, VLM provider, Node.js 18+ (plugin installer) · Models: Volcengine, OpenAI, Codex OAuth, Kimi, GLM · [Repo](https://github.com/volcengine/openviking) · [▶️ Demo ↗](https://openviking.ai/studio) · [📖 Docs ↗](https://docs.openviking.ai/) · [🌐 Site ↗](https://www.openviking.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openviking/)</sub>

<a name="mem0"></a>
### #&#8288;5 [Mem0](https://github.com/mem0ai/mem0) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: fair (80) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 67k · Apache-2.0 · Oct 2026</sub>

**Memory layer for agents with a self-hosted server, SDKs and CLI.**

Mem0 adds long-term memory to assistants and agents at user, session and agent level. It ships as a Python and npm library, a self-hosted server via docker compose (dashboard on port 3000, auth on by default) and a managed cloud. Memories are extracted by an LLM (gpt-5-mini by default) and retrieved with semantic, BM25 and entity matching; an optional NLP extra adds spaCy for hybrid search.

- **+** Library, self-hosted server with dashboard and API keys, or managed platform share one API
- **+** Multi-signal retrieval: semantic, BM25 keyword and entity matching with temporal reasoning
- **+** CLI and agent skills for Claude Code, Codex, Cursor and others
- **+** Apache-2.0; evaluation framework is open source
- **−** Requires an LLM for extraction; OpenAI gpt-5-mini and text-embedding-3-small are the defaults
- **−** Benchmark scores reflect the managed platform, not the open-source SDK
- **−** Self-hosted server exposes only teasers of advanced features; all included in cloud
- **−** Hybrid search recommends at least a 600M-parameter embedding model

<sub>no GPU · Models: OpenAI gpt-5-mini (default), OpenAI text-embedding-3-small (default), other providers per docs · port 3000 · [Repo](https://github.com/mem0ai/mem0) · [▶️ Demo ↗](https://mem0.dev/demo) · [📖 Docs ↗](https://docs.mem0.ai) · [🌐 Site ↗](https://mem0.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mem0/)</sub>

<a name="agentmemory"></a>
### #&#8288;6 [agentmemory](https://github.com/rohitg00/agentmemory) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (40) · Freshness: active (100) · Maintenance: healthy (82) · Easy to run: very easy (83) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Oct 2026</sub>

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

<a name="graphiti"></a>
### #&#8288;7 [Graphiti](https://github.com/getzep/graphiti) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · Apache-2.0 · Oct 2026</sub>

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
### #&#8288;8 [Supermemory](https://github.com/supermemoryai/supermemory) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (47) · Freshness: active (100) · Maintenance: healthy (92) · Easy to run: easy (50) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · MIT · Oct 2026</sub>

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
### #&#8288;9 [MemOS](https://github.com/memtensor/memos) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: healthy (88) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Sep 2026</sub>

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

<a name="engram"></a>
### #&#8288;10 [Engram](https://github.com/gentleman-programming/engram) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (14) · Freshness: active (100) · Maintenance: healthy (97) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.2k · MIT · Oct 2026</sub>

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

<a name="honcho"></a>
### #&#8288;11 [Honcho](https://github.com/plastic-labs/honcho) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (19) · Freshness: active (100) · Maintenance: healthy (85) · Easy to run: some setup (33) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · AGPL-3.0 · Oct 2026</sub>

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
### #&#8288;12 [Letta](https://github.com/letta-ai/letta-code) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (4) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.6k · Apache-2.0 · Oct 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
