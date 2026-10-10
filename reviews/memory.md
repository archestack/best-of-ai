# 🗂️ Memory reviews · Best of Open-Source AI

Long-term memory engines that store and retrieve facts for agents across sessions. Back to the [leaderboard](../README.md#%EF%B8%8F-memory).

<a name="hindsight"></a>
### 🥇 [hindsight](https://github.com/vectorize-io/hindsight) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: widely used (81) · Freshness: active (100) · Maintenance: healthy (93) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 48k · MIT · Oct 2026</sub>

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

<sub>Docker · Needs LLM provider (hosted or local), PostgreSQL (embedded pg0 by default), Oracle AI Database (optional) · Models: openai, anthropic, gemini, groq, bedrock · port 9999 · [Repo](https://github.com/vectorize-io/hindsight) · [📖 Docs ↗](https://hindsight.vectorize.io) · [🌐 Site ↗](https://hindsight.vectorize.io)</sub>

<a name="mempalace"></a>
### 🥈 [MemPalace](https://github.com/mempalace/mempalace) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: healthy (84) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 59k · MIT · Oct 2026</sub>

**Local verbatim memory for coding agents on ChromaDB with 45 MCP tools.**

MemPalace stores conversation history verbatim, never summarised, and retrieves it by scoped semantic search over a palace of wings (people, projects), rooms (topics) and drawers. It runs locally with Python 3.9+ and ChromaDB by default, exposes 45 MCP tools plus a CLI, mines Claude Code, Codex and Cursor transcripts via hooks, and needs no API key: 96.6% R@5 on LongMemEval without an LLM.

- **+** Verbatim storage; nothing is summarised or paraphrased
- **+** 96.6% R@5 on LongMemEval with no LLM or API key; results reproducible from the repo
- **+** Pluggable backends: ChromaDB, sqlite, Rust-native, Milvus, Qdrant, pgvector
- **+** Multi-arch Docker image; auto-save hooks for Claude Code, Codex and Cursor
- **−** First run downloads an 80 to 300 MB embedding model; Docker needs network then
- **−** No native Android/Termux; GPU image is x86_64-only and unpublished
- **−** Docker image runs as uid 1000, so bind mounts must be readable by that uid
- **−** README warns about impostor domains distributing malware

<sub>no GPU · Docker + Compose · Models: local embeddings (MiniLM, EmbeddingGemma), OpenAI-compatible embedding endpoints, Ollama · [Repo](https://github.com/mempalace/mempalace) · [📖 Docs ↗](https://mempalaceofficial.com/guide/getting-started.html) · [🌐 Site ↗](https://mempalaceofficial.com)</sub>

<a name="agentmemory"></a>
### 🥉 [agentmemory](https://github.com/rohitg00/agentmemory) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: known (48) · Freshness: active (100) · Maintenance: healthy (81) · Easy to run: very easy (83) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Oct 2026</sub>

**Persistent memory server for coding agents, exposed over MCP and REST.**

agentmemory captures what a coding agent does across sessions, stores it as searchable memory, and injects relevant context at the start of the next session. It runs as a local Node.js server on the pinned iii engine and connects to agents through hooks, MCP, or REST, with 20 adapters listed. Keyless mode uses BM25 search; vector embeddings need a provider or the local Xenova/all-MiniLM-L6-v2 model.

- **+** No external database; state lives in a local iii engine data directory
- **+** Works with 20 listed agents through hooks, MCP, or REST
- **+** Keyless BM25 mode works without any API key
- **+** Local embeddings via EMBEDDING_PROVIDER=local after a one-time model download
- **−** Keyless mode has no vector search, so semantic queries can return nothing
- **−** Pinned to iii-engine v0.22.1; refuses to attach to other engine versions
- **−** Native Windows needs manual iii.exe install; WSL2 or Docker recommended
- **−** Uses four local ports (3111, 3112, 3113, 49134)

<sub>no GPU · Docker + Compose · Needs Node.js 20+, iii-engine v0.22.1 · Models: Xenova/all-MiniLM-L6-v2 (local embeddings) · port 3113 · [Repo](https://github.com/rohitg00/agentmemory)</sub>

<a name="openviking"></a>
### #&#8288;4 [OpenViking](https://github.com/volcengine/openviking) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: healthy (88) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 40k · AGPL-3.0 · Oct 2026</sub>

**Context database exposing agent memory, knowledge and skills as a filesystem.**

OpenViking organises everything an agent knows as a viking:// virtual filesystem of resources, memories and skills, browsed with ls, tree, read and grep, with search scoped to a subtree. Each directory carries generated summaries so agents read full content only when needed. The server needs Python 3.10+ plus an embedding model and a VLM; plugins cover Claude Code, Codex, Cursor and OpenClaw.

- **+** Memory is inspectable and editable as Markdown files under viking:// URIs
- **+** LoCoMo accuracy 80 to 83% for OpenClaw, Hermes and Claude Code at far fewer tokens
- **+** Python, Go and TypeScript SDKs plus HTTP API; multi-tenant accounts and ACLs
- **+** Hosted Studio playground at openviking.ai/studio; Railway one-click deploy
- **−** AGPL-3.0 license
- **−** Needs both an embedding model and a vision-language model from a provider
- **−** Memory plugin installer is macOS/Linux only; Windows uses the beta desktop app
- **−** Benchmarks were run with Volcengine Doubao models

<sub>no GPU · Docker + Compose · Models: Volcengine, OpenAI, Codex OAuth, Kimi, GLM · [Repo](https://github.com/volcengine/openviking) · [▶️ Demo ↗](https://openviking.ai/studio) · [📖 Docs ↗](https://docs.openviking.ai/) · [🌐 Site ↗](https://www.openviking.ai)</sub>

<a name="mem0"></a>
### #&#8288;5 [Mem0](https://github.com/mem0ai/mem0) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: healthy (80) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 67k · Apache-2.0 · Oct 2026</sub>

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

<sub>no GPU · Models: OpenAI gpt-5-mini (default), OpenAI text-embedding-3-small (default), other providers per docs · port 3000 · [Repo](https://github.com/mem0ai/mem0) · [▶️ Demo ↗](https://mem0.dev/demo) · [📖 Docs ↗](https://docs.mem0.ai) · [🌐 Site ↗](https://mem0.ai)</sub>

<a name="cognee"></a>
### #&#8288;6 [Cognee](https://github.com/topoteretes/cognee) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · Apache-2.0 · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · Compose runs Neo4j, PostgreSQL, Redis · Models: local GLiNER + embeddings (keyless), OpenAI, Ollama, other providers per docs · port 8000 · [Repo](https://github.com/topoteretes/cognee) · [📖 Docs ↗](https://docs.cognee.ai/) · [🌐 Site ↗](https://cognee.ai)</sub>

<a name="graphiti"></a>
### #&#8288;7 [Graphiti](https://github.com/getzep/graphiti) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (60) · Freshness: active (100) · Maintenance: healthy (84) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · Apache-2.0 · Oct 2026</sub>

**Temporal knowledge graph framework for agent memory with REST and MCP servers.**

Graphiti builds context graphs where every fact has a validity window and traces back to its source episode, ingesting text and JSON incrementally. Retrieval fuses embeddings, BM25 and graph traversal. It needs a graph database (Neo4j, FalkorDB or Neptune) and defaults to OpenAI, with Anthropic, Gemini, Groq and OpenAI-compatible servers supported; REST and MCP servers ship in the repo.

- **+** Bi-temporal facts: old facts are invalidated, not deleted, so history stays queryable
- **+** Hybrid retrieval combines embeddings, BM25 and graph traversal with sub-second latency claims
- **+** Custom entity and edge types via Pydantic models
- **+** Docker Compose profiles for Neo4j or FalkorDB; MCP and REST servers included
- **−** Requires Neo4j, FalkorDB or Amazon Neptune plus OpenSearch; Kuzu is deprecated
- **−** Defaults to OpenAI; needs structured-output models, smaller models may fail ingestion
- **−** Default SEMAPHORE_LIMIT of 10 keeps ingestion slow to avoid 429 errors
- **−** Users, threads and dashboards are left to the commercial Zep platform

<sub>no GPU · Docker + Compose · Needs Neo4j 5.26, FalkorDB 1.1.2 or Amazon Neptune · Models: OpenAI (default), Azure OpenAI, Anthropic, Google Gemini, Groq · [Repo](https://github.com/getzep/graphiti)</sub>

<a name="memos"></a>
### #&#8288;8 [MemOS](https://github.com/memtensor/memos) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: known (33) · Freshness: active (100) · Maintenance: healthy (88) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Sep 2026</sub>

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

<sub>no GPU · Docker + Compose · Needs Neo4j, Qdrant · port 8000 · [Repo](https://github.com/memtensor/memos) · [📖 Docs ↗](https://memos-docs.openmem.net/home/overview/) · [🌐 Site ↗](https://memos.openmem.net/)</sub>

<a name="supermemory"></a>
### #&#8288;9 [Supermemory](https://github.com/supermemoryai/supermemory) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: healthy (91) · Easy to run: some setup (33) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · MIT · Oct 2026</sub>

**Memory and context API with user profiles, connectors and a local server.**

Supermemory extracts facts from conversations, maintains per-user profiles and answers hybrid queries that mix RAG over documents with personal memory, through one API with npm and pip SDKs. The self-hosted path is a single binary (port 6767) with an embedded graph engine and local bge-base embeddings, usable offline with Ollama; the hosted platform adds Drive, Gmail, Notion and GitHub connectors.

- **+** One binary, zero config; local Xenova/bge-base-en-v1.5 embeddings need no API key
- **+** Plugins for Claude Code, Cursor, Codex, OpenCode, OpenClaw and Hermes plus an MCP server
- **+** Framework wrappers for Vercel AI SDK, LangChain, LangGraph, OpenAI Agents SDK and Mastra
- **+** Open-source MemoryBench to compare memory providers
- **−** URL ingestion uses a hosted reader service even in local mode
- **−** Telemetry is on unless SUPERMEMORY_DISABLE_TELEMETRY=1 is set
- **−** Connectors (Drive, Gmail, Notion, GitHub) are described for the platform, not local
- **−** README leads with benchmark rankings; the MCP server URL points to the hosted service

<sub>no GPU · Models: OpenAI, Anthropic, Gemini, Groq, OpenAI-compatible endpoints · port 6767 · [Repo](https://github.com/supermemoryai/supermemory) · [📖 Docs ↗](https://supermemory.ai/docs)</sub>

<a name="honcho"></a>
### #&#8288;10 [Honcho](https://github.com/plastic-labs/honcho) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: healthy (85) · Easy to run: some setup (33) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · AGPL-3.0 · Oct 2026</sub>

**Memory service modelling users, agents and groups as evolving peers.**

Honcho is a FastAPI memory server where humans and agents are peers that exchange messages in sessions; a background deriver reasons over them and maintains per-peer representations and summaries you query via peer.chat, hybrid search or prompt-ready context. Run it managed at api.honcho.dev, locally with honcho start (API, deriver, Postgres and Redis in Docker) or from source with Docker Compose on port 8000.

- **+** First-party plugins for Claude Code, Codex, Cursor, DeepSeek Harness, OpenCode, OpenClaw and Hermes
- **+** Peer model handles multi-participant sessions and what one peer knows about another
- **+** Python and TypeScript SDKs with .to_openai and .to_anthropic context helpers
- **+** honcho start --setup brings up the whole local stack with one command
- **−** AGPL-3.0 license
- **−** Needs Postgres with pgvector and Redis plus an LLM key for the deriver
- **−** Background reasoning is asynchronous; new messages are not reflected immediately
- **−** README mixes marketing claims (Pareto frontier, data moats) with the technical content

<sub>no GPU · Docker · Needs PostgreSQL with pgvector, Redis · Models: Gemini, Anthropic, OpenAI · port 8000 · [Repo](https://github.com/plastic-labs/honcho) · [▶️ Demo ↗](https://app.honcho.dev) · [📖 Docs ↗](https://honcho.dev/docs/v3/documentation/reference/sdk)</sub>

<a name="engram"></a>
### #&#8288;11 [Engram](https://github.com/gentleman-programming/engram) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: healthy (96) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · MIT · Oct 2026</sub>

**Single Go binary memory for coding agents on SQLite FTS5 with MCP.**

Engram is one Go binary that stores agent memory in a local SQLite database with FTS5 full-text search and exposes it over MCP stdio, a CLI, a local HTTP API and an interactive TUI. The engram setup command configures 14 agents including Claude Code, OpenCode, Gemini CLI, Codex, Cursor and Windsurf; memory is project-aware, can sync through Git as compressed chunks, and optionally replicates to Engram Cloud.

- **+** No Node.js, Python or Docker; one binary and one SQLite file
- **+** engram setup targets 14 agents plus any MCP-compatible client
- **+** Git Sync shares memory across machines without a server
- **+** engram doctor and binary self-tests for diagnostics; MIT license
- **−** Full-text search only; no vector or semantic retrieval mentioned
- **−** Engram Cloud replication is optional and separate from the local store
- **−** Project detection can halt with project_transition_conflict after git init
- **−** Install docs for Windows and Linux live in docs/, not the README

<sub>no GPU · Docker + Compose · [Repo](https://github.com/gentleman-programming/engram) · [🌐 Site ↗](https://engram.gentlemanprogramming.com/)</sub>

<a name="letta"></a>
### #&#8288;12 [Letta](https://github.com/letta-ai/letta-code) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (5) · Freshness: active (100) · Maintenance: healthy (82) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.6k · Apache-2.0 · Oct 2026</sub>

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

<sub>no GPU · Docker · Models: OpenAI / ChatGPT, Anthropic, Z.ai coding plan · [Repo](https://github.com/letta-ai/letta-code) · [▶️ Demo ↗](https://chat.letta.com) · [📖 Docs ↗](https://docs.letta.com/letta-code/cli)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
