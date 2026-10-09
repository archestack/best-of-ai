# 🔁 Workflow automation with AI reviews · Best of Open-Source AI

Workflow and integration platforms with AI steps or agent nodes, for wiring models into the rest of your tools. Back to the [leaderboard](../README.md#-workflow-automation-with-ai).

<a name="n8n"></a>
### 🥇 [n8n](https://github.com/n8n-io/n8n) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (92) · Easy to run: some setup (33) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 207k · custom license · Oct 2026</sub>

**Visual workflow automation with code steps, AI agent nodes and 1500+ integrations.**

n8n is a fair-code workflow platform that runs as one Docker container (docker.n8n.io/n8nio/n8n, port 5678) and combines a visual canvas with JavaScript, Python and npm code nodes. AI agent and workflow nodes connect to OpenAI, Anthropic, Google or open-source models, with human-approval steps and observability, and 1500+ integrations plus 9,000+ templates cover the rest of the stack.

- **+** 1500+ integrations and 9,000+ ready-made workflow templates
- **+** Code nodes run JavaScript or Python and can pull npm packages
- **+** Single container on port 5678 with one data volume
- **+** Switch model providers without rebuilding the workflow
- **−** Sustainable Use License (fair-code, source-available), not an OSI license
- **−** Some features require a separate n8n Enterprise License
- **−** README states no database, RAM or CPU requirements

<sub>no GPU · Models: OpenAI, Anthropic, Google, open-source models · port 5678 · [Repo](https://github.com/n8n-io/n8n) · [📖 Docs ↗](https://docs.n8n.io)</sub>

<a name="activepieces"></a>
### 🥈 [Activepieces](https://github.com/activepieces/activepieces) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: healthy (86) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · custom license · Oct 2026</sub>

**Self-hosted workflow automation with TypeScript integrations, alternative to Zapier.**

Activepieces is a no-code workflow builder with loops, branches, auto retries, HTTP calls and npm-backed code steps, and flows are versioned. Integrations are called pieces: TypeScript npm packages, 280+ of which are exposed as MCP servers for Claude Desktop, Cursor or Windsurf. It also has AI pieces for several providers, human-in-the-loop approvals, and chat and form triggers.

- **+** Pieces are open-source TypeScript npm packages with hot reloading for local development
- **+** 280+ pieces usable as MCP servers from Claude Desktop, Cursor or Windsurf
- **+** Flows are versioned and support loops, branches and auto retries
- **+** Built-in approval, delay, chat and form triggers for human-in-the-loop flows
- **−** Enterprise features sit under a separate commercial license, not MIT
- **−** README does not state RAM, CPU or database requirements
- **−** Automation-first; AI agents are one feature rather than the core design
- **−** README claims of 200+ and 280+ pieces are inconsistent

<sub>no GPU · Docker + Compose · Compose runs PostgreSQL, Redis · Models: OpenAI · [Repo](https://github.com/activepieces/activepieces) · [📖 Docs ↗](https://www.activepieces.com/docs) · [🌐 Site ↗](https://activepieces.com)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
