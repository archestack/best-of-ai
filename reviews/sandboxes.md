# 🛡️ Sandboxes reviews · Best of Self-Hosted AI

Isolated runtimes where agents execute code, browse or use tools safely. Back to the [leaderboard](../README.md#%EF%B8%8F-sandboxes).

<a name="lightpanda"></a>
### 🥇 [Lightpanda](https://github.com/lightpanda-io/browser) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: healthy (91) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · AGPL-3.0 · Oct 2026</sub>

**Headless browser in Zig with CDP, MCP and an agent mode.**

Browser engine written in Zig (V8, libcurl, html5ever) with no graphical renderer. Exposes a CDP server on port 9222 for Puppeteer and Playwright plus WebDriver BiDi, a fetch command that dumps HTML, markdown, PNG or PDF, an MCP server over stdio or HTTP with per-client sessions, and an agent mode driven by Anthropic, OpenAI, Gemini, Ollama, llama.cpp or any OpenAI-compatible endpoint. For scraping and agent fleets where Chrome is too heavy.

- **+** 100 pages: 123 MB and 5 s versus 2 GB and 46 s for Chrome
- **+** CDP and WebDriver BiDi servers work with existing Puppeteer and Playwright scripts
- **+** Agent mode records deterministic PandaScript JS you can replay without an LLM
- **+** MCP over HTTP isolates each client in its own browsing session
- **−** No graphical rendering engine; PNG and PDF dumps are text-only renderings
- **−** Nightly builds only via Homebrew, AUR and GitHub releases; no native Windows binary
- **−** Usage telemetry on by default; set LIGHTPANDA_DISABLE_TELEMETRY=true
- **−** AGPL-3.0 license and a CLA for contributions

<sub>no GPU · Docker · Models: Anthropic, OpenAI, Gemini, Google Vertex AI, Mistral · port 9222 · [Repo](https://github.com/lightpanda-io/browser) · [📖 Docs ↗](https://lightpanda.io/docs/usage/agent) · [🌐 Site ↗](https://lightpanda.io)</sub>

<a name="obscura"></a>
### 🥈 [Obscura](https://github.com/h4ckf0r0day/obscura) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: healthy (91) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Oct 2026</sub>

**Rust headless browser with CDP, native rendering and stealth mode.**

Headless browser engine in Rust running V8 that speaks the Chrome DevTools Protocol, so Puppeteer and Playwright connect on port 9222 as if to Chrome. Ships its own layout and paint engine for screenshots, screencasts and PDF export, a stealth build with per-session fingerprint randomization, a parallel scrape command and an MCP server. Claims 30 MB memory and 85 ms page loads against 200+ MB and about 500 ms for Chrome.

- **+** Single binary around 70 MiB, no Chrome or Node.js; distroless Docker image about 57 MB
- **+** Stealth build randomizes fingerprints per session and blocks 3,520 tracker domains
- **+** SSRF protection blocks private IPs by default; CDP token on the Docker image
- **+** Fetch.takeResponseBodyAsStream and IO.read stream large downloads in chunks
- **−** Independent rendering engine; long-tail CSS, media playback and fonts can differ from Chromium
- **−** Stealth builds need CMake, Clang and libclang; first source build takes about 5 minutes
- **−** README carries heavy proxy-vendor sponsorship and discount codes
- **−** Linux binaries target glibc 2.35 or newer (Ubuntu 22.04)

<sub>no GPU · Docker · port 9222 · [Repo](https://github.com/h4ckf0r0day/obscura) · [📖 Docs ↗](https://docs.obscura.sh) · [🌐 Site ↗](https://obscura.sh)</sub>

<a name="nemoclaw"></a>
### 🥉 [NemoClaw](https://github.com/nvidia/nemoclaw) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: fair (76) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · Apache-2.0 · Oct 2026</sub>

**NVIDIA reference stack running OpenClaw and Hermes inside OpenShell sandboxes.**

CLI and installer that provision OpenShell sandboxes for OpenClaw (default), Hermes or LangChain Deep Agents Code, with guided onboarding, inference provider selection, baseline network policies with operator approval, managed integrations and persistent sandbox state. Express install targets DGX hosts and Windows WSL; a starter prompt lets Cursor, Claude Code or Codex drive setup. For personal agents with kernel-enforced isolation.

- **+** Three supported agents: OpenClaw, Hermes, LangChain Deep Agents Code
- **+** Network policy with operator approval flow and egress control from OpenShell
- **+** Express preset install on DGX and WSL hosts
- **+** Documented sandbox hardening: capability drops and process limits
- **−** Alpha project; maintainers review issues without guaranteed response times
- **−** Depends on OpenShell as the runtime; details live in NVIDIA docs, not the README
- **−** README is mostly links; no architecture or resource figures in the repo itself
- **−** Supported platforms are limited to those on the prerequisites page

<sub>no GPU · Docker · Needs NVIDIA OpenShell, Inference provider (local or routed) · Models: providers configured through OpenShell routed inference · [Repo](https://github.com/nvidia/nemoclaw) · [📖 Docs ↗](https://docs.nvidia.com/nemoclaw/latest/)</sub>

<a name="openshell"></a>
### #&#8288;4 [OpenShell](https://github.com/nvidia/openshell) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: known (44) · Freshness: active (100) · Maintenance: healthy (88) · Easy to run: easy (50) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Oct 2026</sub>

**Policy-enforced sandbox runtime for autonomous agents with credential brokering.**

Runs each agent in a sandbox with kernel-enforced limits on file access and system calls; every outbound connection passes a policy check, and agents never see real credentials, which a gateway injects only for approved endpoints. Policy changes are checked with formal verification before approval. Installs via a shell script on Linux, Apple Silicon macOS or WSL 2; Helm for Kubernetes; SDKs for Python, TypeScript, Go and Rust.

- **+** Credentials attached by the gateway only to approved endpoints; sandboxes never hold them
- **+** Formal verification flags risky new access before a policy change is applied
- **+** Kubernetes deployment via Helm; GPU use inside sandboxes documented
- **+** Python, TypeScript, Go and Rust SDKs plus agent skills via npx skills add
- **−** Windows support is WSL 2 only and experimental
- **−** Default sandbox image is minimal Ubuntu with no agent; running one follows the docs walkthrough
- **−** Anonymous telemetry on by default; disable with OPENSHELL_TELEMETRY_ENABLED=false
- **−** Kubernetes installs require a CNI that enforces NetworkPolicy

<sub>no GPU · Docker + Compose · Needs Docker, Podman or host virtualization · Models: any provider via routed inference credentials · [Repo](https://github.com/nvidia/openshell) · [📖 Docs ↗](https://docs.nvidia.com/openshell/latest/index.html)</sub>

<a name="microsandbox"></a>
### #&#8288;5 [microsandbox](https://github.com/superradcompany/microsandbox) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (30) · Freshness: active (100) · Maintenance: healthy (86) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.6k · Apache-2.0 · Oct 2026</sub>

**Local microVMs for untrusted code with fork, snapshot and SDKs.**

Boots OCI images as hardware-isolated microVMs in under 100 ms on Linux with KVM, Apple Silicon macOS or Windows with WHP, driven by the msb CLI or embedded via TypeScript, Rust, Python, Go and Ruby SDKs with no daemon. Running sandboxes fork live or snapshot and restore; network access is allow-listed per host and secrets are injected only toward an allowed host. For agent-generated code, CI jobs and plugins.

- **+** Sub-100 ms average boot; sandboxes spawn as child processes of your app
- **+** Live fork and full snapshot restore with copy-on-write memory
- **+** Per-sandbox network allow-lists and secrets scoped to one host
- **+** MCP server and agent skills let coding agents create their own sandboxes
- **−** Beta software; breaking changes and missing features expected
- **−** Needs KVM on Linux, Apple Silicon on macOS or WHP on Windows; no Intel Mac
- **−** No Dockerfile or compose file; it replaces containers rather than running in one
- **−** Image pulls on first create add startup time

<sub>no GPU · Docker · Needs KVM (Linux), Apple Silicon (macOS) or WHP (Windows) · [Repo](https://github.com/superradcompany/microsandbox) · [📖 Docs ↗](https://docs.microsandbox.dev/cli/overview)</sub>

<a name="steel-browser"></a>
### #&#8288;6 [Steel Browser](https://github.com/steel-dev/steel-browser) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: patchy (42) · Easy to run: very easy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.8k · Apache-2.0 · Oct 2026</sub>

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

<sub>no GPU · Docker + Compose · Needs Google Chrome (non-Docker runs), Node.js (non-Docker runs) · port 3000 · [Repo](https://github.com/steel-dev/steel-browser) · [📖 Docs ↗](https://docs.steel.dev/) · [🌐 Site ↗](https://steel.dev)</sub>

<a name="browser-use-web-ui"></a>
### #&#8288;7 [Browser Use Web UI](https://github.com/browser-use/web-ui) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: popular (52) · Freshness: recent (67) · Maintenance: weak (0) · Easy to run: easy (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · MIT · May 2026</sub>

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

<sub>no GPU · Docker + Compose · Needs Playwright browsers, LLM API key or Ollama, Chrome (optional, own-browser mode) · Models: Google, OpenAI, Azure OpenAI, Anthropic, DeepSeek · port 7788 · [Repo](https://github.com/browser-use/web-ui) · [📖 Docs ↗](https://docs.browser-use.com)</sub>

<a name="open-terminal"></a>
### #&#8288;8 [Open Terminal](https://github.com/open-webui/open-terminal) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: niche (5) · Freshness: active (100) · Maintenance: fair (70) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · MIT · Sep 2026</sub>

**REST-driven shell and file sandbox for AI agents, from Open WebUI.**

Container or pip package exposing a shell and file management over a REST API with an API key on port 8000, so agents can run commands and code. The latest image (about 4 GB) bundles Python, Node.js, gcc, ffmpeg, LibreOffice, LaTeX and the Docker CLI behind an egress firewall; slim (430 MB) and alpine (230 MB) variants keep git, curl and jq. Integrates with Open WebUI as a terminal with a file sidebar.

- **+** API key auto-generated if unset; interactive API docs at /docs
- **+** Extra apt, pip and npm packages installed at startup via env vars
- **+** Four image variants from 230 MB alpine to a 4 GB full toolkit
- **+** Office previews: DOCX and PPTX rendered to PDF when LibreOffice is present
- **−** Multi-user mode shares one container and is explicitly not a security boundary
- **−** Per-user isolation requires Terminals, which needs an Open WebUI Enterprise license
- **−** Mounting the Docker socket gives the container root-equivalent host access
- **−** Bare-metal mode runs commands directly as your user with no sandbox

<sub>no GPU · Docker · port 8000 · [Repo](https://github.com/open-webui/open-terminal)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-selfhosted-ai/issues/new/choose).</sub>
