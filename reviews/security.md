# 🔐 Security reviews · Best of Open-Source AI

AI agents and tools for penetration testing, red-teaming and finding vulnerabilities in your own apps and models. Back to the [leaderboard](../README.md#-security).

<sub>🌐 Also on the web: [Security on archestack.com](https://archestack.com/best-of-ai/security/), each project on its own page.</sub>

<a name="strix"></a>
### 🥇 [Strix](https://github.com/usestrix/strix) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: fair (77) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 69k · Apache-2.0 · Oct 2026</sub>

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

<a name="shannon"></a>
### 🥈 [shannon](https://github.com/keygraphhq/shannon) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (34) · Freshness: active (100) · Maintenance: healthy (93) · Easy to run: easy (50) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 49k · AGPL-3.0 · Oct 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
