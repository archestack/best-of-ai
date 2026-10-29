# 🛡️ Sandboxes reviews · Best of Open-Source AI

Isolated runtimes where agents execute code, browse or use tools safely. Back to the [leaderboard](../README.md#%EF%B8%8F-sandboxes).

<sub>🌐 Also on the web: [Sandboxes on archestack.com](https://archestack.com/best-of-ai/sandboxes/), each project on its own page.</sub>

<a name="lightpanda"></a>
### 🥇 [Lightpanda](https://github.com/lightpanda-io/browser) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: healthy (92) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · AGPL-3.0 · Oct 2026</sub>

**Headless browser written in Zig for agents and scraping, with CDP and MCP.**

Lightpanda is a headless browser written from scratch in Zig, using V8 for JavaScript, libcurl for HTTP and html5ever for parsing, with no graphical rendering. It exposes a CDP server for Puppeteer and Playwright, WebDriver BiDi, an MCP server over stdio or HTTP, and a fetch command that dumps pages as HTML or Markdown. An agent mode records sessions as replayable scripts.

- **+** README benchmark: 123MB peak vs 2GB for headless Chrome over 100 pages
- **+** Speaks CDP, WebDriver BiDi and MCP, so Puppeteer and Playwright clients can connect
- **+** Agent mode supports many LLM providers and local Ollama or llama.cpp, or runs with --no-llm
- **+** Agent sessions export to deterministic scripts that replay without a model
- **−** No graphical rendering; web platform coverage is partial (see WPT results)
- **−** No native Windows binary; needs WSL2, and Linux binaries need glibc
- **−** Usage telemetry is on by default and must be disabled via environment variable
- **−** AGPL-3.0 license and a CLA required for contributions

<sub>no GPU · Docker · Needs Puppeteer or Playwright (optional client), LLM provider API key (agent mode only) · Models: Anthropic, OpenAI, Gemini, Google Vertex AI, Mistral · port 9222 · [Repo](https://github.com/lightpanda-io/browser) · [📖 Docs ↗](https://lightpanda.io/docs/usage/agent) · [🌐 Site ↗](https://lightpanda.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lightpanda/)</sub>

<a name="openshell"></a>
### 🥈 [OpenShell](https://github.com/nvidia/openshell) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: popular (67) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · Apache-2.0 · Oct 2026</sub>

**Policy-enforced sandbox runtime for autonomous AI agents.**

OpenShell runs each agent in an isolated sandbox where kernel controls restrict file access and system calls, and every outbound network connection is checked against a declared policy. Real credentials are injected only into requests bound for approved endpoints, and policy changes are checked with formal verification so risky new access waits for human review. It ships a CLI and gateway, SDKs for four languages, and a Helm chart.

- **+** Filesystem, syscall and network rules declared per agent in a policy
- **+** Agents never see real credentials; injected only for approved endpoints
- **+** Policy changes are formally verified and gated for human review
- **+** SDKs for Python, TypeScript, Go and Rust; Helm chart for Kubernetes
- **−** Default sandbox image is minimal Ubuntu with no agent installed
- **−** Windows support is via WSL 2 and marked experimental
- **−** Kubernetes needs a CNI that enforces NetworkPolicy
- **−** Anonymous telemetry is on by default; opt-out required

<sub>GPU optional · Docker + Compose · Needs Docker, Podman or host virtualization, Kubernetes with NetworkPolicy-enforcing CNI (optional) · Models: OpenRouter (example provider) · [Repo](https://github.com/nvidia/openshell) · [▶️ Demo ↗](https://brev.nvidia.com/launchable/deploy/now?launchableID=env-3Ap3tL55zq4a8kew1AuW0FpSLsg) · [📖 Docs ↗](https://docs.nvidia.com/openshell/latest/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openshell/)</sub>

<a name="obscura"></a>
### 🥉 [Obscura](https://github.com/h4ckf0r0day/obscura) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Oct 2026</sub>

**Rust headless browser with V8 and CDP for scraping and agents.**

Obscura is a headless browser engine written in Rust that runs JavaScript through embedded V8 and exposes the Chrome DevTools Protocol, so Puppeteer and Playwright can connect to it. It has its own rendering layer for screenshots, screencasts and PDF export without Chromium, plus an optional stealth build with fingerprint randomization and tracker blocking. A CLI covers single-page fetch, parallel scrape, and a CDP server on port 9222.

- **+** No Chrome or Node.js needed; release archives ship as prebuilt binaries for Linux, macOS and Windows
- **+** Connects to existing Puppeteer and Playwright scripts over CDP
- **+** README claims ~30 MB memory and ~85 ms page load versus headless Chrome
- **+** Parallel scrape command and DOM-to-Markdown CDP method suit LLM pipelines
- **−** Independent rendering engine; long-tail CSS, some Web APIs and media playback may differ from Chromium
- **−** Stealth transport needs a separate build or archive, compiling BoringSSL with CMake and Clang
- **−** Blocks private-network fetches by default; local dev servers need --allow-private-network
- **−** Speed and memory figures are the project's own; independent verification not given in README

<sub>no GPU · Docker · port 9222 · [Repo](https://github.com/h4ckf0r0day/obscura) · [📖 Docs ↗](https://docs.obscura.sh) · [🌐 Site ↗](https://obscura.sh) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/obscura/)</sub>

<a name="nemoclaw"></a>
### #&#8288;4 [NemoClaw](https://github.com/nvidia/nemoclaw) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · Apache-2.0 · Oct 2026</sub>

**Reference stack for running OpenClaw, Hermes and Deep Agents in OpenShell sandboxes.**

NemoClaw is a CLI-driven reference stack that installs a supported AI agent (OpenClaw by default, Hermes, or LangChain Deep Agents Code) inside an NVIDIA OpenShell sandbox. It adds guided onboarding, managed inference, network egress policy with operator approval, managed integrations and state persistence. The README labels it alpha.

- **+** Network policy with baseline rules, presets and operator approval for egress
- **+** Supports three agents: OpenClaw, Hermes and LangChain Deep Agents Code
- **+** Guided installer with express presets for DGX and WSL hosts
- **+** Official docs cover architecture, sandbox hardening and CLI commands
- **−** Labeled alpha; maintainer responses carry no guaranteed timelines
- **−** Depends on NVIDIA OpenShell as the sandbox runtime
- **−** No tagged release published
- **−** Hardware and RAM requirements are only in external docs, not the README

<sub>Docker · Needs NVIDIA OpenShell · Models: OpenClaw, Hermes, LangChain Deep Agents Code · [Repo](https://github.com/nvidia/nemoclaw) · [📖 Docs ↗](https://docs.nvidia.com/nemoclaw/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nemoclaw/)</sub>

<a name="opensandbox"></a>
### #&#8288;5 [opensandbox](https://github.com/opensandbox-group/opensandbox) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Oct 2026</sub>

**Sandbox API for running AI agent code, commands and browsers in isolation.**

OpenSandbox provides isolated environments where agents execute code, run shell commands, manage files and drive browsers or desktops, through a single lifecycle API. It runs locally on Docker and scales to Kubernetes, with SDKs for Python, Java/Kotlin, TypeScript, C#/.NET and Go, plus an `osb` CLI and an MCP server. Egress policies, an ingress gateway and a credential vault control network access.

- **+** SDKs in five languages plus osb CLI and MCP server
- **+** Same lifecycle API for local Docker and Kubernetes deployments
- **+** Per-sandbox egress policies and a credential vault keep real secrets out of workloads
- **+** Firecracker runtime with pause/resume; reported 64 ms P50 creation time
- **−** Docker required for local use; Kubernetes setup needed for the fast runtime
- **−** No hosted demo or playground listed in the README
- **−** Firecracker and pause/resume features documented only for the Kubernetes fast runtime
- **−** Server needs separate install and TOML configuration before first use

<sub>no GPU · Needs Docker, Python 3.10+, Kubernetes (optional, for cluster deployment) · [Repo](https://github.com/opensandbox-group/opensandbox) · [📖 Docs ↗](https://open-sandbox.ai) · [🌐 Site ↗](https://open-sandbox.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/opensandbox/)</sub>

<a name="cubesandbox"></a>
### #&#8288;6 [cubesandbox](https://github.com/tencentcloud/cubesandbox) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · custom license · Oct 2026</sub>

**MicroVM sandbox service for AI agents with an E2B-compatible API.**

CubeSandbox runs each agent sandbox in its own KVM MicroVM, built on RustVMM, and exposes an E2B-compatible API so existing E2B SDK clients can point at it by changing an environment variable. It runs on a single node or a multi-node cluster and includes snapshot/rollback, pause/resume, an eBPF network layer and an L7 egress proxy with credential injection. The README reports under 60ms cold start and under 5MB memory overhead per sandbox.

- **+** Each sandbox gets a dedicated kernel in its own KVM MicroVM, not shared-kernel containers
- **+** E2B SDK compatible; README says switching needs one environment variable change
- **+** Snapshot, clone and rollback, plus auto pause/resume of idle sandboxes
- **+** Egress proxy injects credentials so API keys never enter the sandbox
- **−** Requires x86_64 Linux with KVM for the quick start path
- **−** Multi-component stack (API, master, cubelet, eBPF switch, proxy), heavier than a single binary
- **−** Kubernetes deploy and cross-node pause/resume are marked preview
- **−** License detected as NOASSERTION; README badge says Apache 2.0, so verify

<sub>no GPU · Docker · Needs KVM, Linux x86_64, S3 (optional, for cross-node pause/resume) · port 12088 · [Repo](https://github.com/tencentcloud/cubesandbox) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cubesandbox/)</sub>

<a name="monty"></a>
### #&#8288;7 [monty](https://github.com/pydantic/monty) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.8k · MIT · Oct 2026</sub>

**Embedded Python interpreter in Rust for running LLM-generated code.**

Monty is a Python 3.14 subset interpreter written in Rust, installed as a Python, JavaScript or Rust package. It runs model-written code with no filesystem, environment variables or network, so the code reaches the host only through functions and mounts the caller passes in. The README reports under 1ms to get a new sandbox from a running pool, compared with about 1500ms for a sandbox service.

- **+** No filesystem, env vars or network inside; host access only via passed-in functions and mounts
- **+** Reported under 1ms sandbox start from a pool, versus about 1500ms for a sandbox service
- **+** Packages for Python (pydantic-monty), npm (@pydantic/monty) and Rust (monty crate)
- **+** Documents resource limits and snapshots; MIT licensed
- **−** Runs only a subset of Python, so some model-written code will not execute
- **−** Server mode (Full Monty, WebSocket service) is a separate commercial product
- **−** Go and Dart bindings are community-maintained, not official
- **−** Latency figures come from the project's own docs, not independent benchmarks

<sub>no GPU · [Repo](https://github.com/pydantic/monty) · [📖 Docs ↗](https://pydantic.dev/docs/monty/) · [🌐 Site ↗](https://pydantic.dev/docs/monty/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/monty/)</sub>

<a name="microsandbox"></a>
### #&#8288;8 [microsandbox](https://github.com/superradcompany/microsandbox) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: niche (29) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.9k · Apache-2.0 · Oct 2026</sub>

**Embeddable local microVM sandboxes for running untrusted code and AI agents.**

Microsandbox boots OCI images (Docker Hub, GHCR, any registry) as hardware-isolated microVMs, with reported average boot times under 100 ms. It ships an `msb` CLI and SDKs for TypeScript, Rust, Python, Go and Ruby that spawn VMs as child processes, with no server or daemon. It supports forking live sandboxes, snapshots, network allowlists and secrets that never enter the VM. The README marks it as beta software.

- **+** Embeddable SDKs spawn microVMs in-process; no setup server or long-running daemon
- **+** Fork running sandboxes and snapshot or restore full state
- **+** Runs standard OCI images on Linux (KVM), macOS (Apple Silicon) and Windows (WHP)
- **+** Secrets stay outside the VM; network access limited by host allowlist
- **−** README warns of beta status: breaking changes, missing features, rough edges
- **−** Needs KVM on Linux, Apple Silicon on macOS, or WHP on Windows
- **−** First create() pulls the image, so initial start depends on network
- **−** Intel Macs are not listed as supported

<sub>no GPU · Docker · Needs KVM (Linux), WHP (Windows), OCI registry access · [Repo](https://github.com/superradcompany/microsandbox) · [📖 Docs ↗](https://docs.microsandbox.dev) · [🌐 Site ↗](https://microsandbox.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/microsandbox/)</sub>

<a name="open-terminal"></a>
### #&#8288;9 [Open Terminal](https://github.com/open-webui/open-terminal) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (1) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · MIT · Oct 2026</sub>

**REST API shell and file server for AI agents to run commands and code.**

Open Terminal is a Python server that exposes a shell, file management, search and code execution over a REST API, with interactive docs at /docs. It runs either in a Docker container (latest, slim, alpine and openshift images) or on bare metal via pip or uvx. It integrates with Open WebUI as a direct or admin-level connection, with a file sidebar.

- **+** Runs via Docker or bare metal with `pip install open-terminal` or `uvx`
- **+** Four image variants, from ~230 MB alpine to ~4 GB full toolkit image
- **+** Configurable by CLI flags, environment variables or TOML config files
- **+** Built-in OpenAPI docs at /docs and file browser endpoints
- **−** Bare metal mode runs commands with your user's permissions, with no sandbox
- **−** Multi-user mode shares one container and is not a security boundary
- **−** Per-user container isolation needs Terminals, which requires an Open WebUI Enterprise License
- **−** Mounting the Docker socket gives effective root on the host

<sub>no GPU · Docker · Needs Docker (optional), Python (bare metal) · port 8000 · [Repo](https://github.com/open-webui/open-terminal) · [📖 Docs ↗](https://docs.openwebui.com/features/open-terminal/terminals/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/open-terminal/)</sub>

<a name="steel-browser"></a>
### #&#8288;10 [Steel Browser](https://github.com/steel-dev/steel-browser) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: fair (54) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.9k · Apache-2.0 · Oct 2026</sub>

**Browser API that manages Chrome sessions for Puppeteer, Playwright and Selenium.**

REST API and UI on port 3000 that launches Chrome sessions with persisted cookies and storage, proxy chains, stealth plugins and request logging, then hands you a CDP endpoint for Puppeteer or Playwright or a WebDriver endpoint for Selenium. Quick-action endpoints return a page as HTML, markdown, screenshot or PDF. Runs from a prebuilt ghcr.io image or docker compose; Node and Python SDKs target cloud or self-hosted instances.

- **+** One image serves API, UI and console debugger (ports 3000 and 9223)
- **+** Session API persists cookies and storage; Selenium sessions via isSelenium
- **+** Swagger UI at /documentation on the local instance
- **+** Node and Python SDKs switch between cloud and self-host with baseURL
- **−** Public beta; API still changing
- **−** Runs full Chrome; needs a Chrome executable when run outside Docker
- **−** Selenium integration lacks some features of the CDP session API
- **−** Apple Silicon compose needs DOCKER_DEFAULT_PLATFORM=linux/arm64

<sub>no GPU · Docker + Compose · Needs Google Chrome (non-Docker runs), Node.js (non-Docker runs) · port 3000 · [Repo](https://github.com/steel-dev/steel-browser) · [📖 Docs ↗](https://docs.steel.dev/) · [🌐 Site ↗](https://steel.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/steel-browser/)</sub>

<a name="browser-use-web-ui"></a>
### #&#8288;11 [Browser Use Web UI](https://github.com/browser-use/web-ui) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: popular (59) · Freshness: recent (60) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · MIT · May 2026</sub>

**Gradio UI for running browser-use agents with your own Chrome.**

Gradio front end over the browser-use library that takes a task, drives a Playwright browser with an LLM (Google, OpenAI, Azure OpenAI, Anthropic, DeepSeek or Ollama) and shows the run. Can attach to your own Chrome profile to reuse logins, keep the browser open between tasks and record video. Runs with uv and Python 3.11 on port 7788, or via docker compose with a noVNC viewer on port 6080.

- **+** Own-browser mode reuses existing Chrome logins and cookies
- **+** Docker compose includes noVNC so you can watch the agent at localhost:6080
- **+** Persistent browser sessions keep history visible between tasks
- **+** Supports Ollama and DeepSeek-R1 alongside cloud providers
- **−** Changelog stops in January 2025; last commit May 2026
- **−** Default VNC password is published in the README; change VNC_PASSWORD
- **−** Own-browser mode requires closing all Chrome windows and using another browser for the UI
- **−** Gradio single-user UI; no auth or multi-user features described

<sub>no GPU · Docker + Compose · Needs Playwright browsers, LLM API key or Ollama, Chrome (optional, own-browser mode) · Models: Google, OpenAI, Azure OpenAI, Anthropic, DeepSeek · port 7788 · [Repo](https://github.com/browser-use/web-ui) · [📖 Docs ↗](https://docs.browser-use.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/browser-use-web-ui/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
