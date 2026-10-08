# 🗂️ Memory — reviews

Long-term memory engines that store and retrieve facts for agents across sessions. Back to the [leaderboard](../README.md#-memory).

<a name="mem0"></a>
### 🥇 [Mem0](https://github.com/mem0ai/mem0) <sub>⭐ 67k · Apache-2.0 · Oct 2026</sub>

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

<sub>no GPU · Models: OpenAI gpt-5-mini (default), OpenAI text-embedding-3-small (default), other providers per docs · port 3000 · [Repo](https://github.com/mem0ai/mem0) · [🧪 Demo](https://mem0.dev/demo) · [📖 Docs](https://docs.mem0.ai) · [🌐 Site](https://mem0.ai)</sub>

<a name="mempalace"></a>
### 🥈 [MemPalace](https://github.com/MemPalace/mempalace) <sub>⭐ 59k · MIT · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · Models: local embeddings (MiniLM, EmbeddingGemma), OpenAI-compatible embedding endpoints, Ollama · [Repo](https://github.com/MemPalace/mempalace) · [📖 Docs](https://mempalaceofficial.com/guide/getting-started.html) · [🌐 Site](https://mempalaceofficial.com)</sub>

<a name="openviking"></a>
### 🥉 [OpenViking](https://github.com/volcengine/OpenViking) <sub>⭐ 39k · AGPL-3.0 · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · Models: Volcengine, OpenAI, Codex OAuth, Kimi, GLM · [Repo](https://github.com/volcengine/OpenViking) · [🧪 Demo](https://openviking.ai/studio) · [📖 Docs](https://docs.openviking.ai/) · [🌐 Site](https://www.openviking.ai)</sub>

<a name="cognee"></a>
### 4 [Cognee](https://github.com/topoteretes/cognee) <sub>⭐ 32k · Apache-2.0 · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · Models: local GLiNER + embeddings (keyless), OpenAI, Ollama, other providers per docs · port 8000 · [Repo](https://github.com/topoteretes/cognee) · [📖 Docs](https://docs.cognee.ai/) · [🌐 Site](https://cognee.ai)</sub>

<a name="graphiti"></a>
### 5 [Graphiti](https://github.com/getzep/graphiti) <sub>⭐ 32k · Apache-2.0 · Oct 2026</sub>

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

<a name="supermemory"></a>
### 6 [Supermemory](https://github.com/supermemoryai/supermemory) <sub>⭐ 31k · MIT · Oct 2026</sub>

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

<sub>no GPU · Models: OpenAI, Anthropic, Gemini, Groq, OpenAI-compatible endpoints · port 6767 · [Repo](https://github.com/supermemoryai/supermemory) · [📖 Docs](https://supermemory.ai/docs)</sub>

<a name="agentmemory"></a>
### 7 [agentmemory](https://github.com/rohitg00/agentmemory) <sub>⭐ 29k · Apache-2.0 · Oct 2026</sub>

**Persistent memory server for coding agents built on the iii engine.**

agentmemory captures agent activity via hooks, compresses it into searchable memory and injects context when the next session starts. One npx command (Node.js 20+) installs the server and pinned iii engine, wires Claude Code, Codex, Cursor and 17 other adapters, and serves REST and MCP on port 3111 with a viewer on 3113. Keyless mode uses BM25; a local MiniLM model or a provider adds semantic recall.

- **+** 20 agent adapters; Claude Code, Codex and Cursor get native plugins with hooks
- **+** No external databases; state lives in a platform data directory
- **+** Keyless by default; EMBEDDING_PROVIDER=local adds on-device semantic search
- **+** Real-time viewer on port 3113; 54 MCP tools and 17 skills
- **−** Pins iii-engine v0.22.1 and refuses to attach to any other engine version
- **−** Native Windows needs iii.exe installed by hand; WSL2 or Docker recommended
- **−** Uses four ports (3111, 3112, 3113, 49134)
- **−** LLM observation compression is off until AGENTMEMORY_AUTO_COMPRESS=true

<sub>no GPU · Compose · Needs iii-engine v0.22.1 (bundled) · Models: keyless BM25, local Xenova/all-MiniLM-L6-v2, LLM provider (optional) · port 3111 · [Repo](https://github.com/rohitg00/agentmemory)</sub>

<a name="memos"></a>
### 8 [MemOS](https://github.com/MemTensor/MemOS) <sub>⭐ 12k · Apache-2.0 · Sep 2026</sub>

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

<sub>no GPU · Docker · Needs Neo4j, Qdrant · port 8000 · [Repo](https://github.com/MemTensor/MemOS) · [📖 Docs](https://memos-docs.openmem.net/home/overview/) · [🌐 Site](https://memos.openmem.net/)</sub>

<a name="honcho"></a>
### 9 [Honcho](https://github.com/plastic-labs/honcho) <sub>⭐ 7.5k · AGPL-3.0 · Oct 2026</sub>

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

<sub>no GPU · Docker · Needs PostgreSQL with pgvector, Redis · Models: Gemini, Anthropic, OpenAI · port 8000 · [Repo](https://github.com/plastic-labs/honcho) · [🧪 Demo](https://app.honcho.dev) · [📖 Docs](https://honcho.dev/docs/v3/documentation/reference/sdk)</sub>

<a name="engram"></a>
### 10 [Engram](https://github.com/Gentleman-Programming/engram) <sub>⭐ 7.1k · MIT · Oct 2026</sub>

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

<sub>no GPU · [Repo](https://github.com/Gentleman-Programming/engram) · [🌐 Site](https://engram.gentlemanprogramming.com/)</sub>

<a name="letta"></a>
### 11 [Letta](https://github.com/letta-ai/letta-code) <sub>⭐ 3.5k · Apache-2.0 · Oct 2026</sub>

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

<sub>no GPU · Models: OpenAI / ChatGPT, Anthropic, Z.ai coding plan · [Repo](https://github.com/letta-ai/letta-code) · [🧪 Demo](https://chat.letta.com) · [📖 Docs](https://docs.letta.com/letta-code/cli)</sub>

<sub>Written from each project README and checked facts; see [how entries are written](../README.md#-how-it-works). Wrong? [Tell us](https://github.com/archestack/best-of-selfhosted-ai/issues/new/choose).</sub>
