# 🔌 MCP servers reviews · Best of Open-Source AI

Model Context Protocol servers that give AI assistants tools and data. Coding-focused ones are on Best of Vibe Coding. Back to the [leaderboard](../README.md#-mcp-servers).

<sub>🌐 Also on the web: [MCP servers on archestack.com](https://archestack.com/best-of-ai/mcp-servers/), each project on its own page.</sub>

<a name="servers"></a>
### 🥇 [servers](https://github.com/modelcontextprotocol/servers) <sub>score [94](../README.md#-how-we-rank "Score 94/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 92k · custom license · Nov 2026</sub>

**Reference MCP servers for files, git, fetch, memory and time.**

Official collection of reference Model Context Protocol servers maintained by the MCP steering group: Everything, Fetch, Filesystem, Git, Memory, Sequential Thinking and Time. TypeScript servers start with npx and Python ones with uvx or pip. All serve stdio; only Everything also serves Streamable HTTP. The README states they are educational examples, not production-ready.

- **+** Maintained by the MCP steering group, so it tracks the spec and official SDKs
- **+** Seven small servers covering files, git, web fetch, knowledge-graph memory and time
- **+** Starts with one command: npx for TypeScript servers, uvx or pip for Python ones
- **+** Everything server exercises prompts, resources and tools, and also serves Streamable HTTP
- **−** README says these are reference implementations, not production-ready
- **−** Only Everything supports Streamable HTTP; the other servers are stdio only
- **−** Many earlier servers (GitHub, Postgres, Slack, Redis and others) are archived
- **−** License is reported as NOASSERTION: Apache-2.0 for new contributions, MIT for older code

<sub>no GPU · Needs Node.js (npx), uv or pip (Python servers), MCP client · [Repo](https://github.com/modelcontextprotocol/servers) · [📖 Docs ↗](https://modelcontextprotocol.io/introduction) · [🌐 Site ↗](https://modelcontextprotocol.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/servers/)</sub>

<a name="ha-mcp"></a>
### 🥈 [ha-mcp](https://github.com/homeassistant-ai/ha-mcp) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.1k · MIT · Nov 2026</sub>

**MCP server that lets AI assistants configure and control Home Assistant.**

ha-mcp exposes 87 tools over the Model Context Protocol so clients such as Claude, ChatGPT and Cursor can search entities, control devices, and create or edit automations, scripts, helpers and dashboards in Home Assistant. It is built on FastMCP and installs as an in-process HACS/Marketplace integration, a Home Assistant app (add-on), Docker, or uvx/PyPI. Safety features include read-only mode, per-tool disabling and automatic edit backups.

- **+** 87 tools covering automations, dashboards, helpers, areas, backups, traces and device registry
- **+** In-process integration works on OS, Supervised, Container and Core installs
- **+** Read Only Mode, per-tool enable/disable and automatic backups before edits
- **+** Setup Wizard generates config for 15+ clients; demo server available to try first
- **−** Integration requires Home Assistant 2026.8.0 or newer
- **−** Acts with an administrator token; a leaked token or secret URL grants broad access
- **−** stdio transport has known connection problems; README recommends it only for demos
- **−** Several install paths exist; running more than one per client causes connection hangs

<sub>no GPU · Docker + Compose · Needs Home Assistant 2026.8.0+, Home Assistant administrator access token, FastMCP · Models: Claude, ChatGPT, Gemini CLI, Open WebUI, Cursor · port 9584 · [Repo](https://github.com/homeassistant-ai/ha-mcp) · [📖 Docs ↗](https://homeassistant-ai.github.io/ha-mcp/faq/) · [🌐 Site ↗](https://homeassistant-ai.github.io/ha-mcp/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ha-mcp/)</sub>

<a name="apify-mcp-server"></a>
### 🥉 [apify-mcp-server](https://github.com/apify/apify-mcp-server) <sub>score [91](../README.md#-how-we-rank "Score 91/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · MIT · Nov 2026</sub>

**Official MCP server exposing Apify Store Actors as tools for web scraping.**

MCP server that lets an agent search Apify Store, read an Actor's input schema and pricing, run it, and fetch results from its dataset. It runs hosted at mcp.apify.com over Streamable HTTP with OAuth or a bearer token, or locally over stdio via the @apify/actors-mcp-server npm package. Actors execute on the Apify platform in both modes.

- **+** One connection reaches thousands of Store Actors instead of a separate MCP server per site
- **+** Tool categories selectable via `tools` URL parameter, `--tools` flag or `TOOLS` env var
- **+** Hosted OAuth endpoint plus local stdio mode and an .mcpb bundle for supported clients
- **+** Also covers Actor builds, schedules, tasks, storage and Apify API access as opt-in tools
- **−** Requires an Apify account; Actors run and store results on Apify's platform, not locally
- **−** Actor runs are paid per Actor pricing; cost depends on each Actor
- **−** call-actor waits only 30 seconds by default, up to 45; longer runs need polling
- **−** Local stdio mode lacks inferred output schemas for Actor results

<sub>no GPU · Docker · Needs Apify account and API token or OAuth, Apify platform (Actors), Node.js 22+ for local stdio · [Repo](https://github.com/apify/apify-mcp-server) · [📖 Docs ↗](https://docs.apify.com/mcp) · [🌐 Site ↗](https://mcp.apify.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/apify-mcp-server/)</sub>

<a name="davinci-resolve-mcp"></a>
### #&#8288;4 [davinci-resolve-mcp](https://github.com/samuelgursky/davinci-resolve-mcp) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: popular (65) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.4k · MIT · Nov 2026</sub>

**MCP server that lets AI assistants drive DaVinci Resolve via its scripting API.**

Python MCP server that controls a live DaVinci Resolve Studio session through the official Scripting API, covering projects, media pool, timelines, grading, Fusion, Fairlight and render queues. It runs as a 37-tool compound server or a 390-tool granular one. An optional Node server edits .drp/.drt/.drx files with no Resolve running, and a loopback browser control panel is included.

- **+** Compound mode groups operations into 37 tools; full mode exposes 390, one per API method
- **+** Optional Node server edits .drp, .drt and .drx files offline, without Resolve running
- **+** Tool results include an _operation block with status, readback verification and change deltas
- **+** Installer configures many clients, including Claude Desktop, Cursor, VS Code and Codex CLI
- **−** External scripting needs Resolve Studio; the free edition relies on an in-app bridge
- **−** Free-edition bridge is a 21.0.x path; on 21.1 Python scripts no longer list
- **−** Bridge depends on Blackmagic leaving that path open; README says it could be closed
- **−** Live-tested API coverage is 93.6%, not 100%

<sub>no GPU · Needs DaVinci Resolve Studio 18.5+, Python 3.10+, Node.js (advanced server), ffmpeg (optional, audio tool) · port 8765 · [Repo](https://github.com/samuelgursky/davinci-resolve-mcp) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/davinci-resolve-mcp/)</sub>

<a name="excel-mcp-server"></a>
### #&#8288;5 [excel-mcp-server](https://github.com/haris-musa/excel-mcp-server) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · MIT · Nov 2026</sub>

**MCP server that lets AI clients create and edit Excel files without Excel.**

Python MCP server built on openpyxl that exposes tools for reading and editing .xlsx, .xlsm, .xltx and .xltm workbooks: cells, tables, charts, PivotTables, slicers, conditional formatting, CSV import/export and VBA reading. A built-in calculator with 479 functions computes formula values without Excel. It runs over stdio or Streamable HTTP, with folder confinement, read-only mode and bearer-token auth.

- **+** No Microsoft Excel needed; runs on Windows, macOS and Linux via uvx
- **+** Built-in calculator with 479 functions returns formula values for files never opened in Excel
- **+** Safety options: --allow-dir confinement, --read-only, formula safety checks, atomic saves
- **+** Streams reads and edits only touched rows, so 200,000-row sheets stay workable
- **−** Legacy .xls files are not supported; only CSV import as a workaround
- **−** Formulas the calculator cannot reproduce return null and are listed as uncalculated
- **−** Writing VBA is opt-in and risky if the model reads untrusted content
- **−** Large PivotTable sources can take a minute and about 2 GB of memory

<sub>no GPU · Docker · Needs uv, openpyxl · Models: Claude, Cursor, VS Code Copilot, OpenAI Codex, Gemini CLI · port 8017 · [Repo](https://github.com/haris-musa/excel-mcp-server) · [🌐 Site ↗](https://excelmcpserver.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/excel-mcp-server/)</sub>

<a name="mcp-atlassian"></a>
### #&#8288;6 [mcp-atlassian](https://github.com/sooperset/mcp-atlassian) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · MIT · Nov 2026</sub>

**MCP server exposing Jira and Confluence tools to AI assistants.**

Python MCP server that lets an AI client search, read, create and update Jira issues and Confluence pages, using JQL and CQL for queries. It works with Atlassian Cloud and Server/Data Center (Jira 8.14+, Confluence 6.0+), authenticating with API tokens, personal access tokens or OAuth 2.0. It ships 98 tools and runs over stdio via uvx, or over SSE and streamable-http.

- **+** Covers both Jira and Confluence in one server, with 98 tools
- **+** Supports Cloud and Server/Data Center with API token, PAT or OAuth 2.0
- **+** Starts with a single uvx command; Docker, pip and source installs also documented
- **+** SSE and streamable-http transports, with multi-user mode documented
- **−** Not an official Atlassian product
- **−** 98 tools may crowd an assistant's tool list or context
- **−** Covers only Jira and Confluence; no other Atlassian products listed
- **−** Quick start puts API tokens in client config env vars

<sub>no GPU · Docker · Needs Jira, Confluence, uv · [Repo](https://github.com/sooperset/mcp-atlassian) · [📖 Docs ↗](https://mcp-atlassian.soomiles.com/docs/installation) · [🌐 Site ↗](https://mcp-atlassian.soomiles.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mcp-atlassian/)</sub>

<a name="xiaohongshu-mcp"></a>
### #&#8288;7 [xiaohongshu-mcp](https://github.com/xpzouying/xiaohongshu-mcp) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Nov 2026</sub>

**MCP server that lets AI clients post, search and comment on Xiaohongshu.**

A Go MCP server that drives a headless browser to operate a logged-in Xiaohongshu account. It exposes 13 tools over streamable HTTP at /mcp: publish image or video posts (with tags, scheduling, visibility), search with filters, read feeds, post details and comments, reply, like, favorite and fetch user profiles. Works with Claude Code, Cursor, VS Code, Gemini CLI and Cline.

- **+** Covers publishing, search, comments, likes, favorites and profiles as MCP tools
- **+** Prebuilt binaries for macOS arm64, Windows x64 and Linux x64, plus Docker images
- **+** Optional Bearer token auth via AUTH_TOKEN and optional proxy via XHS_PROXY
- **+** README gives config snippets for Claude Code, Cursor, VS Code, Gemini CLI and Cline
- **−** Automates the web UI, so site changes or risk controls can break posting
- **−** One account cannot stay logged in on other web clients without kicking the MCP session
- **−** No prebuilt binary for macOS Intel or Linux ARM64
- **−** Auth is off by default; the noVNC GUI image has no password and must not be public

<sub>no GPU · Docker + Compose · Needs Headless browser (about 150MB, auto-downloaded on first run), Xiaohongshu account · port 18060 · [Repo](https://github.com/xpzouying/xiaohongshu-mcp) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/xiaohongshu-mcp/)</sub>

<a name="zotero-mcp"></a>
### #&#8288;8 [zotero-mcp](https://github.com/54yyyu/zotero-mcp) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.1k · MIT · Nov 2026</sub>

**MCP server and CLI that lets AI assistants search and annotate Zotero.**

Zotero MCP exposes a Zotero library to MCP clients such as Claude Desktop, ChatGPT and Cherry Studio. It searches by metadata, full text or embeddings, reads PDFs, places annotations, and adds items by DOI, URL, ISBN or BibTeX. The same package ships a zotero-cli with an agent skill for shell-based agents, and a plugin that adds a chat panel inside Zotero.

- **+** Local mode reads straight from zotero.sqlite; no web API key needed for reads
- **+** Agent skill uses 98 tokens of context versus 7,939 for the default 38-tool MCP profile
- **+** Semantic search supports local, OpenAI, Gemini or Ollama embeddings
- **+** Annotations are placed on exact text, figures or equations; adds items by DOI, ISBN or BibTeX
- **−** As an MCP server, tool schemas cost about 8k to 11k tokens on every request
- **−** Local writes need Zotero 10+ and a one-time authorize step, or a web API key
- **−** Semantic search, PDF layout and Scite are optional extras needing extra installs
- **−** Zotero Agent plugin is AGPL-3.0, while the server and CLI are MIT

<sub>GPU optional · Docker · Needs Zotero 7+ with local API enabled, Python 3.10+, ChromaDB and sentence-transformers (semantic extra), PyMuPDF (pdf extra) · Models: OpenAI embeddings, Gemini embeddings, Ollama embeddings, sentence-transformers (local) · [Repo](https://github.com/54yyyu/zotero-mcp) · [📖 Docs ↗](https://github.com/54yyyu/zotero-mcp/blob/main/docs/getting-started.md) · [🌐 Site ↗](https://stevenyuyy.com/zotero-mcp/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/zotero-mcp/)</sub>

<a name="figma-console-mcp"></a>
### #&#8288;9 [figma-console-mcp](https://github.com/southleft/figma-console-mcp) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (58) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · MIT · Oct 2026</sub>

**MCP server that reads and writes Figma files, variables and components.**

TypeScript MCP server exposing about 130 tools that let an AI client read and edit Figma files through a Desktop Bridge plugin: frames, components, variables, FigJam boards and Slides. It also exports tokens to DTCG JSON, compares Figma components against code, and runs WCAG and design-system health checks. It runs via npx, a cloud relay for web clients, or a read-only remote SSE endpoint.

- **+** Writes to Figma: creates components, frames, variables and FigJam boards, not just read access
- **+** Bidirectional token sync with DTCG JSON export plus 9 other formats
- **+** Deterministic checks: 14 WCAG design checks, design-code parity, scored health audit
- **+** Four connection modes, including a cloud relay for Claude.ai, v0 and Replit
- **−** Writing requires Figma Desktop with a manually imported Desktop Bridge plugin
- **−** Tool count varies by mode: 130 local, 105 cloud, read-only subset on remote SSE
- **−** Real-time monitoring and codebase extraction (figma_ds_*) work only in local mode
- **−** Plugin is cached by Figma, so some upgrades require re-importing the manifest

<sub>no GPU · Needs Node.js 18+, Figma Desktop, Figma personal access token, Desktop Bridge plugin · Models: Claude, OpenAI Codex, Gemini CLI, Cursor, Windsurf · [Repo](https://github.com/southleft/figma-console-mcp) · [📖 Docs ↗](https://docs.figma-console-mcp.southleft.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/figma-console-mcp/)</sub>

<a name="supergateway"></a>
### #&#8288;10 [supergateway](https://github.com/supercorp-ai/supergateway) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.0k · MIT · Nov 2026</sub>

**Bridges MCP servers between stdio, SSE, WebSocket and Streamable HTTP.**

Supergateway is a TypeScript CLI that wraps an MCP server and exposes it over a different transport. It converts stdio servers to SSE, WebSocket or Streamable HTTP, and remote SSE or Streamable HTTP servers to stdio or another HTTP transport. It also offers API-key auth, CORS, health endpoints, tool filtering and prefixing, and serving several servers from one mcpServers config file.

- **+** Converts between stdio, SSE, WS and Streamable HTTP with one command
- **+** Reads the Claude Desktop mcpServers config format, serving each server at /<name>
- **+** Built-in API key auth, tool allowlist and prefix, health checks, JSON logs
- **+** Ships standalone executables and a Homebrew formula, so Node is optional
- **−** Each SSE or WS connection spawns its own server process
- **−** Listens on every interface by default; no auth unless --apiKey is set
- **−** --apiKey is refused in SSE→stdio and Streamable HTTP→stdio modes
- **−** Combined-server entries go one level deep and do not support tasks yet

<sub>no GPU · Docker · Needs Node.js (or standalone executable) · port 8000 · [Repo](https://github.com/supercorp-ai/supergateway) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/supergateway/)</sub>

<a name="korean-law-mcp"></a>
### #&#8288;11 [korean-law-mcp](https://github.com/chrisryugj/korean-law-mcp) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · MIT · Nov 2026</sub>

**MCP server and CLI for Korean statutes, case law and citation checking.**

Wraps 42 Korean Ministry of Government Legislation (법제처) Open APIs into 10 MCP tools covering statutes, precedents, administrative rules, ordinances, treaties and interpretations across 23 decision domains. It also checks citations in AI-written legal answers against the official database, flagging missing articles, title mismatches and repealed laws. It runs as a hosted endpoint or locally via npm, and includes a CLI.

- **+** verify_citations checks cited articles and cases against the official DB, with the valid article range
- **+** Hosted endpoint needs no install; local npm install and CLI are also supported
- **+** 42 APIs folded into 10 tools, keeping the tool list small in client context
- **+** Point-in-time lookup, version diffs and amendment comparison tables for statutes
- **−** Korean law only; README and tool output are mostly in Korean
- **−** Keyless use of the public server shares one rate limit across all users
- **−** Local install requires a 법제처 OC key and Node.js 20.19 or newer
- **−** Depends on live 법제처 and taxlaw.nts.go.kr servers; no bundled data

<sub>no GPU · Docker · Needs 법제처 Open API (OC key), Node.js 20.19+, taxlaw.nts.go.kr · [Repo](https://github.com/chrisryugj/korean-law-mcp) · [📖 Docs ↗](https://github.com/chrisryugj/korean-law-mcp/blob/main/docs/API.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/korean-law-mcp/)</sub>

<a name="mcp"></a>
### #&#8288;12 [microsoft/mcp](https://github.com/microsoft/mcp) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.9k · MIT · Nov 2026</sub>

**Monorepo for Microsoft's Azure and Fabric MCP servers, written in C#.**

Holds the shared libraries, test frameworks and build pipelines for Microsoft's MCP servers, mainly the Azure MCP Server and the Microsoft Fabric MCP Server. The Azure server exposes Azure service tools to AI agents and installs through extensions for VS Code, Visual Studio, IntelliJ, Eclipse and Claude Code. The README also indexes other Microsoft MCP servers (Foundry, ARM, Azure DevOps, AKS, GitHub, Markitdown) that live in separate repositories or are hosted remotely.

- **+** Azure MCP Server bundles all Azure tools into one local server
- **+** Install paths for VS Code, Visual Studio, IntelliJ, Eclipse and Claude Code
- **+** Shared libraries and test tooling reduce duplication across Microsoft MCP servers
- **+** Per-server changelogs, troubleshooting guides and releases, plus Microsoft Learn docs
- **−** Tools target Azure and Fabric, so they are of little use outside Microsoft's cloud
- **−** Many listed servers live in other repos or are remote-only hosted endpoints
- **−** README is largely an index; setup detail sits in per-server READMEs
- **−** Needs Azure credentials and subscriptions to do anything useful

<sub>no GPU · Docker · Needs Azure subscription, Microsoft Fabric · [Repo](https://github.com/microsoft/mcp) · [📖 Docs ↗](https://learn.microsoft.com/azure/developer/azure-mcp-server/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mcp/)</sub>

<a name="letsfg"></a>
### #&#8288;13 [letsfg](https://github.com/letsfg/letsfg) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: known (43) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · custom license · Nov 2026</sub>

**Flight and hotel search and booking for AI agents via MCP, CLI and API.**

LetsFG is a hosted flight and hotel search and booking service that agents reach through a remote MCP server (https://letsfg.co/mcp), a Python/npm SDK and CLI, or a bearer-token HTTP API. Search runs on LetsFG's servers and is free after a one-tap connect. Booking holds the fare on a card and captures it once a PNR exists. The SDKs rank results locally.

- **+** Remote MCP endpoint works in Claude, ChatGPT, Cursor and Windsurf without a local install
- **+** Free search; booking holds the fare and captures only after a real airline PNR
- **+** Covers hotels as well as flights, with cabin class filter and CLI search
- **+** Free sandbox endpoints in the Developer API simulate booking end to end
- **−** Search and booking engine runs on LetsFG servers and is not self-hostable
- **−** Needs a hosted account token; booking requires a payment method via Revolut
- **−** Developer API is paid after 200 free searches per booking, then $0.01 each
- **−** Price-saving claims come from the vendor's own five-route comparison on one day

<sub>no GPU · Docker + Compose · Needs letsfg.co hosted API, Revolut payment setup for booking · [Repo](https://github.com/letsfg/letsfg) · [▶️ Demo ↗](https://letsfg.co) · [📖 Docs ↗](https://letsfg.co/developers/api/docs) · [🌐 Site ↗](https://letsfg.co) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/letsfg/)</sub>

<a name="toolhive"></a>
### #&#8288;14 [toolhive](https://github.com/stacklok/toolhive) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: known (45) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · Apache-2.0 · Nov 2026</sub>

**Runs MCP servers in isolated containers behind a gateway and registry.**

ToolHive runs MCP servers in isolated containers locally via Docker or Podman, or on Kubernetes through an operator with CRDs. A gateway adds OIDC/OAuth identity, access policy, audit logging and tool filtering, and a registry server curates approved servers. It ships a desktop UI, a CLI and OpenTelemetry and Prometheus support.

- **+** Each MCP server runs in its own container with a minimal permission file
- **+** Kubernetes operator with CRDs, OIDC/OAuth SSO, OpenTelemetry and Prometheus metrics
- **+** Same runtime across desktop UI, CLI and cluster deployments
- **+** Tool search and filtering to cut token usage (README claims up to 85%)
- **−** Needs Docker, Podman or Kubernetes to run servers
- **−** Registry server and desktop UI live in separate repositories
- **−** Some added capabilities are in Stacklok Enterprise, not the open-source edition
- **−** Manages and secures MCP servers; ships no MCP tools of its own

<sub>no GPU · Docker · Needs Docker or Podman, Kubernetes (for the operator) · [Repo](https://github.com/stacklok/toolhive) · [📖 Docs ↗](https://docs.stacklok.com/toolhive/) · [🌐 Site ↗](https://stacklok.com/download/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/toolhive/)</sub>

<a name="inspector"></a>
### #&#8288;15 [mcpjam/inspector](https://github.com/mcpjam/inspector) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · custom license · Nov 2026</sub>

**Inspector and eval runner for testing MCP servers across clients and models.**

MCPJam is a TypeScript tool for developers building MCP servers. It lets you call tools, resources and prompts by hand, step through OAuth flows, and chat with a server in a playground that logs every JSON-RPC message. It also runs eval test cases with expected tool calls across multiple LLMs, and ships a CLI, SDK and CI integration.

- **+** Guided OAuth debugger covers spec versions 2025-03-26 to the 2026-07-28 draft, with DCR and CIMD
- **+** Evals run expected-tool-call test cases across LLMs and track accuracy over time
- **+** CLI, SDK and CI/CD support let checks run on every PR
- **+** Runs hosted, as a Mac/Windows desktop app, via npx, or in Docker
- **−** Hosted app supports only HTTPS servers: no STDIO, tunneling, skills or tasks
- **−** Hosted skills are only available on accounts where the feature is enabled
- **−** Needs Node.js 20+ for the npx install
- **−** Workspace team sync appears to depend on the hosted service

<sub>no GPU · Needs Node.js 20+ (npx install only) · Models: 170+ models, 16 client configurations (ChatGPT, Claude, Cursor, Copilot) · port 6274 · [Repo](https://github.com/mcpjam/inspector) · [▶️ Demo ↗](https://app.mcpjam.com) · [📖 Docs ↗](https://docs.mcpjam.com) · [🌐 Site ↗](https://www.mcpjam.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/inspector/)</sub>

<a name="telegram-mcp"></a>
### #&#8288;16 [telegram-mcp](https://github.com/chigwell/telegram-mcp) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (40) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · Apache-2.0 · Nov 2026</sub>

**MCP server exposing a Telegram account to AI clients via Telethon.**

Python MCP server built on Telethon that lets Claude, Cursor and other MCP clients act on a Telegram user account. It provides 80+ tools covering chats, messages, contacts, media, folders, drafts and admin actions, with multi-account routing. It also adds voice transcription (Groq, Telegram Premium, OpenAI-compatible endpoints, local faster-whisper) and contact aliases.

- **+** 80+ tools spanning messages, chats, contacts, media, folders, drafts and admin operations
- **+** Chat allowlist and TELEGRAM_EXPOSED_TOOLS=read-only limit what an agent can touch
- **+** Four transcription engines, including local faster-whisper where audio stays on the machine
- **+** Contact aliases only send on exact saved names; fuzzy matches ask for confirmation
- **−** Acts as a full user account, not a bot, so mistakes can message real contacts
- **−** Rich message formatting requires Telegram Premium on the account
- **−** Default Groq transcription uploads voice recordings to a third party and needs an API key
- **−** Local whisper engine is unavailable in the Alpine Docker image

<sub>GPU optional · Docker + Compose · Needs Telegram account and API credentials, Telethon, Groq API key (optional, default transcription), faster-whisper (optional) · Models: MCP clients (Claude, Cursor), Groq whisper-large-v3-turbo, OpenAI-compatible /audio/transcriptions, faster-whisper · [Repo](https://github.com/chigwell/telegram-mcp) · [📖 Docs ↗](https://github.com/chigwell/telegram-mcp/blob/main/skills/README.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/telegram-mcp/)</sub>

<a name="meigen-ai-design-mcp"></a>
### #&#8288;17 [meigen-ai-design-mcp](https://github.com/jau123/meigen-ai-design-mcp) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (33) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · MIT · Nov 2026</sub>

**MCP bridge to MeiGen's hosted image and video generation and inspiration search.**

Connects MCP clients such as ChatGPT, Claude, Cursor and OpenClaw to the hosted MeiGen service. It searches inspiration images with their prompts, generates images and videos, and handles background removal, upscaling, and product or poster visuals. The main path is a remote Streamable HTTP URL with OAuth, plus an npm stdio bridge (meigen 4.0.0) for clients that need it.

- **+** Remote MCP URL with OAuth; no Node.js install or API key needed
- **+** Search and model lookups do not spend generation credits
- **+** Documented setup for ChatGPT, Claude, Cursor, VS Code, Codex and OpenClaw
- **+** Can browse saved favorites, past creations, characters and references from chat
- **−** Generation runs on the hosted service and uses purchased credits only
- **−** Only the client bridge and guides are MIT; hosted service is separate
- **−** 4.0 dropped BYOK, local file handling and prompt enhancement; these stay in 3.4.0
- **−** Interactive UI needs an MCP Apps-compatible client; others get text and media

<sub>no GPU · Docker · Needs MeiGen hosted service account (OAuth), Node.js 22.19+ (npm bridge only) · Models: Hosted image and video models via MeiGen (list unknown) · [Repo](https://github.com/jau123/meigen-ai-design-mcp) · [📖 Docs ↗](https://github.com/jau123/MeiGen-AI-Design-MCP/blob/main/SETUP.md) · [🌐 Site ↗](https://www.meigen.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/meigen-ai-design-mcp/)</sub>

<a name="firecrawl-mcp-server"></a>
### #&#8288;18 [firecrawl-mcp-server](https://github.com/firecrawl/firecrawl-mcp-server) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.9k · MIT · Nov 2026</sub>

**MCP server giving agents Firecrawl web search, scraping, crawling and browser actions.**

Wraps the Firecrawl API as an MCP server so clients like Cursor, Windsurf, VS Code and Claude Desktop can search, scrape, crawl, map and interact with web pages and get back Markdown or structured data. It runs over stdio via npx or Docker, as local Streamable HTTP on port 3000, or as a hosted endpoint with a keyless free tier limited to scrape, search and parse. It can target the cloud API or a self-hosted Firecrawl through FIRECRAWL_API_URL.

- **+** Covers scrape, crawl, map, search, browser interact, monitoring and agent jobs in one server
- **+** Hosted keyless endpoint offers scrape, search and parse without signup
- **+** Runs via npx, Docker image or local Streamable HTTP; supports self-hosted Firecrawl
- **+** Local HTTP mode checks Host and Origin headers to block DNS rebinding
- **−** Cloud use needs a Firecrawl API key and consumes paid credits
- **−** Full profile registers 31 tools, which can strain clients with tool-slot limits
- **−** Keyless tier is rate-limited and excludes crawl, map and agent
- **−** Interact calls run one turn to completion; no step-by-step client-side control

<sub>no GPU · Docker · Needs Firecrawl API (cloud or self-hosted), Node.js (npx) · port 3000 · [Repo](https://github.com/firecrawl/firecrawl-mcp-server) · [▶️ Demo ↗](https://mcp.so/playground?server=firecrawl-mcp-server) · [📖 Docs ↗](https://docs.firecrawl.dev/mcp-server) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/firecrawl-mcp-server/)</sub>

<a name="pomerado"></a>
### #&#8288;19 [pomerado](https://github.com/pomerado/pomerado) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (34) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · MIT · Nov 2026</sub>

**Generates MCP servers for websites from a plain-language task description.**

Pomerado drives a real Chromium browser to explore a site, complete an example task, and generalize it into a deterministic integration saved as TypeScript source. Each integration runs as its own local MCP stdio server and makes no model call at run time. Minting uses OpenAI models and a review step called Guardian that checks browser actions and the final source.

- **+** Needs only a text task description; no HAR file or recording required
- **+** Minted integrations run with no model request; only minting needs an API key
- **+** Works on sites behind login and two-factor authentication without saving credentials
- **+** MIT core includes minter, Guardian and local host; no account required
- **−** Minting requires an OpenAI API key; no other provider is listed for building
- **−** Supports macOS and Linux only, and Node 24.21 up to below 25
- **−** Each mint is limited to 20 minutes of active work
- **−** Hosting, saved logins and automatic repair when sites change are Cloud-only

<sub>no GPU · Needs Node 24.21+ (<25), Chromium via Playwright, OpenAI API key, MCP client · Models: OpenAI (minting), any model for the calling agent · [Repo](https://github.com/pomerado/pomerado) · [📖 Docs ↗](https://docs.pomerado.ai) · [🌐 Site ↗](https://pomerado.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pomerado/)</sub>

<a name="tooluniverse"></a>
### #&#8288;20 [tooluniverse](https://github.com/mims-harvard/tooluniverse) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (32) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · Apache-2.0 · Nov 2026</sub>

**Catalog of 2,700+ scientific tools exposed to LLM agents via MCP and Python.**

ToolUniverse packages more than 2,700 scientific models, datasets, APIs and packages behind one tool-calling interface, served as an MCP server, a Python SDK and a `tu` CLI. It targets biomedical and drug-discovery work, with unified literature search, async long-running jobs, a two-tier result cache and 153 prebuilt agent skills. A compact mode cuts the exposed tools to 4-5 discovery tools to save context.

- **+** Compact mode reduces 2,700+ tools to 4-5 discovery tools, saving context window
- **+** Runs via uvx as an MCP server, or as Python SDK and tu CLI
- **+** Two-tier cache (in-memory LRU plus SQLite) allows offline reruns and reproducibility
- **+** Local-only: no telemetry, and tool arguments go only to each tool's data provider
- **−** Tool coverage is biomedical and life-science oriented, not general-purpose
- **−** Many tools call third-party APIs and need separate API keys
- **−** Local ML and cheminformatics tools need extras; 63 skills install GPU-backed models
- **−** Apple Silicon needs macOS 14 or newer because of the faiss-cpu wheel

<sub>GPU optional · Docker · Needs Python 3.10+, uv, third-party data provider APIs (UniProt, openFDA, Open Targets) · Models: Claude, GPT, Gemini, Qwen, Deepseek · [Repo](https://github.com/mims-harvard/tooluniverse) · [📖 Docs ↗](https://zitniklab.hms.harvard.edu/ToolUniverse/) · [🌐 Site ↗](https://aiscientist.tools) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tooluniverse/)</sub>

<a name="maverick-mcp"></a>
### #&#8288;21 [maverick-mcp](https://github.com/wshobson/maverick-mcp) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 737 · MIT · Nov 2026</sub>

**MCP server for stock quotes, technical analysis, screening and portfolio tracking.**

MaverickMCP exposes Yahoo Finance data (via yfinance) to MCP clients such as Claude Desktop, Codex, Cursor and VS Code. v1.2.1 ships 38 core tools for quotes, RSI/MACD, screens, portfolios, watchlists and a trade journal, plus 12 optional backtesting tools and 3 optional research tools. Data is stored locally in SQLite or PostgreSQL, and it does not place orders.

- **+** Core tools need no API key; market data comes from yfinance
- **+** Portfolio, watchlists and trade journal persist locally in SQLite, with optional PostgreSQL
- **+** Supports STDIO and Streamable HTTP, with setup guides for several MCP clients
- **+** Backtesting and research are optional extras, so the core install stays small
- **−** HTTP endpoint has no authentication; it binds to 127.0.0.1 by default
- **−** Daily history supports US symbols and only six exchange suffixes
- **−** Depends on Yahoo Finance and finviz, which can rate limit, delay or return wrong data
- **−** Screening returns nothing until you fetch history for your own symbols

<sub>no GPU · Docker + Compose · Needs Python 3.12+, uv, Yahoo Finance (yfinance), SQLite, Redis (optional), PostgreSQL (optional), Exa or SearXNG (optional, research) · Models: anthropic, openai, openrouter, openai_compatible · port 8003 · [Repo](https://github.com/wshobson/maverick-mcp) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/maverick-mcp/)</sub>

<a name="biomcp"></a>
### #&#8288;22 [biomcp](https://github.com/genomoncology/biomcp) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 685 · MIT · Nov 2026</sub>

**CLI and MCP server for querying biomedical databases like PubMed and ClinVar.**

BioMCP is a Rust CLI with one command grammar (search, get, pivot helpers, enrich, batch) over 72 biomedical sources, including PubMed, ClinVar, ClinicalTrials.gov, OncoKB and Reactome. The same binary runs as an MCP server over stdio or Streamable HTTP, so agents such as Claude Code, Codex and Claude Desktop can call it. It also includes local study analytics for downloaded cBioPortal-style datasets.

- **+** Single binary with stdio MCP and HTTP serve modes, plus Claude Code plugin and embedded skills
- **+** Cross-entity pivots (variant to trials, drug to adverse events) without rebuilding filters
- **+** Most commands need no API key; optional keys raise rate limits or enable OncoKB, DisGeNET
- **+** JSON output includes per-section source provenance and suggested next commands
- **−** Depends on live upstream APIs; some sources restrict commercial or clinical use
- **−** Rate limiting is process-local, so many workers need one shared HTTP endpoint
- **−** HTTP server has no built-in authentication or TLS; needs a proxy or private network
- **−** PyPI package is named biomcp-cli; the plain biomcp package is unrelated

<sub>no GPU · Docker · Needs Upstream public biomedical APIs, Optional API keys: NCBI, Semantic Scholar, OpenFDA, NCI, OncoKB, DisGeNET, AlphaGenome · port 8080 · [Repo](https://github.com/genomoncology/biomcp) · [📖 Docs ↗](https://biomcp.org/) · [🌐 Site ↗](https://biomcp.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/biomcp/)</sub>

<a name="mcpproxy-go"></a>
### #&#8288;23 [mcpproxy-go](https://github.com/smart-mcp-proxy/mcpproxy-go) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 435 · MIT · Nov 2026</sub>

**MCP proxy that federates many MCP servers behind one quarantined endpoint.**

MCPProxy is a Go single-binary proxy between an AI client and many upstream MCP servers. Agents see a few discovery and call tools (retrieve_tools with BM25 search, describe_tool, call_tool_read/write/destructive) instead of every upstream schema. New servers are quarantined until reviewed, optional Docker-based scanners can check them, and calls go to a local activity log.

- **+** Single binary for macOS, Linux and Windows with the web UI embedded
- **+** New servers are quarantined and tool definition changes held for review by default
- **+** Pluggable Docker scanners (Snyk, Semgrep, Trivy, Cisco) with SARIF output and risk score
- **+** Local activity log plus a preflight command with exit codes for cron and CI
- **−** On the 45-tool benchmark the initial menu is larger than listing all tools (2625 vs 1730 tokens)
- **−** Quarantine has documented gaps: schema-only edits, and auto mode does not hold changes
- **−** Secret detection only flags by default; redaction is optional and skips arguments and non-text
- **−** Menu-bar app is macOS only; Windows gets a tray app, Linux is headless

<sub>no GPU · Docker · Needs Docker (optional, for security scanners and server isolation) · port 8080 · [Repo](https://github.com/smart-mcp-proxy/mcpproxy-go) · [📖 Docs ↗](https://docs.mcpproxy.app/) · [🌐 Site ↗](https://mcpproxy.app) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mcpproxy-go/)</sub>

<a name="blockrun-mcp"></a>
### #&#8288;24 [blockrun-mcp](https://github.com/blockrunai/blockrun-mcp) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (4) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 391 · MIT · Nov 2026</sub>

**MCP server for market data, search, media and Polymarket trades, paid per call.**

Stdio MCP server, run via npx, that exposes 19 tools to Claude Code, Codex CLI, Cursor and other MCP clients. Tools cover chat across 91 LLMs, image and video generation, web and news search, prediction-market data, on-chain queries across 40 chains, and confirm-gated Polymarket trading. Calls are paid in USDC from a local wallet via x402, or from account credit using a BlockRun API key.

- **+** Two payment modes: self-custody USDC wallet (Solana, Base, Arc) or API key with card-funded credit
- **+** Optional spend confirmation and BLOCKRUN_BUDGET_LIMIT cap paid calls
- **+** Tool profiles (trading, media, research, chat) cut schema context from 14.3K to as low as 2.2K tokens
- **+** Ships a script that measures tool-schema token cost for this or any stdio MCP server
- **−** Full profile costs about 14.3K tokens of context on every turn
- **−** Polymarket trading needs a wallet keypair; API key mode cannot trade
- **−** Depends on the hosted BlockRun gateway; wallet mode adds a $0.001 network fee per call
- **−** Spend dialog works on some clients only; Codex CLI, Gemini CLI and Windsurf proceed without asking

<sub>no GPU · Docker · Needs Node.js >=20.19, BlockRun API (api.blockrun.ai), USDC wallet (Solana, Base or Arc) or BlockRun API key · Models: 91 hosted LLMs via BlockRun · [Repo](https://github.com/blockrunai/blockrun-mcp) · [🌐 Site ↗](https://user.blockrun.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/blockrun-mcp/)</sub>

<a name="tradingview-mcp"></a>
### #&#8288;25 [tradingview-mcp](https://github.com/atilaahmettaner/tradingview-mcp) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: fair (55) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.3k · MIT · Nov 2026</sub>

**MCP server for market data, technical analysis and backtesting across stocks and crypto.**

Python MCP server exposing 39 tools to MCP clients such as Claude, Cursor, ChatGPT and Copilot. It covers screeners, technical indicators, multi-timeframe analysis, Yahoo Finance prices, news and sentiment via Marketaux, and backtesting with 9 strategies plus walk-forward validation. It uses public market data endpoints and needs no TradingView account; a paid hosted version, TradingMCP, is also offered.

- **+** 39 tools covering screeners, indicators, multi-timeframe analysis and news in one server
- **+** Backtesting with 9 strategies, walk-forward split and overfitting verdict
- **+** No TradingView account or API key needed; installs via pip or uvx
- **+** Retry, 60s cache and TA throttle reduce TradingView rate-limit errors
- **−** Depends on unofficial public endpoints, so data can be delayed, incomplete or break
- **−** News and sentiment need a Marketaux key; free tier is 100 requests/day
- **−** In-chat interactive charts are only in the paid hosted version
- **−** Informational only: no trade execution, and outputs are not financial advice

<sub>no GPU · Docker + Compose · Needs Python 3.10-3.13, uv, Marketaux API key (optional), Yahoo Finance, TradingView public endpoints · [Repo](https://github.com/atilaahmettaner/tradingview-mcp) · [📖 Docs ↗](https://tradingmcp.ai/docs) · [🌐 Site ↗](https://tradingmcp.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tradingview-mcp/)</sub>

<a name="brightdata-mcp"></a>
### #&#8288;26 [brightdata-mcp](https://github.com/brightdata/brightdata-mcp) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (50) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.7k · MIT · Nov 2026</sub>

**MCP server for web search, page scraping and remote browser control.**

Bright Data's MCP server exposes 30 tools to MCP clients: Bing/Google search, URL fetch as Markdown, text, HTML or JSON-LD, 1,200+ pre-built scrapers returning JSON, a 14-tool remote browser, and ChatGPT/Perplexity answer collection. It runs as a hosted endpoint at mcp.brightdata.com or locally via npx @brightdata/mcp with an API token. Tool groups limit what is loaded into the agent's context.

- **+** Hosted URL or local npx; documented for Claude, Cursor, VS Code, Zed, Warp and others
- **+** 1,200+ pre-built scrapers return JSON for Amazon, LinkedIn, TikTok, npm, PyPI
- **+** GROUPS and TOOLS options cut the 30 tools down to what an agent needs
- **+** Free tier of 5,000 requests per month, no credit card
- **−** Requires a Bright Data account and API token; usage beyond the free tier is paid
- **−** Backed by Bright Data's hosted scraping service, so not self-contained or offline
- **−** Scrape tools do not render JavaScript; dynamic pages need the browser tools
- **−** Batch tools capped at 5 items; pages over 40,000 characters are cut

<sub>no GPU · Docker · Needs Bright Data account and API token, Node.js (for npx) · Models: Any MCP-compatible client · [Repo](https://github.com/brightdata/brightdata-mcp) · [📖 Docs ↗](https://docs.brightdata.com/ai/mcp-server/tools) · [🌐 Site ↗](https://brightdata.com/ai/mcp-server) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/brightdata-mcp/)</sub>

<a name="mcp-server-excel"></a>
### #&#8288;27 [mcp-server-excel](https://github.com/sbroenne/mcp-server-excel) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 965 · MIT · Nov 2026</sub>

**MCP server and CLI that drive the real Microsoft Excel app via COM.**

ExcelMcp lets MCP clients and coding agents control the installed Excel application through its COM API, rather than parsing files. It exposes 64 MCP tools covering 437 operations, including Power Query, DAX, PivotTables, charts, VBA and Python in Excel. A separate CLI (excelcli) offers the same commands with built-in help and usually fewer tokens.

- **+** Uses real Excel, so PivotTables, macros, Data Model and formatting are preserved
- **+** Covers Power Query, DAX, VBA, Python =PY(), Goal Seek and charts
- **+** Same commands available as MCP server or CLI for token-lean agents
- **+** VS Code extension and Copilot CLI plugins available for install
- **−** Windows only; not intended for Linux, macOS or server-side batch use
- **−** Requires Microsoft Excel 2016 or later, a paid dependency
- **−** Needs an interactive desktop session
- **−** Cannot run on headless or CI machines

<sub>no GPU · Needs Windows, Microsoft Excel 2016 or later, .NET 10 · Models: Any MCP-compatible client, GitHub Copilot, Claude, ChatGPT · [Repo](https://github.com/sbroenne/mcp-server-excel) · [▶️ Demo ↗](https://youtu.be/wbw3-hPcE2o) · [📖 Docs ↗](https://excelmcpserver.dev/installation/) · [🌐 Site ↗](https://excelmcpserver.dev/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mcp-server-excel/)</sub>

<a name="mcpvault"></a>
### #&#8288;28 [mcpvault](https://github.com/bitbonsai/mcpvault) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: known (31) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · MIT · Nov 2026</sub>

**Local MCP server to read, search and edit Obsidian vault notes.**

MCPVault is a stdio MCP server that gives clients such as Claude Desktop, Claude Code, Cursor and Gemini CLI direct access to the files of an Obsidian vault. It exposes eighteen tools for reading, writing, patching, moving, tagging and searching notes (BM25-reranked), and restricts file operations to the vault root. Obsidian does not need to be running and no plugin is required.

- **+** Works on vault files directly; no Obsidian plugin or running Obsidian needed
- **+** Path checks block traversal, symlink escapes, dotfiles, .obsidian and .git
- **+** Optional --read-only flag removes all mutating tools from discovery
- **+** Frontmatter updates preserve formatting of unchanged YAML fields
- **−** Stdio only; no remote or HTTP transport is documented
- **−** Requires Node.js v22.12.0 or later
- **−** Note tools handle only .md, .markdown, .txt, .base and .canvas files
- **−** Search is keyword with BM25 reranking, not semantic or embedding-based

<sub>no GPU · Needs Node.js >= 22.12.0, Obsidian vault (local directory), MCP-compatible client · [Repo](https://github.com/bitbonsai/mcpvault) · [🌐 Site ↗](https://mcpvault.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mcpvault/)</sub>

<a name="open-seo-mcp-skills"></a>
### #&#8288;29 [open-seo-mcp-skills](https://github.com/ryze-ai-adgent/open-seo-mcp-skills) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: patchy (34) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Oct 2026</sub>

**Claude skills for SEO and AI-visibility work via the hosted Ryze MCP.**

Eight Markdown skills for Claude (seo-audit, keyword-research, rank-tracking, competitor-gap, backlink-check, ai-visibility, content-brief, seo-vs-ads), installable as a Claude Code plugin or copied into ~/.claude/skills. They call tools on the hosted Ryze MCP connector, which reads your Search Console, GA4 and Google Ads data, plus DataForSEO for competitor and backlink data. The MCP server itself is not in this repo.

- **+** Rankings and traffic come from your own Search Console and GA4, not scraped estimates
- **+** Skills are plain Markdown under MIT, so they can be edited or pasted into other clients
- **+** Covers audits, rank movers, competitor gaps, backlinks and GA4 AI-referral reports
- **+** Installs with three claude CLI commands or a manual copy to ~/.claude/skills
- **−** Every skill depends on the hosted Ryze connector, which is not part of this repo
- **−** Competitor and backlink data goes through DataForSEO via Ryze; pricing terms are not documented here
- **−** README is largely promotional, with comparison claims against other tools that are not substantiated
- **−** Tool availability varies by workspace, so skills rely on fallbacks

<sub>no GPU · Needs Ryze MCP connector (connector.get-ryze.ai/mcp), Google Search Console, Google Analytics 4, Google Ads, DataForSEO (via Ryze), Claude Code or other MCP client · Models: Claude · [Repo](https://github.com/ryze-ai-adgent/open-seo-mcp-skills) · [📖 Docs ↗](https://www.get-ryze.ai/how-to-connect-claude-to-google-meta-ads-mcp) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-seo-mcp-skills/)</sub>

<a name="ms-365-mcp-server"></a>
### #&#8288;30 [ms-365-mcp-server](https://github.com/softeria/ms-365-mcp-server) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (19) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · MIT · Nov 2026</sub>

**MCP server exposing 300+ Microsoft Graph endpoints for Outlook, Teams and OneDrive.**

TypeScript MCP server that maps each tool 1-to-1 to a Microsoft Graph endpoint, covering mail, calendar, OneDrive, Excel, OneNote, Planner and To Do, plus Teams, SharePoint and shared mailboxes in org mode. Authentication uses MSAL, with stdio for Claude Desktop and Claude Code and an HTTP mode with OAuth for clients such as Open WebUI. Tool surface can be cut with read-only mode, presets, regex filters and a scope allowlist.

- **+** 300+ tools defined declaratively in src/endpoints.json, one per Graph endpoint
- **+** Read-only mode, tool presets, regex filters and --allowed-scopes limit access and token use
- **+** Supports Global, China 21Vianet and GCC High clouds
- **+** --list-permissions prints required Graph scopes for pre-approved admin consent
- **−** Teams, SharePoint and shared mailboxes need --org-mode set from the start
- **−** GCC High needs your own Azure app registration and client ID
- **−** --user-fields is not a full authorization boundary; other Graph routes can leak profile data
- **−** TOON output format is experimental

<sub>no GPU · Docker · Needs Node.js >= 20, Microsoft 365 account, Azure app registration (custom or GCC High use) · [Repo](https://github.com/softeria/ms-365-mcp-server) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ms-365-mcp-server/)</sub>

<a name="oracle3-prediction-market-agent"></a>
### #&#8288;31 [oracle3-prediction-market-agent](https://github.com/yichengyang-ethan/oracle3-prediction-market-agent) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (7) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: partly (60) (each out of 100, weighted). Click for how we rank.") · ⭐ 573 · Apache-2.0 · Nov 2026</sub>

**MCP server and Python engine for prediction-market research on Kalshi and Polymarket.**

Oracle3 exposes 14 MCP tools for searching Kalshi and Polymarket contracts, reading quotes and order books, and checking fee-aware relationships (implication, exclusivity, complement, same event, event sum). It also ships six agent Skills and a Python engine with paper and live trading adapters. MCP covers market data and a local paper ledger; real orders go through the separate CLI/Python engine.

- **+** Public Kalshi and Polymarket reads need no exchange credentials
- **+** Constraint checks return baskets, per-leg fees and net edge, and work offline
- **+** Includes six Skills and a Python strategy interface with paper and live adapters
- **+** CI tests the built package through real MCP sessions on SDK 1.x and 2.x
- **−** Quickstart is an editable install from a git checkout; no Docker image
- **−** Live order execution is outside MCP and needs the separate CLI/Python engine
- **−** Model-level agent evaluation is listed as future work
- **−** Venue, data-provider and wallet integrations live in a separate oracle3-extras repo

<sub>no GPU · Needs Python 3.10+, Kalshi, Polymarket · [Repo](https://github.com/yichengyang-ethan/oracle3-prediction-market-agent) · [📖 Docs ↗](https://yichengyang-ethan.github.io/oracle3-prediction-market-agent/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/oracle3-prediction-market-agent/)</sub>

<a name="paper-search-mcp"></a>
### #&#8288;32 [paper-search-mcp](https://github.com/openags/paper-search-mcp) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (55) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.2k · MIT · Oct 2026</sub>

**MCP server for searching and downloading academic papers from 20+ sources.**

Python MCP server and Claude Code skill that searches papers across arXiv, PubMed, bioRxiv, Semantic Scholar, Crossref, OpenAlex, CORE, Europe PMC and others, then returns standardized, deduplicated results. It downloads PDFs through an open-access fallback chain (source-native, repository discovery, Unpaywall, optional Sci-Hub) and extracts text. Supports stdio, sse and streamable-http transports, with optional OAuth resource-server mode.

- **+** Concurrent multi-source search with deduplication and a single standardized Paper format
- **+** Works without API keys; optional keys for Semantic Scholar, OpenAlex, CORE, DOAJ raise limits
- **+** Open-access-first download fallback chain, with Sci-Hub off by default
- **+** Many install paths: uvx, pip, Docker, Smithery, and a CLI
- **−** Google Scholar search is often blocked by upstream bot detection and rate limits
- **−** Several sources are metadata-only or unreliable: PubMed, Crossref, OpenAIRE, BASE, CiteSeerX
- **−** Unpaywall is disabled unless an email env var is set
- **−** Local HTTP mode without OAuth is open; TLS and rate limits are left to the deployer

<sub>no GPU · Docker · Needs Python 3.10+, Unpaywall email (optional), API keys for CORE, Semantic Scholar, OpenAlex, DOAJ, IEEE (optional) · [Repo](https://github.com/openags/paper-search-mcp) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paper-search-mcp/)</sub>

<a name="google-ads-mcp"></a>
### #&#8288;33 [google-ads-mcp](https://github.com/googleads/google-ads-mcp) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · Apache-2.0 · Nov 2026</sub>

**MCP server for querying and managing Google Ads accounts from LLM agents.**

Python MCP server built on FastMCP that lets an agent run GAQL queries, read resource metadata, list accessible customers, and create assets and labels in Google Ads. Write tools use a propose-and-confirm flow: a validate_only dry run returns a checksum that must be passed back to commit. It runs over stdio with Application Default Credentials, or as a Streamable HTTP service with an OAuth proxy, including on Cloud Run.

- **+** Mutating tools require a validate_only proposal and a matching checksum before committing
- **+** tools_config.yaml toggles tools by namespace; read-only mode is two settings
- **+** Runs over stdio with ADC or Streamable HTTP with OAuth proxy; Cloud Run steps documented
- **+** OAuth state storage can use filetree, Redis, Firestore or memory
- **−** Only seven tools; no campaign, ad group or budget mutation tools are listed
- **−** Image path and video upload tools work only in local stdio mode
- **−** Connected LLM can see account data; the README warns of this
- **−** Firestore OAuth storage never deletes expired entries and needs a cleanup job

<sub>no GPU · Docker · Needs Google Ads API, Google Cloud project, OAuth client or Application Default Credentials, pipx, Redis or Firestore (optional) · port 8080 · [Repo](https://github.com/googleads/google-ads-mcp) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/google-ads-mcp/)</sub>

<a name="jacobian"></a>
### #&#8288;34 [jacobian](https://github.com/morluto/jacobian) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 378 · MIT · Nov 2026</sub>

**MCP server exposing typed math operations that agents can search and run.**

Jacobian is an MCP server with a library of narrowly scoped mathematical operations. Agents use `math.find` to match a need or inspect a contract, then `math.run` to execute it and get a typed result. Operations are backed by SymPy, NetworkX, Z3 and Python-FLINT, and the same library is available through a CLI and a Python API.

- **+** Two-step find/run interface keeps the agent's tool surface small
- **+** Operations return exact results, and mark approximation or incompleteness explicitly
- **+** Same library usable via MCP, CLI and Python API
- **+** Covers linear algebra, graphs, polynomials, SAT/SMT, finite algebra and probability
- **−** Pre-stable (0.23.0); experimental operation contracts may change between releases
- **−** Tested install contract is only CPython 3.12/3.13 on glibc Linux x86-64
- **−** Alpine/musl cannot install the full mandatory backend stack from PyPI
- **−** Singular and QEPCAD must be installed separately for a subset of operations

<sub>no GPU · Docker · Needs Python 3.12 or 3.13, uv (uvx), Node.js 20.17+ (for npx setup), Singular (optional), QEPCAD (optional) · [Repo](https://github.com/morluto/jacobian) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/jacobian/)</sub>

<a name="alpaca-mcp-server"></a>
### #&#8288;35 [alpaca-mcp-server](https://github.com/alpacahq/alpaca-mcp-server) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.1k · MIT · Nov 2026</sub>

**MCP server exposing Alpaca trading and market data tools to AI assistants.**

Python MCP server, built on FastMCP and Alpaca's OpenAPI specs, that lets clients such as Claude Desktop, Cursor and VS Code place orders and query account and market data through Alpaca's Trading API. It covers stocks, options (including multi-leg), crypto, positions, watchlists, news and corporate actions. It runs over stdio via uvx, defaults to paper trading, and can limit tools with ALPACA_TOOLSETS.

- **+** Covers stocks, options, crypto, positions, watchlists, news and corporate actions in one server
- **+** Paper trading is the default; live trading needs ALPACA_PAPER_TRADE=false
- **+** ALPACA_TOOLSETS restricts exposed tools, e.g. to read-only stock-data and crypto-data
- **+** Configured only by env vars in the client config; no files written to disk
- **−** v2 is a full rewrite with no backward compatibility with v1 tools or config
- **−** Local stdio only; no remote MCP auth, so ChatGPT and Claude Mobile are unsupported
- **−** Tied to Alpaca; requires an Alpaca account and API keys
- **−** Latest 15-minute market data needs a paid Algo Trader Plus subscription

<sub>no GPU · Docker · Needs Alpaca Trading API keys, Python 3.10+, uv, MCP client · [Repo](https://github.com/alpacahq/alpaca-mcp-server) · [📖 Docs ↗](https://docs.alpaca.markets/docs/getting-started) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/alpaca-mcp-server/)</sub>

<a name="open-websearch"></a>
### #&#8288;36 [open-websearch](https://github.com/aas-ee/open-websearch) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: known (37) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · Apache-2.0 · Nov 2026</sub>

**Keyless web search and page fetching over MCP, CLI or local HTTP.**

open-websearch scrapes results from engines such as Bing, DuckDuckGo, Brave, Exa, Baidu and Startpage, and returns titles, URLs and descriptions without API keys. It also fetches page content: generic HTTP(S) and Markdown pages, GitHub READMEs, and CSDN and Juejin articles. It runs as an MCP server (stdio, HTTP or SSE), a one-shot CLI, or a local HTTP daemon.

- **+** No API keys needed; supports 12 engines including Bing, DuckDuckGo, Brave, Exa and Hacker News
- **+** Three interfaces: MCP (stdio/HTTP/SSE), CLI, and a local daemon with POST /search and /fetch-*
- **+** Optional Playwright fallback can use a remote browser or an existing Chrome over CDP
- **+** Env vars restrict engines, rename or disable MCP tools, and route traffic through an HTTP proxy
- **−** Scrapes result pages, so blocking or markup changes can break engines; linux.do is currently unsupported
- **−** No Google support; it is still listed as a TODO
- **−** Without Playwright, JS-heavy or cookie-gated pages may fail to fetch
- **−** Local browser profiles persist cookies, so sharing one daemon across untrusted callers needs isolated browsers

<sub>no GPU · Docker + Compose · Needs Node.js, Playwright (optional) · port 3000 · [Repo](https://github.com/aas-ee/open-websearch) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-websearch/)</sub>

<a name="brave-search-mcp-server"></a>
### #&#8288;37 [brave-search-mcp-server](https://github.com/brave/brave-search-mcp-server) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: fair (71) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · MIT · Nov 2026</sub>

**MCP server exposing Brave Search web, news, image, video and place search.**

TypeScript MCP server that wraps the Brave Search API as tools: web, local, place, image, video and news search, an LLM context endpoint for grounding, and a summarizer. It runs over STDIO by default, or HTTP on port 8080. Requires a Brave Search API key; tools can be whitelisted or blacklisted by environment variable.

- **+** Nine tools cover web, news, image, video, place, local, summarizer and LLM context
- **+** Runs via npx or Docker; STDIO default, HTTP transport optional
- **+** Tools can be restricted with enabled/disabled tool lists
- **+** HTTP mode has Origin and optional Host checks against DNS rebinding
- **−** Needs a Brave Search API key; search is a hosted service, not local
- **−** HTTP endpoint has no authentication of its own
- **−** Local search needs a Pro plan, otherwise falls back to web search
- **−** Extra snippets are limited to Pro plans

<sub>no GPU · Docker + Compose · Needs Brave Search API key, Node.js 22+ (for local build) · port 8080 · [Repo](https://github.com/brave/brave-search-mcp-server) · [🌐 Site ↗](https://brave.com/search/api/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/brave-search-mcp-server/)</sub>

<a name="duckduckgo-mcp-server"></a>
### #&#8288;38 [duckduckgo-mcp-server](https://github.com/nickclyde/duckduckgo-mcp-server) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: fair (53) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · MIT · Sep 2026</sub>

**MCP server for DuckDuckGo web search and webpage text fetching.**

Python MCP server exposing three tools: search (DuckDuckGo), fetch_content (page download and text extraction with pagination) and expand_link. It runs over stdio by default, with SSE and streamable HTTP transports available. Search falls back to a curl_cffi Chrome-impersonating backend when DuckDuckGo blocks plain httpx.

- **+** Runs with one command: uvx duckduckgo-mcp-server, no API key mentioned
- **+** fetch_content has text, main and markdown parse modes plus an in-memory page cache
- **+** Blocks private, loopback and cloud-metadata addresses in fetch_content by default, including redirects
- **+** Configurable rate limits, SafeSearch, region, CA bundle and DNS-rebinding allow-lists
- **−** Search scrapes html.duckduckgo.com, which currently blocks plain httpx and can return no results
- **−** Reliable search needs the optional [browser] extra (curl_cffi) installed
- **−** Default limits of 30 searches and 20 fetches per minute
- **−** Parsed-page cache and ref:// tokens are in memory and lost on restart

<sub>no GPU · Docker · Needs DuckDuckGo (html.duckduckgo.com), uv, curl_cffi (optional, [browser] extra) · port 8000 · [Repo](https://github.com/nickclyde/duckduckgo-mcp-server) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/duckduckgo-mcp-server/)</sub>

<a name="yutu"></a>
### #&#8288;39 [yutu](https://github.com/eat-pray-ai/yutu) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 736 · Apache-2.0 · Nov 2026</sub>

**YouTube API CLI, MCP server and built-in agent for managing channels.**

yutu is a Go CLI that wraps the YouTube Data API with subcommands for videos, playlists, comments, captions, thumbnails, live broadcasts and more. The same binary runs as an MCP server, installable into agents such as Claude, opencode, pi and Codex via `yutu mcp setup`. It also has an agent mode that talks to Google, OpenAI-compatible or Anthropic endpoints, and ships a skill for other agents.

- **+** Covers a wide YouTube API surface: about 35 subcommands including live chat, captions and memberships
- **+** One binary serves as CLI, MCP server and agent, with a bundled agent skill
- **+** Agent mode supports Google, OpenAI-compatible (Ollama, vLLM) and Anthropic providers
- **+** Distributed via Homebrew, winget, npm, Docker and go install, with signed attestations
- **−** Requires creating a GCP project, enabling APIs and OAuth desktop credentials before first use
- **−** Only targets YouTube, so it is no use for other platforms
- **−** OAuth token is stored in a local JSON file, and the browser flow suits desktops better than servers
- **−** Analytics and Reporting APIs are optional extra setup in Google Cloud

<sub>no GPU · Docker · Needs Google Cloud project with YouTube Data API v3, OAuth client credentials (client_secret.json), LLM API key (agent mode only) · Models: Google Gemini, OpenAI-compatible (OpenAI, DeepSeek, Ollama, vLLM), Anthropic · port 8216 · [Repo](https://github.com/eat-pray-ai/yutu) · [▶️ Demo ↗](https://asciinema.org/a/wXIHU4ciFBAKrHfaFNkMoIs12) · [🌐 Site ↗](https://yutu.ifor.dev/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/yutu/)</sub>

<a name="ros-mcp-server"></a>
### #&#8288;40 [ros-mcp-server](https://github.com/robotmcp/ros-mcp-server) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: fair (62) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · Apache-2.0 · Sep 2026</sub>

**MCP server that lets LLMs control and inspect ROS and ROS 2 robots.**

Python MCP server that connects to a robot through the rosbridge node. An MCP client can then publish and subscribe to topics, call services, set parameters and read sensor data. It discovers available topics, services and actions, including custom types, and needs no changes to the robot's source code. It supports ROS 1 and ROS 2 (Jazzy, Humble and others).

- **+** No robot source changes; only a rosbridge node is added to the existing ROS setup
- **+** Covers topics, services, parameters and sensor reads, and can observe robot state
- **+** Works with ROS 1 and ROS 2 distros and any MCP client
- **+** Discovers custom message and service types and their syntax at runtime
- **−** Requires a rosbridge node running on the robot or network
- **−** README lists permissions as a wanted feature, so no permission layer is documented
- **−** README lists action support as a wanted contribution, so coverage may be partial
- **−** No Docker image or compose file provided

<sub>no GPU · Needs rosbridge, ROS or ROS 2, Python 3.10+ · Models: Claude, GPT, Gemini, any MCP client · [Repo](https://github.com/robotmcp/ros-mcp-server) · [▶️ Demo ↗](https://youtu.be/Yy1loJAn9sA) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ros-mcp-server/)</sub>

<a name="fetch-mcp"></a>
### #&#8288;41 [fetch-mcp](https://github.com/zcaceres/fetch-mcp) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 835 · MIT · Nov 2026</sub>

**MCP server that fetches web pages as HTML, Markdown, text, JSON or transcripts.**

A TypeScript MCP server exposing six tools: fetch_html, fetch_markdown, fetch_txt, fetch_json, fetch_readable (Mozilla Readability extraction to Markdown) and fetch_youtube_transcript. Output is paginated with max_length and start_index, and requests can use custom headers or a proxy. Private and localhost addresses are blocked. The same functions are also available as an mcp-fetch CLI.

- **+** Readability tool strips navigation and ads, returning article content as Markdown
- **+** SSRF protection blocks private/localhost addresses and DNS rebinding
- **+** Runs with npx mcp-fetch-server; same tools usable as a CLI
- **+** Pagination, custom headers, proxy and 10 MB response cap are configurable
- **−** Default output limit of 5000 characters truncates most pages unless raised
- **−** No JavaScript rendering mentioned, so script-heavy pages may return incomplete content
- **−** YouTube transcripts fall back to page extraction when yt-dlp is not installed
- **−** No tagged releases on the repository

<sub>no GPU · Needs Node.js (npx), yt-dlp (optional) · [Repo](https://github.com/zcaceres/fetch-mcp) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fetch-mcp/)</sub>

<a name="meta-ads-mcp"></a>
### #&#8288;42 [meta-ads-mcp](https://github.com/pipeboard-co/meta-ads-mcp) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (23) · Freshness: active (100) · Maintenance: fair (57) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.4k · custom license · Oct 2026</sub>

**MCP server for running Meta Ads campaigns and reporting from AI clients.**

MCP server that lets Claude, Cursor, ChatGPT or any MCP client create and update Meta (Facebook and Instagram) campaigns, ad sets, ads and creatives, and pull performance insights. The README recommends the hosted endpoint at meta-ads.mcp.pipeboard.co, which signs in through a Pipeboard account. A local streamable HTTP mode is documented in a separate guide.

- **+** Hosted remote MCP: no Meta developer token or self-hosting on the recommended path
- **+** Covers campaigns, ad sets, ads, creatives, image upload, targeting and insights (42 tools)
- **+** New campaigns, ad sets and ads default to PAUSED; writes need explicit confirmation
- **+** Token-in-URL auth available for clients that cannot do interactive login
- **−** Recommended setup depends on Pipeboard's hosted service and account, with paid tiers after the free plan
- **−** Local install needs your own Meta Developer App and is documented only briefly
- **−** License is reported as NOASSERTION, so reuse terms are unclear
- **−** README is largely about the wider Pipeboard family; the other four servers are not in this repo

<sub>no GPU · Docker · Needs Pipeboard account (hosted), Meta Ads account, Meta Developer App (local install) · Models: Claude, ChatGPT, Perplexity, Cursor, any MCP client · [Repo](https://github.com/pipeboard-co/meta-ads-mcp) · [🌐 Site ↗](https://pipeboard.co) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/meta-ads-mcp/)</sub>

<a name="financemcp"></a>
### #&#8288;43 [financemcp](https://github.com/guangxiangdebizi/financemcp) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 875 · MIT · Nov 2026</sub>

**MCP server for stock, fund, macro and crypto data with source routing.**

FinanceMCP exposes 19 MCP tools for A-share, HK and US equities, indexes, funds, bonds, futures, macro series, news and crypto candles. Requests are routed across Tushare, Qveris, Twingly and Binance with automatic fallback, and each result is labelled with the actual data source. It runs over stdio via npx or as a Streamable HTTP server, and computes MACD, RSI, KDJ, BOLL and MA locally.

- **+** Each result names the data source and shows the fallback route when one occurred
- **+** Per-request source priority via X-Finance-Source-Priority header; HTTP keys isolated per request
- **+** Binance candles and Baidu news work without any API key
- **+** tools/list is trimmed to the tools the supplied credentials can actually serve
- **−** Most tools need a Tushare token, which is gated by account points
- **−** Official hosted endpoint is offline; HTTP use requires self-deployment
- **−** README is mainly Chinese, and most tool coverage is China A-share focused
- **−** Qveris calls may consume credits; Twingly news needs a paid key

<sub>no GPU · Docker · Needs Node.js 20+, Tushare Pro token, Qveris API key (optional), Twingly API key (optional), Binance public API · port 3000 · [Repo](https://github.com/guangxiangdebizi/financemcp) · [📖 Docs ↗](https://github.com/guangxiangdebizi/FinanceMCP/blob/main/README_EN.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/financemcp/)</sub>

<a name="mcp-obsidian"></a>
### #&#8288;44 [mcp-obsidian](https://github.com/markuspfundstein/mcp-obsidian) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.6k · MIT · Aug 2026</sub>

**MCP server that reads and edits Obsidian notes via the Local REST API plugin.**

Python MCP server that lets an MCP client such as Claude Desktop list, read, search, append to, patch and delete notes in an Obsidian vault. It talks to Obsidian through the Local REST API community plugin, using an API key plus host and port (defaults 127.0.0.1 and 27124). It runs over stdio via uvx, uv, or a Docker Compose service.

- **+** Seven tools: list, read, search, append, patch, delete files and directories
- **+** Runs via uvx with no clone, or through a provided Docker Compose file
- **+** Patch inserts relative to a heading, block reference or frontmatter field
- **+** MIT licensed, small Python codebase
- **−** Requires Obsidian running with the Local REST API plugin enabled
- **−** Pinned to mcp 1.x; mcp 2.0 crashes at import
- **−** Search is a plain text query; no semantic or embedding search
- **−** delete_file can remove files or directories, so client permissions need care

<sub>no GPU · Docker + Compose · Needs Obsidian, obsidian-local-rest-api plugin, Python >= 3.11, uv · [Repo](https://github.com/markuspfundstein/mcp-obsidian) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mcp-obsidian/)</sub>

<a name="wenyan-mcp"></a>
### #&#8288;45 [wenyan-mcp](https://github.com/caol64/wenyan-mcp) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: patchy (35) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.4k · Apache-2.0 · Sep 2026</sub>

**MCP server that renders Markdown and publishes it to WeChat Official Account drafts.**

Wenyan MCP exposes the Wenyan Markdown typesetting engine as MCP tools, so a client such as Claude Desktop can render an article with a theme, manage themes and push it to the WeChat Official Account draft box. Local images and covers are uploaded to the WeChat media library automatically. It runs over stdio via npm or Docker, or as a client to a remote Wenyan Server to avoid IP whitelist problems.

- **+** Uploads local, relative and remote images and covers to WeChat automatically
- **+** Built-in themes plus custom themes registered from a CSS URL
- **+** Remote Server mode avoids IP whitelist changes and supports multiple official accounts
- **+** Installs from npm or a Docker image; Inspector debugging documented
- **−** Targets WeChat Official Accounts only; other platforms are handled by other Wenyan editions
- **−** Requires WeChat app ID and secret plus the host IP on the whitelist
- **−** Every article needs frontmatter with at least a title
- **−** README and docs are mostly in Chinese

<sub>no GPU · Docker · Needs Node.js, WeChat Official Account API credentials (WECHAT_APP_ID, WECHAT_APP_SECRET), Wenyan Server (optional, for remote mode) · [Repo](https://github.com/caol64/wenyan-mcp) · [📖 Docs ↗](https://yuzhi.tech/docs/wenyan/upload) · [🌐 Site ↗](https://wenyan.yuzhi.tech) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/wenyan-mcp/)</sub>

<a name="agent-trade-kit"></a>
### #&#8288;46 [agent-trade-kit](https://github.com/okx/agent-trade-kit) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: patchy (46) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 520 · MIT · Nov 2026</sub>

**MCP server and CLI that let AI clients trade and query an OKX account.**

Provides an MCP server (okx-trade-mcp) and a CLI (okx-trade-cli) that expose 170 tools across 11 modules of the OKX exchange API: market data, spot, swap, futures, options, account, earn, bots, event contracts, news and smart-money signals. It runs as a local stdio process with API keys kept on the user's machine. It also ships skill files for agent frameworks that drive the okx CLI.

- **+** Covers spot, swap, futures, options, earn, bots and algo orders in one tool set
- **+** Local stdio process; no server or database, keys stay on your machine
- **+** --read-only flag, per-module filtering and a built-in rate limiter limit risk
- **+** Setup command registers with Claude Desktop, Cursor, Claude Code and VS Code
- **−** Works only with OKX; no other exchanges supported
- **−** Gives an LLM write access to a live trading account, with real financial risk
- **−** 170 tools can bloat model context unless modules are filtered
- **−** No GitHub release published; versions are tracked through npm only

<sub>no GPU · Needs Node.js >= 18, OKX API credentials · Models: Any MCP-compatible client (Claude Desktop, Cursor, Claude Code, VS Code) · [Repo](https://github.com/okx/agent-trade-kit) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agent-trade-kit/)</sub>

<a name="mcp-server-mysql"></a>
### #&#8288;47 [mcp-server-mysql](https://github.com/benborla/mcp-server-mysql) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: known (42) · Freshness: active (92) · Maintenance: weak (4) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · MIT · Jul 2026</sub>

**MCP server that lets LLMs inspect and query MySQL databases.**

Exposes a MySQL database to MCP clients such as Claude Code and Claude Desktop through a single `mysql_query` tool and a `mysql://tables` resource for schema metadata. Queries are read-only unless INSERT, UPDATE or DELETE are enabled with env flags. It also supports SSH tunnels, multi-database mode, per-schema permissions, PII redaction and an HTTP remote mode with bearer auth.

- **+** Read-only by default; INSERT, UPDATE and DELETE each need a separate env flag
- **+** Per-schema read/write permissions and multi-database mode
- **+** Built-in SSH tunnel, SSL/TLS with optional mTLS, and PII masking of results
- **+** Runs via npx with no install; also offers HTTP transport with bearer token
- **−** Only one query tool, so all access goes through raw SQL
- **−** MySQL only; no other database engines
- **−** Requires Node.js 20+ and a MySQL user with suitable privileges
- **−** Quick-install examples use the root user and a plaintext password in env

<sub>no GPU · Docker · Needs Node.js 20+, MySQL 5.7+ (8.0+ recommended) · Models: Claude Code, Claude Desktop, Any MCP client · [Repo](https://github.com/benborla/mcp-server-mysql) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mcp-server-mysql/)</sub>

<a name="opennews-mcp"></a>
### #&#8288;48 [opennews-mcp](https://github.com/6551team/opennews-mcp) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: known (47) · Freshness: active (96) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · MIT · Aug 2026</sub>

**MCP server exposing crypto and financial news, signals and filings to AI assistants.**

Python MCP server that wraps the hosted 6551 API (ai.6551.io) and gives assistants tools to search news from 85+ sources across news, listing, onchain, meme, market and prediction engines. Articles carry an AI impact score (0-100), a long/short/neutral signal and EN/ZH summaries. It also offers SEC/DART company lookups, 13F holdings, and a WebSocket feed for live updates.

- **+** Filters by coin, source, engine type, AI score and trading signal
- **+** WebSocket subscription for live news with coin and engine filters
- **+** Small dependency set: mcp, httpx, websockets
- **+** Also covers company filings, 13F holdings and politician stock disclosures
- **−** Requires an API token from 6551.io; data comes from a hosted service
- **−** Strategy tools and strategy.triggered pushes need a paid subscription
- **−** Each strategy REST/MCP call consumes quota
- **−** No Docker image or release published

<sub>no GPU · Needs 6551 API (ai.6551.io), OPENNEWS_TOKEN, uv · [Repo](https://github.com/6551team/opennews-mcp) · [🌐 Site ↗](https://6551.io/mcp) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/opennews-mcp/)</sub>

<a name="opentabs"></a>
### #&#8288;49 [opentabs](https://github.com/opentabs-dev/opentabs) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (17) · Freshness: active (88) · Maintenance: weak (8) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.0k · MIT · Jul 2026</sub>

**MCP server that lets AI call web APIs through your logged-in Chrome session.**

OpenTabs pairs a local Node.js MCP server with a Chrome extension so an AI client can call the internal web APIs of sites you are already logged into, instead of using screenshots or DOM scraping. It ships 100+ plugins (about 2,000 tools) for services such as Slack, GitHub, Jira, Notion and Stripe, plus built-in browser tools. A CLI mode is available for clients without MCP.

- **+** Uses your existing browser session, so no API keys or OAuth setup
- **+** 100+ plugins covering about 2,000 tools, installed with one command
- **+** Per-plugin and per-tool permissions (Off, Ask, Auto); all tools start disabled
- **+** Plugin SDK publishes to npm; AI can generate plugins for new sites
- **−** Chrome only; extension must be loaded unpacked in developer mode
- **−** Acts with your logged-in accounts, so Auto permission can cause real side effects
- **−** Sends anonymous telemetry unless you opt out
- **−** No tagged release; installed from npm as a global CLI

<sub>no GPU · Docker · Needs Node.js 22+, Chrome · Models: Any MCP client · [Repo](https://github.com/opentabs-dev/opentabs) · [📖 Docs ↗](https://opentabs.dev/docs) · [🌐 Site ↗](https://opentabs.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/opentabs/)</sub>

<a name="sec-edgar-mcp"></a>
### #&#8288;50 [sec-edgar-mcp](https://github.com/stefanoamorelli/sec-edgar-mcp) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: niche (3) · Freshness: active (100) · Maintenance: patchy (38) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 389 · AGPL-3.0 · Oct 2026</sub>

**MCP server exposing SEC EDGAR filings, XBRL financials and insider trades.**

Python MCP server that lets an AI assistant look up companies by CIK, retrieve 10-K, 10-Q and 8-K filings with section extraction, and read XBRL-parsed balance sheet, income statement and cash flow data. It also covers Form 3/4/5 insider transactions. Runs over stdio by default, with an optional streamable HTTP transport for platforms such as Dify.

- **+** Financial statements parsed from XBRL, aimed at exact numeric values
- **+** Responses include SEC filing URLs so results can be checked
- **+** Covers 10-K, 10-Q, 8-K and Form 3/4/5 insider transactions
- **+** Promptfoo evaluation suite included in the repo
- **−** HTTP transport has no authentication; README says private networks only
- **−** AGPL-3.0; commercial use needs a separate license from the author
- **−** Limited to SEC EDGAR data; no other regulators or markets
- **−** Requires an SEC user agent string set via environment variable

<sub>no GPU · Docker · Needs SEC EDGAR, Docker or Python 3.11+ · port 9870 · [Repo](https://github.com/stefanoamorelli/sec-edgar-mcp) · [🌐 Site ↗](https://sec-edgar-mcp.amorelli.tech/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sec-edgar-mcp/)</sub>

<a name="terminator"></a>
### #&#8288;51 [terminator](https://github.com/mediar-ai/terminator) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: niche (29) · Freshness: recent (73) · Maintenance: weak (0) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · MIT · Jun 2026</sub>

**MCP server and SDKs that let AI control Windows desktop apps.**

Terminator is a Rust project that drives Windows applications through the accessibility tree, and it ships an MCP server (terminator-mcp-agent) for clients like Claude Code, Cursor and VS Code. It also provides Rust, TypeScript and partial Python SDKs, a CLI, and a workflow recorder. Workflows are meant to run as deterministic code, with a model called only for recovery.

- **+** Selects UI elements by name, role and window through the Windows accessibility tree
- **+** Installs into Claude Code or other MCP clients with one npx command
- **+** Records human workflows and turns them into deterministic automations
- **+** SDKs for Rust, TypeScript and a CLI, under the MIT license
- **−** Windows only; macOS and Linux are not supported
- **−** Python SDK is marked partial or experimental
- **−** Speed and >95% success claims come with no benchmark method in the README
- **−** Browser control needs a Chrome extension; README says many parts are experimental

<sub>Needs Node.js (npx), Chrome extension for browser automation, Windows · [Repo](https://github.com/mediar-ai/terminator) · [🌐 Site ↗](https://t8r.tech) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/terminator/)</sub>

<a name="mcp-pandoc"></a>
### #&#8288;52 [mcp-pandoc](https://github.com/vivekvells/mcp-pandoc) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: niche (8) · Freshness: active (97) · Maintenance: weak (0) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 587 · MIT · Aug 2026</sub>

**MCP server that converts documents between formats using pandoc.**

An MCP server that exposes a single `convert-contents` tool, which calls pandoc to convert text or files between markdown, html, docx, odt, rst, latex, epub, ipynb and txt, and writes pdf and pptx. It supports reference documents for docx/odt/pptx styling, YAML defaults files and pandoc filters. It runs over stdio, typically launched with `uvx mcp-pandoc` from an MCP client such as Claude Desktop.

- **+** Writes docx, odt, pptx with a reference document for custom styling
- **+** Accepts pandoc defaults files and filters for reusable conversion settings
- **+** Launches with `uvx mcp-pandoc`, no separate server process or port
- **+** Test suite covers the bidirectional conversion matrix
- **−** PDF and PPTX are write-only; pandoc cannot read PDF, and pptx input is not offered
- **−** PDF output needs a TeX Live install (xelatex) on the host
- **−** Requires a separately installed pandoc; no minimum version is declared
- **−** Advanced formats need a full output_file path; no filenames are generated

<sub>no GPU · Docker · Needs pandoc, uv, TeX Live (for PDF output) · [Repo](https://github.com/vivekvells/mcp-pandoc) · [▶️ Demo ↗](https://youtu.be/vN3VOb0rygM) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mcp-pandoc/)</sub>

<a name="mcp-server-youtube-transcript"></a>
### #&#8288;53 [mcp-server-youtube-transcript](https://github.com/kimtaeyoon83/mcp-server-youtube-transcript) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: niche (9) · Freshness: active (100) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 610 · MIT · Nov 2026</sub>

**MCP server that fetches YouTube video transcripts for AI assistants.**

A TypeScript MCP server run over stdio via npx. Its get_transcript tool takes a YouTube URL, Shorts URL or video ID and returns captions, with optional timestamps, language fallback and chapter-based sponsorship stripping. An optional analyze_video tool calls TwelveLabs Pegasus for videos with little speech, and needs a TwelveLabs API key and a direct video URL.

- **+** Accepts watch URLs, Shorts URLs and bare video IDs
- **+** Transcript fetching needs no API key or extra services
- **+** Ad and sponsorship stripping from chapter markers, on by default
- **+** Falls back to an available caption language when the requested one is missing
- **−** Only works on videos that have captions or subtitles
- **−** analyze_video needs a TwelveLabs key and rejects YouTube watch page URLs
- **−** Ad stripping depends on chapter markers being present
- **−** No tagged releases; installed from npm via npx

<sub>no GPU · Docker · Needs Node.js 18+, TwelveLabs API key (optional, for analyze_video) · Models: TwelveLabs Pegasus 1.2, TwelveLabs Pegasus 1.5 · [Repo](https://github.com/kimtaeyoon83/mcp-server-youtube-transcript) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mcp-server-youtube-transcript/)</sub>

<a name="yahoo-finance-mcp"></a>
### #&#8288;54 [yahoo-finance-mcp](https://github.com/alex2yang97/yahoo-finance-mcp) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: niche (0) · Freshness: active (100) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 372 · MIT · Sep 2026</sub>

**MCP server for Yahoo Finance stock, financials and options data.**

Python MCP server built on yfinance that gives assistants nine tools: historical OHLCV prices, stock info, news, dividends and splits, financial statements, holders, options chains and analyst recommendations. It runs locally via uvx or uv, and the README includes a Claude for Desktop config example.

- **+** Nine tools cover prices, statements, holders, options chains and analyst ratings
- **+** Launches with one uvx command straight from the Git repository
- **+** Needs only Python and uv; no GPU or model
- **+** MIT licensed
- **−** Read-only market data; no trading, screening or portfolio tools
- **−** README documents only Claude for Desktop setup, no other MCP clients
- **−** No tagged releases; uvx install tracks the Git default branch
- **−** Requires Python 3.14.6 or higher, which is a very recent version

<sub>no GPU · Docker · Needs Yahoo Finance (via yfinance), uv, Python 3.14.6+ · [Repo](https://github.com/alex2yang97/yahoo-finance-mcp) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/yahoo-finance-mcp/)</sub>

<a name="slack-mcp-server"></a>
### #&#8288;55 [slack-mcp-server](https://github.com/korotovsky/slack-mcp-server) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: known (36) · Freshness: recent (72) · Maintenance: weak (3) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · MIT · May 2026</sub>

**Slack workspace MCP server for reading, searching and posting messages.**

Go MCP server that exposes Slack to MCP clients over Stdio, SSE or HTTP. It provides tools for channel history, threads, message search, unreads, reactions, user groups and Save for Later, plus CSV resources for channels and users. It authenticates with OAuth tokens or browser session tokens (xoxc/xoxd), and posting and reactions are off by default.

- **+** Works with browser session tokens, so no Slack app install or scopes are needed
- **+** Write tools (post, reactions, mark-read) are off by default, with optional per-channel allowlists
- **+** Supports Stdio, SSE and HTTP transports plus outbound proxy settings
- **+** Covers DMs, group DMs, threads, unreads with mention filter, and user groups
- **−** Message search and unreads are unavailable with bot tokens (xoxb)
- **−** Saved-items tools require browser session tokens (xoxc/xoxd)
- **−** Unreads fall back to one API call per channel with xoxp tokens, slow on large workspaces
- **−** Browser-token mode depends on extracting session tokens from a logged-in browser

<sub>no GPU · Docker + Compose · Needs Slack workspace, Slack OAuth or browser session tokens · [Repo](https://github.com/korotovsky/slack-mcp-server) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/slack-mcp-server/)</sub>

<a name="mcp-massive"></a>
### #&#8288;56 [mcp_massive](https://github.com/massive-com/mcp_massive) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: niche (5) · Freshness: active (98) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 405 · MIT · Oct 2026</sub>

**MCP server exposing the Massive.com financial data API via search, call and SQL tools.**

Python MCP server for the Massive.com market data API. Instead of one tool per endpoint, it offers three tools: search_endpoints, call_api and query_data. API results can be stored as in-memory SQLite tables, queried with SQL, and post-processed with built-in functions such as Black-Scholes greeks, return metrics, SMA and EMA.

- **+** Three composable tools cover the whole API instead of one tool per endpoint
- **+** Endpoint index loads from llms.txt at startup, so it tracks API changes
- **+** In-memory SQLite storage with SQL (CTEs, window functions) for analyzing results
- **+** Built-in Black-Scholes greeks, Sharpe/Sortino, SMA and EMA; hosted option at mcp.massive.com
- **−** Requires a Massive.com API key; data access depends on that vendor
- **−** README marks the project experimental with possible breaking changes
- **−** PRs not tied to a prior issue are generally declined
- **−** Tied to one vendor's API, not a general financial data server

<sub>no GPU · Docker + Compose · Needs Massive.com API key, Python 3.12+, uv 0.4.0+ · Models: Any MCP client (Claude Code, Claude Desktop) · [Repo](https://github.com/massive-com/mcp_massive) · [▶️ Demo ↗](https://mcp.massive.com) · [📖 Docs ↗](https://massive.com/docs) · [🌐 Site ↗](https://massive.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mcp-massive/)</sub>

<a name="metatrader-mcp-server"></a>
### #&#8288;57 [metatrader-mcp-server](https://github.com/ariadng/metatrader-mcp-server) <sub>score [19](../README.md#-how-we-rank "Score 19/100. Adoption: niche (14) · Freshness: slowing (31) · Maintenance: weak (0) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 859 · MIT · Mar 2026</sub>

**MCP server exposing MetaTrader 5 trading and market data to AI assistants.**

Python bridge that exposes MetaTrader 5 account info, market data, order placement and position management as MCP tools. It runs over stdio, SSE or streamable-http, and also ships a REST API for Open WebUI, a WebSocket tick streamer and a Python client library. It needs a local MT5 terminal, so remote use means running it on a Windows VPS.

- **+** Covers account, candles, market and pending orders, and bulk position closes
- **+** Several interfaces: MCP (stdio, SSE, streamable-http), REST with OpenAPI docs, WebSocket quotes
- **+** Also usable as a Python library, installed with pip
- **+** Includes a Claude skill that chains the trading tools
- **−** MCP SSE server has no authentication; README advises firewall, proxy or SSH tunnel
- **−** Requires a running MT5 terminal; remote use needs a Windows VPS
- **−** No Docker image; listed as planned on the roadmap
- **−** Bundled skill executes trades without extra confirmation

<sub>no GPU · Needs MetaTrader 5 terminal, MT5 trading account, Python 3.10+ · Models: Claude Desktop, Claude Code, Open WebUI · port 8080 · [Repo](https://github.com/ariadng/metatrader-mcp-server) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/metatrader-mcp-server/)</sub>

<a name="evm-mcp-server"></a>
### #&#8288;58 [evm-mcp-server](https://github.com/mcpdotdirect/evm-mcp-server) <sub>score [19](../README.md#-how-we-rank "Score 19/100. Adoption: niche (2) · Freshness: recent (63) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 381 · MIT · Jun 2026</sub>

**MCP server for reading and writing to 60+ EVM chains, with ENS support.**

TypeScript MCP server built on viem that lets agents query blocks, transactions, balances and contracts on 34 EVM mainnets and 26 testnets. It also sends native, ERC20, ERC721 and ERC1155 transfers, signs messages and EIP-712 data, and fetches ABIs through the Etherscan v2 API. It runs over stdio or HTTP with SSE, and accepts ENS names wherever an address is expected.

- **+** Covers 60+ EVM networks behind one tool interface, with ENS names accepted for addresses
- **+** Auto-fetches contract ABIs via Etherscan v2, so contract calls need no ABI up front
- **+** Runs through npx in stdio mode or as an HTTP/SSE server
- **+** Wallet can be set from a private key or a BIP-39 mnemonic with HD account index
- **−** Private key or mnemonic sits in an environment variable for write and signing tools
- **−** HTTP mode binds 0.0.0.0:3001, hardcoded in source, with no auth described
- **−** README states 22 tools in one place and 25 in another
- **−** Default chain and server host/port can only be changed by editing source files

<sub>no GPU · Needs Bun 1.0+ or Node.js 20+, Etherscan API key (optional, for ABI fetching), EVM RPC endpoints · port 3001 · [Repo](https://github.com/mcpdotdirect/evm-mcp-server) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/evm-mcp-server/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
