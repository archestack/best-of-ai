# 🔐 Security reviews · Best of Open-Source AI

AI agents and tools for penetration testing, red-teaming and finding vulnerabilities in your own apps and models. Back to the [leaderboard](../README.md#-security).

<sub>🌐 Also on the web: [Security on archestack.com](https://archestack.com/best-of-ai/security/), each project on its own page.</sub>

<a name="shannon"></a>
### 🥇 [shannon](https://github.com/keygraphhq/shannon) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: healthy (94) · Easy to run: easy (50) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 49k · AGPL-3.0 · Oct 2026</sub>

**Autonomous pentester that exploits web apps and APIs using source code analysis.**

Shannon reads a web application's source, maps attack paths, then uses browser automation and command-line tools to run real exploits against the running app and its APIs. Only findings with a working proof of concept reach the PDF, Markdown, JSON or SARIF 2.1.0 report. It runs from an npx launcher with an ephemeral Docker worker, and also ships a GitHub Action and a GitLab CI component.

- **+** Reports only exploits with a reproducible proof of concept, which cuts speculative scanner noise
- **+** Outputs PDF, Markdown, JSON and SARIF 2.1.0; GitHub Action and GitLab CI can gate on exploited findings
- **+** Bring your own key: Anthropic, OpenAI, xAI, Bedrock, gateways, or local Ollama, vLLM and LM Studio
- **+** Supports authenticated scans (login flows, TOTP) and resumable workspaces
- **−** Needs source code of the target; black-box testing is only in paid Pro and Enterprise
- **−** Actively executes exploits, so it must not be pointed at production systems
- **−** Anthropic and OpenAI cyber safeguards can interrupt scans unless you complete their verification
- **−** Claude Code subscriptions unsupported after version 1.9.0; model API costs are yours

<sub>no GPU · Docker + Compose · Needs Docker, Node.js 18+, AI provider API key or subscription · Models: Anthropic, OpenAI, xAI, AWS Bedrock, Ollama · [Repo](https://github.com/keygraphhq/shannon) · [📖 Docs ↗](https://github.com/KeygraphHQ/shannon/blob/main/docs/ai-providers.md) · [🌐 Site ↗](https://keygraph.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/shannon/)</sub>

<a name="strix"></a>
### 🥈 [Strix](https://github.com/usestrix/strix) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: fair (78) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 69k · Apache-2.0 · Oct 2026</sub>

**Autonomous AI pentesting agents that validate vulnerabilities with working exploits.**

Strix runs teams of LLM-driven agents against a local codebase, repo URL, web app or API spec, using a Caido HTTP proxy, browser automation, shell and a Python exploit runtime inside a Docker sandbox. Findings come with proof-of-concept exploits and are written to strix_runs/, viewable with a local dashboard via `strix view`. It also runs headless in CI such as GitHub Actions and connects to user-defined MCP servers.

- **+** Validates findings with working PoCs rather than only static-analysis pattern matches
- **+** Targets code, live URLs, GitHub repos and OpenAPI/Postman specs from one CLI
- **+** Headless mode exits non-zero on findings, with a documented GitHub Actions workflow
- **+** Works with many LLM providers via LiteLLM, including local models through LLM_API_BASE
- **−** Needs a running Docker daemon and an LLM API key or ChatGPT subscription
- **−** SSO, compliance reports and VPC deployment are Enterprise-only
- **−** One-click autofix and PR reviews are listed under the paid Cloud offering
- **−** Scan quality and cost depend on the chosen model; README gives no cost or hardware figures

<sub>no GPU · Docker · Needs Docker, LLM API key, Caido, LiteLLM · Models: OpenAI, Anthropic, Google Vertex AI, DeepSeek, Moonshot · [Repo](https://github.com/usestrix/strix) · [📖 Docs ↗](https://docs.strix.ai) · [🌐 Site ↗](https://strix.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/strix/)</sub>

<a name="pentagi"></a>
### 🥉 [pentagi](https://github.com/vxcontrol/pentagi) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (57) · Freshness: active (100) · Maintenance: fair (73) · Easy to run: easy (67) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 31k · MIT · Oct 2026</sub>

**Autonomous multi-agent penetration testing system with sandboxed security tools.**

PentAGI takes a target and goal in plain language, then uses a team of specialized agents (orchestrator, researcher, developer, executor) to plan and run 20+ tools such as nmap, Metasploit and sqlmap inside an isolated Docker sandbox. Findings are stored in PostgreSQL with pgvector, with an optional Neo4j/Graphiti knowledge graph, and it produces vulnerability reports. It works with 10+ LLM providers, any OpenAI-compatible endpoint, or local models via Ollama or vLLM.

- **+** Runs 20+ pentest tools (nmap, Metasploit, sqlmap) in an isolated Docker sandbox
- **+** Supports 10+ LLM providers, custom OpenAI-compatible endpoints, and local Ollama or vLLM
- **+** Persistent memory in PostgreSQL with pgvector, optional Neo4j knowledge graph via Graphiti
- **+** REST and GraphQL APIs with Bearer tokens; Langfuse, Grafana and Prometheus integrations
- **−** Full stack spans many containers (Postgres, Neo4j, Langfuse, ClickHouse, Grafana), heavy to self-host
- **−** Agent profiles, plugins, MCP servers and attack-chain view are Enterprise-only
- **−** Not a BAS or adversary emulation tool; no predefined campaigns
- **−** Report export limited to web, Markdown and PDF; no JSON export

<sub>GPU optional · Docker + Compose · Needs Docker, Docker Compose, PostgreSQL with pgvector, Neo4j (optional), Langfuse (optional), Grafana/Prometheus (optional) · Models: OpenAI, Anthropic, Google Gemini, AWS Bedrock, Ollama · [Repo](https://github.com/vxcontrol/pentagi) · [🌐 Site ↗](https://vxcontrol.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pentagi/)</sub>

<a name="ifixai"></a>
### #&#8288;4 [ifixai](https://github.com/ifixai-ai/ifixai) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: known (42) · Freshness: active (100) · Maintenance: healthy (100) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Oct 2026</sub>

**Python CLI that audits AI agents for policy, access and reliability failures.**

iFixAi runs up to 60 inspections against a model or a deployed agent's HTTP endpoint and grades the answers with a separate judge model. The default run covers 10 checks, such as role-based tool access, prompt injection, privilege escalation and data leakage between users. It writes JSON and Markdown reports plus a terminal scorecard, and also ships as a Claude Code and Codex plugin and a skill for other agents.

- **+** Tests a real agent over its HTTP endpoint, not only a bare model API
- **+** Default 10-check suite ends in a grade; --full-run covers all 60 inspections
- **+** Citable grades use a judge from a different vendor than the system under test
- **+** Runs from CLI, CI flags, a Claude Code/Codex plugin, or a skill for other editors
- **−** A citable grade needs two API keys from different vendors
- **−** Full-suite judging costs roughly $10-18 per run, plus the agent's own bill
- **−** Bundled default fixture has seeded defects, so a custom fixture is needed for real grades
- **−** Full mode requires a hand-built fixture

<sub>no GPU · Needs Python 3.10+, LLM provider API keys (system under test and judge), uv (for skill install) · Models: OpenAI, Anthropic, Gemini, Azure, Bedrock · [Repo](https://github.com/ifixai-ai/ifixai) · [🌐 Site ↗](https://www.ifixai.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ifixai/)</sub>

<a name="pentestgpt"></a>
### #&#8288;5 [pentestgpt](https://github.com/greydgl/pentestgpt) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: niche (14) · Freshness: active (89) · Maintenance: weak (17) · Easy to run: some setup (33) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · MIT · Jul 2026</sub>

**Autonomous pentest agent that drives Claude Code or Codex against a target.**

PentestGPT runs a staged pipeline against a target IP or URL, using Claude Code or Codex as the backend to run tools and reason. CTF mode goes recon, exploit, walkthrough; pentest mode goes asset discovery, vulnerability identification, report. A separate pentestgpt-legacy mode keeps the interactive three-session design from the USENIX Security 2024 paper and supports several providers plus Ollama.

- **+** Staged pipelines for CTF and pentest modes, with saved and resumable sessions
- **+** Legacy interactive mode supports OpenAI, Anthropic, Gemini, DeepSeek, xAI, Qwen, Kimi and Ollama
- **+** Docker image bundles Claude Code and Codex CLIs, with logins persisted in volumes
- **+** Backed by a USENIX Security 2024 paper; reports 90/104 on an XBOW suite run in Dec 2025
- **−** Autonomous pipeline supports only Claude Code and Codex backends
- **−** Needs an authenticated Claude Code or Codex CLI, so a paid account or API access
- **−** Sends anonymous usage telemetry to Langfuse by default; opt out with a flag
- **−** XBOW result is historical; the shipped CLI has no XBOW runner

<sub>no GPU · Docker + Compose · Needs Python 3.12+, uv, Claude Code CLI, Codex CLI, Langfuse (telemetry, can be disabled) · Models: Claude, OpenAI, Google Gemini, DeepSeek, xAI Grok · [Repo](https://github.com/greydgl/pentestgpt) · [🌐 Site ↗](https://pentestgpt.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pentestgpt/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
