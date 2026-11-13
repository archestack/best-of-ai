# 🔐 Security reviews · Best of Open-Source AI

AI agents and tools for penetration testing, red-teaming and finding vulnerabilities in your own apps and models. Back to the [leaderboard](../README.md#-security).

<sub>🌐 Also on the web: [Security on archestack.com](https://archestack.com/best-of-ai/security/), each project on its own page.</sub>

<a name="shannon"></a>
### 🥇 [shannon](https://github.com/keygraphhq/shannon) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 52k · AGPL-3.0 · Nov 2026</sub>

**Autonomous pentester that exploits web apps and APIs using source analysis.**

Shannon reads a target app's source, builds a queue of candidate attack paths, then uses browser automation and CLI tools to try real exploits against the running app. Only findings with a working proof of concept reach the PDF, Markdown, JSON or SARIF 2.1.0 report. It runs from an npx launcher with a Docker worker, and has GitHub Actions and GitLab CI components that can fail a pipeline on exploited vulnerabilities.

- **+** Reports only exploits with a reproducible proof of concept, which cuts speculative findings
- **+** Outputs PDF, Markdown, JSON and SARIF 2.1.0, with GitHub and GitLab CI integrations
- **+** Bring your own key: Anthropic, OpenAI, xAI, Bedrock, gateways, or local Ollama, vLLM, LM Studio
- **+** Supports authenticated scans (login flows, TOTP) and resumable workspaces
- **−** Needs the target's source code; black-box testing is only in paid editions
- **−** Actively executes exploits, so it must not be run against production
- **−** Covers injection, XSS, SSRF, authentication and authorization only
- **−** Claude Code subscriptions unsupported after version 1.9.0; AGPL-3.0 license

<sub>no GPU · Docker + Compose · Needs Docker, Node.js 22+, LLM provider credentials · Models: Anthropic, OpenAI, xAI, AWS Bedrock, Ollama · [Repo](https://github.com/keygraphhq/shannon) · [📖 Docs ↗](https://github.com/KeygraphHQ/shannon-action) · [🌐 Site ↗](https://keygraph.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/shannon/)</sub>

<a name="ifixai"></a>
### 🥈 [ifixai](https://github.com/ifixai-ai/ifixai) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 45k · Apache-2.0 · Nov 2026</sub>

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

<a name="strix"></a>
### 🥉 [Strix](https://github.com/usestrix/strix) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 75k · Apache-2.0 · Nov 2026</sub>

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

<a name="ai-infra-guard"></a>
### #&#8288;4 [ai-infra-guard](https://github.com/tencent/ai-infra-guard) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: known (47) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · Apache-2.0 · Nov 2026</sub>

**Red-teaming platform for AI infra CVEs, MCP servers, agent skills and jailbreaks.**

A.I.G (AI-Infra-Guard) from Tencent Zhuque Lab is a web platform that fingerprints running AI services such as Ollama, vLLM, ComfyUI and n8n against 2000+ CVE rules. It also scans MCP servers and agent skills from source or URL, runs jailbreak evaluations against a target LLM API, and includes a model and API relay checker. Standalone CLIs exist for skill, MCP and agent scanning.

- **+** Fingerprints 100+ AI components (Ollama, vLLM, ComfyUI, n8n, Triton) against 2000+ CVE rules
- **+** Covers infra CVEs, MCP and skill scanning, and jailbreak evaluation in one web UI
- **+** Separate CLIs such as pip-installable aig-skill-scan fit into CI/CD pipelines
- **+** Rules are YAML files under data/, so contributing fingerprints is straightforward
- **−** No authentication; README says not to deploy on public networks
- **−** Skill scanning needs an external LLM API key
- **−** Online Pro version with extra features requires an invitation code
- **−** API checker from source needs a Python venv and a Go build

<sub>RAM ≥ 4 GB · no GPU · Docker + Compose · Needs Docker 20.10+, LLM API key for skill, MCP and jailbreak scans · Models: OpenAI-compatible LLM APIs (base URL + key) · port 8088 · [Repo](https://github.com/tencent/ai-infra-guard) · [📖 Docs ↗](https://tencent.github.io/AI-Infra-Guard/) · [🌐 Site ↗](https://aigsec.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai-infra-guard/)</sub>

<a name="pentagi"></a>
### #&#8288;5 [pentagi](https://github.com/vxcontrol/pentagi) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: fair (60) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · MIT · Oct 2026</sub>

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

<a name="aisoc"></a>
### #&#8288;6 [aisoc](https://github.com/beenuar/aisoc) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: known (49) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · MIT · Nov 2026</sub>

**Self-hosted SOC that detects threats and investigates alerts with auditable AI agents.**

AiSOC ingests security telemetry through 91 connectors and four cloud collectors, runs 2966 executable detection rules, correlates alerts into incidents, and has AI agents triage them. Every prompt and tool call goes to an Investigation Ledger that exports as a signed bundle, and response actions need human approval. The core stack bundles a local llama3.2:3b model via Ollama and runs on Kafka, Postgres, Redis and Qdrant.

- **+** Every agent prompt, tool call and citation is logged and exports as a signed evidence bundle
- **+** Ships a local model, so triage works with no API key or hosted provider
- **+** Response actions and playbooks default to preview and need a separate approver
- **+** Detection rules count as executable only after replay proves they fire
- **−** Heavy stack: 16 services and about 8 GB RAM for core, about 12 GB for full
- **−** No hosted LLM provider has been tested; bundled 3B model is not frontier-class
- **−** Event lake, entity graph and full-text search need the larger full profile
- **−** Splunk rule migration is mostly partial: 1,711 of 1,734 translated rules

<sub>RAM ≥ 8 GB · GPU optional · Compose · Needs Docker Compose v2, Kafka, Postgres, Redis, Qdrant, Ollama, ClickHouse (full), Neo4j (full), OpenSearch (full) · Models: Ollama llama3.2:3b-instruct-q4_K_M (bundled), Local OpenAI-compatible endpoints, Custom providers via console · [Repo](https://github.com/beenuar/aisoc) · [📖 Docs ↗](https://beenuar.github.io/AiSOC/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/aisoc/)</sub>

<a name="failproofai"></a>
### #&#8288;7 [failproofai](https://github.com/failproofai/failproofai) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: popular (57) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.8k · custom license · Nov 2026</sub>

**Policy enforcement and run tracing for coding agent CLIs and gateways.**

Failproof AI installs hooks into 12 agent harnesses (Claude Code, Codex, Copilot CLI, Cursor Agent, OpenCode, Hermes, OpenClaw and others). It blocks tool calls such as rm -rf, sudo, force pushes and .env reads before they run, using 40 built-in policies plus custom JS policies. A local dashboard on localhost:8020 shows session history, hook decisions and an offline audit of past runs.

- **+** Pre-execution blocking of tool calls verified on all 12 supported harnesses
- **+** Custom policies are JS files in .failproofai/policies/, committed and shared with the team
- **+** Local dashboard and audit read existing history with no account or upload
- **+** Policy API is small: allow, deny, instruct
- **−** License is MIT with Commons Clause, not OSI open source; resale needs a separate agreement
- **−** Setup selects no policies; only block-failproofai-commands is active until a pack is added
- **−** Turn-end gates work on 8 of 12 harnesses; capabilities differ per harness
- **−** Fleet-wide observability and cluster self-hosting are hosted or Enterprise offerings

<sub>no GPU · Docker · Needs Node.js (npm) · port 8020 · [Repo](https://github.com/failproofai/failproofai) · [📖 Docs ↗](https://docs.befailproof.ai/) · [🌐 Site ↗](https://befailproof.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/failproofai/)</sub>

<a name="garak"></a>
### #&#8288;8 [garak](https://github.com/nvidia/garak) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Nov 2026</sub>

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

<a name="nvidia-nemo-guardrails"></a>
### #&#8288;9 [guardrails](https://github.com/nvidia-nemo/guardrails) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (44) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · custom license · Nov 2026</sub>

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

<a name="decepticon"></a>
### #&#8288;10 [decepticon](https://github.com/bittersecurity/decepticon) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (35) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.6k · Apache-2.0 · Nov 2026</sub>

**Autonomous red-team agents that run multi-stage attack chains from an approved plan.**

Decepticon is a red-team system with 16 specialist agents covering recon, exploitation, post-exploitation, AD, cloud and reversing. Commands run in persistent tmux sessions inside a Kali sandbox on a separate network, and findings go to a Neo4j knowledge graph. Models are routed through LiteLLM, and it ships a terminal CLI, an on-demand web dashboard and an MCP server for Claude Code and Codex.

- **+** Reports 102/104 (98.08%) on XBOW validation benchmarks, with per-challenge results published
- **+** Persistent tmux sessions let interactive tools like msfconsole and evil-winrm work
- **+** Kali sandbox runs on its own network, separate from the management plane
- **+** Supports ten providers including local Ollama, with tiered fallback chains
- **−** Needs Docker Compose with several services: LiteLLM, PostgreSQL, Neo4j, LangGraph, sandbox
- **−** LangGraph drives the sandbox through the Docker socket, which widens host exposure
- **−** Offensive Vaccine defense loop is described as planned, not shipped
- **−** Hosted app and commercial demo are promoted; the gap to the open-source CLI is unclear

<sub>no GPU · Docker + Compose · Needs Docker, Docker Compose v2, LiteLLM, PostgreSQL, Neo4j, LangGraph · Models: Anthropic, OpenAI, Google Gemini, MiniMax, DeepSeek · [Repo](https://github.com/bittersecurity/decepticon) · [▶️ Demo ↗](https://app.decepticon.red) · [📖 Docs ↗](https://docs.decepticon.red) · [🌐 Site ↗](https://decepticon.red) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/decepticon/)</sub>

<a name="cyberstrikeai"></a>
### #&#8288;11 [cyberstrikeai](https://github.com/aipentest/cyberstrikeai) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.6k · Apache-2.0 · Nov 2026</sub>

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

<a name="bla"></a>
### #&#8288;12 [bla](https://github.com/qybaihe/bla) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: niche (23) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.4k · MIT · Nov 2026</sub>

**Hardens release artifacts against AI reverse-engineering agents.**

BLA (npm package bla-agents) is a TypeScript CLI and MCP server that rewrites release artifacts with decoys, honey SourceMaps and format-specific resource-limit triggers, so AI reverse-engineering agents such as morluto/rea hit budget or capacity errors. It covers 19+ formats including JS, Electron ASAR, WASM, SQLite, Safetensors, GGUF and PE, and ships Vite, Rollup, Webpack and esbuild plugins.

- **+** Format shields are pure TypeScript/Node, with no Ghidra, IDA or packer dependency
- **+** One setup command registers MCP tools with Claude Code, Cursor, Codex, Gemini CLI and others
- **+** Empirical table names the exact REA limit tripped per format, reproducible via npm run redteam:rea
- **+** Bundler plugins for Vite, Rollup, Webpack and esbuild; opt-in ed25519 signed manifests
- **−** Token and USD amplification figures are internal estimates, not measured against live agents
- **−** Ghidra, Frida, LLDB, JADX and firmware paths are not empirically tested
- **−** Runtime equivalence is verified only on bundled fixtures; custom artifacts need your own tests
- **−** Protection depends on specific REA analyzer limits; other tools may not be affected

<sub>no GPU · Needs Node.js ^22.23.4 or >=24, Wabt (optional, red-team suite), tshark (optional, red-team suite) · Models: Safetensors, GGUF · [Repo](https://github.com/qybaihe/bla) · [📖 Docs ↗](https://bla.tools/guides/) · [🌐 Site ↗](https://bla.tools/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/bla/)</sub>

<a name="agentic-bug-hunter"></a>
### #&#8288;13 [agentic-bug-hunter](https://github.com/awarexone/agentic-bug-hunter) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · MIT · Nov 2026</sub>

**Bug bounty CLI that runs recon, hunting, validation and report writing with LLMs.**

Python CLI (`bughunter`) and Claude Code plugin that drives a bug bounty workflow: recon with external tools, LLM-guided testing for web and smart contract bug classes, a 7-Question validation gate, and report drafts for HackerOne, Bugcrowd, Intigriti and Immunefi. It works with Ollama, Groq, DeepSeek, Claude, OpenAI, OpenRouter, LiteLLM and others, and keeps hunt memory across sessions. An MCP server is also included.

- **+** Supports Ollama for fully local runs, plus about ten cloud providers and gateways
- **+** Covers recon, hunt, validate and report in one CLI, also as Claude Code slash commands
- **+** Persistent hunt memory with resume via /pickup and a 10 MB rotated JSONL cap
- **+** Ships an MCP server where active tools require scope and explicit approval
- **−** Full recon needs subfinder, httpx, nuclei, katana, ffuf and nmap installed separately
- **−** No Docker or compose setup; installs via pip, uv or install.sh
- **−** Output quality depends on the chosen model; local setup suggests a ~9 GB qwen2.5:14b
- **−** README gives payout ranges and logos but no benchmarks of real findings

<sub>GPU optional · Needs subfinder, httpx, nuclei, katana, ffuf, nmap, Ollama or a cloud LLM API key · Models: Ollama, Groq, DeepSeek, Claude API, OpenAI · [Repo](https://github.com/awarexone/agentic-bug-hunter) · [📖 Docs ↗](https://github.com/awarexone/Agentic-Bug-Hunter/blob/main/docs/mcp.md) · [🌐 Site ↗](https://www.awarexone.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agentic-bug-hunter/)</sub>

<a name="t3mp3st"></a>
### #&#8288;14 [t3mp3st](https://github.com/elder-plinius/t3mp3st) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: known (40) · Freshness: active (100) · Maintenance: fair (77) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.0k · AGPL-3.0 · Sep 2026</sub>

**Multi-agent offensive-security framework driven by your coding agent or local model.**

T3MP3ST runs a recon, exploit and report kill chain against authorized targets from a browser War Room or CLI. It uses a connected local coding agent (Claude Code, Codex, Hermes, OpenCode, Oh My Pi), an API key, or an offline model via Ollama or an OpenAI-compatible server. Its benchmark claims (XBEN 90.1% pass@1, Cybench 23/40) come from a single-agent loop and recompute with `npm run verify-claims`.

- **+** Benchmark numbers re-derive from committed data with `npm run verify-claims`
- **+** Works keyless via a signed-in local coding agent or an offline model
- **+** Egress-scope containment is on by default and refuses off-target public hosts
- **+** Status table separates stable, experimental and planned components
- **−** Multi-operator swarm exploitation is unbenchmarked and described as unreliable
- **−** Cloud, mobile, AD and binary domains are scaffolding only
- **−** Raw benchmark transcripts are stripped, so only graded verdicts can be re-checked
- **−** AGPL-3.0 license limits use in closed network services

<sub>GPU optional · Docker + Compose · Needs Node.js/npm, git, Docker (optional), Ollama or OpenAI-compatible server (optional) · Models: Claude Code, Codex, Hermes, OpenCode, Oh My Pi · port 3333 · [Repo](https://github.com/elder-plinius/t3mp3st) · [📖 Docs ↗](https://github.com/elder-plinius/T3MP3ST/blob/main/docs/GETTING_STARTED.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/t3mp3st/)</sub>

<a name="pyrit"></a>
### #&#8288;15 [pyrit](https://github.com/microsoft/pyrit) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.8k · MIT · Nov 2026</sub>

**AI red teaming toolkit for scanning generative AI models and applications.**

PyRIT is a Microsoft AI Red Team toolkit for finding security and safety weaknesses in generative AI systems. It offers a command-line scanner for repeatable assessments, a browser GUI called CoPyRIT, and a Python framework for building custom attack workflows, including adaptive multi-turn attacks. Targets include many hosted and local model providers as well as full applications over HTTP, WebSockets or Playwright.

- **+** Three interfaces: CLI scanner, CoPyRIT browser GUI, and extensible Python framework
- **+** Connects to OpenAI, Anthropic, Bedrock, Vertex AI, Ollama, Hugging Face and more
- **+** Can test whole applications via HTTP, WebSocket or Playwright browser targets
- **+** Maintained by the Microsoft AI Red Team; MIT licensed with recent commits
- **−** Extra providers beyond built-in ones need the optional LiteLLM adapter
- **−** Feature availability varies by target and model
- **−** No Docker or compose setup shipped in the repo
- **−** Requires API keys or secrets configured per provider

<sub>Docker + Compose · Needs Model provider API keys, Playwright (optional, browser targets), LiteLLM (optional adapter) · Models: OpenAI, Anthropic, Azure OpenAI, Microsoft Foundry, Azure Machine Learning · [Repo](https://github.com/microsoft/pyrit) · [📖 Docs ↗](https://microsoft.github.io/PyRIT/latest/code/framework/) · [🌐 Site ↗](https://microsoft.github.io/PyRIT/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pyrit/)</sub>

<a name="dsh-infinite-gen-5"></a>
### #&#8288;16 [dsh-infinite-gen-5](https://github.com/minglink/dsh-infinite-gen-5) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (7) · Freshness: active (100) · Maintenance: fair (69) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.2k · custom license · Nov 2026</sub>

**Reverse-engineering plugin for DeepSeek Harness using Ghidra, x64dbg and Unicorn.**

IG5 is a plugin for DeepSeek Harness (DSH) that exposes 43 reverse-engineering tools and 8 workflow skills to an agent. It combines Ghidra static analysis, x64dbg native debugging and Unicorn single-function emulation with HTTP/HTTPS capture, XOR/AES candidate search and protocol framing. Thirteen modify or execute tools require host approval before running. Ships as a self-contained Windows x64 package.

- **+** Bundles Ghidra, JDK, Python and x64dbg in the Windows package; no commercial IDA needed
- **+** 13 mutating or executing tools gated by host approval, with undo and audit log
- **+** Per-function dossier combines pseudocode, CFG, call graph and stack frame from one revision
- **+** Default Core 8 toolset keeps the tool surface small; Full 43 is opt-in
- **−** Requires an existing DeepSeek Harness install, pinned to >=0.2.0-rc.1 <0.3.0-0
- **−** Full support only on Windows x64; macOS is Ghidra static only and experimental
- **−** CC BY-NC-SA 4.0 license forbids commercial use
- **−** README is heavy on self-promotion; star and fork counts there differ from detected 2,745

<sub>Needs DeepSeek Harness (@deepseek-ai/dsh >=0.2.0-rc.1 <0.3.0-0), Ghidra, x64dbg, Unicorn, PowerShell · [Repo](https://github.com/minglink/dsh-infinite-gen-5) · [📖 Docs ↗](https://github.com/Minglink/dsh-infinite-gen-5/blob/master/docs/CAPABILITIES.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dsh-infinite-gen-5/)</sub>

<a name="pentestgpt"></a>
### #&#8288;17 [pentestgpt](https://github.com/greydgl/pentestgpt) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: popular (76) · Freshness: recent (80) · Maintenance: weak (7) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · MIT · Jul 2026</sub>

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
### #&#8288;18 [hexstrike-ai](https://github.com/0x4m4/hexstrike-ai) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: popular (71) · Freshness: active (96) · Maintenance: weak (4) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Aug 2026</sub>

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

<a name="pwnagotchi"></a>
### #&#8288;19 [pwnagotchi](https://github.com/evilsocket/pwnagotchi) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: popular (60) · Freshness: recent (70) · Maintenance: patchy (40) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.3k · custom license · Aug 2026</sub>

**WiFi handshake-capturing agent that tunes its attacks with reinforcement learning.**

Pwnagotchi runs an A2C reinforcement-learning agent (LSTM policy with MLP feature extractor) on top of bettercap to capture WPA key material from nearby WiFi. It saves PMKIDs and full or half handshakes as PCAP files that hashcat can crack. It adjusts its parameters over epochs, and nearby units can split channels between them.

- **+** Captures PMKIDs and full or half WPA handshakes as PCAPs usable by hashcat
- **+** Agent tunes its own parameters per environment over time using A2C with an LSTM policy
- **+** Multiple units detect each other and divide channels between them
- **+** Docs, forum and community channels are listed on the project site
- **−** Last tagged release is 2021-04-18, though commits continue
- **−** License detected as NOASSERTION, while the README states GPL3
- **−** Performs poorly at first and needs time in varied WiFi environments to learn
- **−** README gives no hardware requirements, RAM figures or supported boards

<sub>Needs bettercap, hashcat · Models: A2C (stable-baselines, MlpLstmPolicy) · [Repo](https://github.com/evilsocket/pwnagotchi) · [📖 Docs ↗](https://www.pwnagotchi.ai) · [🌐 Site ↗](https://pwnagotchi.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pwnagotchi/)</sub>

<a name="adversarial-robustness-toolbox"></a>
### #&#8288;20 [adversarial-robustness-toolbox](https://github.com/trusted-ai/adversarial-robustness-toolbox) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: known (31) · Freshness: recent (74) · Maintenance: patchy (38) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · MIT · Nov 2026</sub>

**Python library for attacking and defending ML models against adversarial threats.**

ART is a Python library for evaluating and hardening machine learning models against evasion, poisoning, extraction and inference attacks. It wraps models from TensorFlow, Keras, PyTorch, scikit-learn, XGBoost, LightGBM, CatBoost and GPy behind common estimator interfaces. It covers images, tables, audio and video, and is hosted by LF AI & Data.

- **+** Covers four threat classes: evasion, poisoning, extraction and inference
- **+** Works across TensorFlow, PyTorch, scikit-learn, XGBoost, LightGBM, CatBoost and GPy
- **+** Supports images, tables, audio and video, plus detection and speech tasks
- **+** MIT license, LF AI & Data project, with examples and notebooks
- **−** README does not mention LLM-specific red-teaming; focus is classic model robustness
- **−** Last release (2025-07-07) is older than recent commits
- **−** Library only, no UI or hosted service; you write Python to use it
- **−** Main docs sit on a GitHub wiki, with API reference on Read the Docs

<sub>GPU optional · Docker · Models: TensorFlow, Keras, PyTorch, scikit-learn, XGBoost · [Repo](https://github.com/trusted-ai/adversarial-robustness-toolbox) · [📖 Docs ↗](https://adversarial-robustness-toolbox.readthedocs.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/adversarial-robustness-toolbox/)</sub>

<a name="purplellama"></a>
### #&#8288;21 [purplellama](https://github.com/meta-llama/purplellama) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: weak (25) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.5k · custom license · Nov 2026</sub>

**Meta's safety classifiers and cybersecurity benchmarks for LLM inputs, outputs and code.**

Purple Llama is an umbrella repo from Meta with input/output safeguards and security evals for generative AI. It includes Llama Guard 3 moderation models, Prompt Guard for prompt injection and jailbreak detection, and Code Shield for filtering insecure LLM-generated code. The CyberSec Eval benchmarks (v1 to v3) measure insecure code suggestions, code interpreter abuse, prompt injection, spear phishing and autonomous offensive operations.

- **+** Covers both defence (Llama Guard, Prompt Guard, Code Shield) and attack-side evals in one repo
- **+** CyberSec Eval maps to CWE and MITRE ATT&CK; public leaderboard on Hugging Face
- **+** Llama Guard 3 supports MLCommons hazard taxonomy, 128k context, and 1B, 8B and 11B-vision sizes
- **+** Code Shield example notebook provided; evals and Code Shield are MIT licensed
- **−** Mixed licensing: MIT for evals and Code Shield, Llama Community licenses for models
- **−** README has no install, hardware or usage instructions; points to llama-recipes instead
- **−** Llama Guard weights are hosted on Hugging Face, not in this repo
- **−** Safeguard models are tied to the Llama family and its license terms

<sub>Models: Llama Guard 3-8B, Llama Guard 3-1B, Llama Guard 3-11B-vision, Llama Guard 2, Llama Guard · [Repo](https://github.com/meta-llama/purplellama) · [📖 Docs ↗](https://github.com/meta-llama/llama-recipes) · [🌐 Site ↗](https://ai.meta.com/llama/purple-llama) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/purplellama/)</sub>

<a name="superagent"></a>
### #&#8288;22 [superagent](https://github.com/superagent-ai/superagent) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: known (38) · Freshness: recent (80) · Maintenance: weak (16) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.9k · MIT · Aug 2026</sub>

**SDK that blocks prompt injections and redacts PII in AI agent apps.**

Superagent is a TypeScript and Python SDK (package `safety-agent`) with a guard call for detecting prompt injections and unsafe tool calls, a redact call for removing PII, PHI and secrets, and a scan call for finding repo poisoning aimed at agents. A red-team `test` call is listed as coming soon. It needs an API key from superagent.sh, and also ships a CLI and an MCP server.

- **+** Guard, redact and scan exposed as simple calls in both TypeScript and Python
- **+** Works with several providers: OpenAI, Anthropic, Google, Groq, Bedrock
- **+** Open-weight Guard models on HuggingFace, quoted at 50-100ms latency when self-hosted
- **+** Also ships a CLI and an MCP server for Claude Code and Claude Desktop
- **−** Setup requires an API key from the hosted superagent.sh service
- **−** Red-team `test` feature is marked coming soon, not available yet
- **−** No self-hosting instructions or Docker setup in the README
- **−** Latest release is 2025-09-14, older than recent commits

<sub>Needs Superagent API key (superagent.sh) · Models: OpenAI, Anthropic, Google, Groq, Bedrock · [Repo](https://github.com/superagent-ai/superagent) · [📖 Docs ↗](https://docs.superagent.sh) · [🌐 Site ↗](https://superagent.sh) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/superagent/)</sub>

<a name="cairn"></a>
### #&#8288;23 [cairn](https://github.com/oritera/cairn) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: niche (19) · Freshness: active (99) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.1k · AGPL-3.0 · Sep 2026</sub>

**Blackboard-based multi-agent engine for AI penetration testing and CTF solving.**

Cairn searches for a path from an origin to a goal by having agent workers read and write a shared graph of Facts, Intents and human Hints. A server keeps the graph consistent, and a dispatcher schedules Bootstrap, Reason and Explore tasks to workers running Claude Code, Codex or Pi. Penetration testing is the validated use case; the README reports 54 of 54 problems solved at a Tencent Cloud hackathon.

- **+** No fixed agent roles; tasks are generated at runtime from the shared graph
- **+** Hackathon result reported: 54/54 problems solved, 3rd place overall
- **+** Workers run in per-project containers or locally via existing claude/codex/pi CLIs
- **+** Humans can inject Hints that agents pick up on their next read
- **−** Local mode runs agents with your user's permissions and no sandbox
- **−** AGPL-3.0; commercial or proprietary use needs a separate paid license
- **−** Depends on external coding-agent backends (Claude Code, Codex, Pi) and LLM API access
- **−** Benchmark results come from one competition; no independent evaluation is cited

<sub>no GPU · Docker + Compose · Needs Docker (not needed in local mode), Python >= 3.12, uv, Claude Code, Codex or Pi CLI/LLM endpoints · Models: Claude Code, Codex, Pi · port 8000 · [Repo](https://github.com/oritera/cairn) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cairn/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
