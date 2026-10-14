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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
