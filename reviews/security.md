# 🔐 Security reviews · Best of Open-Source AI

AI agents and tools for penetration testing, red-teaming and finding vulnerabilities in your own apps and models. Back to the [leaderboard](../README.md#-security).

<sub>🌐 Also on the web: [Security on archestack.com](https://archestack.com/best-of-ai/security/), each project on its own page.</sub>

<a name="shannon"></a>
### 🥇 [keygraphhq/shannon](https://github.com/keygraphhq/shannon) <sub>score [93](../README.md#-how-we-rank "Score 93/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 52k · AGPL-3.0 · Nov 2026</sub>

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
### 🥈 [ifixai](https://github.com/ifixai-ai/ifixai) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 47k · Apache-2.0 · Nov 2026</sub>

**Audits AI agents for policy violations in a simulated business environment.**

iFixAi runs an agent against a simulated version of your business, sends it requests that include ones pushing past its role, and has an LLM judge from a different provider grade each reply. A default run covers 10 inspections (access control, prompt injection, data leakage, destructive actions); `--full-run` covers 61. Output is an A to F grade plus JSON and Markdown reports, usable as a CI gate with `--min-score`.

- **+** Every finding shows the request and what the agent did, so results are checkable
- **+** Judge is chosen from a different provider than the agent under test
- **+** Mock provider lets you try the full flow without any API key
- **+** Reports in JSON and Markdown; `--min-score` gates CI; `--dry-run` shows cost before billing
- **−** Probes are real requests, so it must be pointed at a staging copy of the agent
- **−** Grading depends on an external LLM judge, which adds API cost and judge variance
- **−** Non-OpenAI-compatible agents need a few lines of custom Python
- **−** Default run covers only 10 of 61 inspections

<sub>no GPU · Needs Python 3.10+, LLM judge API key (OpenAI, Anthropic, Gemini, Azure, Bedrock, OpenRouter) · Models: OpenAI-compatible agent endpoints, OpenAI, Anthropic, Gemini, Azure · [Repo](https://github.com/ifixai-ai/ifixai) · [📖 Docs ↗](https://github.com/ifixai-ai/iFixAi/tree/main/docs) · [🌐 Site ↗](https://www.ifixai.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ifixai/)</sub>

<a name="ai-infra-guard"></a>
### 🥉 [ai-infra-guard](https://github.com/tencent/ai-infra-guard) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · Apache-2.0 · Nov 2026</sub>

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

<a name="decepticon"></a>
### #&#8288;4 [decepticon](https://github.com/bittersecurity/decepticon) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.7k · Apache-2.0 · Nov 2026</sub>

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

<a name="strix"></a>
### #&#8288;5 [Strix](https://github.com/usestrix/strix) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 77k · Apache-2.0 · Nov 2026</sub>

**Autonomous multi-agent pentesting CLI that validates vulnerabilities with working PoCs.**

Strix runs LLM-driven pentest agents against a local codebase, repository URL, live web app or API spec (OpenAPI, Postman). Agents use a Caido HTTP proxy, a browser, a shell and a Python exploit sandbox, and report findings with proof-of-concept exploits, CVSS scoring and remediation guidance. It runs from a CLI with a local results viewer, headless mode for CI, and optional MCP server connections.

- **+** Findings come with working PoCs, which cuts false positives versus static scanners
- **+** Accepts source dirs, GitHub URLs, live apps, OpenAPI and Postman targets
- **+** Headless mode exits non-zero on findings; GitHub Actions example scopes PR scans to changed files
- **+** Works with many LLM providers via LiteLLM, including local models through LLM_API_BASE
- **−** Needs a running Docker daemon; sandbox image is pulled on first run
- **−** Needs an LLM; recommended models are hosted, and some require provider access programs
- **−** SSO, compliance reports and VPC deployment are in the paid Enterprise tier
- **−** Active testing can cause damage; only usable against systems you are authorized to test

<sub>no GPU · Docker · Needs Docker, LLM API key or local LLM endpoint, Caido, Nuclei, Playwright · Models: OpenAI, Anthropic, Google Vertex AI, AWS Bedrock, Azure · [Repo](https://github.com/usestrix/strix) · [📖 Docs ↗](https://docs.strix.ai) · [🌐 Site ↗](https://strix.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/strix/)</sub>

<a name="failproofai"></a>
### #&#8288;6 [failproofai](https://github.com/failproofai/failproofai) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · custom license · Nov 2026</sub>

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

<a name="aisoc"></a>
### #&#8288;7 [aisoc](https://github.com/beenuar/aisoc) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: healthy (99) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.2k · MIT · Nov 2026</sub>

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

<a name="nvidia-nemo-guardrails"></a>
### #&#8288;8 [nvidia-nemo/guardrails](https://github.com/nvidia-nemo/guardrails) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · custom license · Nov 2026</sub>

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

<a name="bla"></a>
### #&#8288;9 [bla](https://github.com/qybaihe/bla) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · MIT · Nov 2026</sub>

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

<a name="pentagi"></a>
### #&#8288;10 [pentagi](https://github.com/vxcontrol/pentagi) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: fair (60) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · MIT · Oct 2026</sub>

**Multi-agent system that runs autonomous pentests with nmap, Metasploit and sqlmap.**

PentAGI takes a target and goal in plain language. A team of specialized agents (researcher, developer, executor) then plans the work and runs 20+ security tools in an isolated Docker sandbox. Findings are stored in PostgreSQL with pgvector, with an optional Neo4j/Graphiti knowledge graph, and it produces a vulnerability report. It works with 10+ LLM providers, any OpenAI-compatible endpoint, or local models via Ollama or vLLM.

- **+** Runs 20+ tools such as nmap, Metasploit and sqlmap in an isolated Docker sandbox
- **+** Supports 10+ LLM providers, custom OpenAI-compatible endpoints, and local Ollama or vLLM
- **+** Persistent memory in PostgreSQL with pgvector, plus optional Neo4j knowledge graph
- **+** REST and GraphQL APIs with Bearer tokens; Langfuse and Grafana integrations
- **−** Full stack spans many containers (Postgres, Neo4j, Langfuse, ClickHouse, Grafana), a heavy footprint
- **−** Not a breach-and-attack-simulation tool; no predefined campaigns or attack plans
- **−** Report export is Markdown and PDF only; JSON export is not documented
- **−** Agent profiles, plugins, MCP servers and attack-chain view are Enterprise-only

<sub>GPU optional · Docker + Compose · Needs Docker, Docker Compose, PostgreSQL with pgvector, Neo4j and Graphiti (optional), Langfuse (optional) · Models: OpenAI, Anthropic, Google Gemini, AWS Bedrock, Ollama · [Repo](https://github.com/vxcontrol/pentagi) · [🌐 Site ↗](https://vxcontrol.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pentagi/)</sub>

<a name="garak"></a>
### #&#8288;11 [garak](https://github.com/nvidia/garak) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 10k · Apache-2.0 · Nov 2026</sub>

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
### #&#8288;12 [cyberstrikeai](https://github.com/aipentest/cyberstrikeai) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.9k · Apache-2.0 · Nov 2026</sub>

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

<a name="redamon"></a>
### #&#8288;13 [redamon](https://github.com/samugit83/redamon) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: known (39) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.5k · MIT · Nov 2026</sub>

**Self-hosted AI pentest agent with Neo4j attack-surface graph and auto-fix PRs.**

RedAmon runs a parallel recon pipeline, stores the attack surface in a Neo4j graph, and hands it to an LLM agent that attempts exploitation behind human approval gates. A triage agent and a CodeFix agent then rank findings and open GitHub pull requests with fixes. It has multi-user RBAC and audit trails, and supports OpenAI, Anthropic, Bedrock, OpenRouter and OpenAI-compatible endpoints such as Ollama.

- **+** Claims 101/104 on the XBOW web benchmark black-box, with raw agent sessions published
- **+** Recon results merge into a Neo4j graph the agent can query in natural language
- **+** Closes the loop: triage agent plus CodeFix agent that opens GitHub PRs
- **+** Multi-user RBAC, Rules of Engagement enforcement, approval gates and audit trails
- **−** Heavy footprint: 9 containers, 7 GB RAM and 80 GB disk minimum without OpenVAS
- **−** OpenVAS option needs about 10 GB RAM and a ~30 minute first feed sync
- **−** Benchmark and coverage figures are self-reported; the audit lists 210 classes still in backlog
- **−** Autonomous exploitation tooling carries legal risk if pointed at targets you lack permission to test

<sub>RAM ≥ 7 GB · no GPU · Compose · Needs Docker Engine 28+, Docker Compose v2, Neo4j, PostgreSQL, Kali sandbox, Metasploit, OpenVAS (optional) · Models: OpenAI, Anthropic, OpenRouter, AWS Bedrock, OpenAI-compatible (Ollama, vLLM, Groq) · port 3000 · [Repo](https://github.com/samugit83/redamon) · [📖 Docs ↗](https://github.com/samugit83/redamon/wiki) · [🌐 Site ↗](https://www.redamon.org/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/redamon/)</sub>

<a name="cyberstrike"></a>
### #&#8288;14 [cyberstrike](https://github.com/cyberstrikeus/cyberstrike) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: known (42) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · AGPL-3.0 · Nov 2026</sub>

**Terminal agent that runs LLM-driven web penetration tests and writes reports.**

CyberStrike is a TypeScript CLI that drives an LLM through reconnaissance, vulnerability testing and reporting against a target. It loads OWASP methodology documents as skills, uses a built-in intercepting browser (HackBrowser) and HTTP engine (Vortex), and confirms findings with a baseline, attack and response-diff check. Tools can run on remote hosts through Bolt, and MCP servers add more security tooling.

- **+** Works with Anthropic, OpenAI, Gemini, Bedrock, or local Ollama/LM Studio models
- **+** Findings confirmed by a 3-gate baseline/attack/response-diff check; speculative results discarded
- **+** Built-in intercepting browser and traffic engine feed requests straight to testing agents
- **+** Bolt runs tools on remote servers, paired with Ed25519 keys
- **−** Cloud, internal network and mobile agents are in the paid Pro edition
- **−** AGPL-3.0 license; commercial use needs a separate license
- **−** Open-source agents focus on web testing (OWASP WSTG)
- **−** No Docker image or compose file; installs through npm, Homebrew, Scoop or curl

<sub>no GPU · Needs Node.js/npm, LLM provider account or local model server · Models: Anthropic Claude, OpenAI GPT, Google Gemini, Amazon Bedrock, Azure OpenAI · [Repo](https://github.com/cyberstrikeus/cyberstrike) · [▶️ Demo ↗](https://app.cyberstrike.io) · [📖 Docs ↗](https://docs.cyberstrike.io) · [🌐 Site ↗](https://cyberstrike.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cyberstrike/)</sub>

<a name="pyrit"></a>
### #&#8288;15 [pyrit](https://github.com/microsoft/pyrit) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.0k · MIT · Nov 2026</sub>

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

<a name="t3mp3st"></a>
### #&#8288;16 [t3mp3st](https://github.com/elder-plinius/t3mp3st) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · AGPL-3.0 · Sep 2026</sub>

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

<a name="artex-global"></a>
### #&#8288;17 [artex-global](https://github.com/jiwoochris/artex-global) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (48) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.4k · AGPL-3.0 · Nov 2026</sub>

**Autonomous penetration-testing system using LLM planner and worker agents.**

ARTEX runs a planner and several worker agents that break a pentest goal into tasks, execute real tools such as nmap and curl, and record discovered assets and findings in PostgreSQL. It ships as a Go binary with an embedded Next.js UI, a traffic-recording proxy, a tool-approval gate and human-in-the-loop chat. This is a localized fork of the Chinese upstream project, with output selectable in five languages.

- **+** Single Go binary with embedded Next.js UI; PostgreSQL is the only datastore
- **+** Supports Anthropic, OpenAI and any OpenAI-compatible endpoint via ARTEX_LLM_BASE_URL
- **+** Tool-approval gate, traffic-recording proxy and human chat let you steer and audit runs
- **+** Binds to 127.0.0.1 and requires a setup token on first run
- **−** Offensive tool that can carry out intrusion; only legal against authorized targets
- **−** Output language relies on a prompt directive; smaller models drift back to Chinese
- **−** Internal reasoning prompts remain in Chinese; the upstream repository is unreachable
- **−** OpenAI-compatible path needs max_tokens lowered to 16,384 for gpt-4o or calls fail

<sub>no GPU · Docker + Compose · Needs PostgreSQL, Anthropic or OpenAI-compatible LLM API, Docker Compose (optional) · Models: Anthropic Claude (default claude-opus-4-8), OpenAI gpt-4o, OpenAI-compatible endpoints · port 8787 · [Repo](https://github.com/jiwoochris/artex-global) · [📖 Docs ↗](https://github.com/jiwoochris/artex-global/blob/main/docs/defense-en.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/artex-global/)</sub>

<a name="vulnclaw"></a>
### #&#8288;18 [vulnclaw](https://github.com/netw0rknoob/vulnclaw) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.0k · MIT · Oct 2026</sub>

**LLM agent CLI that runs penetration tests from natural-language prompts.**

VulnClaw is a Python CLI and agent that takes a target and a plain-language goal, then lets the model drive recon, vulnerability discovery, exploitation and report generation. It uses built-in fetch, shell, Python and nmap tools plus MCP servers (Burp, Chrome DevTools). Tool output is stored as raw evidence, and claimed flags must match it. It also ships a REPL, a TUI, a local Web UI and a source-code scanner.

- **+** Evidence gate rejects flags or conclusions that do not appear verbatim in tool output
- **+** 13 LLM provider presets including local Ollama, plus any OpenAI-compatible base URL
- **+** Generates Markdown reports and runnable Python PoC scripts after a run
- **+** Ships 50 skill reference packs the model loads on demand, plus a local code scanner
- **−** Full Web UI requires building the React frontend from source; the PyPI wheel lacks it
- **−** python_execute is described as high-risk and not a strong sandbox
- **−** Burp and Chrome DevTools MCP integrations need separate manual deployment
- **−** README is mainly Chinese; the English version is in a separate file

<sub>no GPU · Docker + Compose · Needs Python 3.10+, LLM API key or Ollama, Node.js 18+ (Web UI build, npx MCP servers), nmap (optional), Burp Suite Professional (optional), Chrome (optional) · Models: OpenAI, Anthropic, MiniMax, DeepSeek, Zhipu · port 7788 · [Repo](https://github.com/netw0rknoob/vulnclaw) · [🌐 Site ↗](https://unclecheng-li.github.io/vulnclaw.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vulnclaw/)</sub>

<a name="agentic-bug-hunter"></a>
### #&#8288;19 [agentic-bug-hunter](https://github.com/awarexone/agentic-bug-hunter) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: fair (55) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.0k · MIT · Nov 2026</sub>

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

<a name="dsh-infinite-gen-5"></a>
### #&#8288;20 [dsh-infinite-gen-5](https://github.com/minglink/dsh-infinite-gen-5) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: fair (69) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.6k · custom license · Nov 2026</sub>

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

<a name="raptor"></a>
### #&#8288;21 [raptor](https://github.com/gadievron/raptor) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: known (46) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.0k · custom license · Nov 2026</sub>

**Security research framework chaining scanners, LLM triage, PoC and patch generation.**

RAPTOR is a Python framework built on Claude Code that runs Semgrep and CodeQL scans, uses an LLM to filter false positives, checks exploitability, and generates PoCs and patches for review. It also covers software composition analysis with SBOMs, binary analysis, fuzzing, crash analysis, Frida instrumentation and open-source project forensics, driven by slash commands. Untrusted execution is isolated with namespaces, Landlock and seccomp on Linux, or Seatbelt on macOS.

- **+** Covers source, dependencies, binaries, fuzzing and crashes in one workflow
- **+** Custom sandbox: Linux namespaces, Landlock, seccomp, or Seatbelt on macOS
- **+** Mechanical scans and SCA run without an LLM (/scan, --no-llm)
- **+** Per-run cost ceilings, e.g. --max-cost-usd 5; /agentic defaults to $10
- **−** Authors call it not polished software; most of the code is AI-generated
- **−** Interactive shell needs Claude Code with a subscription or Anthropic API key
- **−** Prompt injection remains possible; sandbox guarantees differ by platform and profile
- **−** Maturity varies by workflow; some commands are less complete than others

<sub>Needs Claude Code, Semgrep, CodeQL, uv, Python 3.13+, Node.js 18+, Docker (optional) · Models: Claude (Claude Code or Anthropic API), other providers, local models · [Repo](https://github.com/gadievron/raptor) · [📖 Docs ↗](https://github.com/gadievron/raptor/blob/main/docs/README.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/raptor/)</sub>

<a name="pentest-swarm-ai"></a>
### #&#8288;22 [pentest-swarm-ai](https://github.com/armur-ai/pentest-swarm-ai) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (35) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · AGPL-3.0 · Nov 2026</sub>

**Autonomous API and web-app pentester using concurrent agents on a shared blackboard.**

Pentest Swarm AI is a Go CLI that runs many LLM agents against a target. They coordinate through a pgvector-backed blackboard with decaying pheromone weights, and attempt exploits such as BOLA/IDOR, JWT forgery, SSRF and SQL injection. Non-LLM oracles (out-of-band, differential, timing) confirm findings. It works with Claude, OpenAI-compatible APIs, Gemini, Ollama or LM Studio, and the README marks it alpha.

- **+** Non-LLM verification oracles (OOB, differential, timing) mark confirmed findings as VERIFIED
- **+** Runs on Claude, Gemini, OpenAI-compatible APIs or fully local Ollama and LM Studio
- **+** Scope enforced fail-closed at tool layer and executor, with an audit trail
- **+** Bundled vulnerable labs (crAPI, Juice Shop, VAmPI, DVGA) and eight playbooks
- **−** Marked alpha in the README badges
- **−** AGPL-3.0 license may restrict use inside proprietary services
- **−** Sends real attack traffic to live targets; requires written authorization
- **−** Blackboard relies on pgvector, so a Postgres dependency is implied

<sub>GPU optional · Docker + Compose · Needs Docker (for bundled labs), Postgres with pgvector (blackboard), LLM provider or Ollama/LM Studio · Models: Claude, OpenAI-compatible, Together AI, Gemini, Ollama · port 7777 · [Repo](https://github.com/armur-ai/pentest-swarm-ai) · [📖 Docs ↗](https://armur-ai.github.io/Pentest-Swarm-AI/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pentest-swarm-ai/)</sub>

<a name="scopeweaver"></a>
### #&#8288;23 [scopeweaver](https://github.com/cskwork/scopeweaver) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (7) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · AGPL-3.0 · Nov 2026</sub>

**Multi-agent LLM penetration-testing system with Go backend and Next.js UI.**

ScopeWeaver runs LLM agents that explore targets, record assets and save confirmed findings, with task queues, report export and interception rules for tool calls. It is a rebranded, English/Korean-translated derivative of Autumn-27/ARTEX, stores data in PostgreSQL, and can import assets from ScopeSentry. Models come from Anthropic, OpenAI, GLM templates, an OpenCode SDK bridge or native Ollama.

- **+** Supports keyless native Ollama, with an optional local-only network mode
- **+** Interception rules and approval records gate agent tool calls, with built-in destructive-command rules
- **+** Single Go binary with embedded frontend, plus Docker Compose and in-app updates
- **+** Imports assets from ScopeSentry by project or task
- **−** Scope is prompt-level guidance, not a network boundary; egress control must be external
- **−** Requires PostgreSQL, and only one server per database is supported
- **−** Derivative of ARTEX; README says the modification date is not a release tag
- **−** OpenCode SDK bridge unsupported on Windows; Linux CI results pending

<sub>no GPU · Docker + Compose · Needs PostgreSQL, LLM provider (Anthropic, OpenAI, Ollama or other) · Models: Anthropic, OpenAI, GLM (Z.ai), Ollama (native), OpenCode SDK bridge · port 8787 · [Repo](https://github.com/cskwork/scopeweaver) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/scopeweaver/)</sub>

<a name="cybermes"></a>
### #&#8288;24 [cybermes](https://github.com/zyrexnn/cybermes) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: niche (3) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.1k · Apache-2.0 · Nov 2026</sub>

**Bug bounty automation with a Go MCP server and 200+ security playbooks.**

Cybermes runs authorized recon and vulnerability research either as a standalone CLI agent (Hermes) or as a Go MCP server (cybermes-mcp) for AI editors such as Cursor, Claude Desktop and Cline. It orchestrates subfinder, httpx, katana, ffuf, nuclei and sqlmap, filters their output with a Go stream filter, and requires a Python PoC script before a finding is logged. Results are compiled into SUMMARY.md, metadata.json, HTML and PDF reports.

- **+** Two modes: autonomous CLI agent, or MCP server for existing AI editors
- **+** Offline knowledge base of 200+ playbooks plus PayloadsAllTheThings and HackTricks data
- **+** smart_pipe filter archives raw tool output and passes only high-signal lines to the model
- **+** Per-target workspaces with PoC scripts, evidence and PDF/HTML/Markdown reports
- **−** Depends on external tools (subfinder, httpx, katana, ffuf, nuclei, sqlmap) installed separately
- **−** 'Zero-false-positive' claim rests on a PoC gate; no benchmark is given
- **−** README is heavy on sponsor and donation promotion, including an affiliate API link

<sub>Docker + Compose · Needs Go 1.22+, Python 3.11+, subfinder, httpx, katana, ffuf, nuclei, sqlmap, Node.js (npx) for cybermes-mcp · [Repo](https://github.com/zyrexnn/cybermes) · [📖 Docs ↗](https://github.com/Zyrexnn/Cybermes/tree/main/docs) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cybermes/)</sub>

<a name="nebula"></a>
### #&#8288;25 [berylliumsec/nebula](https://github.com/berylliumsec/nebula) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · BSD-2-Clause · Nov 2026</sub>

**Pentest workbench with AI agents, Kali containers and an intercepting browser.**

Nebula groups a penetration-testing engagement into one Project: assets, Kali terminals, an intercepting security browser with Repeater, notes, findings and reports. AI assistants and missions run within operator-set scope, approvals and budgets, using Codex, Grok or Claude harnesses, or Claude, OpenRouter, Ollama and vLLM providers. Evidence is kept as hashed artifacts with execution provenance.

- **+** Scope, approvals and budgets constrain what assistants and missions can do
- **+** Hashed artifacts and execution provenance link evidence to findings and reports
- **+** Works with local providers (Ollama, vLLM) as well as Claude, OpenRouter and harnesses
- **+** Custom SKILL.md skills can be added per Project and selected in chat
- **−** Prebuilt packages are a Linux x86_64 preview only; other platforms build from source
- **−** Source build needs Python, Poetry, Node.js, Rust and Tauri prerequisites
- **−** Butler Voice requires a direct OpenAI API key and incurs API charges
- **−** Host mode uses the host filesystem and network, widening the blast radius

<sub>GPU optional · Docker + Compose · Needs Docker or Podman, Kali container, OpenVPN (optional), Chromium via Playwright, OpenAI API key (optional, for Voice) · Models: Claude, OpenRouter, Ollama, vLLM, Codex harness · [Repo](https://github.com/berylliumsec/nebula) · [📖 Docs ↗](https://github.com/BerylliumSec/nebula/blob/main/docs/README.md) · [🌐 Site ↗](https://berylliumsec.github.io/nebula-apt/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nebula/)</sub>

<a name="seep-reverse-lab"></a>
### #&#8288;26 [seep-reverse-lab](https://github.com/angusdevgo/seep-reverse-lab) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (23) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · GPL-3.0 · Nov 2026</sub>

**Agent-driven reverse engineering workbench with 38 MCP tools.**

Wraps Radare2, JADX, Apktool, Frida and a custom Windows PE engine behind 38 MCP tools, with an orchestrator that classifies platform and task type to drive autonomous APK/PE/web analysis, patching and Frida hook generation. It ships a 294-entry field-journal knowledge base and 14 desensitized case studies, plus prompt layers meant to stop the underlying LLM refusing security-audit tasks. Install paths exist for a 'Pi Agent' and DeepSeek Harness via an npm plugin, with ~657MB of toolchains bundled for offline use.

- **+** 38 MCP tools unify Radare2, JADX, Apktool, Frida and a PE engine behind one API
- **+** Fully offline after setup: toolchains pre-bundled, no network dependency
- **+** Token-budget modes (fold/summary) cut decompile output by up to 90%
- **+** 294 field journals plus 14 desensitized industrial cases as a searchable KB
- **−** No Docker or Compose support; install is via PowerShell/npm scripts only
- **−** Heavily Windows-oriented (PE engine, install.ps1) with less parity on Linux/macOS
- **−** Includes explicit prompt-engineering layers built to bypass model safety refusals
- **−** 881MB footprint with hardcoded relative paths noted in the repo layout

<sub>no GPU · Needs Radare2, JADX, Apktool, Frida, IDA Pro (optional) · [Repo](https://github.com/angusdevgo/seep-reverse-lab) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/seep-reverse-lab/)</sub>

<a name="pentest-ai"></a>
### #&#8288;27 [pentest-ai](https://github.com/0xsteph/pentest-ai) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · MIT · Nov 2026</sub>

**AI-driven pentest and bug-bounty tool that verifies findings with exploit oracles.**

Pentest-AI connects an AI client or local model to a web-application pentest workflow through MCP, a CLI (ptai) or CI. Findings stay candidates until a named oracle replays the exploit and checks a control, and verified ones keep the requests and responses as evidence. A bug-bounty mode enforces per-program scope, rate and a researcher header, and drafts reports from verified findings only.

- **+** Oracle verification: the model cannot award a verified verdict, and evidence is stored per finding
- **+** Bug-bounty profiles enforce scope, request rate and an X-Bug-Bounty header, with a --dry-run plan
- **+** Works via MCP clients (Claude Code, Codex, Cursor, VS Code), CLI, or CI with SARIF export
- **+** Bundled demo runs against a vulnerable app with no API key or external target
- **−** Findings without a supported verification recipe stay candidates; README expects incomplete coverage
- **−** Optional scanners need separate binaries, and some integrations return only raw output
- **−** Blind-vulnerability checks may use an external out-of-band collaborator unless --no-oast is set
- **−** Ollama route needs a tool-calling model; result quality depends on model and memory

<sub>GPU optional · Docker + Compose · Needs Python 3.10-3.14, pipx, MCP-capable AI client or Ollama, optional scanner binaries · Models: Claude Code, Codex, Ollama (tool-calling models), cloud model providers · [Repo](https://github.com/0xsteph/pentest-ai) · [📖 Docs ↗](https://github.com/0xSteph/pentest-ai/tree/main/docs) · [🌐 Site ↗](https://pentestai.xyz/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pentest-ai/)</sub>

<a name="clawsec"></a>
### #&#8288;28 [clawsec](https://github.com/prompt-security/clawsec) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: fair (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.1k · AGPL-3.0 · Nov 2026</sub>

**Security skills and signed advisory feed for OpenClaw-family agent runtimes.**

ClawSec is a set of security skills for agent runtimes (OpenClaw, NanoClaw, Hermes, Picoclaw). It verifies a signed advisory feed against installed skills, gates risky installs behind a second confirmation, and detects drift in protected agent files and config. The feed combines NVD CVEs, GitHub advisories and community reports, polled daily.

- **+** Advisory feed is signed with a pinned Ed25519 key and has a documented verification runbook
- **+** Guarded installer stops on advisory matches and needs explicit second confirmation
- **+** Separate skill packages for OpenClaw, NanoClaw, Hermes and Picoclaw
- **+** Hook setup prints a preflight before changing persistent OpenClaw configuration
- **−** Only useful alongside the Claw-family agent runtimes it targets
- **−** The *-traffic-guardian directories are specs only, not shipped runtime proxies
- **−** Recommends and gates actions; does not sandbox agent behavior itself
- **−** AGPL-3.0 license may constrain embedding in proprietary products

<sub>no GPU · Needs Node.js, npx skills, OpenClaw, NanoClaw, Hermes or Picoclaw · [Repo](https://github.com/prompt-security/clawsec) · [📖 Docs ↗](https://github.com/prompt-security/clawsec/blob/main/wiki/INDEX.md) · [🌐 Site ↗](https://clawsec.prompt.security) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/clawsec/)</sub>

<a name="open-kritt"></a>
### #&#8288;29 [open-kritt](https://github.com/kritt-ai/open-kritt) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: fair (59) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · AGPL-3.0 · Oct 2026</sub>

**Workflow builder that runs AI agents in parallel to find code vulnerabilities.**

open·kritt splits vulnerability research into small prompt steps, runs them across Codex, Claude Code or Grok Build agents in disposable job containers, and merges the output into de-duplicated, ranked findings. Post-scripts can validate issues, build proofs of concept and write reports, and results export as a ZIP. It has a web UI on port 5173 and a headless CLI.

- **+** Reusable prompt workflows with custom severity rankers and a consistent finding schema
- **+** Automatic de-duplication of findings; post-scripts build PoCs and reports
- **+** Model access via Codex login, OpenAI, Anthropic, DeepSeek, OpenRouter or xAI
- **+** Headless CLI imports workflows, creates scans and exports finding bundles
- **−** Backend has no application authentication; the stack must be kept private
- **−** Agents run as root with direct internet access; needs a dedicated Docker host or VM
- **−** AGPL-3.0 license may restrict use in closed or hosted products
- **−** Depends on external agent CLIs or provider APIs; no local model support stated

<sub>no GPU · Compose · Needs Docker with Docker Compose, Node.js 20+, Git, Model provider login or API key, GitHub token (optional, private repos) · Models: Codex, Claude Code, Grok Build, OpenAI, Anthropic · port 5173 · [Repo](https://github.com/kritt-ai/open-kritt) · [📖 Docs ↗](https://docs.kritt.ai) · [🌐 Site ↗](https://kritt.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-kritt/)</sub>

<a name="reconmap"></a>
### #&#8288;30 [reconmap](https://github.com/reconmap/reconmap) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.0k · MIT · Nov 2026</sub>

**AI-assisted pentest scanning, triage and reporting across many engagements.**

Reconmap takes a target (URL, domain, IP or repo), has an LLM pick and order tools from a command catalog, and runs them through Go runners on your own machines. Output is parsed (SARIF, CycloneDX, Nmap, Testssl, Subfinder, others via an LLM parser), triaged for severity and false positives, and exported to Word, Markdown or HTML. It also has an MCP server.

- **+** Runners execute commands on your own machines and return output to the server
- **+** Built-in parsers for SARIF, CycloneDX, Nmap, Testssl and Subfinder, plus LLM fallback
- **+** Works with Ollama for local inference or OpenAI-compatible endpoints
- **+** Multi-project, multi-user with Keycloak SSO; includes MCP server and rmap CLI
- **−** Needs PostgreSQL, Redis and Keycloak alongside the API and dashboard
- **−** Multi-component stack (.NET API, React, Go runner and CLI) is heavier to operate
- **−** Triage and planning quality depends on the chosen LLM
- **−** Report export lists only Word, Markdown and HTML

<sub>GPU optional · Compose · Needs PostgreSQL, Redis, Keycloak, Docker Compose · Models: Ollama, Azure OpenAI, OpenRouter, OpenAI-compatible endpoints · port 5500 · [Repo](https://github.com/reconmap/reconmap) · [▶️ Demo ↗](https://reconmap.com/overview/live-demo/) · [📖 Docs ↗](https://reconmap.com) · [🌐 Site ↗](https://reconmap.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/reconmap/)</sub>

<a name="sapper-v2"></a>
### #&#8288;31 [sapper-v2](https://github.com/n1neman/sapper-v2) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: fair (61) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · MIT · Nov 2026</sub>

**Multi-agent harness for autonomous CTF-style penetration testing.**

sapper-v2 runs a commander agent that dispatches generals, soldiers and scouts as AI CLI sessions in tmux panes. A watchdog script restarts crashed agents and rotates keys, and findings go into a layered fact-intent graph shared by all agents. It won a Tencent Cloud attack-defense qualifier (85 flags, 1.0B tokens) and is wired to that competition's platform API.

- **+** Agent CLI and model are swappable per role (Claude Code, Codex, DeepSeek, GLM)
- **+** Model tiering reported at 85 flags on 1.0B tokens versus runner-up's 4.5B
- **+** Core CLI is Python stdlib only; a pre-built ~1.2GB Kali image is offered
- **+** Watchdog handles commander restarts, key rotation and end-of-run wrap-up
- **−** Boot requires BENCHMARK_BASE_URL competition API; other setups must stub it
- **−** Doctrine is a 426-line CTF-specific SKILL.md that must be rewritten for other uses
- **−** Results are self-reported from one competition; no independent benchmark cited
- **−** Agents are driven by typing into tmux panes, which depends on each CLI's interactive UI

<sub>Docker · Needs tmux, Agent CLI such as Claude Code or Codex, Model gateway and API keys, Competition platform API (BENCHMARK_BASE_URL), Docker (optional, Kali image) · Models: GLM-5.3, DeepSeek V4.1 Flash, Claude Sonnet, any model via agent CLI · [Repo](https://github.com/n1neman/sapper-v2) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sapper-v2/)</sub>

<a name="pentestgpt"></a>
### #&#8288;32 [pentestgpt](https://github.com/greydgl/pentestgpt) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: widely used (86) · Freshness: recent (77) · Maintenance: weak (7) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · MIT · Jul 2026</sub>

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

<a name="agentic-security"></a>
### #&#8288;33 [agentic_security](https://github.com/msoedov/agentic_security) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (19) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.0k · Apache-2.0 · Nov 2026</sub>

**Jailbreak and prompt-injection scanner for LLM apps, with a CI gate.**

Agentic Security sends jailbreak, prompt-injection, multimodal and fuzzed attack prompts to any HTTP LLM endpoint and reports a failure rate per dataset. The `agentic_security ci` command exits 1 when a module exceeds a configured threshold, so it can fail a build. A separate `agesec` harness sends one attack at a time and takes decisions from a rule set, a CI job, Claude Code or Codex.

- **+** `agentic_security ci` exits 1 when failure rate exceeds `max_th`
- **+** Targets any HTTP API through a request template with a `<<PROMPT>>` placeholder
- **+** Covers image and audio attacks, multi-step jailbreaks and base64/rot13 fuzzing
- **+** Loads garak probes and any local CSV with a `prompt` column
- **−** `scan` runs every dataset (hundreds of thousands of prompts), costly on paid APIs
- **−** Built-in mock LLM refuses at random, so its scores are not meaningful
- **−** Installs from git, not a release; README asks for Python 3.15+
- **−** OWASP tags come from dataset names and do not prove coverage

<sub>no GPU · Needs Python 3.15+, Hugging Face datasets · Models: Any HTTP endpoint, OpenAI, Claude, Gemini, Azure OpenAI · port 8718 · [Repo](https://github.com/msoedov/agentic_security) · [📖 Docs ↗](https://agentic-security.vercel.app) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agentic-security/)</sub>

<a name="hexstrike-ai"></a>
### #&#8288;34 [hexstrike-ai](https://github.com/0x4m4/hexstrike-ai) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: widely used (83) · Freshness: active (92) · Maintenance: weak (4) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Aug 2026</sub>

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

<a name="pentestagent"></a>
### #&#8288;35 [pentestagent](https://github.com/gh05tcrew/pentestagent) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: known (37) · Freshness: active (100) · Maintenance: patchy (31) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · MIT · Nov 2026</sub>

**Terminal pentesting agent with crew mode and MCP client and server.**

PentestAgent is a Python TUI that drives an LLM through terminal, browser, notes and web search tools to run penetration tests against a target. It has assist, agent, crew (an orchestrator that spawns workers) and interact modes, plus black-box playbooks such as thp3_web. It consumes external MCP servers and can also run as an MCP server over stdio or HTTP/SSE.

- **+** Four modes: assist, agent, crew with spawned workers, and guided interact
- **+** Works as MCP client and as MCP server (stdio or SSE, default port 8080)
- **+** Docker images available, including a Kali image with metasploit, sqlmap and hydra
- **+** Any LiteLLM provider, with custom OpenAI- or Anthropic-compatible API bases
- **−** Needs a hosted LLM API key; no local-model setup is documented
- **−** Autonomous agents run real scanning tools, so a scope mistake has real consequences
- **−** Only one playbook (thp3_web) is named in the README
- **−** SSE MCP server binds to 0.0.0.0 by default; no auth is documented

<sub>no GPU · Docker + Compose · Needs Python 3.10+, LLM API key (OpenAI, Anthropic or other LiteLLM provider), Playwright Chromium, Docker (optional), Tavily API key (optional, web_search) · Models: OpenAI, Anthropic, LiteLLM-supported providers, OpenAI-compatible endpoints · port 8080 · [Repo](https://github.com/gh05tcrew/pentestagent) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pentestagent/)</sub>

<a name="adr"></a>
### #&#8288;36 [adr](https://github.com/uber/adr) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: fair (56) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · Apache-2.0 · Oct 2026</sub>

**Discovery, telemetry and LLM-based threat detection for enterprise coding agents.**

ADR is Uber's security system for AI agents. The repo includes an endpoint inventory of AI tools, a sensor that normalizes telemetry from agents such as Claude Code, Cursor, Codex and Copilot CLI, and a dual-agent detector evaluated on ADR-Bench (304 tasks, 134 MCP servers). The prevention component and the offline Explorer red-teaming engine are not included.

- **+** Deployed in production at Uber; paper accepted at MLSys 2026
- **+** Sensor covers Claude Code, Cursor, Codex, Copilot CLI, Gemini CLI on macOS, Linux, Windows
- **+** Includes reproducible benchmark: 304 tasks, 134 MCP servers, figure scripts
- **+** Two-tier detector: high-recall triage, then deeper agentic review of suspicious sessions
- **−** Prevention component is not in the open-source release
- **−** Offline ADR Explorer red-teaming engine is not included
- **−** Default detector needs Anthropic and OpenAI API keys
- **−** Benchmark fixtures are synthetic, so results may not match real environments

<sub>no GPU · Needs uv, Anthropic API, OpenAI API · Models: Anthropic, OpenAI, LlamaFirewall · [Repo](https://github.com/uber/adr) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/adr/)</sub>

<a name="adversarial-robustness-toolbox"></a>
### #&#8288;37 [adversarial-robustness-toolbox](https://github.com/trusted-ai/adversarial-robustness-toolbox) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: popular (61) · Freshness: recent (73) · Maintenance: patchy (39) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · MIT · Nov 2026</sub>

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
### #&#8288;38 [purplellama](https://github.com/meta-llama/purplellama) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: known (50) · Freshness: active (100) · Maintenance: weak (22) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.5k · custom license · Nov 2026</sub>

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

<a name="cairn"></a>
### #&#8288;39 [cairn](https://github.com/oritera/cairn) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: popular (56) · Freshness: active (99) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.6k · AGPL-3.0 · Sep 2026</sub>

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

<a name="pwnagotchi"></a>
### #&#8288;40 [pwnagotchi](https://github.com/evilsocket/pwnagotchi) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: popular (76) · Freshness: recent (69) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.3k · custom license · Aug 2026</sub>

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

<a name="superagent"></a>
### #&#8288;41 [superagent](https://github.com/superagent-ai/superagent) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: popular (65) · Freshness: recent (79) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.9k · MIT · Aug 2026</sub>

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

<a name="textattack"></a>
### #&#8288;42 [textattack](https://github.com/qdata/textattack) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: known (40) · Freshness: active (98) · Maintenance: weak (0) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.5k · MIT · Aug 2026</sub>

**Python framework for adversarial attacks, augmentation and training of NLP models.**

TextAttack is a Python library and `textattack` CLI that runs published adversarial attack recipes (TextFooler, BAE, DeepWordBug, HotFlip, PWWS and others) against NLP classification and sequence-to-sequence models. Attacks are built from goal functions, constraints, transformations and search methods. It also provides text augmentation recipes and single-command model training.

- **+** About 20 attack recipes from papers, runnable with one `textattack attack` command
- **+** Attacks are composable: swap transformation, constraints, goal function and search method
- **+** Augmentation recipes (wordnet, embedding, charswap, eda, back_trans) with a CSV CLI
- **+** Multi-GPU attacks via --parallel; GPU is optional
- **−** Targets classification and seq2seq models; no LLM jailbreak or prompt-injection tooling listed
- **−** Many recipes need downloaded embeddings, sentence encoders and masked language models
- **−** seq2sick is implemented black-box, unlike the white-box attack in its paper
- **−** README gives Python 3.6+ as the baseline, which is dated

<sub>GPU optional · Needs Python 3.6+, pip · Models: BERT, DistilBERT, LSTM, T5, Keras models · [Repo](https://github.com/qdata/textattack) · [📖 Docs ↗](https://textattack.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/textattack/)</sub>

<a name="deepteam"></a>
### #&#8288;43 [deepteam](https://github.com/confident-ai/deepteam) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: known (33) · Freshness: active (84) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.1k · Apache-2.0 · Oct 2026</sub>

**Red teaming framework that attacks LLM apps and scores vulnerabilities.**

DeepTeam generates adversarial prompts (jailbreaks, prompt injection, multi-turn attacks) against an LLM app you wrap in a Python `model_callback`. It scores responses on 50+ vulnerabilities such as PII leakage, bias and SQL injection using local LLM-as-a-judge metrics. It maps tests to OWASP, NIST and MITRE ATLAS, and includes 7 guardrails for production input and output checks.

- **+** 50+ vulnerabilities and 20+ single- and multi-turn attack methods, extensible with custom ones
- **+** Presets for OWASP Top 10 for LLMs 2025, NIST AI RMF, MITRE ATLAS and others
- **+** Needs no dataset: attacks are generated from the chosen vulnerabilities
- **+** Runs from Python or the CLI with YAML configs; results save locally as JSON
- **−** Attack generation and judging need an LLM; the quickstart assumes an OPENAI_API_KEY
- **−** Built on DeepEval, so the install depends on that framework
- **−** Result tracking, production monitoring and team reports use the hosted Confident AI platform
- **−** Last release (2025-11-12) is about a year older than the latest commit

<sub>no GPU · Needs DeepEval, OpenAI API key or other DeepEval-supported LLM · Models: OpenAI, custom models via DeepEval · [Repo](https://github.com/confident-ai/deepteam) · [📖 Docs ↗](https://www.trydeepteam.com/docs/guidelines-and-frameworks) · [🌐 Site ↗](https://www.trydeepteam.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepteam/)</sub>

<a name="pentest-ai-agents"></a>
### #&#8288;44 [pentest-ai-agents](https://github.com/0xsteph/pentest-ai-agents) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: niche (27) · Freshness: active (98) · Maintenance: weak (22) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.5k · MIT · Aug 2026</sub>

**Claude Code subagents for pentesting, from recon to reporting.**

A set of Claude Code subagent definition files, each covering one pentest area such as recon, web, Active Directory, cloud, mobile, C2, reverse engineering, detection engineering and reporting. Claude routes a task to the matching agent. Execution-capable Tier 2 agents require a declared scope and a scope-guard block. It installs by shell script into ~/.claude/agents or as a Claude Code plugin, and adds a SQLite findings database and slash commands.

- **+** Covers recon, exploitation, post-exploitation, detection and reporting with distinct agents
- **+** Tier 2 agents need a declared scope; CI checks the scope-guard block is present
- **+** Installs by copying files or as a Claude Code plugin; no servers or Python deps
- **+** Offensive agents pair techniques with detection content; includes SQLite findings DB
- **−** Requires Claude Code; agents are prompt files, not a standalone runtime
- **−** Underlying tools (nmap, nuclei, sqlmap, etc.) must be installed separately
- **−** README says both 50 and 52 agents, so the count is inconsistent
- **−** Includes C2, evasion and payload agents that are easy to misuse outside authorized work

<sub>no GPU · Docker · Needs Claude Code, nmap, nuclei, sqlmap and other CLI pentest tools (optional, via install.sh --tools), SQLite · Models: Claude · [Repo](https://github.com/0xsteph/pentest-ai-agents) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pentest-ai-agents/)</sub>

<a name="airecon"></a>
### #&#8288;45 [airecon](https://github.com/pikpikcu/airecon) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: niche (4) · Freshness: active (96) · Maintenance: patchy (46) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.1k · MIT · Nov 2026</sub>

**Autonomous pentest agent with Kali sandbox, Caido integration and a terminal UI.**

AIRecon runs a RECON, ANALYSIS, EXPLOIT, REPORT pipeline against a target, using any OpenAI-compatible or Anthropic-protocol LLM endpoint with native tool calling. Commands execute in a Kali Linux Docker sandbox, with built-in Caido proxy tools, a scope guard, an audit log and a Textual TUI. It keeps local SQLite memory of verified findings and can optionally query a ~1.09M-record offline security dataset.

- **+** Scope guard (off/warn/block) and JSONL audit log of every command
- **+** Native Caido tools: list, replay, automate, findings, scope, sitemap, intercept
- **+** Works with local gateways (LiteLLM, vLLM, Ollama) for fully offline operation
- **+** Session resume and MCP server support; only verified findings persist to memory
- **−** Requires a model with native tool calling; agent is non-functional without it
- **−** Models under 8B not recommended; 8B-14B give more tool-call errors
- **−** Needs a separately run LLM gateway plus Docker 20.10+ and Python 3.12+
- **−** Labeled beta (v1.7.1); phase enforcement is soft, so the agent may skip steps

<sub>GPU optional · Needs Docker 20.10+, Python 3.12+, OpenAI-compatible LLM gateway, git, curl · Models: OpenAI-compatible, Anthropic, Ollama, vLLM, LiteLLM · [Repo](https://github.com/pikpikcu/airecon) · [📖 Docs ↗](https://pikpikcu.github.io/airecon/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/airecon/)</sub>

<a name="cybergym"></a>
### #&#8288;46 [cybergym](https://github.com/sunblaze-ucb/cybergym) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: niche (2) · Freshness: active (100) · Maintenance: weak (27) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.1k · Apache-2.0 · Aug 2026</sub>

**Benchmark for AI agents reproducing real vulnerabilities with PoC inputs.**

CyberGym is an evaluation framework that gives an agent a vulnerable codebase from ARVO or OSS-Fuzz tasks and asks it to produce a PoC input. A local Python server runs submitted PoCs in Docker against pre- and post-patch builds and records the results. It also includes a Squid-based domain-allowlist firewall for agent containers and four example agents.

- **+** Scores PoCs by executing them against vulnerable and patched builds
- **+** Built-in Squid allowlist firewall restricts agent containers to approved domains
- **+** Binary-only (~130GB) and 10-task subset options reduce data size
- **+** Difficulty levels and a leaderboard submission guide for comparable results
- **−** Full server data is about 10TB; benchmark data alone is about 240GB
- **−** Server is partly unauthenticated and must never be exposed publicly
- **−** README ships a public placeholder API key that must be replaced
- **−** Evaluates agents only; not a pentest tool for your own apps

<sub>Needs Docker, Git LFS, 7z, Squid (firewall), Hugging Face dataset · port 8666 · [Repo](https://github.com/sunblaze-ucb/cybergym) · [🌐 Site ↗](https://cybergym.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cybergym/)</sub>

<a name="buttercup"></a>
### #&#8288;47 [buttercup](https://github.com/trailofbits/buttercup) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: niche (13) · Freshness: recent (76) · Maintenance: weak (20) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · AGPL-3.0 · Sep 2026</sub>

**Automated fuzzing and LLM-based patching of C and Java OSS-Fuzz projects.**

Buttercup is Trail of Bits' Cyber Reasoning System from DARPA AIxCC. It runs an AI-assisted fuzzing campaign on OSS-Fuzz-compatible C and Java repositories, then uses a multi-agent patcher to fix the vulnerabilities it finds. It deploys to a local cluster through make targets and has a web UI on port 31323.

- **+** Covers the full loop: fuzzing, crash analysis, and patch generation
- **+** Built-in LLM budget setting limits third-party API spend
- **+** SigNoz observability included; optional LangFuse for LLM usage and cost
- **+** Make-based setup and deploy, with an AKS guide for production
- **−** Targets only C and Java projects that already have OSS-Fuzz harnesses
- **−** Requires paid third-party LLM API keys (OpenAI, Anthropic or Google)
- **−** Needs 8 cores, 16 GB RAM and 100 GB disk at minimum
- **−** Last release is from August 2025; ARM64 support is partial

<sub>RAM ≥ 16 GB · no GPU · Needs Docker Desktop or Colima, OpenAI, Anthropic or Google API key, OSS-Fuzz, SigNoz, LangFuse (optional) · Models: OpenAI, Anthropic, Google · port 31323 · [Repo](https://github.com/trailofbits/buttercup) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/buttercup/)</sub>

<a name="guardian-cli"></a>
### #&#8288;48 [guardian-cli](https://github.com/zakirkun/guardian-cli) <sub>score [32](../README.md#-how-we-rank "Score 32/100. Adoption: niche (17) · Freshness: recent (78) · Maintenance: weak (0) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · custom license · Jun 2026</sub>

**Python CLI that runs LLM-planned pentest workflows over 50 security tools.**

Guardian is a Python 3.11+ CLI that uses planner, tool-selector, analyst and reporter agents to drive security tools such as nmap, nuclei, sqlmap and ffuf through YAML DAG workflows. It supports OpenAI, Claude, Gemini, OpenRouter, Requesty, Ollama and OpenAI-compatible endpoints. Findings are linked to tool executions and can be exported as Markdown, HTML, JSON, SARIF, DefectDojo or Slack.

- **+** Supports 7 LLM providers including local Ollama and OpenAI-compatible endpoints
- **+** Findings link to the originating tool execution, with raw output kept as evidence
- **+** Scope checks, confirmation gate for intrusive tools, and safe mode on by default
- **+** Exports SARIF, DefectDojo and Slack; workflows resume from the last completed step
- **−** Wraps external tools that must be installed separately; coverage depends on what is present
- **−** README is inconsistent on tool count: 50 in features, 19 in the architecture diagram
- **−** License is reported as NOASSERTION while the README badge says MIT
- **−** Debate and visual triage add LLM token cost; vision needs a vision-capable provider

<sub>no GPU · Docker + Compose · Needs Python 3.11+, LLM provider API key or Ollama, nmap, nuclei, httpx and other security tools (optional), Playwright with Chromium (visual triage) · Models: OpenAI, Anthropic Claude, Google Gemini, OpenRouter, Requesty · [Repo](https://github.com/zakirkun/guardian-cli) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/guardian-cli/)</sub>

<a name="hackgpt"></a>
### #&#8288;49 [hackgpt](https://github.com/nodatafound/hackgpt) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: niche (9) · Freshness: active (96) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 1.2k · no license · Aug 2026</sub>

**Jupyter notebooks and scripts that send security inputs to OpenAI models.**

hackGPT is a set of Jupyter notebooks and Python scripts (PwnAI.py, PwnAI_bulk.py) that pass security material to OpenAI models, such as malware samples, exploit sources and JSON threat data. README examples include generating CVE exploit and defense output, fixing JIRA bug tickets, and a chatbot opened in a browser tab or Colab. It needs an OpenAI API key set in .env.

- **+** Single and bulk modes (PwnAI.py, PwnAI_bulk.py) with sample input files included
- **+** Can run in Google Colab, so no local setup is needed
- **+** Examples cover CVE exploit generation, threat JSON parsing and JIRA bug fixing
- **−** No license, so reuse terms are unclear
- **−** Depends on the OpenAI API; no local model support is described
- **−** README is mostly screenshots with little written documentation
- **−** No Docker setup and no tagged releases

<sub>no GPU · Needs OpenAI API key, Jupyter Notebook, Python 3 · Models: OpenAI · [Repo](https://github.com/nodatafound/hackgpt) · [▶️ Demo ↗](https://hackgpt.com) · [🌐 Site ↗](https://hackgpt.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hackgpt/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
