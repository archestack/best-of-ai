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

<a name="xiaohongshu-mcp"></a>
### 🥈 [xiaohongshu-mcp](https://github.com/xpzouying/xiaohongshu-mcp) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: popular (80) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Nov 2026</sub>

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

<a name="apify-mcp-server"></a>
### 🥉 [apify-mcp-server](https://github.com/apify/apify-mcp-server) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · MIT · Nov 2026</sub>

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
### #&#8288;4 [ha-mcp](https://github.com/homeassistant-ai/ha-mcp) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: known (45) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.2k · MIT · Nov 2026</sub>

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

<a name="mcp-atlassian"></a>
### #&#8288;5 [mcp-atlassian](https://github.com/sooperset/mcp-atlassian) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: known (36) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.1k · MIT · Nov 2026</sub>

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
### #&#8288;6 [zotero-mcp](https://github.com/54yyyu/zotero-mcp) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (31) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.9k · MIT · Nov 2026</sub>

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
### #&#8288;7 [figma-console-mcp](https://github.com/southleft/figma-console-mcp) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · MIT · Oct 2026</sub>

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

<a name="firecrawl-mcp-server"></a>
### #&#8288;8 [firecrawl-mcp-server](https://github.com/firecrawl/firecrawl-mcp-server) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: fair (53) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.8k · MIT · Nov 2026</sub>

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
### #&#8288;9 [pomerado](https://github.com/pomerado/pomerado) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · MIT · Nov 2026</sub>

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

<a name="open-seo-mcp-skills"></a>
### #&#8288;10 [open-seo-mcp-skills](https://github.com/ryze-ai-adgent/open-seo-mcp-skills) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: popular (60) · Freshness: active (100) · Maintenance: patchy (34) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.3k · MIT · Oct 2026</sub>

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

<a name="google-ads-mcp"></a>
### #&#8288;11 [google-ads-mcp](https://github.com/googleads/google-ads-mcp) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · Apache-2.0 · Nov 2026</sub>

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

<a name="tradingview-mcp"></a>
### #&#8288;12 [tradingview-mcp](https://github.com/atilaahmettaner/tradingview-mcp) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: fair (56) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.3k · MIT · Nov 2026</sub>

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

<a name="opennews-mcp"></a>
### #&#8288;13 [opennews-mcp](https://github.com/6551team/opennews-mcp) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · MIT · Aug 2026</sub>

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
