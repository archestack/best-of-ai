# 🔁 Workflow automation with AI reviews · Best of Open-Source AI

Workflow and integration platforms with AI steps or agent nodes, for wiring models into the rest of your tools. Back to the [leaderboard](../README.md#-workflow-automation-with-ai).

<sub>🌐 Also on the web: [Workflow automation with AI on archestack.com](https://archestack.com/best-of-ai/automation/), each project on its own page.</sub>

<a name="n8n"></a>
### 🥇 [n8n](https://github.com/n8n-io/n8n) <sub>score [94](../README.md#-how-we-rank "Score 94/100. Adoption: widely used (100) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 209k · custom license · Oct 2026</sub>

**Visual workflow automation with AI agent nodes and 1500+ integrations.**

n8n is a node-based canvas for building workflows and multi-step AI agents, with JavaScript, Python and npm packages usable inside nodes. It connects to OpenAI, Anthropic, Google and open-source models, and lists 1500+ integrations and 9,000+ workflow templates. It runs self-hosted or on n8n Cloud, under the Sustainable Use License rather than an OSI license.

- **+** 1500+ integrations and 9,000+ templates cover most common SaaS wiring
- **+** Visual canvas with JavaScript, Python and npm code when needed
- **+** Model-agnostic: OpenAI, Anthropic, Google or open-source models
- **+** Supports human approvals and observability for multi-step AI workflows
- **−** Fair-code Sustainable Use License, not OSI open source; use is restricted
- **−** Role-based access and audit trails fall under the Enterprise License
- **−** RAM and CPU requirements are not stated in the README
- **−** Documented quick start requires Docker

<sub>no GPU · Needs Docker · Models: OpenAI, Anthropic, Google, open-source models · port 5678 · [Repo](https://github.com/n8n-io/n8n) · [📖 Docs ↗](https://docs.n8n.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/n8n/)</sub>

<a name="frigate"></a>
### 🥈 [frigate](https://github.com/blakeblackshear/frigate) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 37k · MIT · Oct 2026</sub>

**Local NVR with realtime object detection for IP cameras.**

Frigate is a network video recorder that runs object detection locally on IP camera streams using OpenCV and TensorFlow. It uses low-overhead motion detection to decide where to run detection, records video with retention based on detected objects, and re-streams over RTSP. It integrates with Home Assistant through a custom component and publishes events over MQTT.

- **+** Runs detection only where motion is found, which limits CPU use
- **+** Retention rules based on detected objects, plus 24/7 recording
- **+** RTSP re-streaming, plus WebRTC and MSE for low-latency live view
- **+** MQTT and a Home Assistant custom component for integration
- **−** README strongly recommends a GPU or AI accelerator for detection
- **−** Tightly oriented to Home Assistant; other setups rely on MQTT
- **−** Hardware requirements and RAM figures are not given in the README
- **−** Frigate name and logo are trademarks excluded from the MIT license

<sub>GPU optional · Docker + Compose · Needs MQTT, Home Assistant (optional), IP cameras (RTSP) · Models: TensorFlow · [Repo](https://github.com/blakeblackshear/frigate) · [📖 Docs ↗](https://docs.frigate.video) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/frigate/)</sub>

<a name="activepieces"></a>
### 🥉 [Activepieces](https://github.com/activepieces/activepieces) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · custom license · Oct 2026</sub>

**Self-hosted workflow automation with TypeScript integrations, alternative to Zapier.**

Activepieces is a no-code workflow builder with loops, branches, auto retries, HTTP calls and npm-backed code steps, and flows are versioned. Integrations are called pieces: TypeScript npm packages, 280+ of which are exposed as MCP servers for Claude Desktop, Cursor or Windsurf. It also has AI pieces for several providers, human-in-the-loop approvals, and chat and form triggers.

- **+** Pieces are open-source TypeScript npm packages with hot reloading for local development
- **+** 280+ pieces usable as MCP servers from Claude Desktop, Cursor or Windsurf
- **+** Flows are versioned and support loops, branches and auto retries
- **+** Built-in approval, delay, chat and form triggers for human-in-the-loop flows
- **−** Enterprise features sit under a separate commercial license, not MIT
- **−** README does not state RAM, CPU or database requirements
- **−** Automation-first; AI agents are one feature rather than the core design
- **−** README claims of 200+ and 280+ pieces are inconsistent

<sub>no GPU · Docker + Compose · Compose runs PostgreSQL, Redis · Models: OpenAI · [Repo](https://github.com/activepieces/activepieces) · [📖 Docs ↗](https://www.activepieces.com/docs) · [🌐 Site ↗](https://activepieces.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/activepieces/)</sub>

<a name="banana-slides"></a>
### #&#8288;4 [banana-slides](https://github.com/anionex/banana-slides) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: niche (27) · Freshness: active (93) · Maintenance: healthy (98) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · AGPL-3.0 · Oct 2026</sub>

**AI slide deck generator that exports PPTX, PDF and narrated video.**

Banana Slides generates presentations from a topic, outline, page descriptions or uploaded PDF/Docx/MD/Txt files, rendering each page as an image with image-generation models such as Nano Banana Pro. Pages can be edited by natural-language instructions or box selection, and exported as PPTX, PDF, editable PPTX (beta) or an MP4 with TTS narration. It runs as a Flask backend plus a web frontend and needs an API key for a text/image provider.

- **+** Several providers: Gemini, OpenAI-format, Volcengine, Vertex AI and LazyLLM vendors like Qwen and DeepSeek
- **+** Exports PPTX, PDF, editable PPTX (beta) and narrated MP4 with subtitles
- **+** Edit pages by natural-language prompt or box selection; per-page templates supported
- **+** Prebuilt Docker Hub images with a docker-compose.prod.yml, plus a CLI and agent skills
- **−** AGPL-3.0 license restricts use in closed-source hosted services
- **−** Needs paid external image-generation API; README warns Nano Banana Pro calls are costly
- **−** Editable PPTX export is beta; better results need a Baidu API key
- **−** README is mostly Chinese; desktop build is at release-candidate stage (v0.9.0-rc.7)

<sub>no GPU · Docker + Compose · Needs Gemini/OpenAI/Volcengine/Vertex or LazyLLM API key, FFmpeg with libass (video export), LibreOffice (optional, PPTX upload), Baidu API key (optional, editable export) · Models: Gemini (Nano Banana Pro), OpenAI-compatible (gpt-image-2), Volcengine Doubao/Seedream, Vertex AI, LazyLLM vendors (Qwen, DeepSeek, GLM, Kimi, MiniMax, SiliconFlow) · port 3011 · [Repo](https://github.com/anionex/banana-slides) · [▶️ Demo ↗](https://bananaslides.online/) · [📖 Docs ↗](https://docs.bananaslides.online/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/banana-slides/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
