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

<a name="apify-mcp-server"></a>
### 🥈 [apify-mcp-server](https://github.com/apify/apify-mcp-server) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · MIT · Nov 2026</sub>

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

<a name="ha-mcp"></a>
### 🥉 [ha-mcp](https://github.com/homeassistant-ai/ha-mcp) <sub>score [89](../README.md#-how-we-rank "Score 89/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.0k · MIT · Nov 2026</sub>

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

<a name="xiaohongshu-mcp"></a>
### #&#8288;4 [xiaohongshu-mcp](https://github.com/xpzouying/xiaohongshu-mcp) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Nov 2026</sub>

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

<a name="excel-mcp-server"></a>
### #&#8288;5 [excel-mcp-server](https://github.com/haris-musa/excel-mcp-server) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: known (49) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · MIT · Nov 2026</sub>

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

<a name="davinci-resolve-mcp"></a>
### #&#8288;6 [davinci-resolve-mcp](https://github.com/samuelgursky/davinci-resolve-mcp) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: known (47) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.2k · MIT · Nov 2026</sub>

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

<a name="mcp-atlassian"></a>
### #&#8288;7 [mcp-atlassian](https://github.com/sooperset/mcp-atlassian) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.1k · MIT · Nov 2026</sub>

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

<a name="zotero-mcp"></a>
### #&#8288;8 [zotero-mcp](https://github.com/54yyyu/zotero-mcp) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · MIT · Nov 2026</sub>

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
### #&#8288;9 [figma-console-mcp](https://github.com/southleft/figma-console-mcp) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (39) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · MIT · Oct 2026</sub>

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

<a name="korean-law-mcp"></a>
### #&#8288;10 [korean-law-mcp](https://github.com/chrisryugj/korean-law-mcp) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (32) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · MIT · Nov 2026</sub>

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

<a name="supergateway"></a>
### #&#8288;11 [supergateway](https://github.com/supercorp-ai/supergateway) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (34) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.0k · MIT · Nov 2026</sub>

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

<a name="letsfg"></a>
### #&#8288;12 [letsfg](https://github.com/letsfg/letsfg) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: niche (23) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · custom license · Nov 2026</sub>

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

<a name="mcp"></a>
### #&#8288;13 [mcp](https://github.com/microsoft/mcp) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.9k · MIT · Nov 2026</sub>

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

<a name="toolhive"></a>
### #&#8288;14 [toolhive](https://github.com/stacklok/toolhive) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;15 [inspector](https://github.com/mcpjam/inspector) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: niche (25) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · custom license · Nov 2026</sub>

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

<a name="firecrawl-mcp-server"></a>
### #&#8288;16 [firecrawl-mcp-server](https://github.com/firecrawl/firecrawl-mcp-server) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.9k · MIT · Nov 2026</sub>

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

<a name="open-seo-mcp-skills"></a>
### #&#8288;17 [open-seo-mcp-skills](https://github.com/ryze-ai-adgent/open-seo-mcp-skills) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: patchy (34) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Oct 2026</sub>

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

<a name="tradingview-mcp"></a>
### #&#8288;18 [tradingview-mcp](https://github.com/atilaahmettaner/tradingview-mcp) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (57) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.3k · MIT · Nov 2026</sub>

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

<a name="telegram-mcp"></a>
### #&#8288;19 [telegram-mcp](https://github.com/chigwell/telegram-mcp) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (19) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;20 [meigen-ai-design-mcp](https://github.com/jau123/meigen-ai-design-mcp) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · MIT · Nov 2026</sub>

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

<a name="pomerado"></a>
### #&#8288;21 [pomerado](https://github.com/pomerado/pomerado) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · MIT · Nov 2026</sub>

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

<a name="brightdata-mcp"></a>
### #&#8288;22 [brightdata-mcp](https://github.com/brightdata/brightdata-mcp) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: known (30) · Freshness: active (100) · Maintenance: fair (71) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.7k · MIT · Nov 2026</sub>

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

<a name="mcpvault"></a>
### #&#8288;23 [mcpvault](https://github.com/bitbonsai/mcpvault) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (10) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · MIT · Nov 2026</sub>

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

<a name="paper-search-mcp"></a>
### #&#8288;24 [paper-search-mcp](https://github.com/openags/paper-search-mcp) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: known (36) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.1k · MIT · Oct 2026</sub>

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
### #&#8288;25 [google-ads-mcp](https://github.com/googleads/google-ads-mcp) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · Apache-2.0 · Nov 2026</sub>

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

<a name="open-websearch"></a>
### #&#8288;26 [open-websearch](https://github.com/aas-ee/open-websearch) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: fair (62) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · Apache-2.0 · Nov 2026</sub>

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

<a name="duckduckgo-mcp-server"></a>
### #&#8288;27 [duckduckgo-mcp-server](https://github.com/nickclyde/duckduckgo-mcp-server) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: fair (53) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · MIT · Sep 2026</sub>

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

<a name="brave-search-mcp-server"></a>
### #&#8288;28 [brave-search-mcp-server](https://github.com/brave/brave-search-mcp-server) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: niche (5) · Freshness: active (100) · Maintenance: fair (68) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · MIT · Nov 2026</sub>

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

<a name="ros-mcp-server"></a>
### #&#8288;29 [ros-mcp-server](https://github.com/robotmcp/ros-mcp-server) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: niche (3) · Freshness: active (100) · Maintenance: fair (62) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · Apache-2.0 · Sep 2026</sub>

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

<a name="mcp-obsidian"></a>
### #&#8288;30 [mcp-obsidian](https://github.com/markuspfundstein/mcp-obsidian) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.5k · MIT · Aug 2026</sub>

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

<a name="mcp-server-mysql"></a>
### #&#8288;31 [mcp-server-mysql](https://github.com/benborla/mcp-server-mysql) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: niche (21) · Freshness: active (94) · Maintenance: weak (4) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · MIT · Jul 2026</sub>

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
### #&#8288;32 [opennews-mcp](https://github.com/6551team/opennews-mcp) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: niche (28) · Freshness: active (99) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · MIT · Aug 2026</sub>

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

<a name="terminator"></a>
### #&#8288;33 [terminator](https://github.com/mediar-ai/terminator) <sub>score [32](../README.md#-how-we-rank "Score 32/100. Adoption: niche (8) · Freshness: recent (76) · Maintenance: weak (0) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · MIT · Jun 2026</sub>

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

<sub>Needs Node.js (npx), Chrome extension for browser automation, Windows · [Repo](https://github.com/mediar-ai/terminator) · [📖 Docs ↗](https://github.com/mediar-ai/terminator/tree/main/terminator-mcp-agent) · [🌐 Site ↗](https://t8r.tech) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/terminator/)</sub>

<a name="slack-mcp-server"></a>
### #&#8288;34 [slack-mcp-server](https://github.com/korotovsky/slack-mcp-server) <sub>score [28](../README.md#-how-we-rank "Score 28/100. Adoption: niche (15) · Freshness: recent (74) · Maintenance: weak (3) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · MIT · May 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
