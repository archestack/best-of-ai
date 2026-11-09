# 🔌 MCP servers reviews · Best of Open-Source AI

Model Context Protocol servers that give AI assistants tools and data. Coding-focused ones are on Best of Vibe Coding. Back to the [leaderboard](../README.md#-mcp-servers).

<sub>🌐 Also on the web: [MCP servers on archestack.com](https://archestack.com/best-of-ai/mcp-servers/), each project on its own page.</sub>

<a name="servers"></a>
### 🥇 [servers](https://github.com/modelcontextprotocol/servers) <sub>score [94](../README.md#-how-we-rank "Score 94/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 92k · custom license · Nov 2026</sub>

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
### 🥈 [ha-mcp](https://github.com/homeassistant-ai/ha-mcp) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: known (38) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · MIT · Nov 2026</sub>

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

<a name="figma-console-mcp"></a>
### 🥉 [figma-console-mcp](https://github.com/southleft/figma-console-mcp) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · MIT · Oct 2026</sub>

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

<a name="opennews-mcp"></a>
### #&#8288;4 [opennews-mcp](https://github.com/6551team/opennews-mcp) <sub>score [34](../README.md#-how-we-rank "Score 34/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · MIT · Aug 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
