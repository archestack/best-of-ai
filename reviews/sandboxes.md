# 🛡️ Sandboxes reviews · Best of Open-Source AI

Isolated runtimes where agents execute code, browse or use tools safely. Back to the [leaderboard](../README.md#%EF%B8%8F-sandboxes).

<sub>🌐 Also on the web: [Sandboxes on archestack.com](https://archestack.com/best-of-ai/sandboxes/), each project on its own page.</sub>

<a name="lightpanda"></a>
### 🥇 [Lightpanda](https://github.com/lightpanda-io/browser) <sub>score [94](../README.md#-how-we-rank "Score 94/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 42k · AGPL-3.0 · Nov 2026</sub>

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
### 🥈 [OpenShell](https://github.com/nvidia/openshell) <sub>score [90](../README.md#-how-we-rank "Score 90/100. Adoption: widely used (80) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 21k · Apache-2.0 · Nov 2026</sub>

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
### 🥉 [Obscura](https://github.com/h4ckf0r0day/obscura) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · Apache-2.0 · Nov 2026</sub>

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

<a name="opensandbox"></a>
### #&#8288;4 [opensandbox](https://github.com/opensandbox-group/opensandbox) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · Apache-2.0 · Nov 2026</sub>

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

<a name="nemoclaw"></a>
### #&#8288;5 [NemoClaw](https://github.com/nvidia/nemoclaw) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · Apache-2.0 · Nov 2026</sub>

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

<a name="cubesandbox"></a>
### #&#8288;6 [cubesandbox](https://github.com/tencentcloud/cubesandbox) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · custom license · Nov 2026</sub>

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
### #&#8288;7 [monty](https://github.com/pydantic/monty) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.9k · MIT · Nov 2026</sub>

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
### #&#8288;8 [microsandbox](https://github.com/superradcompany/microsandbox) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.0k · Apache-2.0 · Nov 2026</sub>

**Embeddable local microVM sandboxes for running untrusted code and AI agents.**

Microsandbox boots OCI images (Docker Hub, GHCR, any registry) as hardware-isolated microVMs, with reported average boot times under 100 ms. It ships an `msb` CLI and SDKs for TypeScript, Rust, Python, Go and Ruby that spawn VMs as child processes, with no server or daemon. It supports forking live sandboxes, snapshots, network allowlists and secrets that never enter the VM. The README marks it as beta software.

- **+** Embeddable SDKs spawn microVMs in-process; no setup server or long-running daemon
- **+** Fork running sandboxes and snapshot or restore full state
- **+** Runs standard OCI images on Linux (KVM), macOS (Apple Silicon) and Windows (WHP)
- **+** Secrets stay outside the VM; network access limited by host allowlist
- **−** README warns of beta status: breaking changes, missing features, rough edges
- **−** Needs KVM on Linux, Apple Silicon on macOS, or WHP on Windows
- **−** First create() pulls the image, so initial start depends on network

<sub>no GPU · Docker · Needs KVM (Linux), WHP (Windows), OCI registry access · [Repo](https://github.com/superradcompany/microsandbox) · [📖 Docs ↗](https://docs.microsandbox.dev) · [🌐 Site ↗](https://microsandbox.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/microsandbox/)</sub>

<a name="smolvm"></a>
### #&#8288;9 [smolvm](https://github.com/smol-machines/smolvm) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (40) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · Apache-2.0 · Nov 2026</sub>

**MicroVM runtime with live checkpoints and branching for agent sandboxes.**

smolvm runs each workload in its own libkrun microVM with a separate guest kernel, using Hypervisor.framework, KVM or Windows Hypervisor Platform. It boots any OCI image without a Docker daemon. It can checkpoint a running machine (RAM, CPU, disks), branch it copy-on-write, and pack it into a single .smolmachine executable. SDKs for Node, Python, Rust and Go embed it in-process.

- **+** Per-workload VM with own kernel; network off by default, egress limited to named hosts
- **+** Live checkpoint and copy-on-write branching of running machines, including RAM and CPU state
- **+** SDKs for Node, Python, Rust and Go run in-process with no daemon
- **+** Runs on macOS Apple Silicon, Linux (KVM) and Windows; packs to one .smolmachine file
- **−** No published macOS Intel build; that platform is untested
- **−** GPU acceleration is unavailable on Windows
- **−** Linux hosts need KVM (/dev/kvm); Windows needs Windows Hypervisor Platform enabled
- **−** SDK source and user docs live in separate repositories

<sub>GPU optional · Needs KVM (Linux), Hypervisor.framework (macOS), Windows Hypervisor Platform (Windows), libkrun · [Repo](https://github.com/smol-machines/smolvm) · [📖 Docs ↗](https://smolmachines.com/docs/) · [🌐 Site ↗](https://smolmachines.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/smolvm/)</sub>

<a name="substrate"></a>
### #&#8288;10 [substrate](https://github.com/agent-substrate/substrate) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (35) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.5k · Apache-2.0 · Nov 2026</sub>

**Kubernetes runtime that sandboxes agents and suspends idle ones to snapshots.**

Agent Substrate maps a large set of stateful actors, such as agents, onto a smaller pool of warm worker pods on Kubernetes. Idle actors are snapshotted out of memory and restored on request, with a stated resume time under 500ms. Each actor runs in a gVisor or Cloud Hypervisor sandbox with a SPIFFE identity, default-deny networking and an egress gateway that injects credentials outside the sandbox.

- **+** Snapshots RAM and filesystem state, so actors resume intact on any worker in the pool
- **+** Egress gateway injects credentials, so sandboxed code never holds them
- **+** Per-actor SPIFFE certificates and default-deny networking; plain containers are not allowed
- **+** Runs standard OCI images; demos cover Claude Code and MCP servers
- **−** Requires a Kubernetes cluster; no standalone or single-host mode
- **−** Several components to operate: API server, atelet, controller, networking and router
- **−** README says the project is very young and may not merge off-roadmap contributions
- **−** Only gVisor and Cloud Hypervisor sandboxes are supported

<sub>Needs Kubernetes, gVisor (runsc), Cloud Hypervisor, Envoy, Go, kubectl, docker · [Repo](https://github.com/agent-substrate/substrate) · [📖 Docs ↗](https://github.com/agent-substrate/substrate/blob/main/docs/concepts/architecture.md) · [🌐 Site ↗](https://ate.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/substrate/)</sub>

<a name="nono"></a>
### #&#8288;11 [nono](https://github.com/nolabs-ai/nono) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: niche (23) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.9k · Apache-2.0 · Nov 2026</sub>

**Kernel-enforced sandbox and policy layer for running AI coding agents.**

nono is a single unprivileged Rust binary that runs agents such as Claude Code, Codex, Goose or custom ones inside a kernel-enforced sandbox. Composable JSON profiles set filesystem, network, tool and credential rules, with proxy-based credential injection, Sigstore verification of skills and instruction files, tamper-evident audit logs and snapshot rollback. It runs on macOS, Linux and Windows via WSL2.

- **+** Single binary, no root needed; runs on laptops, CI, Kubernetes pods and microVMs
- **+** Per-tool rules, e.g. aws may use a credential while curl cannot
- **+** Credentials stay outside the sandbox via proxy injection and phantom tokens
- **+** Registry of ready-made profiles for popular agents, extendable as composable JSON
- **−** README says APIs are still stabilizing ahead of a 1.0 release
- **−** Windows support only through WSL2
- **−** Policy model has a learning curve; detail lives in external docs
- **−** No Docker image or compose file detected

<sub>no GPU · Docker · [Repo](https://github.com/nolabs-ai/nono) · [📖 Docs ↗](https://docs.nono.sh) · [🌐 Site ↗](https://nono.sh) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nono/)</sub>

<a name="agent-sandbox"></a>
### #&#8288;12 [agent-sandbox](https://github.com/kubernetes-sigs/agent-sandbox) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.6k · Apache-2.0 · Nov 2026</sub>

**Kubernetes CRD and controller for stateful, singleton sandbox pods for agents.**

Defines a Sandbox custom resource that manages a single pod with stable hostname, persistent storage and a lifecycle (create, scheduled delete, pause, resume). Extensions add SandboxTemplate, SandboxClaim and SandboxWarmPool for pre-warmed sandboxes. It orchestrates only: isolation comes from runtimes such as gVisor or Kata Containers selected through RuntimeClass.

- **+** Warm pools of pre-created sandboxes cut startup time for claims
- **+** Delegates isolation to gVisor or Kata via RuntimeClass, vendor-neutral
- **+** Go and Python SDKs plus an optional HTTP sandbox router
- **+** Part of Kubernetes SIG Apps; release manifests and Helm chart provided
- **−** Requires an existing Kubernetes cluster, 1.25+ with CEL validation; 1.29+ recommended
- **−** Does not provide isolation itself; you must set up a sandbox runtime
- **−** Gateway-based client access needs Gateway API CRDs, which need Kubernetes 1.31+
- **−** Deep hibernation and memory sharing are listed as goals, not confirmed features

<sub>no GPU · Docker · Needs Kubernetes 1.25+, gVisor or Kata Containers (optional runtime), Gateway API CRDs (optional) · [Repo](https://github.com/kubernetes-sigs/agent-sandbox) · [📖 Docs ↗](https://agent-sandbox.sigs.k8s.io/docs/) · [🌐 Site ↗](https://agent-sandbox.sigs.k8s.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agent-sandbox/)</sub>

<a name="steel-browser"></a>
### #&#8288;13 [Steel Browser](https://github.com/steel-dev/steel-browser) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: known (48) · Freshness: active (100) · Maintenance: fair (75) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.0k · Apache-2.0 · Nov 2026</sub>

**Self-hostable browser API that runs Chrome sessions for agents and scrapers.**

Steel runs managed Chrome instances behind a REST API and exposes them over CDP, so Puppeteer, Playwright or Selenium can connect. It handles sessions with persistent cookies and local storage, proxy chains, Chrome extensions, stealth and fingerprint settings. It also has quick endpoints for scrape, screenshot and PDF, and an experimental Commands API for snapshot-and-click agent control.

- **+** Connects with Puppeteer, Playwright or Selenium, plus Node and Python SDKs
- **+** Session state, proxy chains, extensions and stealth plugins are built in
- **+** /scrape, /screenshot and /pdf endpoints return page content, images or PDFs
- **+** Same SDKs work against Steel Cloud and self-hosted instances
- **−** README labels it public beta, so APIs may change
- **−** Commands API for agents is experimental and off by default
- **−** Selenium sessions do not support all CDP session features
- **−** Node.js run needs a local Chrome install at a known path

<sub>no GPU · Docker + Compose · Needs Chrome, Docker · port 3000 · [Repo](https://github.com/steel-dev/steel-browser) · [📖 Docs ↗](https://docs.steel.dev/) · [🌐 Site ↗](https://steel.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/steel-browser/)</sub>

<a name="sandbox-runtime"></a>
### #&#8288;14 [sandbox-runtime](https://github.com/anthropics/sandbox-runtime) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: known (42) · Freshness: active (100) · Maintenance: fair (69) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · Apache-2.0 · Nov 2026</sub>

**OS-level filesystem and network sandbox for agents and arbitrary processes, no container.**

srt wraps any command in filesystem and network restrictions using sandbox-exec on macOS, bubblewrap on Linux, and a dedicated local user account with Windows Filtering Platform rules on Windows. Network traffic goes through host-side HTTP and SOCKS5 proxies that enforce domain allow and deny lists. It works as a CLI or a TypeScript library, and is aimed at sandboxing agents, local MCP servers and bash commands. It is labelled a beta research preview from Claude Code.

- **+** No container needed; uses native OS primitives on macOS, Linux and Windows
- **+** Deny-by-default network and write access, configured in ~/.srt-settings.json
- **+** Usable as CLI or library, with per-command allow lists and an ask callback
- **+** Config can be updated at runtime for network rules via --control-fd
- **−** Beta research preview; APIs and config formats may change
- **−** Reads are allowed everywhere by default unless denyRead is configured
- **−** Windows filters miss threads with swapped tokens and traffic carried by system services
- **−** Filesystem rules cannot change after the command starts

<sub>no GPU · Needs bubblewrap (Linux), sandbox-exec (macOS), Node.js/npm · [Repo](https://github.com/anthropics/sandbox-runtime) · [📖 Docs ↗](https://docs.claude.com/en/docs/claude-code/sandboxing) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sandbox-runtime/)</sub>

<a name="sandstorm"></a>
### #&#8288;15 [sandstorm](https://github.com/deeplethe/sandstorm) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: known (31) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.1k · Apache-2.0 · Nov 2026</sub>

**Sandbox host that pauses and snapshots idle gVisor or Firecracker sandboxes.**

Sandstorm is a Rust sandbox manager that runs gVisor containers or Firecracker microVMs, each with its own network namespace. Idle sandboxes move through frozen, snapshot and detached tiers and are woken by a gateway when a request arrives, so one machine can hold more sandboxes than it can run at once. A single binary, sandstormd, acts as master, node and web console, with desired state in SQLite.

- **+** Four-tier lifecycle: frozen wake about 0.1 s, snapshot restore about 0.2 s
- **+** Two backends in one fleet; gVisor needs no KVM
- **+** Single binary serves master, node and web console
- **+** Published benchmark methodology and raw results against CubeSandbox, Kata, Docker
- **−** Wakes that cannot start within 2 s are refused with a 503
- **−** Must be built from source with Rust and Node 22.12+
- **−** Linux with cgroup v2 only; Firecracker needs KVM or PVM
- **−** Master capacity reservation on placement is still unchecked on the roadmap

<sub>no GPU · Docker · Needs runsc (gVisor), Firecracker (optional backend), Linux cgroup v2, Rust, Node 22.12+, SQLite · port 8080 · [Repo](https://github.com/deeplethe/sandstorm) · [📖 Docs ↗](https://github.com/deeplethe/sandstorm/blob/main/docs/API.md) · [🌐 Site ↗](https://deeplethe.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sandstorm/)</sub>

<a name="open-terminal"></a>
### #&#8288;16 [Open Terminal](https://github.com/open-webui/open-terminal) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: niche (11) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.6k · MIT · Nov 2026</sub>

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

<a name="mxc"></a>
### #&#8288;17 [mxc](https://github.com/microsoft/mxc) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: niche (8) · Freshness: active (100) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.1k · MIT · Nov 2026</sub>

**Cross-platform sandbox SDK for running untrusted code from models and plugins.**

MXC is an embeddable SDK (Rust, .NET, Node) that launches untrusted workloads inside OS-level sandboxes or VMs, driven by JSON container requests with filesystem, network and UI policies. It picks a backend per platform: ProcessContainer on Windows, Bubblewrap on Linux, Seatbelt on macOS, with LXC, Hyperlight, WSLC and others as options. It also has an audit mode to help author policies.

- **+** Native backends on Windows, Linux and macOS behind one JSON request format
- **+** Separate filesystem, network and UI policies; Node sample sets egress default to deny
- **+** SDKs for Rust, .NET and Node, published on crates.io, NuGet and npm
- **+** Audit and debug modes help find access-denied failures when writing policy
- **−** Windows Sandbox, MicroVM, Hyperlight and IsolationSession backends are marked experimental
- **−** Official Microsoft builds send required telemetry on the 1.1.0-alpha contract
- **−** Network host filtering depends on the backend
- **−** macOS offers only the Seatbelt backend

<sub>no GPU · Needs Rust 1.93 (build from source), Node.js 24+ (build from source), Backend-specific tooling (Bubblewrap, LXC, WSLC) · [Repo](https://github.com/microsoft/mxc) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mxc/)</sub>

<a name="boxlite"></a>
### #&#8288;18 [boxlite](https://github.com/boxlite-ai/boxlite) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: niche (4) · Freshness: active (100) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.6k · Apache-2.0 · Nov 2026</sub>

**Embeddable micro-VM sandboxes that run OCI images for AI agents.**

BoxLite runs each sandbox ("Box") as a hardware-isolated micro-VM with its own kernel, booting any OCI image such as python:slim. It embeds as a library with no daemon or root, with SDKs for Python, Node.js, Go, Rust and C, plus a CLI and an optional REST server (`boxlite serve`). Boxes persist across stop/restart, and egress can be restricted with an allow-list.

- **+** Own kernel per box via KVM or Hypervisor.framework, plus seccomp/sandbox-exec layer
- **+** Daemonless library embed; also CLI, REST server and cloud deployment guides for AWS and GCP
- **+** Runs unmodified OCI images; boxes persist, can be cloned or exported as .boxlite archives
- **+** Egress allow-list and secret injection at host proxy keep real secrets out of the VM
- **−** Needs KVM on Linux; macOS limited to Apple Silicon, macOS 12+
- **−** Windows support only through WSL2 with KVM access
- **−** Go SDK requires CGO and Go 1.24+
- **−** Self-hosted cloud setup needs your own AWS account or GCP project

<sub>no GPU · Needs KVM (Linux), Hypervisor.framework (macOS), WSL2 (Windows) · port 8100 · [Repo](https://github.com/boxlite-ai/boxlite) · [🌐 Site ↗](https://boxlite.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/boxlite/)</sub>

<a name="browser-use-web-ui"></a>
### #&#8288;19 [Browser Use Web UI](https://github.com/browser-use/web-ui) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: popular (72) · Freshness: recent (55) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · MIT · May 2026</sub>

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
