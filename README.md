<p align="center"><img src="https://github.com/archestack.png" width="88" alt="Archestack" /></p>
<h1 align="center">Best of Self-Hosted AI</h1>
<p align="center"><strong>🏆 The leaderboard of self-hosted AI: apps you can run on your own server, ranked.</strong></p>
<p align="center">
  <img alt="projects" src="https://img.shields.io/badge/projects-159-5ac4bf" />
  <img alt="categories" src="https://img.shields.io/badge/categories-14-5ac4bf" />
  <img alt="updated" src="https://img.shields.io/badge/updated-2026-10-08-success" />
  <img alt="data" src="https://img.shields.io/badge/data-CC%20BY%204.0-lightgrey" />
</p>
<p align="center">🤖 found, checked and written by bots &nbsp;·&nbsp; ✍️ every entry states strengths and weaknesses &nbsp;·&nbsp; 🧪 demo and docs links where they exist</p>
<p align="center">Looking for starters and templates to build your own AI app? 👉 <a href="https://github.com/archestack/best-of-ai-starters"><b>Best of AI Starters</b></a></p>

---

## 🏆 Top 10

| # | Project | Category | ⭐ | 🔗 |
|:-:|---|---|--:|---|
| 🥇 | **[OpenClaw](https://github.com/openclaw/openclaw)**<br><sub>Personal assistant gateway that answers in Discord, Slack, WhatsApp and Telegram</sub> | 🤖 [Assistants](#-assistants) | 392k | [📝](reviews/assistants.md#openclaw) [📖](https://docs.openclaw.ai "Docs") [🌐](https://openclaw.ai "Website") |
| 🥈 | **[Hermes Agent](https://github.com/NousResearch/hermes-agent)**<br><sub>Terminal and chat-app agent that writes its own skills and remembers you</sub> | 🤖 [Assistants](#-assistants) | 252k | [📝](reviews/assistants.md#hermes-agent) [📖](https://hermes-agent.nousresearch.com/docs/ "Docs") [🌐](https://hermes-agent.nousresearch.com/ "Website") |
| 🥉 | **[opencode](https://github.com/anomalyco/opencode)**<br><sub>Terminal coding agent with build and plan modes</sub> | 💻 [Coding](#-coding) | 212k | [📝](reviews/coding.md#opencode) [📖](https://opencode.ai/docs "Docs") [🌐](https://opencode.ai "Website") |
| 4 | **[n8n](https://github.com/n8n-io/n8n)**<br><sub>Visual workflow automation with code steps, AI agent nodes and 1500+ integrations</sub> | 🧩 [Agent platforms](#-agent-platforms) | 207k | [📝](reviews/agent-platforms.md#n8n) [📖](https://docs.n8n.io "Docs") |
| 5 | **[Firecrawl](https://github.com/firecrawl/firecrawl)**<br><sub>Web scraping and crawling API that returns LLM-ready markdown</sub> | 🔎 [Search](#-search) | 190k | [📝](reviews/search.md#firecrawl) [🧪](https://firecrawl.dev/playground "Live demo") [📖](https://docs.firecrawl.dev "Docs") [🌐](https://firecrawl.dev "Website") |
| 6 | **[AutoGPT](https://github.com/Significant-Gravitas/AutoGPT)**<br><sub>Block-based builder for agents that run on demand, schedule or trigger</sub> | 🧩 [Agent platforms](#-agent-platforms) | 188k | [📝](reviews/agent-platforms.md#autogpt) [🧪](https://platform.agpt.co/tour "Live demo") [📖](https://docs.agpt.co "Docs") |
| 7 | **[Ollama](https://github.com/ollama/ollama)**<br><sub>Runs open-weight models locally behind a CLI and REST API</sub> | 🧠 [Model serving](#-model-serving) | 183k | [📝](reviews/model-serving.md#ollama) [📖](https://docs.ollama.com/quickstart "Docs") [🌐](https://ollama.com "Website") |
| 8 | **[Dify](https://github.com/langgenius/dify)**<br><sub>Visual LLM app platform with workflows, RAG pipeline, agents and APIs</sub> | 🧩 [Agent platforms](#-agent-platforms) | 158k | [📝](reviews/agent-platforms.md#dify) [🧪](https://cloud.dify.ai "Live demo") [📖](https://docs.dify.ai "Docs") [🌐](https://dify.ai "Website") |
| 9 | **[Langflow](https://github.com/langflow-ai/langflow)**<br><sub>Visual flow builder that deploys agents as APIs or MCP servers</sub> | 🧩 [Agent platforms](#-agent-platforms) | 156k | [📝](reviews/agent-platforms.md#langflow) [📖](https://docs.langflow.org/get-started-installation "Docs") [🌐](https://langflow.org "Website") |
| 10 | **[Open WebUI](https://github.com/open-webui/open-webui)**<br><sub>Self-hosted chat UI for Ollama and OpenAI-compatible APIs with RBAC and RAG</sub> | 💬 [Chat UIs](#-chat-uis) | 154k | [📝](reviews/chat-ui.md#open-webui) [📖](https://docs.openwebui.com/ "Docs") [🌐](https://openwebui.com "Website") |

<sub>Ranked by stars for now; a score that weighs maintenance, deployability and verified builds is on the way.</sub>

## 🗂️ Contents

- 🤖 [Assistants](#-assistants) · 11
- 💬 [Chat UIs](#-chat-uis) · 13
- 🧩 [Agent platforms](#-agent-platforms) · 12
- 📚 [RAG and knowledge](#-rag-and-knowledge) · 15
- 🧠 [Model serving](#-model-serving) · 18
- 🔀 [Gateways](#-gateways) · 13
- 🗂️ [Memory](#-memory) · 11
- 🎙️ [Voice](#-voice) · 11
- 🎨 [Image and video](#-image-and-video) · 8
- 💻 [Coding](#-coding) · 9
- 🔎 [Search](#-search) · 8
- 📈 [Observability](#-observability) · 13
- 🧮 [Vector databases](#-vector-databases) · 9
- 🛡️ [Sandboxes](#-sandboxes) · 8

<sub>Legend: 🥇🥈🥉 top three of a category · ⭐ GitHub stars · 📝 review (strengths, weaknesses, specs) · 🧪 live demo · 📖 docs · 🌐 website · 🐳 Docker image or compose · 🎮 GPU required · ✨ GPU optional</sub>

## 🤖 Assistants

Personal AI assistants you run yourself and talk to through chat apps, with memory and the ability to act. <sub>11 projects · [📝 all reviews](reviews/assistants.md)</sub>

| # | Project | ⭐ | 📄 | 🚀 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[OpenClaw](https://github.com/openclaw/openclaw)**<br><sub>Personal assistant gateway that answers in Discord, Slack, WhatsApp and Telegram</sub> | 392k | MIT | 🐳 | [📝](reviews/assistants.md#openclaw) [📖](https://docs.openclaw.ai "Docs") [🌐](https://openclaw.ai "Website") |
| 🥈 | **[Hermes Agent](https://github.com/NousResearch/hermes-agent)**<br><sub>Terminal and chat-app agent that writes its own skills and remembers you</sub> | 252k | MIT | 🐳 | [📝](reviews/assistants.md#hermes-agent) [📖](https://hermes-agent.nousresearch.com/docs/ "Docs") [🌐](https://hermes-agent.nousresearch.com/ "Website") |
| 🥉 | **[nanobot](https://github.com/HKUDS/nanobot)**<br><sub>Small Python agent runtime with bundled WebUI, TUI and chat channels</sub> | 49k | MIT | 🐳 | [📝](reviews/assistants.md#nanobot) [📖](https://nanobot.wiki/docs/latest/getting-started/nanobot-overview "Docs") |
| 4 | **[AstrBot](https://github.com/AstrBotDevs/AstrBot)**<br><sub>Chatbot platform bridging LLMs to QQ, Telegram, Discord, Slack and more</sub> | 42k | AGPL-3.0 | 🐳 | [📝](reviews/assistants.md#astrbot) [📖](https://astrbot.app/ "Docs") |
| 5 | **[Khoj](https://github.com/khoj-ai/khoj)**<br><sub>Personal assistant that chats with your documents and the web</sub> | 38k | AGPL-3.0 | 🐳 | [📝](reviews/assistants.md#khoj) [🧪](https://app.khoj.dev "Live demo") [📖](https://docs.khoj.dev "Docs") [🌐](https://khoj.dev "Website") |
| 6 | **[QwenPaw](https://github.com/agentscope-ai/QwenPaw)**<br><sub>AgentScope-based personal assistant with local Qwen models and chat channels</sub> | 35k | Apache-2.0 | 🐳 | [📝](reviews/assistants.md#qwenpaw) [🧪](https://platform.agentscope.io/ "Live demo") [📖](https://qwenpaw.agentscope.io/ "Docs") |
| 7 | **[ZeroClaw](https://github.com/zeroclaw-labs/zeroclaw)**<br><sub>Single Rust binary agent runtime with 30+ channels and hardware access</sub> | 33k | Apache-2.0 | 🐳 | [📝](reviews/assistants.md#zeroclaw) [📖](https://docs.zeroclaw.com/master/en/introduction.html "Docs") [🌐](https://www.zeroclaw.com "Website") |
| 8 | **[PicoClaw](https://github.com/sipeed/picoclaw)**<br><sub>Go assistant agent that runs in under 20 MB on $10 boards</sub> | 30k | MIT | – | [📝](reviews/assistants.md#picoclaw) [📖](https://docs.picoclaw.io/ "Docs") [🌐](https://picoclaw.io "Website") |
| 9 | **[IronClaw](https://github.com/nearai/ironclaw)**<br><sub>Rust assistant that sandboxes every untrusted tool in WebAssembly</sub> | 13k | Apache-2.0 | 🐳 | [📝](reviews/assistants.md#ironclaw) |
| 10 | **[Moltis](https://github.com/moltis-org/moltis)**<br><sub>Persistent personal agent server in one Rust binary with sandboxed execution</sub> | 2.9k | MIT | 🐳 | [📝](reviews/assistants.md#moltis) [📖](https://docs.moltis.org/quickstart.html "Docs") [🌐](https://moltis.org "Website") |
| 11 | **[Spacebot](https://github.com/spacedriveapp/spacebot)**<br><sub>Multi-user agent harness for Discord, Slack and Telegram communities</sub> | 2.4k | NOASSERTION | 🐳 | [📝](reviews/assistants.md#spacebot) [📖](https://docs.spacebot.sh "Docs") [🌐](https://spacebot.sh "Website") |

<details><summary>💡 How to choose</summary>

- Check which channels it supports today (WhatsApp, Telegram, Slack, Discord, email) and whether each needs a paid API.
- Look at how memory is stored and whether you can inspect or wipe it.
- Actions need credentials; prefer assistants that scope them per tool.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 💬 Chat UIs

Web front-ends for local or API models, usually with user accounts, chat history and file upload. <sub>13 projects · [📝 all reviews](reviews/chat-ui.md)</sub>

| # | Project | ⭐ | 📄 | 🚀 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[Open WebUI](https://github.com/open-webui/open-webui)**<br><sub>Self-hosted chat UI for Ollama and OpenAI-compatible APIs with RBAC and RAG</sub> | 154k | NOASSERTION | 🐳 ✨ | [📝](reviews/chat-ui.md#open-webui) [📖](https://docs.openwebui.com/ "Docs") [🌐](https://openwebui.com "Website") |
| 🥈 | **[NextChat](https://github.com/ChatGPTNextWeb/NextChat)**<br><sub>Lightweight Next.js chat client for OpenAI, Claude, Gemini and DeepSeek APIs</sub> | 89k | MIT | 🐳 | [📝](reviews/chat-ui.md#nextchat) [🧪](https://app.nextchat.club "Live demo") [🌐](https://nextchat.club "Website") |
| 🥉 | **[LobeHub](https://github.com/lobehub/lobehub)**<br><sub>Agent workspace with builder, groups, scheduling and 10,000+ MCP skills</sub> | 83k | NOASSERTION | 🐳 | [📝](reviews/chat-ui.md#lobehub) |
| 4 | **[AnythingLLM](https://github.com/Mintplex-Labs/anything-llm)**<br><sub>Document chat and agent app with built-in RAG, MCP and multi-user support</sub> | 67k | MIT | – | [📝](reviews/chat-ui.md#anything-llm) [📖](https://docs.anythingllm.com "Docs") [🌐](https://anythingllm.com "Website") |
| 5 | **[LibreChat](https://github.com/LibreChat-AI/LibreChat)**<br><sub>Multi-provider ChatGPT-style app with agents, MCP, code interpreter and auth</sub> | 45k | MIT | 🐳 | [📝](reviews/chat-ui.md#librechat) [📖](https://docs.librechat.ai "Docs") [🌐](https://librechat.ai "Website") |
| 6 | **[SillyTavern](https://github.com/SillyTavern/SillyTavern)**<br><sub>Local chat front end for role-play across many LLM backends</sub> | 34k | AGPL-3.0 | 🐳 | [📝](reviews/chat-ui.md#sillytavern) [📖](https://docs.sillytavern.app/ "Docs") |
| 7 | **[Onyx](https://github.com/onyx-dot-app/onyx)**<br><sub>Team knowledge chat that indexes 50+ apps for RAG and agents</sub> | 32k | NOASSERTION | – | [📝](reviews/chat-ui.md#onyx) [🧪](https://cloud.onyx.app/signup "Live demo") [📖](https://docs.onyx.app/ "Docs") [🌐](https://www.onyx.app/ "Website") |
| 8 | **[Hermes WebUI](https://github.com/nesquena/hermes-webui)**<br><sub>Browser front end for Hermes Agent with sessions, files and voice input</sub> | 19k | MIT | 🐳 | [📝](reviews/chat-ui.md#hermes-webui) |
| 9 | **[HuggingChat UI](https://github.com/huggingface/chat-ui)**<br><sub>SvelteKit chat front end behind HuggingChat for OpenAI-compatible endpoints</sub> | 11k | Apache-2.0 | 🐳 | [📝](reviews/chat-ui.md#huggingface-chat-ui) [🧪](https://huggingface.co/chat "Live demo") |
| 10 | **[big-AGI](https://github.com/enricoros/big-AGI)**<br><sub>Multi-model chat workspace with Beam side-by-side model comparison</sub> | 7.1k | MIT | 🐳 | [📝](reviews/chat-ui.md#big-agi) [🌐](https://big-agi.com "Website") |
| 11 | **[LoLLMs WebUI](https://github.com/ParisNeo/lollms-webui)**<br><sub>Single-user web UI for local and remote LLMs with many personalities</sub> | 4.8k | Apache-2.0 | 🐳 | [📝](reviews/chat-ui.md#lollms-webui) |
| 12 | **[ClaraVerse](https://github.com/claraverse-space/ClaraVerse)**<br><sub>Private AI workspace with chat, agent crews, workflows and Telegram</sub> | 3.9k | NOASSERTION | 🐳 | [📝](reviews/chat-ui.md#claraverse) [🌐](https://claraverse.space "Website") |
| 13 | **[ChatGPT UI](https://github.com/WongSaang/chatgpt-ui)**<br><sub>Multi-user ChatGPT-style web client with pluggable databases</sub> | 1.6k | MIT | 🐳 | [📝](reviews/chat-ui.md#chatgpt-ui) [📖](https://wongsaang.github.io/chatgpt-ui/ "Docs") |

<details><summary>💡 How to choose</summary>

- Confirm it talks to your backend (Ollama, OpenAI-compatible, Anthropic) without a plugin.
- Multi-user auth, RBAC and SSO are where free and paid editions differ most.
- Check what the default compose pulls in (database, vector store) before sizing the host.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 🧩 Agent platforms

Visual or code-first builders for agents and workflows, with orchestration, tools and deployment. <sub>12 projects · [📝 all reviews](reviews/agent-platforms.md)</sub>

| # | Project | ⭐ | 📄 | 🚀 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[n8n](https://github.com/n8n-io/n8n)**<br><sub>Visual workflow automation with code steps, AI agent nodes and 1500+ integrations</sub> | 207k | NOASSERTION | – | [📝](reviews/agent-platforms.md#n8n) [📖](https://docs.n8n.io "Docs") |
| 🥈 | **[AutoGPT](https://github.com/Significant-Gravitas/AutoGPT)**<br><sub>Block-based builder for agents that run on demand, schedule or trigger</sub> | 188k | NOASSERTION | – | [📝](reviews/agent-platforms.md#autogpt) [🧪](https://platform.agpt.co/tour "Live demo") [📖](https://docs.agpt.co "Docs") |
| 🥉 | **[Dify](https://github.com/langgenius/dify)**<br><sub>Visual LLM app platform with workflows, RAG pipeline, agents and APIs</sub> | 158k | NOASSERTION | – | [📝](reviews/agent-platforms.md#dify) [🧪](https://cloud.dify.ai "Live demo") [📖](https://docs.dify.ai "Docs") [🌐](https://dify.ai "Website") |
| 4 | **[Langflow](https://github.com/langflow-ai/langflow)**<br><sub>Visual flow builder that deploys agents as APIs or MCP servers</sub> | 156k | MIT | – | [📝](reviews/agent-platforms.md#langflow) [📖](https://docs.langflow.org/get-started-installation "Docs") [🌐](https://langflow.org "Website") |
| 5 | **[Paperclip](https://github.com/paperclipai/paperclip)**<br><sub>Task manager and org chart for teams of AI agents with budgets</sub> | 99k | MIT | 🐳 | [📝](reviews/agent-platforms.md#paperclip) [📖](https://docs.paperclip.ing "Docs") [🌐](https://paperclip.ing "Website") |
| 6 | **[Multica](https://github.com/multica-ai/multica)**<br><sub>Issue board where coding agents pick up tickets and return pull requests</sub> | 52k | NOASSERTION | 🐳 | [📝](reviews/agent-platforms.md#multica) [📖](https://multica.ai/docs "Docs") [🌐](https://multica.ai "Website") |
| 7 | **[Sim](https://github.com/simstudioai/sim)**<br><sub>Workspace to build, deploy and monitor agents with 1,000+ integrations</sub> | 30k | Apache-2.0 | – | [📝](reviews/agent-platforms.md#sim) [📖](https://docs.sim.ai "Docs") [🌐](https://sim.ai "Website") |
| 8 | **[FastGPT](https://github.com/labring/FastGPT)**<br><sub>Knowledge-base Q&A and visual workflow platform for LLM apps</sub> | 30k | NOASSERTION | – | [📝](reviews/agent-platforms.md#fastgpt) [📖](https://doc.fastgpt.io/guide/getting-started "Docs") [🌐](https://fastgpt.io "Website") |
| 9 | **[Activepieces](https://github.com/activepieces/activepieces)**<br><sub>Zapier-style automation whose 280+ pieces double as MCP servers</sub> | 25k | NOASSERTION | 🐳 | [📝](reviews/agent-platforms.md#activepieces) [📖](https://www.activepieces.com/docs "Docs") [🌐](https://activepieces.com "Website") |
| 10 | **[Skyvern](https://github.com/Skyvern-AI/skyvern)**<br><sub>Browser automation agent driven by vision LLMs over Playwright</sub> | 23k | AGPL-3.0 | 🐳 | [📝](reviews/agent-platforms.md#skyvern) [🧪](https://app.skyvern.com "Live demo") [📖](https://www.skyvern.com/docs/ "Docs") [🌐](https://www.skyvern.com "Website") |
| 11 | **[Agent Zero](https://github.com/agent0ai/agent-zero)**<br><sub>Agent framework that gives the model a full Linux desktop in Docker</sub> | 19k | NOASSERTION | – | [📝](reviews/agent-platforms.md#agent-zero) [🌐](https://agent-zero.ai "Website") |
| 12 | **[Botpress](https://github.com/botpress/botpress)**<br><sub>SDK, CLI and open-source integrations for the Botpress Cloud bot platform</sub> | 15k | MIT | 🐳 | [📝](reviews/agent-platforms.md#botpress) [🧪](https://app.botpress.cloud "Live demo") [📖](https://botpress.com/docs "Docs") [🌐](https://botpress.com "Website") |

<details><summary>💡 How to choose</summary>

- Decide between a visual builder (faster to start) and code-first (easier to test and version).
- Check how workflows are exported; vendor-specific JSON makes migration costly.
- Look at the license for the server part; several are AGPL or source-available.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 📚 RAG and knowledge

Document Q&A, knowledge bases and enterprise search over your own files and data. <sub>15 projects · [📝 all reviews](reviews/rag-knowledge.md)</sub>

| # | Project | ⭐ | 📄 | 🚀 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[RAGFlow](https://github.com/infiniflow/ragflow)**<br><sub>RAG engine with deep document parsing, agentic retrieval and knowledge compilation</sub> | 92k | Apache-2.0 | 🐳 | [📝](reviews/rag-knowledge.md#ragflow) [🧪](https://cloud.ragflow.io "Live demo") [📖](https://ragflow.io/docs/dev/ "Docs") [🌐](https://ragflow.io/ "Website") |
| 🥈 | **[PrivateGPT](https://github.com/zylon-ai/private-gpt)**<br><sub>Anthropic-style API layer for private RAG on local inference servers</sub> | 58k | Apache-2.0 | 🐳 | [📝](reviews/rag-knowledge.md#private-gpt) [📖](https://docs.privategpt.dev/ "Docs") |
| 🥉 | **[LightRAG](https://github.com/HKUDS/LightRAG)**<br><sub>Graph-plus-vector RAG server with web UI and Ollama-compatible API</sub> | 40k | MIT | 🐳 | [📝](reviews/rag-knowledge.md#lightrag) |
| 4 | **[Open Notebook](https://github.com/lfnovo/open-notebook)**<br><sub>Self-hosted NotebookLM alternative with podcasts and 20+ model providers</sub> | 40k | MIT | 🐳 | [📝](reviews/rag-knowledge.md#open-notebook) [🌐](https://www.open-notebook.ai "Website") |
| 5 | **[WeKnora](https://github.com/Tencent/WeKnora)**<br><sub>Enterprise knowledge base combining RAG Q&A, agents and generated wikis</sub> | 33k | NOASSERTION | 🐳 | [📝](reviews/rag-knowledge.md#weknora) [📖](https://weknora.weixin.qq.com/docs/ "Docs") [🌐](https://weknora.weixin.qq.com "Website") |
| 6 | **[Kotaemon](https://github.com/Cinnamon/kotaemon)**<br><sub>Gradio RAG UI with hybrid retrieval, citations and multi-user login</sub> | 26k | Apache-2.0 | 🐳 | [📝](reviews/rag-knowledge.md#kotaemon) [🧪](https://huggingface.co/spaces/cin-model/kotaemon-demo "Live demo") [📖](https://cinnamon.github.io/kotaemon/ "Docs") |
| 7 | **[MaxKB](https://github.com/1Panel-dev/MaxKB)**<br><sub>Enterprise knowledge-base agent platform with RAG, workflows and MCP tools</sub> | 23k | GPL-3.0 | – | [📝](reviews/rag-knowledge.md#maxkb) |
| 8 | **[DB-GPT](https://github.com/eosphoros-ai/DB-GPT)**<br><sub>Agentic data assistant that writes SQL and code over your databases</sub> | 20k | MIT | 🐳 ✨ | [📝](reviews/rag-knowledge.md#db-gpt) [📖](http://docs.dbgpt.cn/docs/overview/ "Docs") [🌐](http://dbgpt.cn/ "Website") |
| 9 | **[DeepWiki-Open](https://github.com/AsyncFuncAI/deepwiki-open)**<br><sub>Generates browsable wikis and diagrams for GitHub, GitLab and Bitbucket repos</sub> | 18k | MIT | 🐳 | [📝](reviews/rag-knowledge.md#deepwiki-open) [🌐](https://grok-wiki.com "Website") |
| 10 | **[SurfSense](https://github.com/MODSetter/SurfSense)**<br><sub>Offline NotebookLM alternative that turns documents into decks, reports and podcasts</sub> | 16k | NOASSERTION | – | [📝](reviews/rag-knowledge.md#surfsense) [📖](https://www.surfsense.com/docs "Docs") [🌐](https://www.surfsense.com/ "Website") |
| 11 | **[Paperless-AI](https://github.com/clusterzx/paperless-ai)**<br><sub>Auto-tags Paperless-ngx documents and adds RAG chat over the archive</sub> | 6.0k | MIT | 🐳 | [📝](reviews/rag-knowledge.md#paperless-ai) [📖](https://github.com/clusterzx/paperless-ai/wiki/2.-Installation "Docs") |
| 12 | **[PipesHub](https://github.com/pipeshub-ai/pipeshub-ai)**<br><sub>Permission-aware search and agent context over 50+ workplace systems</sub> | 3.8k | Apache-2.0 | 🐳 | [📝](reviews/rag-knowledge.md#pipeshub) [📖](https://docs.pipeshub.com/ "Docs") [🌐](https://www.pipeshub.com/ "Website") |
| 13 | **[Morphik](https://github.com/morphik-org/morphik-core)**<br><sub>Multimodal retrieval engine for visually rich PDFs, images and video</sub> | 3.7k | NOASSERTION | 🐳 | [📝](reviews/rag-knowledge.md#morphik) [🧪](https://dev.morphik.ai "Live demo") [📖](https://dev.morphik.ai/docs "Docs") [🌐](https://morphik.ai "Website") |
| 14 | **[paperless-gpt](https://github.com/icereed/paperless-gpt)**<br><sub>LLM-powered OCR, titles, tags and document links for Paperless-ngx</sub> | 2.7k | MIT | 🐳 | [📝](reviews/rag-knowledge.md#paperless-gpt) |
| 15 | **[Docling Serve](https://github.com/docling-project/docling-serve)**<br><sub>Docling document conversion as an HTTP API with playground UI</sub> | 1.8k | MIT | ✨ | [📝](reviews/rag-knowledge.md#docling-serve) |

<details><summary>💡 How to choose</summary>

- Match the ingestion formats you need (PDF with tables, Office, web, Confluence) before anything else.
- Check which embedding models and vector stores are supported and whether they can run offline.
- Look for citations in answers; without them, RAG output is hard to trust.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 🧠 Model serving

Inference engines and model servers that expose local models over an API. <sub>18 projects · [📝 all reviews](reviews/model-serving.md)</sub>

| # | Project | ⭐ | 📄 | 🚀 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[Ollama](https://github.com/ollama/ollama)**<br><sub>Runs open-weight models locally behind a CLI and REST API</sub> | 183k | MIT | 🐳 ✨ | [📝](reviews/model-serving.md#ollama) [📖](https://docs.ollama.com/quickstart "Docs") [🌐](https://ollama.com "Website") |
| 🥈 | **[llama.cpp](https://github.com/ggml-org/llama.cpp)**<br><sub>C/C++ inference engine serving GGUF models over an OpenAI-compatible API</sub> | 131k | MIT | ✨ | [📝](reviews/model-serving.md#llama-cpp) [🌐](https://llama.app "Website") |
| 🥉 | **[vLLM](https://github.com/vllm-project/vllm)**<br><sub>High-throughput LLM serving engine with OpenAI and Anthropic APIs</sub> | 93k | Apache-2.0 | ✨ | [📝](reviews/model-serving.md#vllm) [📖](https://docs.vllm.ai "Docs") [🌐](https://vllm.ai "Website") |
| 4 | **[LocalAI](https://github.com/mudler/LocalAI)**<br><sub>One OpenAI-compatible server for text, speech, image and video models</sub> | 49k | MIT | 🐳 ✨ | [📝](reviews/model-serving.md#localai) [📖](https://localai.io/basics/getting_started/ "Docs") [🌐](https://localai.io/ "Website") |
| 5 | **[Text Generation Web UI](https://github.com/oobabooga/textgen)**<br><sub>Local LLM chat UI and API with five switchable loader backends</sub> | 48k | AGPL-3.0 | ✨ | [📝](reviews/model-serving.md#text-generation-webui) |
| 6 | **[SGLang](https://github.com/sgl-project/sglang)**<br><sub>Inference framework for LLMs, VLMs and diffusion models on many accelerators</sub> | 37k | Apache-2.0 | ✨ | [📝](reviews/model-serving.md#sglang) [📖](https://docs.sglang.io/ "Docs") [🌐](https://www.sglang.io/ "Website") |
| 7 | **[llamafile](https://github.com/mozilla-ai/llamafile)**<br><sub>Single-file executables that bundle llama.cpp with model weights</sub> | 26k | NOASSERTION | ✨ | [📝](reviews/model-serving.md#llamafile) [📖](https://docs.mozilla.ai/llamafile "Docs") |
| 8 | **[KTransformers](https://github.com/kvcache-ai/ktransformers)**<br><sub>CPU-GPU hybrid inference and fine-tuning for very large MoE models</sub> | 20k | Apache-2.0 | 🎮 | [📝](reviews/model-serving.md#ktransformers) [📖](https://kvcache-ai.github.io/ktransformers/ "Docs") |
| 9 | **[OpenLLM](https://github.com/bentoml/OpenLLM)**<br><sub>One-command OpenAI-compatible endpoints for curated open LLMs</sub> | 13k | Apache-2.0 | 🎮 | [📝](reviews/model-serving.md#openllm) |
| 10 | **[Triton Inference Server](https://github.com/triton-inference-server/server)**<br><sub>NVIDIA inference server for TensorRT, PyTorch, ONNX and more over HTTP/gRPC</sub> | 11k | BSD-3-Clause | ✨ | [📝](reviews/model-serving.md#triton-inference-server) [🌐](https://developer.nvidia.com/nvidia-triton-inference-server "Website") |
| 11 | **[Xinference](https://github.com/xorbitsai/inference)**<br><sub>Serves LLM, embedding, speech and image models behind one OpenAI-style API</sub> | 9.6k | Apache-2.0 | ✨ | [📝](reviews/model-serving.md#xinference) [📖](https://inference.readthedocs.io/ "Docs") [🌐](https://xinference.co "Website") |
| 12 | **[LMDeploy](https://github.com/InternLM/lmdeploy)**<br><sub>LLM and VLM serving toolkit with the TurboMind and PyTorch engines</sub> | 8.1k | Apache-2.0 | 🎮 | [📝](reviews/model-serving.md#lmdeploy) [📖](https://lmdeploy.readthedocs.io/en/latest/ "Docs") |
| 13 | **[mistral.rs](https://github.com/EricLBuehler/mistral.rs)**<br><sub>Rust inference server with OpenAI and Anthropic APIs and agent tools</sub> | 7.7k | MIT | 🐳 ✨ | [📝](reviews/model-serving.md#mistral-rs) [📖](https://docs.mistralrs.dev/ "Docs") |
| 14 | **[llama-swap](https://github.com/mostlygeek/llama-swap)**<br><sub>Go proxy that hot-swaps local model servers per request</sub> | 5.9k | MIT | ✨ | [📝](reviews/model-serving.md#llama-swap) |
| 15 | **[Lemonade](https://github.com/lemonade-sdk/lemonade)**<br><sub>Local AI server that targets GPUs and AMD NPUs with OpenAI-style APIs</sub> | 5.8k | Apache-2.0 | 🐳 ✨ | [📝](reviews/model-serving.md#lemonade) |
| 16 | **[GPUStack](https://github.com/gpustack/gpustack)**<br><sub>GPU cluster manager that deploys models on vLLM, SGLang and TensorRT-LLM</sub> | 5.8k | Apache-2.0 | 🎮 | [📝](reviews/model-serving.md#gpustack) [📖](https://docs.gpustack.ai "Docs") |
| 17 | **[Text Embeddings Inference](https://github.com/huggingface/text-embeddings-inference)**<br><sub>Rust server for embedding, reranker and classification models</sub> | 5.1k | Apache-2.0 | 🐳 ✨ | [📝](reviews/model-serving.md#text-embeddings-inference) [📖](https://huggingface.github.io/text-embeddings-inference "Docs") |
| 18 | **[TabbyAPI](https://github.com/theroyallab/tabbyAPI)**<br><sub>OpenAI-compatible API server for ExLlamaV3 models</sub> | 1.5k | AGPL-3.0 | 🎮 | [📝](reviews/model-serving.md#tabbyapi) [📖](https://theroyallab.github.io/tabbyAPI "Docs") |

<details><summary>💡 How to choose</summary>

- Pick by hardware first (CPU, NVIDIA, AMD, Apple Silicon) and by model format (GGUF, safetensors).
- Throughput engines (continuous batching, paged attention) need GPUs; single-user servers do not.
- An OpenAI-compatible API keeps the rest of your stack portable.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 🔀 Gateways

LLM gateways and proxies for routing, caching, rate limits and cost control across providers. <sub>13 projects · [📝 all reviews](reviews/gateways.md)</sub>

| # | Project | ⭐ | 📄 | 🚀 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[OmniRoute](https://github.com/diegosouzapw/OmniRoute)**<br><sub>Free-tier-aware AI gateway routing coding agents across 350+ providers</sub> | 74k | MIT | 🐳 | [📝](reviews/gateways.md#omniroute) [🌐](https://omniroute.online "Website") |
| 🥈 | **[LiteLLM](https://github.com/BerriAI/litellm)**<br><sub>Proxy and SDK that calls 100+ LLM providers in OpenAI format</sub> | 60k | NOASSERTION | 🐳 | [📝](reviews/gateways.md#litellm) [📖](https://docs.litellm.ai/docs/simple_proxy "Docs") [🌐](https://www.litellm.ai/ai-gateway "Website") |
| 🥉 | **[Portkey Gateway](https://github.com/Portkey-AI/gateway)**<br><sub>Node.js LLM gateway with fallbacks, load balancing and guardrails</sub> | 13k | MIT | 🐳 | [📝](reviews/gateways.md#portkey-gateway) |
| 4 | **[Higress](https://github.com/higress-group/higress)**<br><sub>Envoy-based API gateway with LLM proxy plugins and MCP server hosting</sub> | 9.5k | Apache-2.0 | – | [📝](reviews/gateways.md#higress) [🧪](https://demo.higress.io/ "Live demo") [📖](https://higress.cn/en/docs/latest/overview/what-is-higress/ "Docs") [🌐](https://higress.ai/en/ "Website") |
| 5 | **[CoAI](https://github.com/coaidev/coai)**<br><sub>Multi-user chat site plus OpenAI-compatible proxy with billing</sub> | 9.3k | Apache-2.0 | 🐳 | [📝](reviews/gateways.md#coai) [📖](https://coai.dev/docs/deploy "Docs") [🌐](https://coai.dev "Website") |
| 6 | **[Bifrost](https://github.com/maximhq/bifrost)**<br><sub>Go AI gateway with web UI, fallbacks, budgets and semantic caching</sub> | 8.6k | Apache-2.0 | – | [📝](reviews/gateways.md#bifrost) [📖](https://docs.getbifrost.ai "Docs") |
| 7 | **[Plano](https://github.com/katanemo/plano)**<br><sub>Envoy-based data plane that routes, traces and guards agent traffic</sub> | 7.1k | Apache-2.0 | 🐳 | [📝](reviews/gateways.md#plano) [📖](https://docs.planoai.dev "Docs") |
| 8 | **[agentgateway](https://github.com/agentgateway/agentgateway)**<br><sub>One proxy for LLM, MCP and A2A traffic with auth and RBAC</sub> | 5.2k | Apache-2.0 | 🐳 | [📝](reviews/gateways.md#agentgateway) [📖](https://agentgateway.dev/docs/standalone/latest "Docs") |
| 9 | **[ContextForge MCP Gateway](https://github.com/IBM/mcp-context-forge)**<br><sub>Registry and proxy federating MCP, A2A, REST and gRPC behind one endpoint</sub> | 4.6k | Apache-2.0 | 🐳 | [📝](reviews/gateways.md#mcp-context-forge) [📖](https://ibm.github.io/mcp-context-forge/ "Docs") |
| 10 | **[mcpo](https://github.com/open-webui/mcpo)**<br><sub>Exposes any MCP server as an OpenAPI HTTP endpoint</sub> | 4.4k | MIT | 🐳 | [📝](reviews/gateways.md#mcpo) [📖](https://docs.openwebui.com/openapi-servers/open-webui/ "Docs") |
| 11 | **[optillm](https://github.com/algorithmicsuperintelligence/optillm)**<br><sub>OpenAI-compatible proxy applying inference-time reasoning techniques</sub> | 4.3k | Apache-2.0 | 🐳 ✨ | [📝](reviews/gateways.md#optillm) [🧪](https://huggingface.co/spaces/codelion/optillm "Live demo") |
| 12 | **[MetaMCP](https://github.com/metatool-ai/metamcp)**<br><sub>Aggregates MCP servers into namespaced endpoints with auth and middleware</sub> | 2.7k | MIT | 🐳 | [📝](reviews/gateways.md#metamcp) [📖](https://docs.metamcp.com "Docs") |
| 13 | **[GoModel](https://github.com/ENTERPILOT/GoModel)**<br><sub>Go AI gateway with OpenAI and Anthropic APIs, caching and budgets</sub> | 1.2k | MIT | 🐳 | [📝](reviews/gateways.md#gomodel) [🧪](https://demo.enterpilot.io/admin/dashboard "Live demo") [📖](https://gomodel.enterpilot.io/docs "Docs") |

<details><summary>💡 How to choose</summary>

- List the providers you call today; check the gateway's native support rather than generic passthrough.
- Key management, per-team budgets and audit logs separate gateways from simple proxies.
- Check latency overhead and whether streaming is passed through unchanged.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 🗂️ Memory

Long-term memory engines that store and retrieve facts for agents across sessions. <sub>11 projects · [📝 all reviews](reviews/memory.md)</sub>

| # | Project | ⭐ | 📄 | 🚀 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[Mem0](https://github.com/mem0ai/mem0)**<br><sub>Memory layer for agents with a self-hosted server, SDKs and CLI</sub> | 67k | Apache-2.0 | – | [📝](reviews/memory.md#mem0) [🧪](https://mem0.dev/demo "Live demo") [📖](https://docs.mem0.ai "Docs") [🌐](https://mem0.ai "Website") |
| 🥈 | **[MemPalace](https://github.com/MemPalace/mempalace)**<br><sub>Local verbatim memory for coding agents on ChromaDB with 45 MCP tools</sub> | 59k | MIT | 🐳 | [📝](reviews/memory.md#mempalace) [📖](https://mempalaceofficial.com/guide/getting-started.html "Docs") [🌐](https://mempalaceofficial.com "Website") |
| 🥉 | **[OpenViking](https://github.com/volcengine/OpenViking)**<br><sub>Context database exposing agent memory, knowledge and skills as a filesystem</sub> | 39k | AGPL-3.0 | 🐳 | [📝](reviews/memory.md#openviking) [🧪](https://openviking.ai/studio "Live demo") [📖](https://docs.openviking.ai/ "Docs") [🌐](https://www.openviking.ai "Website") |
| 4 | **[Cognee](https://github.com/topoteretes/cognee)**<br><sub>Memory engine that turns documents and code into a knowledge graph</sub> | 32k | Apache-2.0 | 🐳 | [📝](reviews/memory.md#cognee) [📖](https://docs.cognee.ai/ "Docs") [🌐](https://cognee.ai "Website") |
| 5 | **[Graphiti](https://github.com/getzep/graphiti)**<br><sub>Temporal knowledge graph framework for agent memory with REST and MCP servers</sub> | 32k | Apache-2.0 | 🐳 | [📝](reviews/memory.md#graphiti) |
| 6 | **[Supermemory](https://github.com/supermemoryai/supermemory)**<br><sub>Memory and context API with user profiles, connectors and a local server</sub> | 31k | MIT | – | [📝](reviews/memory.md#supermemory) [📖](https://supermemory.ai/docs "Docs") |
| 7 | **[agentmemory](https://github.com/rohitg00/agentmemory)**<br><sub>Persistent memory server for coding agents built on the iii engine</sub> | 29k | Apache-2.0 | 🐳 | [📝](reviews/memory.md#agentmemory) |
| 8 | **[MemOS](https://github.com/MemTensor/MemOS)**<br><sub>Memory operating system for agents with cubes, scheduler and hybrid retrieval</sub> | 12k | Apache-2.0 | 🐳 | [📝](reviews/memory.md#memos) [📖](https://memos-docs.openmem.net/home/overview/ "Docs") [🌐](https://memos.openmem.net/ "Website") |
| 9 | **[Honcho](https://github.com/plastic-labs/honcho)**<br><sub>Memory service modelling users, agents and groups as evolving peers</sub> | 7.5k | AGPL-3.0 | 🐳 | [📝](reviews/memory.md#honcho) [🧪](https://app.honcho.dev "Live demo") [📖](https://honcho.dev/docs/v3/documentation/reference/sdk "Docs") |
| 10 | **[Engram](https://github.com/Gentleman-Programming/engram)**<br><sub>Single Go binary memory for coding agents on SQLite FTS5 with MCP</sub> | 7.1k | MIT | – | [📝](reviews/memory.md#engram) [🌐](https://engram.gentlemanprogramming.com/ "Website") |
| 11 | **[Letta](https://github.com/letta-ai/letta-code)**<br><sub>Stateful agent harness with git-tracked memory, channels and remote computers</sub> | 3.5k | Apache-2.0 | – | [📝](reviews/memory.md#letta) [🧪](https://chat.letta.com "Live demo") [📖](https://docs.letta.com/letta-code/cli "Docs") |

<details><summary>💡 How to choose</summary>

- Check what gets stored (raw messages, extracted facts, graphs) and how it is retrieved.
- Multi-tenant isolation matters if several users or agents share one store.
- Look at the backing store (Postgres, a vector DB, a graph DB) and whether you already run it.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 🎙️ Voice

Speech-to-text, text-to-speech, voice agents and meeting tools that run locally. <sub>11 projects · [📝 all reviews](reviews/voice.md)</sub>

| # | Project | ⭐ | 📄 | 🚀 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[GPT-SoVITS](https://github.com/RVC-Boss/GPT-SoVITS)**<br><sub>Few-shot voice cloning and TTS with a training web UI</sub> | 63k | MIT | 🐳 ✨ | [📝](reviews/voice.md#gpt-sovits) [🧪](https://lj1995-gpt-sovits-proplus.hf.space/ "Live demo") [📖](https://rentry.co/GPT-SoVITS-guide#/ "Docs") |
| 🥈 | **[Voicebox](https://github.com/jamiepine/voicebox)**<br><sub>Local voice studio for cloning, TTS, dictation and agent speech</sub> | 57k | MIT | 🐳 ✨ | [📝](reviews/voice.md#voicebox) [📖](https://docs.voicebox.sh "Docs") [🌐](https://voicebox.sh "Website") |
| 🥉 | **[IndexTTS](https://github.com/index-tts/index-tts)**<br><sub>Zero-shot TTS with emotion, speed and pronunciation control</sub> | 24k | NOASSERTION | – | [📝](reviews/voice.md#index-tts) [🧪](https://huggingface.co/spaces/IndexTeam/IndexTTS-2.5-Demo "Live demo") |
| 4 | **[F5-TTS](https://github.com/SWivid/F5-TTS)**<br><sub>Flow-matching TTS and voice cloning with Gradio and CLI</sub> | 15k | MIT | 🐳 | [📝](reviews/voice.md#f5-tts) [🧪](https://huggingface.co/spaces/mrfakename/E2-F5-TTS "Live demo") |
| 5 | **[Speech-to-Speech](https://github.com/huggingface/speech-to-speech)**<br><sub>Modular voice-agent pipeline behind an OpenAI Realtime-compatible server</sub> | 13k | Apache-2.0 | 🐳 ✨ | [📝](reviews/voice.md#speech-to-speech) |
| 6 | **[Pocket TTS](https://github.com/kyutai-labs/pocket-tts)**<br><sub>100M-parameter CPU text-to-speech with streaming and voice cloning</sub> | 9.8k | MIT | 🐳 | [📝](reviews/voice.md#pocket-tts) [🧪](https://kyutai.org/pocket-tts "Live demo") [📖](https://kyutai-labs.github.io/pocket-tts/ "Docs") |
| 7 | **[Kokoro-FastAPI](https://github.com/remsky/Kokoro-FastAPI)**<br><sub>OpenAI-compatible Kokoro-82M speech API in CPU and GPU images</sub> | 5.5k | Apache-2.0 | ✨ | [📝](reviews/voice.md#kokoro-fastapi) [🧪](https://huggingface.co/spaces/Remsky/FastKoko "Live demo") |
| 8 | **[WhisperLive](https://github.com/collabora/WhisperLive)**<br><sub>Near-real-time Whisper transcription server over WebSocket</sub> | 4.3k | MIT | ✨ | [📝](reviews/voice.md#whisperlive) |
| 9 | **[Speakr](https://github.com/murtaza-nasir/speakr)**<br><sub>Transcribe, summarize and search recordings with pluggable ASR and LLMs</sub> | 4.1k | AGPL-3.0 | 🐳 | [📝](reviews/voice.md#speakr) [📖](https://murtaza-nasir.github.io/speakr "Docs") |
| 10 | **[Speaches](https://github.com/speaches-ai/speaches)**<br><sub>OpenAI-compatible STT and TTS server with faster-whisper, Kokoro and Piper</sub> | 3.7k | MIT | 🐳 ✨ | [📝](reviews/voice.md#speaches) [📖](https://speaches.ai/ "Docs") [🌐](https://speaches.ai/ "Website") |
| 11 | **[OpenReader](https://github.com/richardr1126/openreader)**<br><sub>Reads EPUB, PDF and DOCX aloud with synced word highlighting</sub> | 537 | MIT | 🐳 | [📝](reviews/voice.md#openreader) [📖](https://docs.openreader.richardr.dev/ "Docs") |

<details><summary>💡 How to choose</summary>

- Latency decides usability for voice agents; check the end-to-end numbers the project publishes.
- Most quality models need a GPU; CPU-only setups are slower and limited to smaller models.
- Check language coverage and whether models are downloaded at build or at first run.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 🎨 Image and video

Generation UIs and pipelines for images and video, usually around diffusion models. <sub>8 projects · [📝 all reviews](reviews/image-video.md)</sub>

| # | Project | ⭐ | 📄 | 🚀 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[ComfyUI](https://github.com/Comfy-Org/ComfyUI)**<br><sub>Node-graph engine for diffusion image, video, audio and 3D models</sub> | 137k | GPL-3.0 | ✨ | [📝](reviews/image-video.md#comfyui) [📖](https://docs.comfy.org/ "Docs") [🌐](https://www.comfy.org/ "Website") |
| 🥈 | **[MoneyPrinterTurbo](https://github.com/harry0703/MoneyPrinterTurbo)**<br><sub>Generates short videos from a topic with script, footage, voice and subtitles</sub> | 129k | MIT | 🐳 | [📝](reviews/image-video.md#moneyprinterturbo) |
| 🥉 | **[Pixelle-Video](https://github.com/ATH-MaaS/Pixelle-Video)**<br><sub>Topic-to-short-video pipeline built on ComfyUI workflows and TTS</sub> | 29k | Apache-2.0 | 🐳 | [📝](reviews/image-video.md#pixelle-video) [📖](https://aidc-ai.github.io/Pixelle-Video/zh "Docs") |
| 4 | **[InvokeAI](https://github.com/invoke-ai/InvokeAI)**<br><sub>Canvas-first web UI for Stable Diffusion and Flux image generation</sub> | 28k | Apache-2.0 | – | [📝](reviews/image-video.md#invokeai) [📖](https://invoke.ai/start-here/installation/ "Docs") [🌐](https://invoke.ai "Website") |
| 5 | **[Kohya's GUI](https://github.com/bmaltais/kohya_ss)**<br><sub>Gradio GUI and CLI for Kohya diffusion training scripts</sub> | 13k | Apache-2.0 | 🐳 🎮 | [📝](reviews/image-video.md#kohya-ss) |
| 6 | **[AI Toolkit](https://github.com/ostris/ai-toolkit)**<br><sub>Training suite and web UI for image, video and audio diffusion models</sub> | 12k | MIT | 🐳 🎮 | [📝](reviews/image-video.md#ai-toolkit) |
| 7 | **[FluxGym](https://github.com/cocktailpeanut/fluxgym)**<br><sub>Web UI for training FLUX LoRAs on 12 to 20 GB GPUs</sub> | 3.3k | MIT | 🐳 🎮 | [📝](reviews/image-video.md#fluxgym) |
| 8 | **[biniou](https://github.com/Woolverine94/biniou)**<br><sub>Chat, image, audio, video and 3D generation in one CPU-friendly web UI</sub> | 1.2k | GPL-3.0 | 🐳 ✨ | [📝](reviews/image-video.md#biniou) [📖](https://github.com/Woolverine94/biniou/wiki "Docs") |

<details><summary>💡 How to choose</summary>

- A GPU with enough VRAM is the hard requirement; check the minimum the project states.
- Node-based UIs are flexible but have a learning curve; form-based UIs are quicker to use.
- Check the model licensing separately from the app licensing.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 💻 Coding

Self-hosted coding assistants and agents, from editor completion to autonomous task runners. <sub>9 projects · [📝 all reviews](reviews/coding.md)</sub>

| # | Project | ⭐ | 📄 | 🚀 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[opencode](https://github.com/anomalyco/opencode)**<br><sub>Terminal coding agent with build and plan modes</sub> | 212k | MIT | – | [📝](reviews/coding.md#opencode) [📖](https://opencode.ai/docs "Docs") [🌐](https://opencode.ai "Website") |
| 🥈 | **[OpenHands](https://github.com/OpenHands/OpenHands)**<br><sub>Self-hosted control center for coding agents and automations</sub> | 90k | MIT | – | [📝](reviews/coding.md#openhands) [📖](https://docs.openhands.dev/openhands/usage/agent-canvas/backends "Docs") |
| 🥉 | **[screenshot-to-code](https://github.com/abi/screenshot-to-code)**<br><sub>Turns screenshots and mockups into Tailwind, React or Vue code</sub> | 80k | MIT | 🐳 | [📝](reviews/coding.md#screenshot-to-code) [🧪](https://screenshottocode.com/ "Live demo") |
| 4 | **[Tabby](https://github.com/TabbyML/tabby)**<br><sub>Self-hosted code completion and chat server for IDEs</sub> | 34k | NOASSERTION | ✨ | [📝](reviews/coding.md#tabby) [🧪](https://tabby.tabbyml.com "Live demo") [📖](https://tabby.tabbyml.com/docs/welcome/ "Docs") |
| 5 | **[Onlook](https://github.com/onlook-dev/onlook)**<br><sub>Visual editor that edits Next.js and Tailwind apps with AI</sub> | 27k | Apache-2.0 | 🐳 | [📝](reviews/coding.md#onlook) [🧪](https://onlook.com "Live demo") [📖](https://docs.onlook.com "Docs") |
| 6 | **[Archon](https://github.com/coleam00/Archon)**<br><sub>YAML workflow engine that runs coding agents in isolated worktrees</sub> | 24k | MIT | 🐳 | [📝](reviews/coding.md#archon) [📖](https://archon.diy/docs/ "Docs") |
| 7 | **[OpenChamber](https://github.com/openchamber/openchamber)**<br><sub>Multi-device workspace for running and reviewing OpenCode agent sessions</sub> | 11k | MIT | 🐳 | [📝](reviews/coding.md#openchamber) |
| 8 | **[Open SWE](https://github.com/langchain-ai/open-swe)**<br><sub>LangChain coding agent that plans, implements and reviews pull requests</sub> | 11k | MIT | 🐳 | [📝](reviews/coding.md#open-swe) |
| 9 | **[Background Agents](https://github.com/ColeMurray/background-agents)**<br><sub>Background coding agents on cloud sandboxes with Slack, GitHub and Linear triggers</sub> | 3.3k | MIT | 🐳 | [📝](reviews/coding.md#background-agents) |

<details><summary>💡 How to choose</summary>

- Separate editor completion (needs low latency, small models) from agents that run tasks (need strong models).
- Check sandboxing for agents that execute code or shell commands.
- Look at which editors and model backends are supported without a cloud account.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 🔎 Search

Private search engines and AI answer engines that keep queries on your host. <sub>8 projects · [📝 all reviews](reviews/search.md)</sub>

| # | Project | ⭐ | 📄 | 🚀 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[Firecrawl](https://github.com/firecrawl/firecrawl)**<br><sub>Web scraping and crawling API that returns LLM-ready markdown</sub> | 190k | AGPL-3.0 | 🐳 | [📝](reviews/search.md#firecrawl) [🧪](https://firecrawl.dev/playground "Live demo") [📖](https://docs.firecrawl.dev "Docs") [🌐](https://firecrawl.dev "Website") |
| 🥈 | **[Crawl4AI](https://github.com/unclecode/crawl4ai)**<br><sub>Python crawler that turns pages into LLM-ready markdown, with a Docker API</sub> | 85k | Apache-2.0 | 🐳 | [📝](reviews/search.md#crawl4ai) [📖](https://docs.crawl4ai.com/ "Docs") |
| 🥉 | **[Vane](https://github.com/ItzCrazyKns/Vane)**<br><sub>Self-hosted answer engine with cited sources over SearXNG</sub> | 37k | MIT | 🐳 | [📝](reviews/search.md#vane) |
| 4 | **[GPT Researcher](https://github.com/assafelovic/gpt-researcher)**<br><sub>Research agent that writes cited reports from web and local documents</sub> | 30k | Apache-2.0 | 🐳 | [📝](reviews/search.md#gpt-researcher) [📖](https://docs.gptr.dev "Docs") [🌐](https://gptr.dev "Website") |
| 5 | **[Jina Reader](https://github.com/jina-ai/reader)**<br><sub>Converts any URL or search query into LLM-friendly markdown</sub> | 12k | Apache-2.0 | 🐳 | [📝](reviews/search.md#jina-reader) [🧪](https://jina.ai/reader#demo "Live demo") [📖](https://r.jina.ai/docs "Docs") [🌐](https://jina.ai/reader "Website") |
| 6 | **[Local Deep Research](https://github.com/LearningCircuit/local-deep-research)**<br><sub>Agentic research assistant with local LLMs, SearXNG and encrypted libraries</sub> | 9.2k | MIT | 🐳 ✨ | [📝](reviews/search.md#local-deep-research) |
| 7 | **[Morphic](https://github.com/miurla/morphic)**<br><sub>AI search engine with generative UI and bundled SearXNG</sub> | 9.2k | Apache-2.0 | 🐳 | [📝](reviews/search.md#morphic) |
| 8 | **[MAESTRO](https://github.com/murtaza-nasir/maestro)**<br><sub>Multi-agent research platform that writes long reports from documents and web</sub> | 1.5k | AGPL-3.0 | 🐳 ✨ | [📝](reviews/search.md#maestro) [📖](https://murtaza-nasir.github.io/maestro/ "Docs") |

<details><summary>💡 How to choose</summary>

- Metasearch engines need upstream providers; check rate limits and whether results are cached.
- Answer engines call an LLM per query; budget tokens before exposing them to a team.
- Check how results are attributed; answer engines without citations are hard to verify.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 📈 Observability

Tracing, evaluation and prompt management for LLM applications. <sub>13 projects · [📝 all reviews](reviews/observability.md)</sub>

| # | Project | ⭐ | 📄 | 🚀 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[Langfuse](https://github.com/langfuse/langfuse)**<br><sub>Tracing, prompt management and evals for LLM apps on ClickHouse</sub> | 36k | NOASSERTION | 🐳 | [📝](reviews/observability.md#langfuse) [🧪](https://langfuse.com/demo "Live demo") [📖](https://langfuse.com/docs "Docs") [🌐](https://langfuse.com "Website") |
| 🥈 | **[MLflow](https://github.com/mlflow/mlflow)**<br><sub>Tracing, evals, prompt registry and AI gateway plus classic ML tracking</sub> | 28k | Apache-2.0 | – | [📝](reviews/observability.md#mlflow) [🧪](https://demo.mlflow.org/ "Live demo") [📖](https://mlflow.org/docs/latest "Docs") [🌐](https://mlflow.org/ "Website") |
| 🥉 | **[promptfoo](https://github.com/promptfoo/promptfoo)**<br><sub>CLI for evaluating and red-teaming prompts, agents and RAG</sub> | 26k | MIT | 🐳 | [📝](reviews/observability.md#promptfoo) [📖](https://www.promptfoo.dev/docs/ "Docs") [🌐](https://www.promptfoo.dev "Website") |
| 4 | **[Opik](https://github.com/comet-ml/opik)**<br><sub>Trace, evaluate and monitor LLM apps and agents, Apache-2.0 end to end</sub> | 22k | Apache-2.0 | – | [📝](reviews/observability.md#opik) [📖](https://www.comet.com/docs/opik/ "Docs") [🌐](https://www.comet.com/site/products/opik/ "Website") |
| 5 | **[Phoenix](https://github.com/Arize-ai/phoenix)**<br><sub>OpenTelemetry-based LLM tracing, evals and prompt playground</sub> | 12k | NOASSERTION | 🐳 | [📝](reviews/observability.md#phoenix) [📖](https://arize.com/docs/phoenix/ "Docs") [🌐](https://phoenix.arize.com "Website") |
| 6 | **[Helicone](https://github.com/Helicone/helicone)**<br><sub>LLM proxy gateway with request logging, cost tracking and sessions</sub> | 6.2k | Apache-2.0 | 🐳 | [📝](reviews/observability.md#helicone) [🧪](https://helicone.ai/demo "Live demo") [📖](https://docs.helicone.ai/ "Docs") [🌐](https://www.helicone.ai "Website") |
| 7 | **[LangWatch](https://github.com/langwatch/langwatch)**<br><sub>Agent observability, simulation testing, AI gateway and governance in one</sub> | 4.9k | Apache-2.0 | – | [📝](reviews/observability.md#langwatch) [📖](https://langwatch.ai/docs/introduction "Docs") [🌐](https://langwatch.ai "Website") |
| 8 | **[Agenta](https://github.com/Agenta-AI/agenta)**<br><sub>Team workspace for building chat-driven agents that run in Slack and WhatsApp</sub> | 4.8k | NOASSERTION | – | [📝](reviews/observability.md#agenta) [📖](https://agenta.ai/docs/ "Docs") [🌐](https://agenta.ai "Website") |
| 9 | **[Latitude](https://github.com/latitude-dev/latitude-llm)**<br><sub>Agent observability that groups failures and dispatches coding agents to fix them</sub> | 4.7k | MIT | 🐳 | [📝](reviews/observability.md#latitude-llm) [📖](https://docs.latitude.so "Docs") [🌐](https://latitude.so "Website") |
| 10 | **[Laminar](https://github.com/lmnr-ai/lmnr)**<br><sub>Rust-based agent tracing with SQL queries, signals and evals</sub> | 3.4k | Apache-2.0 | 🐳 | [📝](reviews/observability.md#lmnr) [📖](https://laminar.sh/docs "Docs") [🌐](https://laminar.sh "Website") |
| 11 | **[Pezzo](https://github.com/pezzolabs/pezzo)**<br><sub>Prompt management, observability and caching for LLM apps</sub> | 3.3k | Apache-2.0 | 🐳 | [📝](reviews/observability.md#pezzo) [📖](https://docs.pezzo.ai/ "Docs") [🌐](https://pezzo.ai "Website") |
| 12 | **[OpenLIT](https://github.com/openlit/openlit)**<br><sub>OpenTelemetry-native tracing, evals, guardrails and GPU monitoring for agents</sub> | 2.8k | Apache-2.0 | 🐳 | [📝](reviews/observability.md#openlit) [📖](https://docs.openlit.io/ "Docs") [🌐](https://openlit.io "Website") |
| 13 | **[Future AGI](https://github.com/future-agi/future-agi)**<br><sub>Evals, tracing, simulations, guardrails and a gateway for agents in one stack</sub> | 2.1k | Apache-2.0 | 🐳 | [📝](reviews/observability.md#future-agi) [📖](https://docs.futureagi.com "Docs") [🌐](https://futureagi.com "Website") |

<details><summary>💡 How to choose</summary>

- Confirm SDK support for your framework (OpenTelemetry, LangChain, OpenAI SDK) and your language.
- Evaluation features vary widely; check whether evals run on your data without a cloud account.
- Retention and storage backend decide the host size; traces grow fast.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 🧮 Vector databases

Vector stores and hybrid search engines for embeddings. <sub>9 projects · [📝 all reviews](reviews/vector-db.md)</sub>

| # | Project | ⭐ | 📄 | 🚀 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[Meilisearch](https://github.com/meilisearch/meilisearch)**<br><sub>Rust search engine API with full-text, vector and hybrid search</sub> | 60k | NOASSERTION | 🐳 | [📝](reviews/vector-db.md#meilisearch) [🧪](https://where2watch.meilisearch.com/ "Live demo") [📖](https://www.meilisearch.com/docs "Docs") [🌐](https://www.meilisearch.com "Website") |
| 🥈 | **[Milvus](https://github.com/milvus-io/milvus)**<br><sub>Distributed vector database with dense, sparse and hybrid search at scale</sub> | 46k | Apache-2.0 | 🐳 ✨ | [📝](reviews/vector-db.md#milvus) [🧪](https://milvus.io/milvus-demos "Live demo") [📖](https://milvus.io/docs "Docs") [🌐](https://milvus.io/ "Website") |
| 🥉 | **[Qdrant](https://github.com/qdrant/qdrant)**<br><sub>Rust vector database with payload filtering, REST and gRPC</sub> | 35k | Apache-2.0 | 🐳 ✨ | [📝](reviews/vector-db.md#qdrant) [🧪](https://qdrant.to/semantic-search-demo "Live demo") [📖](https://qdrant.tech/documentation/ "Docs") |
| 4 | **[Chroma](https://github.com/chroma-core/chroma)**<br><sub>Embedding database with a four-function API for Python and JavaScript</sub> | 29k | Apache-2.0 | 🐳 | [📝](reviews/vector-db.md#chroma) [📖](https://docs.trychroma.com/ "Docs") [🌐](https://www.trychroma.com/ "Website") |
| 5 | **[pgvector](https://github.com/pgvector/pgvector)**<br><sub>PostgreSQL extension for vector similarity search with HNSW and IVFFlat</sub> | 23k | NOASSERTION | 🐳 | [📝](reviews/vector-db.md#pgvector) |
| 6 | **[Weaviate](https://github.com/weaviate/weaviate)**<br><sub>Go vector database with built-in vectorizers, hybrid search and RAG</sub> | 17k | NOASSERTION | 🐳 | [📝](reviews/vector-db.md#weaviate) [🧪](https://elysia.weaviate.io "Live demo") [📖](https://docs.weaviate.io "Docs") |
| 7 | **[Vespa](https://github.com/vespa-engine/vespa)**<br><sub>Serving engine for vectors, tensors, text and ML ranking at scale</sub> | 7.1k | Apache-2.0 | – | [📝](reviews/vector-db.md#vespa) [📖](https://docs.vespa.ai "Docs") [🌐](https://vespa.ai "Website") |
| 8 | **[HelixDB](https://github.com/HelixDB/helix-db)**<br><sub>Rust graph database with native vector and BM25 search</sub> | 6.1k | Apache-2.0 | 🐳 | [📝](reviews/vector-db.md#helix-db) [📖](https://docs.helix-db.com "Docs") [🌐](https://helix-db.com "Website") |
| 9 | **[Marqo](https://github.com/marqo-ai/marqo)**<br><sub>Vector search engine with built-in embedding, now deprecated upstream</sub> | 5.0k | Apache-2.0 | 🐳 | [📝](reviews/vector-db.md#marqo) [📖](https://docs.marqo.ai "Docs") [🌐](https://www.marqo.ai "Website") |

<details><summary>💡 How to choose</summary>

- If you already run Postgres, check pgvector-based options before adding a new database.
- Hybrid search (keyword + vector) and filtering are where engines differ most.
- Check memory use per million vectors; it decides the host size.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 🛡️ Sandboxes

Isolated runtimes where agents execute code, browse or use tools safely. <sub>8 projects · [📝 all reviews](reviews/sandboxes.md)</sub>

| # | Project | ⭐ | 📄 | 🚀 | 🔗 |
|:-:|---|--:|---|---|---|
| 🥇 | **[Lightpanda](https://github.com/lightpanda-io/browser)**<br><sub>Headless browser in Zig with CDP, MCP and an agent mode</sub> | 36k | AGPL-3.0 | 🐳 | [📝](reviews/sandboxes.md#lightpanda) [📖](https://lightpanda.io/docs/usage/agent "Docs") [🌐](https://lightpanda.io "Website") |
| 🥈 | **[Obscura](https://github.com/h4ckf0r0day/obscura)**<br><sub>Rust headless browser with CDP, native rendering and stealth mode</sub> | 29k | Apache-2.0 | 🐳 | [📝](reviews/sandboxes.md#obscura) [📖](https://docs.obscura.sh "Docs") [🌐](https://obscura.sh "Website") |
| 🥉 | **[NemoClaw](https://github.com/NVIDIA/NemoClaw)**<br><sub>NVIDIA reference stack running OpenClaw and Hermes inside OpenShell sandboxes</sub> | 23k | Apache-2.0 | 🐳 | [📝](reviews/sandboxes.md#nemoclaw) [📖](https://docs.nvidia.com/nemoclaw/latest/ "Docs") |
| 4 | **[Browser Use Web UI](https://github.com/browser-use/web-ui)**<br><sub>Gradio UI for running browser-use agents with your own Chrome</sub> | 17k | MIT | 🐳 | [📝](reviews/sandboxes.md#browser-use-web-ui) [📖](https://docs.browser-use.com "Docs") |
| 5 | **[OpenShell](https://github.com/NVIDIA/OpenShell)**<br><sub>Policy-enforced sandbox runtime for autonomous agents with credential brokering</sub> | 15k | Apache-2.0 | – | [📝](reviews/sandboxes.md#openshell) [📖](https://docs.nvidia.com/openshell/latest/index.html "Docs") |
| 6 | **[microsandbox](https://github.com/superradcompany/microsandbox)**<br><sub>Local microVMs for untrusted code with fork, snapshot and SDKs</sub> | 8.6k | Apache-2.0 | – | [📝](reviews/sandboxes.md#microsandbox) [📖](https://docs.microsandbox.dev/cli/overview "Docs") |
| 7 | **[Steel Browser](https://github.com/steel-dev/steel-browser)**<br><sub>Browser API that manages Chrome sessions for Puppeteer, Playwright and Selenium</sub> | 7.8k | Apache-2.0 | 🐳 | [📝](reviews/sandboxes.md#steel-browser) [📖](https://docs.steel.dev/ "Docs") [🌐](https://steel.dev "Website") |
| 8 | **[Open Terminal](https://github.com/open-webui/open-terminal)**<br><sub>REST-driven shell and file sandbox for AI agents, from Open WebUI</sub> | 3.3k | MIT | 🐳 | [📝](reviews/sandboxes.md#open-terminal) |

<details><summary>💡 How to choose</summary>

- Isolation level (container, microVM, gVisor) sets the risk you accept when agents run code.
- Check startup time per sandbox; slow starts limit agent loops.
- Look at what is persisted between runs and how secrets are injected.

</details>

<p align="right"><a href="#%EF%B8%8F-contents">↑ contents</a></p>

## 🔧 How it works

- 🔎 **Found by bots** from curated lists, app stores and template galleries, then checked on GitHub: stars, last commit, license, Docker files.
- ✍️ **Written from the README**, not from other lists: what it does, what it needs, strengths and weaknesses as checkable claims. Specs say `unknown` rather than guess.
- 🔄 **Kept current**: entries are rewritten when the README or the latest release changes; projects quiet for 12 months are marked stale, archived ones are removed.

## 📬 Submit, fix or opt out

➕ [Add a project](https://github.com/archestack/best-of-selfhosted-ai/issues/new/choose) · 🛠️ [Report wrong data](https://github.com/archestack/best-of-selfhosted-ai/issues/new/choose) · 🚪 [Opt out](https://github.com/archestack/best-of-selfhosted-ai/issues/new/choose) (honored within 24 hours). The README, reviews and `data/` are generated; please use the forms instead of editing them.

<details><summary>📚 Sources</summary>

Candidates come from these lists, app stores and galleries (facts and links only, no text copied), plus community submissions: [awesome-selfhosted](https://github.com/awesome-selfhosted/awesome-selfhosted) · [awesome-local-llm](https://github.com/rafska/awesome-local-llm) · [compose-examples](https://github.com/Haxxnet/Compose-Examples) · [awesome-homelab](https://github.com/AwesomeHomelab/awesome-homelab) · [self-hosting-guide](https://github.com/mikeroyal/Self-Hosting-Guide) · [awesome-ai-agent-platforms](https://github.com/Agenta-AI/awesome-ai-agent-platforms) · [awesome-openclaw](https://github.com/alvinreal/awesome-openclaw) · [umbrel-apps](https://github.com/getumbrel/umbrel-apps) · [runtipi-appstore](https://github.com/runtipi/runtipi-appstore) · [casaos-appstore](https://github.com/IceWhaleTech/CasaOS-AppStore) · [dokploy-templates](https://templates.dokploy.com/meta.json) · [awesome-opensource-ai](https://github.com/alvinreal/awesome-opensource-ai) · [awesome-llm-services](https://github.com/av/awesome-llm-services) · [awesome-llmops](https://github.com/tensorchord/Awesome-LLMOps) · [awesome-private-ai](https://github.com/tdi/awesome-private-ai) · [awesome-local-llms](https://github.com/vince-lam/awesome-local-llms) · [awesome-llm-webapps](https://github.com/icefort-ai/awesome-llm-webapps).

</details>

## 📄 License

Data (`data/`, this README, `reviews/`) is CC BY 4.0; see LICENSE-DATA. Code is MIT; see LICENSE. Project names and descriptions belong to their owners.

<p align="center"><sub>Maintained by <a href="https://github.com/archestack">Archestack</a> · also see <a href="https://github.com/archestack/best-of-ai-starters">Best of AI Starters</a></sub></p>
