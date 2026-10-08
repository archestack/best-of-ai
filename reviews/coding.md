# 💻 Coding — reviews

Self-hosted coding assistants and agents, from editor completion to autonomous task runners. Back to the [leaderboard](../README.md#-coding).

<a name="opencode"></a>
### 🥇 [opencode](https://github.com/anomalyco/opencode) <sub>⭐ 212k · MIT · Oct 2026</sub>

**Terminal coding agent with build and plan modes.**

Runs an AI coding agent in the terminal with two built-in agents: build (full access) and plan (read-only, asks before running bash), plus a general subagent for multi-step searches. Installs via a curl script, npm, Homebrew, Scoop, Chocolatey, pacman, mise or Nix, and ships a beta desktop app for macOS, Windows and Linux. For developers who want an open, configurable coding agent.

- **+** MIT license; installable from npm, Homebrew, Scoop, Chocolatey, pacman, mise and Nix
- **+** Plan agent denies file edits and asks before bash, for safe codebase exploration
- **+** Desktop app (beta) for macOS, Windows and Linux alongside the terminal UI
- **−** README covers install only; providers, config and server mode are in external docs
- **−** No Dockerfile or compose file in the repo
- **−** Desktop app is still beta

<sub>no GPU · [Repo](https://github.com/anomalyco/opencode) · [📖 Docs](https://opencode.ai/docs) · [🌐 Site](https://opencode.ai)</sub>

<a name="openhands"></a>
### 🥈 [OpenHands](https://github.com/OpenHands/OpenHands) <sub>⭐ 90k · MIT · Oct 2026</sub>

**Self-hosted control center for coding agents and automations.**

Web UI and local stack on port 8000 that runs the OpenHands agent or any ACP-compatible agent (Claude Code, Codex, Gemini) on local, Docker, VM or cloud backends. Automations fire on schedules or webhooks and connect to Slack, GitHub and Linear. Installs via npm (Node 24+, uv) or a Docker image, optionally one container per conversation, for teams running coding agents as a shared service.

- **+** Agent-agnostic through ACP: OpenHands, Claude Code, Codex, Gemini
- **+** Per-conversation Docker sandboxes via OH_CONVERSATION_RUNTIME=docker
- **+** Binds to loopback by default; LAN exposure needs an explicit flag and API key
- **+** Scheduled and webhook-driven automations with Slack, GitHub and Linear
- **−** Project status is beta; the Docker quickstart pins image tag 1.25.0
- **−** Non-sandboxed install gives the agent full access to the host filesystem
- **−** No Dockerfile or compose file in the repo; the image is prebuilt on ghcr.io
- **−** Spread across four repos (Canvas, SDK, TypeScript client, automation)

<sub>no GPU · Needs Node.js 24+, uv, Docker (sandbox modes) · Models: any LLM via LLM profiles, OpenHands agent, Claude Code, Codex, Gemini · port 8000 · [Repo](https://github.com/OpenHands/OpenHands) · [📖 Docs](https://docs.openhands.dev/openhands/usage/agent-canvas/backends)</sub>

<a name="screenshot-to-code"></a>
### 🥉 [screenshot-to-code](https://github.com/abi/screenshot-to-code) <sub>⭐ 80k · MIT · Jul 2026</sub>

**Turns screenshots and mockups into Tailwind, React or Vue code.**

Takes a screenshot, mockup, Figma export or screen recording and generates HTML with Tailwind or CSS, React, Vue, Bootstrap or Ionic code using Gemini 3, GPT-5.5 or Claude Opus models, with Replicate for image generation and background removal. Runs as a React/Vite frontend on port 5173 and a FastAPI backend on 7001, or via docker-compose. For developers prototyping UIs from designs.

- **+** Six output stacks including React, Vue, Bootstrap and Ionic with Tailwind
- **+** Video mode turns a screen recording into a working prototype (needs Gemini)
- **+** Optional headless Chromium lets the agent render and check its own output
- **+** docker-compose brings up frontend and backend with one env file
- **−** Requires at least one OpenAI, Anthropic or Gemini API key; no bundled local model
- **−** Ollama models are possible but the README calls the results poor quality
- **−** Replicate key must be set in backend/.env, not in the UI
- **−** Docker setup has no hot reload; file changes need a rebuild

<sub>no GPU · Compose · Needs OpenAI, Anthropic or Gemini API key, Replicate API key (optional), Playwright Chromium (optional preview) · Models: Gemini 3 Flash Preview, Gemini 3.1 Pro Preview, GPT-5.5, GPT-5.4 Mini, Claude Opus 4.6/4.8 · port 5173 · [Repo](https://github.com/abi/screenshot-to-code) · [🧪 Demo](https://screenshottocode.com/)</sub>

<a name="tabby"></a>
### 4 [Tabby](https://github.com/TabbyML/tabby) <sub>⭐ 34k · NOASSERTION · Jun 2026</sub>

**Self-hosted code completion and chat server for IDEs.**

Serves code completion and chat to VS Code, Vim and JetBrains extensions from one self-contained binary with no external database. Runs local models such as StarCoder-1B and Qwen2-1.5B-Instruct on CUDA or Apple Metal, exposes an OpenAPI interface on port 8080, and adds an Answer Engine, repository and GitLab merge-request indexing and LDAP auth. For teams that want an on-premises Copilot alternative.

- **+** Single binary with embedded storage; no DBMS or cloud service required
- **+** One docker run command starts a server with completion and chat models
- **+** Repository context indexing, GitHub and GitLab integration, LDAP auth, usage reports
- **+** Live demo instance and documented extensions for VS Code, Vim and IntelliJ
- **−** Last commit June 2026; recent news points to the separate Pochi agent
- **−** License is non-standard (GitHub reports NOASSERTION); check terms before deploying
- **−** Model list and hardware guidance live only in the external docs
- **−** Building from source needs Rust, protobuf and OpenBLAS

<sub>GPU optional · Models: StarCoder-1B, Qwen2-1.5B-Instruct, CodeLlama 7B, CodeGemma, CodeQwen · port 8080 · [Repo](https://github.com/TabbyML/tabby) · [🧪 Demo](https://tabby.tabbyml.com) · [📖 Docs](https://tabby.tabbyml.com/docs/welcome/)</sub>

<a name="onlook"></a>
### 5 [Onlook](https://github.com/onlook-dev/onlook) <sub>⭐ 27k · Apache-2.0 · Jul 2026</sub>

**Visual editor that edits Next.js and Tailwind apps with AI.**

Browser-based editor that loads a Next.js and Tailwind project into a web container, renders it in an iframe and maps DOM elements back to source so you can drag, restyle and edit visually or through an AI chat. Built on Next.js, tRPC, Supabase, Drizzle and the Vercel AI SDK with OpenRouter for models and CodeSandbox for sandboxes. For designers and front-end developers working on Next.js codebases.

- **+** Edits map directly to code; right-click any element to open its source location
- **+** Branching, checkpoints and a real-time code editor beside the visual canvas
- **+** Apache-2.0 with Dockerfile and compose file for local runs
- **+** Figma-like layers, pages, brand tokens and asset management
- **−** Next.js plus Tailwind only; other frameworks are roadmap items, not supported
- **−** Depends on hosted services: Supabase, OpenRouter, CodeSandbox SDK, Freestyle
- **−** Team comments, MCP support and image references are unchecked roadmap items
- **−** Maintainers are moving to a hosted early-access product; last commit July 2026

<sub>no GPU · Docker + Compose · Needs Supabase (auth, database, storage), OpenRouter API key, CodeSandbox SDK, Bun · Models: OpenRouter-hosted models, Morph Fast Apply, Relace · [Repo](https://github.com/onlook-dev/onlook) · [🧪 Demo](https://onlook.com) · [📖 Docs](https://docs.onlook.com)</sub>

<a name="archon"></a>
### 6 [Archon](https://github.com/coleam00/Archon) <sub>⭐ 24k · MIT · Oct 2026</sub>

**YAML workflow engine that runs coding agents in isolated worktrees.**

Defines development processes (plan, implement, validate, review, PR) as YAML workflows and runs them through Claude Code, Codex or Pi, each run in its own git worktree. Deterministic nodes mix with AI nodes and human approval gates; runs start from the CLI, a web console, Slack, Telegram, Discord or GitHub webhooks, with state in SQLite or PostgreSQL. For teams standardizing how agents ship code.

- **+** Every run isolated in a git worktree; parallel fixes without conflicts
- **+** Bundled sdlc pack: ship, triage, investigate, plan, deliver, review, validate, upkeep
- **+** Adapters for web, CLI, Slack, Telegram, Discord and GitHub webhooks
- **+** Telemetry documented field by field; DO_NOT_TRACK=1 or CI=true disables it
- **−** Requires Claude Code (or Codex, Pi) installed separately; binaries need CLAUDE_BIN_PATH
- **−** Anonymous telemetry is on by default
- **−** x64 quick-install binaries require AVX2; older CPUs must build from source
- **−** Workflows from v0.11.1 and earlier no longer ship and must be copied manually

<sub>no GPU · Docker + Compose · Needs Bun, Claude Code (or Codex or Pi), GitHub CLI, SQLite or PostgreSQL · Models: Claude Code, Codex, Pi · [Repo](https://github.com/coleam00/Archon) · [📖 Docs](https://archon.diy/docs/)</sub>

<a name="openchamber"></a>
### 7 [OpenChamber](https://github.com/openchamber/openchamber) <sub>⭐ 11k · MIT · Oct 2026</sub>

**Multi-device workspace for running and reviewing OpenCode agent sessions.**

Front end over the OpenCode CLI that starts agent sessions, shows diffs and takes changes through review from desktop (macOS, Windows, Linux), web/PWA, VS Code, iOS and Android. Adds Session Goals that keep an agent iterating toward an outcome, Multi-run to compare up to five models, GitHub issue and PR context, scheduled prompts and encrypted remote access via Private Relay. For developers who run OpenCode.

- **+** Multi-run compares up to five models; Fusion merges the strongest parts
- **+** Private Relay pairs devices by QR code without opening ports; end-to-end encrypted
- **+** Desktop builds bundle the matching OpenCode CLI
- **+** Scheduled tasks with Session Goals continue until done, blocked or capped
- **−** Tied to OpenCode; no other agent runtime
- **−** CLI and Web need Node.js 22+ and a separately installed OpenCode CLI
- **−** Linux AppImages need FUSE (libfuse.so.2) or APPIMAGE_EXTRACT_AND_RUN=1
- **−** Port and reverse-proxy details are in separate docs, not the README

<sub>no GPU · Docker + Compose · Needs OpenCode CLI (bundled in desktop builds), Node.js 22+ (CLI and Web) · Models: models available through OpenCode · [Repo](https://github.com/openchamber/openchamber)</sub>

<a name="open-swe"></a>
### 8 [Open SWE](https://github.com/langchain-ai/open-swe) <sub>⭐ 11k · MIT · Oct 2026</sub>

**LangChain coding agent that plans, implements and reviews pull requests.**

LangGraph-based agent that investigates a repository, implements changes in a per-thread Linux sandbox, validates them and opens a pull request, then reviews PRs and watches CI with /baby-sit. Work starts from a dashboard, GitHub issues or PR comments, Slack or Linear. Deploys into your infrastructure with a backend, dashboard, GitHub and Slack apps, for teams building an internal coding-agent service.

- **+** Covers build, review, investigate and operate flows, with subagents for parallel work
- **+** Durable execution and thread state via LangGraph; sandboxes persist per thread
- **+** Configurable models, reasoning effort, skills, MCP integrations and sandbox providers
- **+** Push approvals gate detected git pushes; PR chat excludes mutation tools
- **−** Production standalone Agent Server deployments require a license key
- **−** Maintainers are not accepting issues or contributions; breaking changes expected
- **−** LangSmith is the default sandbox and tracing provider; alternatives need configuration
- **−** CLI mode executes commands locally as you, with no sandbox isolation

<sub>no GPU · Docker + Compose · Needs LangSmith (default sandbox and tracing), GitHub App, Slack app (optional), model provider credentials · Models: configurable LLM providers · [Repo](https://github.com/langchain-ai/open-swe)</sub>

<a name="background-agents"></a>
### 9 [Background Agents](https://github.com/ColeMurray/background-agents) <sub>⭐ 3.3k · MIT · Oct 2026</sub>

**Background coding agents on cloud sandboxes with Slack, GitHub and Linear triggers.**

Runs coding sessions in cloud sandboxes coordinated by a Cloudflare Workers control plane, driven from a web UI, Slack, GitHub PR comments, Linear issues or webhooks. Sessions use OpenCode or the Claude Agent harness with Anthropic, OpenAI, xAI, DeepSeek or Z.AI models, with multiplayer editing, commit attribution, child sessions and cron or event automations. For single-tenant engineering orgs.

- **+** Snapshot restore, prebuilt images and proactive warming for fast session starts
- **+** Automations from cron, Sentry alerts, GitHub workflow runs and inbound webhooks
- **+** Secrets encrypted with AES-256-GCM and scoped globally, per repo or per environment
- **+** Browser automation, code-server and a web terminal inside each sandbox
- **−** Single-tenant only; all users must be trusted members of one organization
- **−** Control plane requires Cloudflare Workers, Durable Objects and D1
- **−** Sandboxes run on third-party providers (Modal, Daytona, E2B, OpenComputer, Vercel)
- **−** Cached credentials can persist in snapshots; grant removal does not revoke tokens

<sub>no GPU · Compose · Needs Cloudflare Workers, Durable Objects and D1, Sandbox provider (Modal, Daytona, E2B, OpenComputer or Vercel Sandbox), GitHub App, Slack and Linear apps (optional) · Models: Anthropic Claude (API key or subscription), OpenAI Codex via ChatGPT subscription, xAI Grok via SuperGrok, OpenCode Zen and Go, Z.AI Coding Plan · [Repo](https://github.com/ColeMurray/background-agents)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-selfhosted-ai/issues/new/choose).</sub>
