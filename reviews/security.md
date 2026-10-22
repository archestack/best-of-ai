# 🔐 Security reviews · Best of Open-Source AI

AI agents and tools for penetration testing, red-teaming and finding vulnerabilities in your own apps and models. Back to the [leaderboard](../README.md#-security).

<sub>🌐 Also on the web: [Security on archestack.com](https://archestack.com/best-of-ai/security/), each project on its own page.</sub>

<a name="shannon"></a>
### 🥇 [shannon](https://github.com/keygraphhq/shannon) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: healthy (94) · Easy to run: easy (50) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 49k · AGPL-3.0 · Oct 2026</sub>

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
### 🥈 [Strix](https://github.com/usestrix/strix) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: fair (78) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 71k · Apache-2.0 · Oct 2026</sub>

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
### 🥉 [pentagi](https://github.com/vxcontrol/pentagi) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (69) · Freshness: active (100) · Maintenance: fair (73) · Easy to run: easy (67) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · MIT · Oct 2026</sub>

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
### #&#8288;4 [ifixai](https://github.com/ifixai-ai/ifixai) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: healthy (96) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · Apache-2.0 · Oct 2026</sub>

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

<a name="nvidia-nemo-guardrails"></a>
### #&#8288;5 [guardrails](https://github.com/nvidia-nemo/guardrails) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (4) · Freshness: active (100) · Maintenance: fair (74) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.3k · custom license · Oct 2026</sub>

**Programmable input, output and dialog guardrails for LLM applications.**

Python library that sits between application code and the LLM and applies input, dialog, retrieval, execution and output rails. Rails are configured in config.yml and Colang files, and run through the LLMRails API or an HTTP server with a /v1/chat/completions endpoint. Built-in rails cover jailbreak detection, sensitive data masking, fact-checking, hallucination checks and NVIDIA content and topic safety models.

- **+** Five rail types: input, dialog, retrieval, execution and output
- **+** Built-in rails for jailbreak, PII masking, fact-checking and hallucination checks
- **+** Python API plus CLI server with OpenAI-style chat completions endpoint
- **+** Includes an evaluation command and LLM vulnerability scan reports
- **−** Dialog rails require learning Colang, a separate modeling language
- **−** Sends anonymous telemetry to NVIDIA by default; opt-out needed
- **−** LangChain integration is opt-in via environment variable
- **−** License is flagged NOASSERTION by detection while README badge says Apache 2.0

<sub>Docker · Needs Python 3.10-3.13, LLM provider such as OpenAI or NIM · Models: OpenAI GPT-3.5/GPT-4, LLaMa-2, Falcon, Vicuna, Mosaic · [Repo](https://github.com/nvidia-nemo/guardrails) · [📖 Docs ↗](https://docs.nvidia.com/nemo/guardrails) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nvidia-nemo-guardrails/)</sub>

<a name="garak"></a>
### #&#8288;6 [garak](https://github.com/nvidia/garak) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (25) · Freshness: active (100) · Maintenance: fair (74) · Easy to run: some setup (33) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.6k · Apache-2.0 · Oct 2026</sub>

**Command-line scanner that probes LLMs for jailbreaks, leakage and injection.**

garak runs a library of probes against a target LLM (Hugging Face, OpenAI, Bedrock, NIM, Replicate, Cohere, Groq, ggml, LiteLLM or any REST endpoint) and scores the outputs with detectors. Probes cover prompt injection, DAN-style jailbreaks, encoding attacks, toxicity, training data replay, package hallucination, malware generation and XSS. It is a pip-installed CLI that writes a log, a JSONL run report and a hit log.

- **+** Broad built-in probe set: promptinject, dan, encoding, glitch, leakreplay, malwaregen, xss and more
- **+** Many generator backends, plus a configurable REST generator for arbitrary endpoints
- **+** Plugin layout (probes, detectors, generators, harnesses) with base classes for custom additions
- **+** Per-run JSONL report and hit log show which prompts caused failures
- **−** Command-line only; the README describes no web UI
- **−** Default run uses all probes with 10 generations per prompt, which is slow and costly on paid APIs
- **−** Detectors are automated, so FAIL results still need manual review
- **−** PyPI release is updated periodically and can lag the main branch

<sub>GPU optional · Needs Python 3.11-3.14, API keys for hosted targets (OpenAI, Replicate, Cohere, Groq, NIM, Bedrock) · Models: Hugging Face, OpenAI, AWS Bedrock, Replicate, Cohere · [Repo](https://github.com/nvidia/garak) · [📖 Docs ↗](https://docs.garak.ai/) · [🌐 Site ↗](https://garak.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/garak/)</sub>

<a name="cyberstrikeai"></a>
### #&#8288;7 [cyberstrikeai](https://github.com/aipentest/cyberstrikeai) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: healthy (89) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.0k · Apache-2.0 · Oct 2026</sub>

**AI agent platform for authorized penetration testing.**

CyberStrikeAI is a Go-based platform that turns natural-language intent into governed, audited security operations, using Eino-powered multi-agent orchestration, MCP-native tool integration, and RAG knowledge retrieval. It ships 100+ curated security tool recipes (nmap, sqlmap, nuclei, metasploit, etc.), plus asset and vulnerability management, attack-chain modeling, WebShell management, and a built-in C2 framework, with RBAC, approvals and audit logging for authorized engagements.

- **+** 100+ curated tool recipes covering recon, exploitation, forensics and post-exploitation in one workspace
- **+** RBAC, approval workflows, audit logs and regex-based call blocking for governed execution
- **+** Attack-chain modeling with cross-session facts, risk scoring and step-by-step replay
- **+** One-command deployment script and built-in self-update/rollback mechanism
- **−** Includes high-risk capabilities (WebShell, built-in C2) that require careful hardening before use
- **−** No Docker/Compose support listed; deployment relies on local Go/Python setup via run.sh
- **−** Requires external AI provider API keys (OpenAI-compatible) for agent functionality
- **−** Many underlying security tools (nmap, metasploit, hashcat, etc.) must be installed separately

<sub>Needs Go 1.25+, Python 3.10+, OpenAI-compatible API, nmap, metasploit, sqlmap, nuclei, SQLite · Models: OpenAI-compatible models (e.g. GPT-4o, DeepSeek, Qwen) · port 8080 · [Repo](https://github.com/aipentest/cyberstrikeai) · [📖 Docs ↗](https://github.com/aipentest/cyberstrikeai/blob/main/docs/en-US/README.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cyberstrikeai/)</sub>

<a name="pentestgpt"></a>
### #&#8288;8 [pentestgpt](https://github.com/greydgl/pentestgpt) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: known (50) · Freshness: active (87) · Maintenance: weak (17) · Easy to run: some setup (33) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · MIT · Jul 2026</sub>

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

<a name="hexstrike-ai"></a>
### #&#8288;9 [hexstrike-ai](https://github.com/0x4m4/hexstrike-ai) <sub>score [32](../README.md#-how-we-rank "Score 32/100. Adoption: known (39) · Freshness: active (100) · Maintenance: weak (11) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · Aug 2026</sub>

**MCP server that lets AI clients drive 150+ pentesting tools.**

HexStrike AI runs a Python Flask-style server (hexstrike_server.py, default port 8888) and an MCP bridge (hexstrike_mcp.py) that lets clients such as Claude Desktop, Cursor, VS Code Copilot and Roo Code call security tools like nmap, nuclei, sqlmap, hydra, ghidra and prowler. It adds a decision engine for tool selection and 12+ named agent workflows for bug bounty, CTF and CVE work. The tools themselves must be installed separately.

- **+** Covers network, web, cloud, binary, CTF and OSINT tooling behind one MCP interface
- **+** Works with any MCP client; configs shown for Claude Desktop and VS Code Copilot
- **+** Includes a headless Chrome browser agent for screenshots, DOM and header analysis
- **+** MIT license; plain Python setup with requirements.txt
- **−** Most of the 150+ tools are not bundled and must be installed by hand
- **−** No Docker image or compose file; no tagged release
- **−** Can run offensive tools like hydra and sqlmap, so it needs strict scoping and isolation
- **−** README tool and agent counts are marketing figures; the wrappers are not independently verified

<sub>GPU optional · Needs Python 3.8+, nmap, nuclei, sqlmap and other security tools, Chrome/Chromium with chromedriver, MCP-compatible client · Models: Claude, GPT, Copilot, any MCP-compatible client · port 8888 · [Repo](https://github.com/0x4m4/hexstrike-ai) · [🌐 Site ↗](https://overthetop.ae/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hexstrike-ai/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
