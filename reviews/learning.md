# 📖 Learning and cookbooks reviews · Best of Open-Source AI

Courses, cookbooks and guides with runnable code, for learning to build with AI. Back to the [leaderboard](../README.md#-learning-and-cookbooks).

<sub>🌐 Also on the web: [Learning and cookbooks on archestack.com](https://archestack.com/best-of-ai/learning/), each project on its own page.</sub>

<a name="ai-engineering-from-scratch"></a>
### 🥇 [ai-engineering-from-scratch](https://github.com/rohitg00/ai-engineering-from-scratch) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 71k · MIT · Oct 2026</sub>

**Hands-on AI engineering curriculum with 542 lessons across 20 phases.**

A course where learners implement model internals, retrieval pipelines and agent runtimes in Python, TypeScript, Rust and Julia, from math foundations to LLM engineering and agents. Lessons can be read on the website, taught by coding-agent skills installed with `npx skills add`, or run locally. Three projects (retrieval evaluation, agent trace debugger, tool call firewall) ship with staged starters and local graders.

- **+** 542 lessons in 20 phases, each with runnable code in the repo
- **+** Three staged projects with reference solutions and local graders
- **+** Agent skills act as a tutor with placement and per-phase quizzes
- **+** Website lessons need no setup; early local lessons are dependency-free
- **−** Tutor skills need Node.js, npx, python3 and a supported coding-agent host
- **−** Hardware needs for later phases (GPU, RAM) are unknown from the README excerpt
- **−** Large curriculum with no single linear path; learner must pick a route
- **−** Projects need different toolchains: Python, Node.js 22.18+ and Rust

<sub>Needs Python 3.10+, Node.js 22.18+ (agent trace debugger project), Rust (tool call firewall project), npx (tutor skills) · [Repo](https://github.com/rohitg00/ai-engineering-from-scratch) · [🌐 Site ↗](https://aiengineeringfromscratch.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai-engineering-from-scratch/)</sub>

<a name="generative-ai-for-beginners"></a>
### 🥈 [generative-ai-for-beginners](https://github.com/microsoft/generative-ai-for-beginners) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: fair (62) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 122k · MIT · Oct 2026</sub>

**21-lesson course on building generative AI apps in Python and TypeScript.**

A Microsoft Cloud Advocates course of 21 lessons, each a README with a short video and code samples, split into "Learn" concept lessons and "Build" lessons. Topics include prompt engineering, text and chat apps, embeddings search, image generation, function calling, RAG, agents, fine-tuning, and small, Mistral and Meta models. Code targets Azure OpenAI, OpenAI API, Microsoft Foundry Models or Foundry Local.

- **+** Build lessons ship code in both Python and TypeScript where possible
- **+** Covers RAG, function calling, agents, fine-tuning and security in one sequence
- **+** Lessons are independent, so you can start at any number
- **+** MIT license; translations into 50+ languages
- **−** Samples assume Azure OpenAI, OpenAI API or Foundry access, which may need paid accounts
- **−** Several lessons list video as coming soon
- **−** Cloning includes 50+ translations, so sparse checkout is needed for a small download
- **−** GitHub Models lessons are tied to a service retiring end of July 2026

<sub>no GPU · Needs Azure OpenAI Service, OpenAI API, Microsoft Foundry Models, Foundry Local, GitHub account · Models: Azure OpenAI, OpenAI, Microsoft Foundry Models, Foundry Local, Hugging Face open models · [Repo](https://github.com/microsoft/generative-ai-for-beginners) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/generative-ai-for-beginners/)</sub>

<a name="ai-agents-for-beginners"></a>
### 🥉 [ai-agents-for-beginners](https://github.com/microsoft/ai-agents-for-beginners) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: fair (60) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 77k · MIT · Oct 2026</sub>

**18-lesson course on building AI agents with Microsoft Agent Framework.**

A Microsoft course of 18 lessons on building AI agents, each with a written README, a short video for most lessons, and Python code samples in Jupyter notebooks. Topics include tool use, agentic RAG, planning, multi-agent patterns, memory, MCP/A2A/NLWeb protocols, computer-use agents, local agents and securing agents. Samples use Microsoft Agent Framework with Microsoft Foundry Agent Service V2, and some also support OpenAI-compatible providers such as MiniMax.

- **+** Each lesson is standalone, so you can start at any topic
- **+** Covers design patterns plus MCP, A2A, NLWeb, memory and deployment
- **+** Text, short videos and runnable Python samples per lesson
- **+** 50+ language translations kept current by GitHub Action
- **−** Samples are built around Microsoft Agent Framework and Foundry, which need an Azure account
- **−** Some later lessons have no video
- **−** Cloning pulls large translation folders unless sparse checkout is used
- **−** Alternative provider support is only partial, per the README

<sub>no GPU · Needs Microsoft Foundry (Azure account), Microsoft Agent Framework, Microsoft Foundry Agent Service V2 · Models: Microsoft Foundry models, OpenAI-compatible providers (MiniMax) · [Repo](https://github.com/microsoft/ai-agents-for-beginners) · [📖 Docs ↗](https://github.com/microsoft/ai-agents-for-beginners/blob/master/00-course-setup/README.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai-agents-for-beginners/)</sub>

<a name="ai-agent-book"></a>
### #&#8288;4 [ai-agent-book](https://github.com/bojieli/ai-agent-book) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 55k · Apache-2.0 · Sep 2026</sub>

**Open book on AI agent design, with 109 runnable companion experiments.**

A Chinese-language book, "Understanding AI Agents in Depth", with 10 chapters built on the formula Agent = LLM + context + tools. It covers context engineering, memory and RAG, tools and MCP, coding agents, interaction, evaluation, post-training and multi-agent collaboration. The repo holds the book sources, PDF and EPUB builds in 15 languages, and 109 Python experiments installed per chapter with uv or pip.

- **+** 109 companion experiments mapped to chapters, installable per chapter via uv.lock or pip
- **+** PDF and EPUB in 15 languages, plus an online reader
- **+** Covers evaluation and post-training (SFT/RL), not only prompting and tool use
- **+** External repos are pinned to commit SHAs for reproducible setups
- **−** Original text is Chinese; the other 14 translations are community-made and may lag
- **−** README says experiment code is agent-generated and not read line by line by the author
- **−** Installing or cloning does not mean an experiment was run; status is tracked separately
- **−** Most experiments need provider API keys; some need CUDA, browsers or external repos

<sub>GPU optional · Needs Python 3.11-3.13, uv or pip, LLM provider API keys, pandoc and xelatex (only to build the PDF) · Models: Kimi, GLM, DeepSeek, OpenRouter, Siliconflow · [Repo](https://github.com/bojieli/ai-agent-book) · [📖 Docs ↗](https://bojieli.github.io/ai-agent-book/astro/) · [🌐 Site ↗](https://bojieli.github.io/ai-agent-book/astro/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai-agent-book/)</sub>

<a name="llms-from-scratch"></a>
### #&#8288;5 [llms-from-scratch](https://github.com/rasbt/llms-from-scratch) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 107k · custom license · Oct 2026</sub>

**Code for the book on building a GPT-style LLM in PyTorch.**

Official code for the Manning book "Build a Large Language Model (From Scratch)". Notebooks and scripts implement tokenization, attention, a GPT model, pretraining, classification finetuning, instruction finetuning and LoRA in plain PyTorch, without external LLM libraries. Bonus folders add from-scratch Llama 3.2, Qwen3, Gemma 3, Olmo 3, KV cache, MoE and DPO.

- **+** Main chapter code runs on a conventional laptop and uses a GPU automatically if present
- **+** Plain PyTorch with no external LLM libraries, so every component is readable
- **+** Bonus material covers KV cache, GQA, MoE, DPO and several model architectures
- **+** Exercise solutions, a companion video course and CI tests on Linux, Windows and macOS
- **−** Tied to a print book; contributions extending main chapter code are not accepted
- **−** Produces a small educational model, not a production-grade LLM
- **−** License is reported as NOASSERTION; the README states no license terms
- **−** Video course and quiz PDF are hosted by the publisher, not in the repo

<sub>GPU optional · Needs PyTorch, Jupyter, Ollama (optional, ch07 evaluation) · Models: GPT-2, Llama 3.2, Qwen3, Gemma 3, Olmo 3 · [Repo](https://github.com/rasbt/llms-from-scratch) · [🌐 Site ↗](http://mng.bz/orYv) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llms-from-scratch/)</sub>

<a name="ml-for-beginners"></a>
### #&#8288;6 [ml-for-beginners](https://github.com/microsoft/ml-for-beginners) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: fair (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 92k · MIT · Sep 2026</sub>

**12-week, 26-lesson classic machine learning course using Scikit-learn.**

A Microsoft Cloud Advocates curriculum covering classic machine learning (regression, classification, clustering, NLP) with Scikit-learn, deliberately excluding deep learning. Each lesson has pre- and post-lecture quizzes, a written lesson, a solution, a challenge and an assignment, built around datasets from different world regions. Lessons are in Python, with R Markdown versions for many.

- **+** Project-based lessons with solutions in /solution folders and quizzes for each lesson
- **+** Many lessons also provided in R as .rmd files
- **+** Translated into 50+ languages via automated GitHub Action
- **+** MIT license; can run in GitHub Codespaces without local Python setup
- **−** Covers classic ML only; deep learning is in a separate curriculum
- **−** Not about LLMs or generative AI
- **−** Clone is large because of 50+ translations unless sparse checkout is used
- **−** Per-lesson dependencies must be installed manually

<sub>no GPU · Needs Python, Scikit-learn, Jupyter, R (optional) · [Repo](https://github.com/microsoft/ml-for-beginners) · [▶️ Demo ↗](https://ff-quizzes.netlify.app/en/ml/) · [📖 Docs ↗](https://learn.microsoft.com/en-us/collections/qrqzamz1nn2wx3?WT.mc_id=academic-77952-bethanycheum) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ml-for-beginners/)</sub>

<a name="ai-for-beginners"></a>
### #&#8288;7 [ai-for-beginners](https://github.com/microsoft/ai-for-beginners) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: fair (59) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 70k · MIT · Sep 2026</sub>

**12-week, 24-lesson AI curriculum with PyTorch and TensorFlow notebooks.**

A Microsoft course that teaches AI from symbolic and expert systems through neural networks, computer vision, NLP, genetic algorithms, reinforcement learning, multi-agent systems and ethics. Lessons pair text with Jupyter notebooks in PyTorch and/or TensorFlow/Keras, and several have labs. Translations into 50+ languages are generated by a GitHub Action.

- **+** Covers symbolic AI, deep learning, vision, NLP, RL and ethics in one ordered path
- **+** Most lessons have both PyTorch and TensorFlow/Keras notebooks
- **+** Labs for many lessons, plus a Binder badge to run notebooks in the browser
- **+** 50+ automated translations; MIT license
- **−** NLP stops at transformers/BERT and GPT basics; README admits it lags the state of the art
- **−** Excludes classic ML, cloud services and deep math; it points to other courses
- **−** Not every lesson has a lab; some notebooks are TensorFlow-only or PyTorch-only
- **−** Translations inflate clone size; sparse checkout is needed to skip them

<sub>Needs Jupyter, PyTorch, TensorFlow, Keras, OpenCV · [Repo](https://github.com/microsoft/ai-for-beginners) · [▶️ Demo ↗](https://mybinder.org/v2/gh/microsoft/ai-for-beginners/HEAD) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai-for-beginners/)</sub>

<a name="openai-cookbook"></a>
### #&#8288;8 [openai-cookbook](https://github.com/openai/openai-cookbook) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: fair (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 77k · MIT · Oct 2026</sub>

**Example notebooks and guides for building with the OpenAI API.**

Collection of runnable Jupyter notebooks and guides showing common tasks with the OpenAI API. Most examples are in Python, and the README says the concepts apply to other languages. Running them requires an OpenAI account and an API key set as OPENAI_API_KEY. The guides are also browsable at cookbook.openai.com.

- **+** Maintained by OpenAI, so examples track the official API
- **+** Runnable notebooks; API key is read from OPENAI_API_KEY or a .env file
- **+** Also browsable as a site at cookbook.openai.com
- **+** MIT license
- **−** Requires an OpenAI account and API key; examples do not target local models
- **−** Most examples are Python only
- **−** README does not list topics, versions or per-notebook dependencies
- **−** No tagged releases

<sub>no GPU · Needs OpenAI API key, Jupyter · Models: OpenAI API models · [Repo](https://github.com/openai/openai-cookbook) · [📖 Docs ↗](https://platform.openai.com/docs/introduction) · [🌐 Site ↗](https://cookbook.openai.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openai-cookbook/)</sub>

<a name="cs249r-book"></a>
### #&#8288;9 [cs249r_book](https://github.com/harvard-edge/cs249r_book) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (51) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · custom license · Oct 2026</sub>

**Open textbook and course materials for machine learning systems engineering.**

A single repository holding a four-volume ML systems textbook (foundations, scaling, agentic, physical AI) plus companion material. The companions are Marimo labs, TinyTorch (build an ML framework in 20 modules), Arduino and Raspberry Pi hardware kits, the MLSys·im infrastructure simulator, StaffML interview questions, slides and an instructor hub. Volume I is released; Volume II is a preview; Volumes III and IV are drafts.

- **+** Covers theory, framework internals, edge hardware and cluster modeling in one curriculum
- **+** TinyTorch walks through building an ML framework across 20 progressive modules
- **+** Includes instructor syllabi, rubrics, TA handbook and Beamer slides for every chapter
- **+** Interactive Marimo labs let readers change parameters and see trade-offs
- **−** Volumes III and IV are drafts; README asks readers not to cite or teach from them
- **−** Volume II is only a preview
- **−** License is CC-BY-NC-SA 4.0, which restricts commercial use
- **−** A course, not a deployable tool; little of it runs as a service

<sub>[Repo](https://github.com/harvard-edge/cs249r_book) · [📖 Docs ↗](https://mlsysbook.ai/vol1/) · [🌐 Site ↗](https://mlsysbook.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cs249r-book/)</sub>

<a name="hello-agents"></a>
### #&#8288;10 [hello-agents](https://github.com/datawhalechina/hello-agents) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: fair (53) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 84k · custom license · Oct 2026</sub>

**Chinese-language course on building LLM agents from scratch.**

A 16-chapter Chinese tutorial from Datawhale covering agent fundamentals, ReAct, Plan-and-Solve and Reflection, low-code platforms (Coze, Dify, n8n) and frameworks (AutoGen, AgentScope, LangGraph). Later chapters build a custom framework on the OpenAI API and cover memory, RAG, context engineering, MCP/A2A/ANP, Agentic-RL (SFT to GRPO) and evaluation. Chapter code is in the repo's code folder.

- **+** 16 chapters from theory to capstone, with runnable code in the code folder
- **+** Includes an Agentic-RL chapter going from SFT to GRPO training
- **+** Builds a custom agent framework on the OpenAI API, not only framework usage
- **+** Free online reading and PDF download, plus extra chapters on interviews and skills
- **−** Written in Chinese; an English README is linked separately
- **−** License is CC BY-NC-SA 4.0, which bars commercial use
- **−** Assumes basic Python and experience calling an LLM API
- **−** Hardware and model requirements for the exercises are unknown

<sub>Needs OpenAI-compatible LLM API · Models: OpenAI API · [Repo](https://github.com/datawhalechina/hello-agents) · [📖 Docs ↗](https://datawhalechina.github.io/hello-agents/) · [🌐 Site ↗](https://hello-agents.datawhale.cc) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hello-agents/)</sub>

<a name="rag-techniques"></a>
### #&#8288;11 [rag_techniques](https://github.com/nirdiamant/rag_techniques) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (55) · Freshness: active (99) · Maintenance: fair (65) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · custom license · Oct 2026</sub>

**Jupyter notebooks demonstrating 42 RAG techniques, from basic to advanced.**

A collection of 42 runnable Jupyter notebooks, each implementing one RAG technique such as basic RAG, CSV RAG, reliable RAG, chunk-size selection, proposition chunking and query transformations. Notebooks open on GitHub or Colab, and some have companion videos. The README also promotes the author's course, book and newsletter.

- **+** 42 notebooks, each covering a single technique, grouped from foundational to advanced
- **+** Colab badges let notebooks run without local setup
- **+** Covers evaluation notebooks (End-to-End RAG Evaluation, Open-RAG-Eval) as well as retrieval methods
- **+** Updated recently; last commit 2026-09-21
- **−** Teaching notebooks, not a library or deployable RAG system
- **−** README is heavy with course, book and newsletter promotion
- **−** License is not detected (NOASSERTION), so reuse terms are unclear
- **−** Required API keys and package versions are not stated in the visible README

<sub>Needs Jupyter, Google Colab (optional) · [Repo](https://github.com/nirdiamant/rag_techniques) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rag-techniques/)</sub>

<a name="claude-cookbooks"></a>
### #&#8288;12 [claude-cookbooks](https://github.com/anthropics/claude-cookbooks) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: patchy (36) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 54k · MIT · Oct 2026</sub>

**Jupyter notebooks of copy-able Claude API recipes in Python.**

Anthropic's collection of runnable notebooks and guides for building with the Claude API. Recipes cover classification, RAG, summarization, tool use, vision, sub-agents, JSON mode, prompt caching, evals and cost optimization. Examples are mainly Python, and a Claude API key is required.

- **+** Covers tool use, RAG, vision, prompt caching and evals with runnable notebooks
- **+** Maintained by Anthropic, so examples target the Claude API directly
- **+** MIT licensed, snippets can be copied into your own projects
- **+** Includes third-party recipes such as Pinecone, Voyage AI embeddings and Wikipedia search
- **−** Requires a Claude API key; examples do not run on local models
- **−** Examples are primarily Python; other languages must be adapted
- **−** Recipe links in the README point to the older anthropic-cookbook repo path
- **−** Reference snippets, not an installable library or application

<sub>no GPU · Needs Claude API key, Pinecone (some recipes), Voyage AI (some recipes) · Models: Claude · [Repo](https://github.com/anthropics/claude-cookbooks) · [📖 Docs ↗](https://docs.claude.com/claude/docs/guide-to-anthropics-prompt-engineering-resources) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/claude-cookbooks/)</sub>

<a name="agents-towards-production"></a>
### #&#8288;13 [agents-towards-production](https://github.com/nirdiamant/agents-towards-production) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: known (31) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · custom license · Oct 2026</sub>

**Jupyter tutorials for taking LLM agents from prototype to production.**

A collection of 28 tutorial notebooks on production concerns for GenAI agents: stateful workflows with LangGraph, memory (Redis, Mem0), web search APIs, FastAPI and Docker deployment, guardrails, GPU deployment, observability and evaluation. Many tutorials are contributed by vendors the README lists as sponsors. The README also promotes the author's paid course and newsletter.

- **+** 28 tutorials covering memory, deployment, guardrails, GPU scaling, evaluation and UI
- **+** Spans several stacks: LangGraph, Redis, Mem0, Arcade, Inngest, and Kotlin with JetBrains Koog
- **+** Each topic has its own tutorials/ folder, so one can be read without the rest
- **−** Many tutorials are sponsor-contributed and built around the sponsor's hosted product
- **−** Several tutorials need external services such as Tavily, Bright Data and RunPod
- **−** README leads with course and newsletter promotion before the tutorial list
- **−** License is not identified (NOASSERTION); no releases or versioning

<sub>GPU optional · Needs LangGraph, Redis, Mem0, Tavily, Bright Data, Contextual AI, Arcade, RunPod, Inngest · [Repo](https://github.com/nirdiamant/agents-towards-production) · [🌐 Site ↗](https://www.diamant-ai.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agents-towards-production/)</sub>

<a name="self-llm"></a>
### #&#8288;14 [self-llm](https://github.com/datawhalechina/self-llm) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: patchy (40) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · Apache-2.0 · Sep 2026</sub>

**Chinese-language tutorials for deploying and fine-tuning open LLMs on Linux.**

A Datawhale tutorial collection, written mostly in Chinese, that walks through environment setup, local deployment and fine-tuning for 50+ open LLMs such as Qwen, GLM, InternLM, Llama and DeepSeek. Content is Jupyter notebooks and Markdown covering CLI calls, online demos, LangChain integration, LoRA, P-Tuning and distributed full fine-tuning. It also has sections for AMD ROCm, Ascend NPU and Apple M hardware.

- **+** Covers 50+ open models, each with its own deployment and fine-tuning tutorial
- **+** Hardware tracks for AMD ROCm, Ascend NPU and Apple M, beyond NVIDIA
- **+** Worked examples such as LoRA fine-tuning on Zhen Huan dialogue and an advanced-math model
- **+** Active community project with many named contributors and Apache-2.0 license
- **−** Main README and tutorials are in Chinese; English README is a separate file
- **−** Linux-centered; the MetaX section is marked Coming Soon
- **−** Tutorials are tied to specific model versions and may age as models change
- **−** No installable package or app; notebooks only, with no stated hardware requirements

<sub>Needs Linux, Jupyter · Models: Qwen, GLM, InternLM, Llama, DeepSeek · [Repo](https://github.com/datawhalechina/self-llm) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/self-llm/)</sub>

<a name="genai-agents"></a>
### #&#8288;15 [genai_agents](https://github.com/nirdiamant/genai_agents) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: known (41) · Freshness: active (100) · Maintenance: patchy (45) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · custom license · Oct 2026</sub>

**Notebook tutorials for building GenAI agents with LangGraph, LangChain and AutoGen.**

A collection of 57 Jupyter notebooks that walk through agent designs, from simple conversational and Q&A agents to multi-agent systems. Most examples use LangGraph, with others using LangChain, PydanticAI, AutoGen and MCP, across business, educational and creative use cases. The README also promotes the author's paid course and newsletter.

- **+** 57 notebooks spanning beginner to multi-agent examples, each runnable on its own
- **+** Covers several frameworks: LangGraph, LangChain, PydanticAI, AutoGen, MCP
- **+** Applied examples such as contract analysis, customer support and E2E testing agents
- **+** Companion blog post and YouTube explainers for some topics
- **−** Tutorial code, not an installable library or deployable agent product
- **−** Most notebooks depend on LangGraph or LangChain, so framework coverage is narrow
- **−** README carries heavy course, newsletter and sponsor promotion
- **−** License is not identified (NOASSERTION); no releases published

<sub>Needs LangGraph, LangChain, LLM provider API · [Repo](https://github.com/nirdiamant/genai_agents) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/genai-agents/)</sub>

<a name="ml-engineering"></a>
### #&#8288;16 [ml-engineering](https://github.com/stas00/ml-engineering) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (27) · Freshness: active (100) · Maintenance: fair (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · CC-BY-SA-4.0 · Oct 2026</sub>

**Open book of guides and scripts for training LLMs and VLMs at scale.**

A written collection of notes, copy-paste commands and scripts on training, fine-tuning and running large language and multi-modal models, drawn from the author's work on BLOOM-176B and IDEFICS-80B. It covers accelerators, storage, networking, SLURM, training, inference, debugging and testing. It also ships two SKILL.md files for AI agents and PDF/EPUB ebook builds.

- **+** Runnable tools: torch-dist-bench.py for network throughput, mamf-finder.py for real accelerator TFLOPS
- **+** Covers hardware, SLURM, debugging and inference, not only training
- **+** Links a collection of public LLM/VLM training logbooks
- **+** PDF and EPUB downloads, plus two SKILL.md files for AI agents
- **−** Reference text, not an installable framework or library
- **−** Described by the author as a personal brain dump; coverage may be uneven
- **−** Ebooks are rebuilt only every few weeks, so they can lag the repo
- **−** License is CC-BY-SA-4.0; share-alike applies to derived content

<sub>GPU optional · Needs PyTorch, SLURM · [Repo](https://github.com/stas00/ml-engineering) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ml-engineering/)</sub>

<a name="ai-engineering-hub"></a>
### #&#8288;17 [ai-engineering-hub](https://github.com/patchy631/ai-engineering-hub) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: popular (66) · Freshness: active (100) · Maintenance: weak (24) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · MIT · Oct 2026</sub>

**Collection of 93 runnable AI tutorials on RAG, agents, MCP and fine-tuning.**

A monorepo of about 93 example projects, mostly Jupyter notebooks and small apps, grouped into beginner, intermediate and advanced tiers. Topics include local OCR, RAG with LlamaIndex and Ollama, CrewAI and AutoGen agents, MCP servers, voice agents, model comparisons and fine-tuning with Unsloth. Each project sits in its own folder with its own dependencies.

- **+** Roughly 93 self-contained projects, each in its own folder
- **+** Wide coverage: RAG, agents, MCP, voice, OCR, fine-tuning, evaluation
- **+** Projects sorted into beginner, intermediate and advanced tiers
- **+** MIT license; many examples run locally with Ollama and open models
- **−** No single install; each project has its own dependencies and setup
- **−** Many examples need third-party API keys such as Firecrawl or AssemblyAI
- **−** Example code, not a maintained library; 'production-ready' claim is unsupported
- **−** No releases or versioning; project freshness and quality vary

<sub>Needs Ollama, LlamaIndex, CrewAI, Qdrant, Milvus, Firecrawl, AssemblyAI, Opik · Models: Llama 3.2, Llama 3.3, Llama 4, DeepSeek-R1, Qwen3 · [Repo](https://github.com/patchy631/ai-engineering-hub) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai-engineering-hub/)</sub>

<a name="mcp-for-beginners"></a>
### #&#8288;18 [mcp-for-beginners](https://github.com/microsoft/mcp-for-beginners) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: niche (16) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · MIT · Oct 2026</sub>

**Hands-on curriculum for building Model Context Protocol servers and clients.**

A Microsoft course on the Model Context Protocol, organized as numbered modules from core concepts and security to building servers, clients, auth, deployment and a PostgreSQL lab path. Code samples cover C#, Java, JavaScript, Rust, Python and TypeScript. It targets MCP specification 2026-07-28, though some examples are still pinned to 2025-11-25.

- **+** Samples in six languages: C#, Java, JavaScript, Rust, Python, TypeScript
- **+** Covers stdio and HTTP streaming transports, testing, deployment, OAuth2 and Entra ID auth
- **+** Includes a 13-lab PostgreSQL-backed MCP server path as a capstone
- **+** Tracks the 2026-07-28 spec with a migration guide; 50+ translations
- **−** Some examples remain pinned to spec 2025-11-25 while SDK support catches up
- **−** Several modules lean on Microsoft products such as Azure, Foundry and Entra ID
- **−** Clone is large because of 50+ translations unless sparse checkout is used
- **−** Course material only, not a reusable library or server

<sub>no GPU · Needs Azure (some modules), PostgreSQL (module 11) · [Repo](https://github.com/microsoft/mcp-for-beginners) · [📖 Docs ↗](https://modelcontextprotocol.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mcp-for-beginners/)</sub>

<a name="learnopencv"></a>
### #&#8288;19 [learnopencv](https://github.com/spmallick/learnopencv) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: known (36) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 23k · no license · Oct 2026</sub>

**Code for LearnOpenCV blog tutorials on computer vision and deep learning.**

Per-article code folders for the LearnOpenCV.com blog, mostly Jupyter notebooks plus Python and C++ examples. Topics run from classic OpenCV (contours, calibration, optical flow, homography) to YOLO26, RF-DETR, SAM 3, VLMs, RAG and edge deployment on Jetson and Arduino. Maintained by BigVision.AI, a consulting company.

- **+** Covers classic OpenCV and recent models (YOLO26, SAM 3, Qwen3-VL) in one repo
- **+** Many tutorials provide both Python and C++ versions
- **+** Each blog post links to its own code folder
- **+** Active: last commit 2026-10-06, last release 2026-08-29
- **−** No license declared, so reuse terms are unclear
- **−** Several recent posts list no code folder
- **−** Each folder has its own dependencies; no shared environment or Docker setup
- **−** Meant to be read alongside the blog, not used as a library

<sub>GPU optional · Needs OpenCV, Python, C++ · Models: YOLO26, RF-DETR, SAM 3, Qwen3-VL, MiniCPM-o 4.5 · [Repo](https://github.com/spmallick/learnopencv) · [🌐 Site ↗](https://www.LearnOpenCV.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/learnopencv/)</sub>

<a name="cookbook"></a>
### #&#8288;20 [cookbook](https://github.com/google-gemini/cookbook) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (19) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · Apache-2.0 · Oct 2026</sub>

**Jupyter notebook tutorials for the Gemini API, from basics to Live API and agents.**

Official Google collection of Colab-ready notebooks for the hosted Gemini API. Quickstarts cover prompting, thinking levels, TTS, Live API, transcription, image, video and music generation, grounding, code execution, File Search and an Agents API. A separate Examples folder combines several features into larger use cases.

- **+** Maintained by Google; notebooks track new Gemini models and API features
- **+** Each quickstart has an Open in Colab link, so no local setup is required
- **+** Covers many modalities: text, speech, Live API, image, video, music, transcription
- **+** Apache-2.0 licensed with separate Quickstarts and Examples sections
- **−** Requires a Google account and a Google AI Studio API key
- **−** All examples call the hosted Gemini API; nothing runs locally
- **−** Gemma and end-to-end demos live in separate repositories
- **−** Notebooks are tied to current Gemini model names and may go stale

<sub>no GPU · Needs Gemini API key (Google AI Studio), Google account, Google Colab (optional) · Models: Gemini, Veo, Lyria, Nano-Banana · [Repo](https://github.com/google-gemini/cookbook) · [📖 Docs ↗](https://ai.google.dev/gemini-api/docs) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cookbook/)</sub>

<a name="happy-llm"></a>
### #&#8288;21 [happy-llm](https://github.com/datawhalechina/happy-llm) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: popular (62) · Freshness: active (93) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · custom license · Aug 2026</sub>

**Chinese-language course on LLM theory and building a LLaMA2-style model.**

Happy-LLM is a Datawhale course in eight chapters, written in Chinese with an English README. It covers NLP basics, the Transformer and pretrained model families, then implements LLaMA2 in PyTorch, trains a tokenizer, and runs pretraining, SFT, LoRA/QLoRA, RAG, agents and GRPO-based agentic RL. Two 215M checkpoints from chapter 5 are published on ModelScope.

- **+** Covers Transformer basics through pretraining, SFT, LoRA/QLoRA, RAG, agents and agentic RL
- **+** Publishes 215M base and SFT checkpoints plus a ModelScope studio to try them
- **+** Free PDF and companion slides available from the releases page
- **+** Dependencies split per chapter, with an environment preparation guide
- **−** Main content is in Chinese; only the README has an English version
- **−** Content license is CC BY-NC-SA 4.0, which restricts commercial use
- **−** Hardware requirements are not stated in the README, only in a separate doc
- **−** Extra Chapter blog section is marked as in progress

<sub>Needs PyTorch, Transformers · Models: LLaMA2, Happy-LLM-215M-base, Happy-LLM-215M-sft · [Repo](https://github.com/datawhalechina/happy-llm) · [▶️ Demo ↗](https://www.modelscope.cn/studios/kmno4zx/happy_llm_215M_sft) · [📖 Docs ↗](https://datawhalechina.github.io/happy-llm/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/happy-llm/)</sub>

<a name="100-days-of-ml-code"></a>
### #&#8288;22 [100-days-of-ml-code](https://github.com/mleveryday/100-days-of-ml-code) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: known (34) · Freshness: active (100) · Maintenance: patchy (30) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Oct 2026</sub>

**Chinese-language machine learning course with daily scikit-learn and Keras exercises.**

Chinese adaptation of Avik-Jain's 100-Days-Of-ML-Code, with each lesson as a Python script plus generated Markdown and Jupyter notebook. Days 1 to 54 are written, covering preprocessing, regression, SVM, trees, neural networks, CNNs on MNIST and cats/dogs, and clustering. Days 55 to 100 are not yet written.

- **+** Code updated for current scikit-learn and Keras 3, with Python 3.11/3.12 setup docs
- **+** Each lesson ships as script, Markdown and notebook, generated by tools/sync_lessons.py
- **+** Basic lessons need no GPU; deep learning dependencies are installed separately
- **+** Includes an FAQ on data leakage and a dataset guide with field descriptions
- **−** Only Day 1 to 54 of 100 are written
- **−** Chinese only; the README shows no English lessons
- **−** Some theory days still rely on images and external video as supplements
- **−** No releases published

<sub>GPU optional · Needs Python 3.11/3.12, scikit-learn, Keras 3, Jupyter · [Repo](https://github.com/mleveryday/100-days-of-ml-code) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/100-days-of-ml-code/)</sub>

<a name="generative-ai"></a>
### #&#8288;23 [generative-ai](https://github.com/googlecloudplatform/generative-ai) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: patchy (42) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · Apache-2.0 · Oct 2026</sub>

**Notebooks and sample apps for Gemini, Imagen, Veo and Chirp on Google Cloud.**

Jupyter notebooks, code samples and sample apps for building with Gemini, Imagen, Veo and Chirp through Google Cloud's Agent Platform. Folders cover Gemini starters and function calling, Agent Search, RAG and grounding, vision, audio and environment setup. It needs a Google Cloud account, and the README says the code is demonstrative and not an officially supported Google product.

- **+** Organized by topic: Gemini, Agent Search, RAG and grounding, vision, audio, setup
- **+** Links to related Google repos such as ADK Samples and Agent Starter Pack
- **+** Setup guide covers the Gen AI Python SDK, Colab and Workbench
- **+** Apache-2.0 licensed with recent commits
- **−** Tied to Google Cloud services and Google models; no local or open-weight models
- **−** README states code is demonstrative and not officially supported
- **−** Notebooks are samples, not a deployable app or reusable library
- **−** No releases or versioning

<sub>no GPU · Needs Google Cloud account, Agent Platform, Gen AI Python SDK, Google Colab or Workbench · Models: Gemini, Imagen, Veo, Chirp · [Repo](https://github.com/googlecloudplatform/generative-ai) · [📖 Docs ↗](https://docs.cloud.google.com/gemini-enterprise-agent-platform) · [🌐 Site ↗](https://cloud.google.com/ai/generative-ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/generative-ai/)</sub>

<a name="handson-ml"></a>
### #&#8288;24 [handson-ml](https://github.com/ageron/handson-ml) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: known (47) · Freshness: recent (77) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · Apache-2.0 · May 2026</sub>

**Jupyter notebooks for the first edition of Hands-on Machine Learning book.**

Example code and exercise solutions for the 2017 first edition of Aurélien Géron's O'Reilly book on Scikit-Learn and TensorFlow, written as Jupyter notebooks. The README states the edition is outdated and points to the third edition and a PyTorch version in separate repositories. Notebooks can be run in Colab, Binder or Deepnote, or locally via a conda environment (tf1) on Python 3.7.

- **+** Covers book examples and exercise solutions as runnable notebooks
- **+** Runs in Colab, Binder or Deepnote without local install
- **+** Provides environment.yml for conda and Docker instructions
- **+** Apache-2.0 licensed
- **−** First edition from 2017; README says it is outdated
- **−** Targets TensorFlow 1 and Python 3.7, which are old
- **−** Newer editions live in separate repositories
- **−** Needs the book for full explanations

<sub>GPU optional · Docker + Compose · Needs Anaconda or Miniconda, git, Jupyter, TensorFlow 1, Scikit-Learn · [Repo](https://github.com/ageron/handson-ml) · [▶️ Demo ↗](https://colab.research.google.com/github/ageron/handson-ml/blob/master/) · [🌐 Site ↗](https://homl.info/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/handson-ml/)</sub>

<a name="llm-course"></a>
### #&#8288;25 [llm-course](https://github.com/mlabonne/llm-course) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: widely used (92) · Freshness: slowing (40) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 84k · Apache-2.0 · Feb 2026</sub>

**Free LLM course with roadmaps and Colab notebooks for fine-tuning and quantization.**

A three-part course covering LLM fundamentals (math, Python, neural networks), an LLM Scientist track on building models, and an LLM Engineer track on building and deploying applications. It pairs roadmaps and curated links with Colab notebooks and articles on fine-tuning (Unsloth, ORPO, DPO, QLoRA, Axolotl), quantization (GGUF, GPTQ, EXL2) and model merging with MergeKit.

- **+** Runnable Colab notebooks for fine-tuning, quantization and merging, most with a linked article
- **+** Separate tracks for fundamentals, model building and application deployment
- **+** Quantization notebooks cover GGUF, GPTQ, EXL2, AWQ and HQQ
- **+** Free to use under Apache-2.0
- **−** Mostly curated external links rather than self-contained lessons
- **−** Several notebooks target older models such as Llama 2 and Mistral-7b
- **−** Notebooks run on Google Colab or RunPod, not a documented local setup
- **−** Coverage reflects one author's selection of topics and resources

<sub>GPU optional · Needs Google Colab, RunPod, Hugging Face · Models: Llama 3.1, Llama 3, Llama 2, Mistral-7b, CodeLlama · [Repo](https://github.com/mlabonne/llm-course) · [📖 Docs ↗](https://deepwiki.com/mlabonne/llm-course/) · [🌐 Site ↗](https://mlabonne.github.io/blog) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llm-course/)</sub>

<a name="made-with-ml"></a>
### #&#8288;26 [made-with-ml](https://github.com/gokumohandas/made-with-ml) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: popular (72) · Freshness: recent (61) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 50k · MIT · Mar 2026</sub>

**MLOps course with code for training, tuning, and serving a text classifier.**

A course repository that walks through building a text classifier end to end: a Jupyter notebook, then refactored Python scripts for training, tuning, evaluation, inference and serving. It uses Ray for distributed workloads, MLflow for experiment tracking, pytest for code, data and model tests, and Anyscale Jobs and Services for production deployment.

- **+** Covers the full path: notebook, scripts, tests, MLflow tracking, Ray Serve, CI/CD
- **+** Runs on a laptop without a GPU, with configurable worker counts
- **+** Separate pytest suites for code, data and trained models
- **+** Plain Python scripts with documented CLI arguments for each workload
- **−** Production section depends on Anyscale (account, CLI token, S3 upload paths)
- **−** Example task is a small text classifier, not an LLM application
- **−** Setup is built around Ray; other stacks need adaptation
- **−** README promotes a paid live cohort

<sub>GPU optional · Needs Ray, MLflow, Anyscale, AWS S3, pytest, pre-commit · port 8000 · [Repo](https://github.com/gokumohandas/made-with-ml) · [📖 Docs ↗](https://madewithml.com/) · [🌐 Site ↗](https://madewithml.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/made-with-ml/)</sub>

<a name="fastbook"></a>
### #&#8288;27 [fastbook](https://github.com/fastai/fastbook) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: known (45) · Freshness: recent (70) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · custom license · Oct 2026</sub>

**Jupyter notebooks for the fastai and PyTorch deep learning book and course.**

The notebooks behind "Deep Learning for Coders with fastai and PyTorch", covering 20 chapters from a Jupyter intro through image classification, tabular, NLP and collaborative filtering to ResNets, optimizers, GradCAM and building a Learner from scratch. They also serve as the material for the fast.ai MOOC. Each chapter opens in Google Colab, so no local setup is needed.

- **+** Runs in Google Colab from per-chapter links, no local Python setup required
- **+** Covers 20 chapters, from basic classifiers to writing a Learner from scratch
- **+** Tied to a published O'Reilly book and the fast.ai MOOC
- **+** Code is GPL v3, and the repo still receives commits
- **−** Prose and markdown cells are not licensed for redistribution or commercial use
- **−** Teaches fastai and PyTorch; README mentions no LLM or agent content
- **−** Last tagged release is from 2022-04
- **−** Pull requests assign copyright to the authors

<sub>Needs fastai, PyTorch, Jupyter, Google Colab (optional) · [Repo](https://github.com/fastai/fastbook) · [📖 Docs ↗](https://docs.fast.ai/) · [🌐 Site ↗](https://course.fast.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fastbook/)</sub>

<a name="micrograd"></a>
### #&#8288;28 [micrograd](https://github.com/karpathy/micrograd) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · MIT · Aug 2026</sub>

**Scalar-valued autograd engine and tiny neural net library in about 150 lines of Python.**

micrograd implements reverse-mode autodiff over a dynamically built DAG of scalar values, with a small PyTorch-like neural network module on top. The engine is about 100 lines and the nn library about 50. A demo notebook trains a 2-layer MLP with two 16-node hidden layers as a binary classifier on the moon dataset, using an SVM max-margin loss and SGD.

- **+** Engine and nn library are about 100 and 50 lines, readable in one sitting
- **+** PyTorch-like API: Value, Neuron and MLP classes with backward()
- **+** Notebook demos training on the moon dataset and graphviz graph tracing
- **+** Unit tests check gradients against PyTorch as a reference
- **−** Operates on scalars only, so no tensors and very slow for real models
- **−** No GPU support
- **−** Demo covers only binary classification with an SVM loss and SGD
- **−** Tests need PyTorch installed; no tagged releases

<sub>no GPU · Needs PyTorch (tests only), graphviz (tracing notebook) · [Repo](https://github.com/karpathy/micrograd) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/micrograd/)</sub>

<a name="hands-on-large-language-models"></a>
### #&#8288;29 [hands-on-large-language-models](https://github.com/handsonllm/hands-on-large-language-models) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: popular (53) · Freshness: recent (68) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Apr 2026</sub>

**Companion notebooks for the O'Reilly book Hands-On Large Language Models.**

Code for every example in the book by Jay Alammar and Maarten Grootendorst, as one Jupyter notebook per chapter. Chapters cover tokens and embeddings, transformer internals, classification, clustering, prompt engineering, semantic search and RAG, multimodal models, and fine-tuning. Notebooks were built and tested on Google Colab with a free 16GB T4 GPU.

- **+** One notebook per chapter (12), each with an Open in Colab link
- **+** Covers embeddings, RAG, multimodal models and fine-tuning of BERT and generation models
- **+** Tested mainly on free Colab T4 16GB, so no local GPU is required
- **+** Bonus folder links to visual guides on Mamba, quantization and mixture of experts
- **−** Explanatory text and figures are in the paid book, not in the repo
- **−** Local setup is only a quick-start guide; results may differ by OS and versions
- **−** No tagged releases; README states no pinned package versions
- **−** Not a library or tool, only teaching code

<sub>GPU optional · Needs Google Colab, Jupyter, PyTorch · [Repo](https://github.com/handsonllm/hands-on-large-language-models) · [🌐 Site ↗](https://www.oreilly.com/library/view/hands-on-large-language/9781098150952/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hands-on-large-language-models/)</sub>

<a name="annotated-deep-learning-paper-implementations"></a>
### #&#8288;30 [annotated_deep_learning_paper_implementations](https://github.com/labmlai/annotated_deep_learning_paper_implementations) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: widely used (80) · Freshness: slowing (35) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 68k · MIT · Jan 2026</sub>

**Annotated PyTorch implementations of deep learning papers with side-by-side notes.**

A collection of short PyTorch implementations of neural network architectures and algorithms, each rendered on nn.labml.ai as code beside explanatory notes. It covers transformers (including Flash Attention in Triton, RoPE, ALiBi), LoRA, diffusion models, GANs, reinforcement learning, optimizers, normalization layers and more. Installable as the labml-nn pip package.

- **+** Broad coverage: transformers, diffusion, GANs, RL, optimizers, normalization, LoRA, GNNs, CFR
- **+** Each implementation has side-by-side code and explanation on a hosted website
- **+** Compact PyTorch code that is readable for studying the original papers
- **+** MIT license; install with pip install labml-nn
- **−** Written for study, not as an optimized production library
- **−** No release tags; versioning is only via the pip package
- **−** Many entries cover older papers; recent architectures are sparse
- **−** README gives no hardware requirements beyond GPU notes for the GPT-NeoX examples

<sub>GPU optional · Needs PyTorch · Models: PyTorch, JAX (transformer example), Triton (Flash Attention) · [Repo](https://github.com/labmlai/annotated_deep_learning_paper_implementations) · [📖 Docs ↗](https://nn.labml.ai/index.html) · [🌐 Site ↗](https://nn.labml.ai/index.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/annotated-deep-learning-paper-implementations/)</sub>

<a name="cv"></a>
### #&#8288;31 [cv](https://github.com/accumulatemore/cv) <sub>score [34](../README.md#-how-we-rank "Score 34/100. Adoption: known (39) · Freshness: active (100) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 24k · no license · Sep 2026</sub>

**Chinese-language Jupyter notes on deep learning, CV, NLP, LLMs and agents.**

Jupyter Notebook study notes in Chinese, numbered to follow video courses by 土堆 (PyTorch, notes 100-122), 李沐 (200-268), 吴恩达 (300-354) and 大飞 (LLM agents, 400-409). Course datasets are shared through a Baidu Netdisk link. Much of the README is promotion for chat groups, job referrals and mentoring rather than technical content.

- **+** Notes are numbered to match specific video courses, so they can be followed alongside them
- **+** Spans PyTorch basics through CV, NLP, LLMs and agents in one repository
- **+** Course datasets are shared via a Baidu Netdisk link
- **−** No license declared, so reuse rights are unclear
- **−** README is Chinese only, with no English version
- **−** Most README text is job referral and mentoring promotion
- **−** GitHub renders images and formulas poorly; notes must be opened locally in Anaconda Jupyter

<sub>Needs Jupyter Notebook (Anaconda), Baidu Netdisk (datasets) · [Repo](https://github.com/accumulatemore/cv) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cv/)</sub>

<a name="homemade-machine-learning"></a>
### #&#8288;32 [homemade-machine-learning](https://github.com/trekhleb/homemade-machine-learning) <sub>score [17](../README.md#-how-we-rank "Score 17/100. Adoption: known (43) · Freshness: quiet (13) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · MIT · Nov 2025</sub>

**From-scratch Python implementations of classic ML algorithms with Jupyter demos.**

Educational repository implementing linear regression, logistic regression, k-means, Gaussian anomaly detection and a multilayer perceptron in Python, each with a math write-up. Every algorithm has a Jupyter notebook demo on datasets such as MNIST, Fashion MNIST and Iris, viewable in NBViewer or runnable in Binder. The author states the code is for learning, not production.

- **+** Each algorithm has a math explanation, a Python implementation and a notebook demo
- **+** Notebooks open in NBViewer or Binder without a local install
- **+** Demos use concrete datasets: MNIST, Fashion MNIST, Iris, country happiness
- **−** Author states the implementations are not intended for production use
- **−** Covers only a handful of classic algorithms; no CNNs, transformers or LLMs
- **−** Explanations largely follow Andrew Ng's Coursera course
- **−** No releases; last commit 2025-11-23

<sub>no GPU · Needs Python, Jupyter Notebook · port 8888 · [Repo](https://github.com/trekhleb/homemade-machine-learning) · [▶️ Demo ↗](https://mybinder.org/v2/gh/trekhleb/homemade-machine-learning/master?filepath=notebooks) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/homemade-machine-learning/)</sub>

<a name="llama-cookbook"></a>
### #&#8288;33 [llama-cookbook](https://github.com/meta-llama/llama-cookbook) <sub>score [9](../README.md#-how-we-rank "Score 9/100. Adoption: niche (24) · Freshness: quiet (4) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Nov 2025</sub>

**Official Meta notebooks for running, fine-tuning and building apps with Llama models.**

Meta's cookbook of Jupyter notebooks and scripts covering Llama inference, fine-tuning, RAG and end-to-end use cases, such as a WhatsApp bot on Llama API, research paper analysis and book character mind maps. It also holds third-party provider recipes and the source of the original llama-recipes fine-tuning library. Recipes target Llama 4 text and vision models, with older Llama versions covered too.

- **+** Maintained by Meta, with recipes for Llama 4 Scout and Maverick
- **+** Covers inference, fine-tuning, RAG and end-to-end apps in one repository
- **+** Includes third-party provider integrations and a fine-tuning FAQ
- **+** MIT-licensed code
- **−** Llama-specific; recipes do not target other model families
- **−** Model weights fall under separate Meta Llama licenses and use policies
- **−** Last tagged release is January 2025; repo refactor broke some old links
- **−** Notebook format; no installable app or service

<sub>Needs Jupyter, Llama API (some recipes), Hugging Face · Models: Llama 4, Llama 3.3, Llama 3.2, Llama 3.1, Llama 3 · [Repo](https://github.com/meta-llama/llama-cookbook) · [📖 Docs ↗](https://www.llama.com/docs/overview/) · [🌐 Site ↗](https://www.llama.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llama-cookbook/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
