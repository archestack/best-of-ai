# 🔐 Security — reviews

AI agents and tools for penetration testing, red-teaming and finding vulnerabilities in your own apps and models. Back to the [leaderboard](../README.md#-security).

<a name="strix"></a>
### 🥉 59 [Strix](https://github.com/usestrix/strix) <sub>⭐ 67k · Apache-2.0 · Oct 2026</sub>

**Autonomous AI pentesting agents that validate findings with working exploits.**

CLI that runs a team of LLM agents (recon, exploitation, post-exploitation) against a local codebase, GitHub repo, live URL or OpenAPI/Postman spec. Agents work in a Docker sandbox with a Caido HTTP proxy, a Playwright browser, a shell and a Python exploit runtime, and each finding needs a working proof-of-concept. Installed by a curl script (PyPI package strix-agent); STRIX_LLM takes LiteLLM-style model strings, so OpenAI, Anthropic, Google, Bedrock, Azure, OpenRouter or a local Ollama/LM Studio endpoint all work.

- **+** Each finding is validated with a working proof-of-concept exploit, not just a pattern match
- **+** Targets code, GitHub repos, live URLs, OpenAPI/Swagger and Postman specs, or a target list
- **+** Headless mode exits non-zero on findings; GitHub Actions runs scope to changed files
- **+** Local web viewer (strix view) reads run results from disk, bound to 127.0.0.1
- **−** Needs Docker running; the first run pulls the sandbox image
- **−** Requires an LLM API key; local models only via LLM_API_BASE (Ollama, LM Studio)
- **−** Autofix PRs, continuous scanning and Jira/Slack hooks are Cloud; SSO and compliance reports are Enterprise
- **−** README documents install only as curl | bash, though a PyPI package (strix-agent) exists

<sub>no GPU · Needs docker, LLM API key · Models: OpenAI, Anthropic, Google / Vertex AI, OpenRouter, DeepSeek · [Repo](https://github.com/usestrix/strix) · [📖 Docs ↗](https://docs.strix.ai) · [🌐 Site ↗](https://strix.ai)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-selfhosted-ai/issues/new/choose).</sub>
