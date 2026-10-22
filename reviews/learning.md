# 📖 Learning and cookbooks reviews · Best of Open-Source AI

Courses, cookbooks and guides with runnable code, for learning to build with AI. Back to the [leaderboard](../README.md#-learning-and-cookbooks).

<sub>🌐 Also on the web: [Learning and cookbooks on archestack.com](https://archestack.com/best-of-ai/learning/), each project on its own page.</sub>

<a name="ai-engineering-from-scratch"></a>
### 🥇 [ai-engineering-from-scratch](https://github.com/rohitg00/ai-engineering-from-scratch) <sub>score [90](../README.md#-how-we-rank "Score 90/100. Adoption: widely used (90) · Freshness: active (100) · Maintenance: healthy (96) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 72k · MIT · Oct 2026</sub>

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
### 🥈 [generative-ai-for-beginners](https://github.com/microsoft/generative-ai-for-beginners) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: fair (62) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 122k · MIT · Oct 2026</sub>

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
### 🥉 [ai-agents-for-beginners](https://github.com/microsoft/ai-agents-for-beginners) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: fair (60) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 78k · MIT · Oct 2026</sub>

**18-lesson course on building AI agents with Microsoft Agent Framework.**

A Microsoft course of 18 lessons on building AI agents. Each lesson has a written README and Python samples, and most have a short video. Topics include tool use, agentic RAG, planning, multi-agent design, memory, MCP/A2A/NLWeb, computer use agents, deployment and security. Samples use Microsoft Agent Framework with Foundry Agent Service V2, and some accept OpenAI-compatible providers such as MiniMax.

- **+** Covers design patterns, RAG, memory, protocols, deployment and security across 18 lessons
- **+** Each lesson pairs a README with Python samples; most also have a video
- **+** Translated into 50+ languages via Co-op Translator
- **+** MIT license; lessons can be taken in any order
- **−** Samples depend on Microsoft Foundry, which requires an Azure account
- **−** Code centers on Microsoft Agent Framework, not other agent libraries
- **−** Lessons 14 to 18 have no video listed
- **−** Clone is large unless translations are excluded with sparse checkout

<sub>no GPU · Needs Microsoft Foundry (Azure account), Microsoft Agent Framework, Microsoft Foundry Agent Service V2 · Models: Microsoft Foundry models, OpenAI-compatible providers (MiniMax) · [Repo](https://github.com/microsoft/ai-agents-for-beginners) · [📖 Docs ↗](https://github.com/microsoft/ai-agents-for-beginners/blob/master/00-course-setup/README.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai-agents-for-beginners/)</sub>

<a name="cs249r-book"></a>
### #&#8288;4 [cs249r_book](https://github.com/harvard-edge/cs249r_book) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · custom license · Oct 2026</sub>

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

<a name="llms-from-scratch"></a>
### #&#8288;5 [llms-from-scratch](https://github.com/rasbt/llms-from-scratch) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 107k · custom license · Oct 2026</sub>

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

<a name="ai-for-beginners"></a>
### #&#8288;6 [ai-for-beginners](https://github.com/microsoft/ai-for-beginners) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: fair (59) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 70k · MIT · Sep 2026</sub>

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

<a name="ml-for-beginners"></a>
### #&#8288;7 [ml-for-beginners](https://github.com/microsoft/ml-for-beginners) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: patchy (47) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 92k · MIT · Sep 2026</sub>

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

<a name="openai-cookbook"></a>
### #&#8288;8 [openai-cookbook](https://github.com/openai/openai-cookbook) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: fair (51) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 77k · MIT · Oct 2026</sub>

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

<a name="agents-course"></a>
### #&#8288;9 [agents-course](https://github.com/huggingface/agents-course) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (75) · Freshness: active (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · Apache-2.0 · Oct 2026</sub>

**Free Hugging Face course on building agents with smolagents, LlamaIndex, LangGraph.**

Source repository for the Hugging Face Agents Course, written as MDX lessons hosted at hf.co/learn/agents-course. It runs from agent basics through three frameworks (smolagents, LlamaIndex, LangGraph) to agentic RAG and a final assignment scored automatically on a leaderboard. Bonus units cover function-calling fine-tuning, observability and evaluation, and agents in Pokemon games.

- **+** Covers three frameworks: smolagents, LlamaIndex and LangGraph
- **+** Final project has automated evaluation and a student leaderboard
- **+** Bonus units on function-calling fine-tuning and agent tracing and evaluation
- **+** Apache-2.0 licensed, with an open contribution process
- **−** Repository holds course source; lessons are read on the Hugging Face site
- **−** Requires basic Python and basic LLM knowledge
- **−** Sign-up needed for the course; certification details are not in the README
- **−** Hardware and API requirements per unit are not stated

<sub>[Repo](https://github.com/huggingface/agents-course) · [🌐 Site ↗](https://hf.co/learn/agents-course) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agents-course/)</sub>

<a name="hello-agents"></a>
### #&#8288;10 [hello-agents](https://github.com/datawhalechina/hello-agents) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 84k · custom license · Oct 2026</sub>

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

<a name="ai-agent-book"></a>
### #&#8288;11 [ai-agent-book](https://github.com/bojieli/ai-agent-book) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 55k · Apache-2.0 · Sep 2026</sub>

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

<a name="rag-techniques"></a>
### #&#8288;12 [rag_techniques](https://github.com/nirdiamant/rag_techniques) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (71) · Freshness: active (99) · Maintenance: fair (59) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · custom license · Oct 2026</sub>

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
### #&#8288;13 [claude-cookbooks](https://github.com/anthropics/claude-cookbooks) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: patchy (34) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 54k · MIT · Oct 2026</sub>

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
### #&#8288;14 [agents-towards-production](https://github.com/nirdiamant/agents-towards-production) <sub>score [70](../README.md#-how-we-rank "Score 70/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · custom license · Oct 2026</sub>

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

<a name="genai-agents"></a>
### #&#8288;15 [genai_agents](https://github.com/nirdiamant/genai_agents) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (62) · Freshness: active (100) · Maintenance: patchy (44) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · custom license · Oct 2026</sub>

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
### #&#8288;16 [ml-engineering](https://github.com/stas00/ml-engineering) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: fair (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · CC-BY-SA-4.0 · Oct 2026</sub>

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

<a name="mcp-for-beginners"></a>
### #&#8288;17 [mcp-for-beginners](https://github.com/microsoft/mcp-for-beginners) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: known (45) · Freshness: active (100) · Maintenance: fair (61) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · MIT · Oct 2026</sub>

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

<a name="self-llm"></a>
### #&#8288;18 [self-llm](https://github.com/datawhalechina/self-llm) <sub>score [64](../README.md#-how-we-rank "Score 64/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: patchy (40) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · Apache-2.0 · Sep 2026</sub>

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

<a name="cookbook"></a>
### #&#8288;19 [cookbook](https://github.com/google-gemini/cookbook) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: known (48) · Freshness: active (100) · Maintenance: fair (61) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · Apache-2.0 · Oct 2026</sub>

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

<a name="ai-engineering-hub"></a>
### #&#8288;20 [ai-engineering-hub](https://github.com/patchy631/ai-engineering-hub) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: weak (24) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · MIT · Oct 2026</sub>

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

<a name="learnopencv"></a>
### #&#8288;21 [learnopencv](https://github.com/spmallick/learnopencv) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: fair (67) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 23k · no license · Oct 2026</sub>

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

<a name="generative-ai"></a>
### #&#8288;22 [generative-ai](https://github.com/googlecloudplatform/generative-ai) <sub>score [57](../README.md#-how-we-rank "Score 57/100. Adoption: known (46) · Freshness: active (100) · Maintenance: patchy (43) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · Apache-2.0 · Oct 2026</sub>

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

<a name="100-days-of-ml-code"></a>
### #&#8288;23 [100-days-of-ml-code](https://github.com/mleveryday/100-days-of-ml-code) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: popular (57) · Freshness: active (100) · Maintenance: patchy (30) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · MIT · Oct 2026</sub>

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

<a name="happy-llm"></a>
### #&#8288;24 [happy-llm](https://github.com/datawhalechina/happy-llm) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: popular (76) · Freshness: active (93) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · custom license · Aug 2026</sub>

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

<a name="prompt-engineering"></a>
### #&#8288;25 [prompt_engineering](https://github.com/nirdiamant/prompt_engineering) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: niche (9) · Freshness: active (100) · Maintenance: fair (60) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.9k · custom license · Oct 2026</sub>

**22 Jupyter notebooks teaching prompt engineering with OpenAI and LangChain.**

A set of 22 Jupyter notebooks covering prompt engineering, from basic prompt structures and Jinja2 templates to chain-of-thought, self-consistency, prompt chaining, optimization, prompt security and evaluation. Examples use OpenAI models and LangChain. The README also promotes a paid course ($199), a book and a newsletter by the author.

- **+** 22 notebooks ordered from fundamentals to optimization, security and evaluation
- **+** Covers named techniques: zero-shot, few-shot, CoT, self-consistency, prompt chaining
- **+** Runnable code in notebooks rather than prose-only guides
- **+** Includes a Jinja2 templating notebook and a prompt security notebook
- **−** Examples rely on OpenAI and LangChain; local model use is not described
- **−** README is heavy with promotion for a paid course, book and newsletter
- **−** License is reported as NOASSERTION, so reuse terms are unclear
- **−** No release tags and no setup or version requirements in the visible README

<sub>no GPU · Needs OpenAI API, LangChain, Jinja2 · Models: OpenAI GPT · [Repo](https://github.com/nirdiamant/prompt_engineering) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/prompt-engineering/)</sub>

<a name="transformers-tutorials"></a>
### #&#8288;26 [transformers-tutorials](https://github.com/nielsrogge/transformers-tutorials) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (30) · Freshness: active (100) · Maintenance: patchy (38) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · MIT · Sep 2026</sub>

**Colab notebooks for running and fine-tuning Hugging Face Transformers models.**

A collection of Jupyter notebooks by Niels Rogge showing inference and fine-tuning with Hugging Face Transformers in PyTorch. Coverage is mostly vision and document models (DETR, LayoutLM v1-v3, Donut, MaskFormer, Perceiver), plus some BERT, audio and GPT-J notebooks. Each demo links to a Colab notebook and the source paper.

- **+** Every demo has an Open in Colab badge, so no local setup is needed
- **+** Covers document AI in depth: LayoutLM v1-v3, LayoutXLM, Donut, DiT, MarkupLM
- **+** Includes both inference and fine-tuning notebooks, some using HF Trainer or PyTorch Lightning
- **+** MIT licensed, with a recent commit on 2026-09-17
- **−** PyTorch only; no TensorFlow or JAX notebooks
- **−** Many notebooks use older APIs (e.g. DetrFeatureExtractor) and may need version pinning
- **−** Mostly older architectures; no modern LLM fine-tuning notebooks in the visible README
- **−** No releases and no packaged library; notebooks only

<sub>GPU optional · Needs Hugging Face Transformers, PyTorch, Google Colab · Models: DETR, LayoutLM, LayoutLMv2, LayoutLMv3, Donut · [Repo](https://github.com/nielsrogge/transformers-tutorials) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/transformers-tutorials/)</sub>

<a name="amazon-sagemaker-examples"></a>
### #&#8288;27 [amazon-sagemaker-examples](https://github.com/aws/amazon-sagemaker-examples) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: patchy (36) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · Apache-2.0 · Oct 2026</sub>

**Official notebooks for training, tuning, deploying and operating models on SageMaker.**

AWS-maintained collection of Jupyter notebooks covering Amazon SageMaker features: training with ModelTrainer (SDK v3), fine-tuning (SFT, DPO, RLVR, RLAIF, CPT), evaluation, inference endpoints via ModelBuilder, and MLOps with Pipelines and Model Registry. Notebooks are self-contained and load automatically into SageMaker Notebook Instances. They can run elsewhere with a changed IAM role and installed libraries.

- **+** Maintained by the SageMaker team, covering training, customization, evaluation, inference and MLOps
- **+** Each notebook is self-contained with its own scripts, data and relative paths
- **+** Covers fine-tuning methods: SFT, DPO, RLVR, RLAIF, MTRL and CPT
- **+** Preloaded in SageMaker Notebook Instances under the SageMaker Examples tab
- **−** Requires an AWS account, IAM role setup and an S3 bucket
- **−** Tied to AWS services; running elsewhere needs modification
- **−** Only accepts examples for features not already covered; others go to a community repo
- **−** Running examples incurs AWS charges; README gives no cost or instance sizing

<sub>Needs AWS account, IAM role, Amazon S3, Amazon SageMaker, Jupyter · Models: JumpStart foundation models, custom containers, SageMaker Python SDK v3 · [Repo](https://github.com/aws/amazon-sagemaker-examples) · [📖 Docs ↗](https://sagemaker.readthedocs.io/en/stable/api/sagemaker_core.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/amazon-sagemaker-examples/)</sub>

<a name="handson-ml"></a>
### #&#8288;28 [handson-ml](https://github.com/ageron/handson-ml) <sub>score [52](../README.md#-how-we-rank "Score 52/100. Adoption: popular (65) · Freshness: recent (76) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 26k · Apache-2.0 · May 2026</sub>

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

<a name="mlops-zoomcamp"></a>
### #&#8288;29 [mlops-zoomcamp](https://github.com/datatalksclub/mlops-zoomcamp) <sub>score [48](../README.md#-how-we-rank "Score 48/100. Adoption: known (42) · Freshness: active (100) · Maintenance: fair (50) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 15k · no license · Sep 2026</sub>

**Free 9-week MLOps course covering tracking, orchestration, deployment and monitoring.**

Course materials for DataTalks.Club's MLOps Zoomcamp: six modules with pre-recorded lectures, homework and a final project, built around the NY Taxi dataset. Topics include MLflow experiment tracking and model registry, workflow orchestration, Flask, AWS Kinesis and Lambda deployment, monitoring with Prometheus, Evidently and Grafana, and CI/CD with GitHub Actions and Terraform.

- **+** Covers the full lifecycle: tracking, orchestration, deployment, monitoring, testing, CI/CD, Terraform
- **+** Pre-recorded video lectures on YouTube; self-paced study available at any time
- **+** Single running example (NY Taxi dataset) and a final end-to-end project
- **+** Taught by three named instructors with a Slack channel and FAQ
- **−** No live cohort planned for 2026; no graded homework or peer review in self-paced mode
- **−** Certificates only go to learners who finish the project in a live cohort
- **−** Requires prior Python, Docker and ML experience
- **−** No license detected for the repository

<sub>Needs Python, Docker, MLflow, Prefect, AWS Kinesis, AWS Lambda, Prometheus, Grafana, Evidently, MongoDB, Terraform, GitHub Actions · [Repo](https://github.com/datatalksclub/mlops-zoomcamp) · [📖 Docs ↗](https://datatalks.club/docs/courses/mlops-zoomcamp/) · [🌐 Site ↗](https://courses.datatalks.club/register/mlops-zoomcamp/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mlops-zoomcamp/)</sub>

<a name="micrograd"></a>
### #&#8288;30 [micrograd](https://github.com/karpathy/micrograd) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: known (49) · Freshness: active (100) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 18k · MIT · Aug 2026</sub>

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

<a name="all-in-rag"></a>
### #&#8288;31 [all-in-rag](https://github.com/datawhalechina/all-in-rag) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: known (32) · Freshness: active (100) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 12k · no license · Sep 2026</sub>

**Chinese-language RAG tutorial with code, from chunking to Graph RAG.**

A Datawhale course on building retrieval-augmented generation systems in Python, written mainly in Chinese with an English README. It covers data loading, chunking, text and multimodal embeddings, Milvus, hybrid search, Text2SQL, query rewriting, evaluation and a knowledge-graph RAG chapter. Chapters 8 and 9 build a full project and then add Graph RAG; chapter 10 is still planned.

- **+** Covers the full pipeline: loading, chunking, embedding, Milvus, hybrid search, Text2SQL, evaluation
- **+** Includes multimodal embedding and Graph RAG chapters plus a worked end-to-end project
- **+** Each chapter pairs written explanation with code in the repo
- **+** Online reader site and an English README are available
- **−** Main tutorial text is in Chinese; the English version is a separate README
- **−** CC BY-NC-SA 4.0 terms bar commercial use; no license was detected by tooling
- **−** Chapter 10, the second project, is listed as planned and not written
- **−** Only Extra-chapter pull requests are accepted for documentation

<sub>Needs Python 3.12.7, Milvus, Neo4j, Docker · [Repo](https://github.com/datawhalechina/all-in-rag) · [📖 Docs ↗](https://datawhalechina.github.io/all-in-rag/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/all-in-rag/)</sub>

<a name="agentguide"></a>
### #&#8288;32 [agentguide](https://github.com/adongwanai/agentguide) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: niche (27) · Freshness: active (100) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 11k · no license · Sep 2026</sub>

**Chinese-language study guide and interview prep for AI agent engineering roles.**

A documentation repository (MDX) that organizes AI agent learning into role-based roadmaps for development and algorithm tracks, with tutorials on LangGraph, RAG, context engineering, SFT and RL. It also collects 1500+ interview questions, resume advice and links to external courses and projects. Content is in Chinese and no runnable software is shipped.

- **+** Separate development and algorithm roadmaps, stated as 8-12 and 10-15 weeks
- **+** Covers agent harness, context engineering, MCP, RAG, eval and agentic RL topics
- **+** Includes an interview question bank (1500+ claimed) and resume guidance
- **+** Links to external resources such as learn-workbuddy and hello-agents instead of duplicating them
- **−** Written in Chinese; English readers need translation
- **−** No license detected, so reuse terms are unclear
- **−** Much of the README is job-search advice rather than runnable code
- **−** Many topics point to third-party material rather than original content

<sub>no GPU · [Repo](https://github.com/adongwanai/agentguide) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agentguide/)</sub>

<a name="arc-task-gen"></a>
### #&#8288;33 [arc-task-gen](https://github.com/pathwaycom/arc-task-gen) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: niche (25) · Freshness: active (100) · Maintenance: weak (25) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Aug 2026</sub>

**Generator of fresh ARC-AGI-1-style tasks for private model evaluation.**

Generates new ARC-AGI-1-style tasks that resemble the public dataset, written to a tasks.json in standard ARC train/test format. It gives a private evaluation set for comparing public-benchmark scores with scores on unseen tasks. It accompanies the BDH-CQ paper, which reports 29.5% pass@2 for a 150M-parameter model on the public ARC-AGI-1 evaluation set.

- **+** Output follows standard ARC JSON format, compatible with existing ARC evaluation harnesses
- **+** Produces tasks unlikely to be in model training data, useful for checking benchmark familiarity
- **+** MIT licensed, written in Python
- **−** README gives no usage steps; setup is deferred to instructions.md
- **−** README does not say how the generator works or what it needs to run
- **−** Does not include the BDH-CQ model; the repo only generates tasks
- **−** No releases published

<sub>Models: ARC task JSON · [Repo](https://github.com/pathwaycom/arc-task-gen) · [🌐 Site ↗](https://pathway.com/blog/pathway-150m-model-breaks-arc-agi-1-cost-efficiency-frontier) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/arc-task-gen/)</sub>

<a name="nlp-course"></a>
### #&#8288;34 [nlp_course](https://github.com/yandexdataschool/nlp_course) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: weak (22) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Oct 2026</sub>

**University NLP course with lecture and notebook homework, from embeddings to agents.**

Course materials for the YSDA Natural Language Processing course, 2025 edition, organized as 14 weekly folders. Topics run from word embeddings, language models and attention to transfer learning, LLMs, prompting, PEFT/RLHF, efficiency, RAG, agents and interpretability. Each week has lecture notes, seminars and homework, mostly in Jupyter Notebook.

- **+** Covers classic NLP and current LLM topics (RAG, agents, PEFT, quantization) in one syllabus
- **+** Seminar and homework notebooks for most weeks
- **+** Links to interactive lecture materials by Elena Voita for weeks 1 to 4
- **+** MIT license, with an issue thread for installation troubleshooting
- **−** Weeks 12 to 14 list only titles in the README, no content described
- **−** Materials are added as prepared, so some weeks may be incomplete
- **−** No hardware or RAM requirements stated for the notebooks
- **−** No release or packaged environment; setup is left to the reader

<sub>Models: BERT, open-source LLMs · [Repo](https://github.com/yandexdataschool/nlp_course) · [🌐 Site ↗](https://lena-voita.github.io/nlp_course.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nlp-course/)</sub>

<a name="made-with-ml"></a>
### #&#8288;35 [made-with-ml](https://github.com/gokumohandas/made-with-ml) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: widely used (83) · Freshness: recent (60) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 50k · MIT · Mar 2026</sub>

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
### #&#8288;36 [fastbook](https://github.com/fastai/fastbook) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: popular (64) · Freshness: recent (70) · Maintenance: weak (11) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · custom license · Oct 2026</sub>

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

<a name="hands-on-large-language-models"></a>
### #&#8288;37 [hands-on-large-language-models](https://github.com/handsonllm/hands-on-large-language-models) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: popular (70) · Freshness: recent (67) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Apr 2026</sub>

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

<a name="machine-learning-zoomcamp"></a>
### #&#8288;38 [machine-learning-zoomcamp](https://github.com/datatalksclub/machine-learning-zoomcamp) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: known (39) · Freshness: recent (79) · Maintenance: fair (52) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 15k · no license · Oct 2026</sub>

**Free ML engineering course from regression to Kubernetes deployment.**

Course materials for DataTalks.Club's Machine Learning Zoomcamp: pre-recorded lectures, notebooks and homework. It covers regression, classification, evaluation, tree models and deep learning, then deployment with FastAPI, Docker, AWS Lambda and Kubernetes. It can be followed self-paced or in a yearly live cohort with graded homework, peer review and certificates.

- **+** Covers the full path from data prep to a deployed service, including Docker, Lambda and Kubernetes
- **+** Self-paced use is free, with lectures on YouTube and homework available unscored
- **+** Midterm and capstone projects produce end-to-end portfolio work
- **+** No local GPU needed; deep learning modules use cloud resources
- **−** Certificates, scored homework and peer review only in the live cohort (starts September 14, 2026)
- **−** No license detected for the repository
- **−** Expects about one year of programming experience and command line comfort
- **−** Not aimed at advanced ML research; syllabus has no LLM module

<sub>GPU optional · Needs Python, Docker, Kubernetes, AWS Lambda · Models: scikit-learn, XGBoost, TensorFlow, PyTorch, Keras · [Repo](https://github.com/datatalksclub/machine-learning-zoomcamp) · [📖 Docs ↗](https://datatalks.club/docs/courses/ml-zoomcamp/) · [🌐 Site ↗](https://courses.datatalks.club/ml-zoomcamp-2026/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/machine-learning-zoomcamp/)</sub>

<a name="llm-course"></a>
### #&#8288;39 [llm-course](https://github.com/mlabonne/llm-course) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: widely used (95) · Freshness: slowing (39) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 85k · Apache-2.0 · Feb 2026</sub>

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

<a name="cv"></a>
### #&#8288;40 [cv](https://github.com/accumulatemore/cv) <sub>score [40](../README.md#-how-we-rank "Score 40/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 24k · no license · Sep 2026</sub>

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

<a name="annotated-deep-learning-paper-implementations"></a>
### #&#8288;41 [annotated_deep_learning_paper_implementations](https://github.com/labmlai/annotated_deep_learning_paper_implementations) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: widely used (88) · Freshness: slowing (33) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 68k · MIT · Jan 2026</sub>

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

<a name="llm-universe"></a>
### #&#8288;42 [llm-universe](https://github.com/datawhalechina/llm-universe) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: known (37) · Freshness: recent (70) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 14k · no license · Aug 2026</sub>

**Chinese-language course on building a RAG knowledge-base assistant with LLM APIs.**

A Jupyter Notebook tutorial from Datawhale that walks beginners through building a personal knowledge-base assistant. It covers calling LLM APIs (OpenAI, Baidu Wenxin, iFlytek Spark, Zhipu GLM), building a vector store, a LangChain retrieval QA chain, Streamlit deployment, and evaluation. Part 1 is complete; the advanced RAG and case-study parts are still in progress.

- **+** Single worked project from API calls to Streamlit deployment and evaluation
- **+** Wraps several LLM APIs (GPT, Wenxin, Spark, GLM) behind one calling interface
- **+** No GPU needed; runs on a laptop or a server
- **+** Online book and PDF release available alongside the notebooks
- **−** Written in Chinese; the README gives no English version
- **−** Parts 2 and 3 (advanced RAG, case studies) are unfinished
- **−** Relies on third-party model APIs rather than local models
- **−** No license detected; last release was April 2024

<sub>no GPU · Needs Python 3.8+, LangChain, Streamlit, LLM provider API keys · Models: OpenAI GPT, Baidu Wenxin, iFlytek Spark, Zhipu GLM · [Repo](https://github.com/datawhalechina/llm-universe) · [📖 Docs ↗](https://datawhalechina.github.io/llm-universe/) · [🌐 Site ↗](https://datawhalechina.github.io/llm-universe/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llm-universe/)</sub>

<a name="examples"></a>
### #&#8288;43 [examples](https://github.com/tensorflow/examples) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: niche (11) · Freshness: recent (70) · Maintenance: patchy (39) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.3k · Apache-2.0 · Oct 2026</sub>

**Official TensorFlow example notebooks, community samples and course material.**

Repository of example code maintained by the TensorFlow team. It holds material referenced from tensorflow.org, community-contributed examples, Udacity Deep Learning course files, and supporting code for the TensorFlow blog and YouTube channel. The README points to the tensorflow/docs repo as the main place to learn TensorFlow.

- **+** Maintained under the official TensorFlow organization, Apache-2.0 licensed
- **+** Covers tensorflow.org, blog and YouTube material in one repo
- **+** Includes Udacity Deep Learning course files and a community examples folder
- **+** Recent commits (2026-10-05) despite the old release tag
- **−** Last release was 2021-05-16, so some examples may be dated
- **−** README does not list examples, versions or requirements per example
- **−** Issues are filed in tensorflow/tensorflow, not in this repo
- **−** Not a single runnable app; upkeep and quality vary by folder

<sub>Needs TensorFlow · [Repo](https://github.com/tensorflow/examples) · [📖 Docs ↗](http://github.com/tensorflow/docs) · [🌐 Site ↗](https://www.tensorflow.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/examples/)</sub>

<a name="python-machine-learning-book"></a>
### #&#8288;44 [python-machine-learning-book](https://github.com/rasbt/python-machine-learning-book) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: known (33) · Freshness: recent (68) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · Jul 2026</sub>

**Jupyter notebooks for the first edition of Python Machine Learning.**

Code companion to the 1st edition (2015) of Sebastian Raschka's Python Machine Learning book. It provides notebooks for 13 chapters covering classification, preprocessing, dimensionality reduction, ensembles, sentiment analysis, regression, clustering and neural networks, using NumPy, scikit-learn and Theano. Bonus notebooks and an equation reference are included; 2nd edition code is in a separate repository.

- **+** 13 chapter notebooks plus bonus ones such as nested cross-validation and softmax regression
- **+** Includes an equation reference (PDF and TEX) and a barebones Flask web app example
- **+** MIT licensed, with errata and reference lists in docs
- **−** Covers only the 1st edition; the README points to a separate 2nd edition repository
- **−** Neural network chapters use Theano
- **−** Notebooks are of limited use without the book's text and formulae
- **−** Last release is from 2016-09-30; the README lists no pinned dependency versions

<sub>GPU optional · Needs Python, Jupyter Notebook, NumPy, scikit-learn, Theano, Flask · [Repo](https://github.com/rasbt/python-machine-learning-book) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/python-machine-learning-book/)</sub>

<a name="machine-learning-examples"></a>
### #&#8288;45 [machine_learning_examples](https://github.com/lazyprogrammer/machine_learning_examples) <sub>score [28](../README.md#-how-we-rank "Score 28/100. Adoption: niche (15) · Freshness: active (100) · Maintenance: weak (10) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 8.9k · no license · Sep 2026</sub>

**Python code for Lazy Programmer's online machine learning courses.**

A repository of Python example code for the author's paid courses on deep learning, NLP, reinforcement learning, time series and related topics. Each folder matches one course, and newer TensorFlow 2 material lives in Google Colab notebooks linked from the lectures rather than here. The README gives no setup instructions, requirements file or license.

- **+** Covers many topics: CNNs, RNNs, GANs, HMMs, reinforcement learning, Bayesian methods, recommenders
- **+** One folder per course, so code maps directly to lectures
- **+** Still updated: last commit 2026-09-28
- **−** No license stated, so reuse rights are unclear
- **−** Written to accompany paid courses; little standalone explanation in the README
- **−** Not all course code is here; newer TensorFlow 2 work is in Colab
- **−** No install steps or pinned dependency list in the README

<sub>[Repo](https://github.com/lazyprogrammer/machine_learning_examples) · [🌐 Site ↗](https://lazyprogrammer.me) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/machine-learning-examples/)</sub>

<a name="easy-rl"></a>
### #&#8288;46 [easy-rl](https://github.com/datawhalechina/easy-rl) <sub>score [27](../README.md#-how-we-rank "Score 27/100. Adoption: known (40) · Freshness: quiet (18) · Maintenance: patchy (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · custom license · Dec 2025</sub>

**Chinese-language reinforcement learning textbook with Jupyter notebook implementations.**

"Mushroom Book" (蘑菇书) is a Chinese reinforcement learning tutorial built from Hung-yi Lee's deep RL lectures, Bolei Zhou's RL course notes and Baidu's hands-on RL course. It has 13 chapters with exercises, plus notebooks for Q-learning, Sarsa, Monte Carlo, policy gradient, PPO, DQN variants, A2C and DDPG. Content is readable online and as a PDF, and a print edition exists.

- **+** Runnable notebooks for policy gradient, PPO, DQN variants, A2C and DDPG
- **+** Chapters include exercises and a public errata page
- **+** Free online version and PDF releases, plus a printed edition
- **+** Includes paper walkthroughs and links to JoyRL code
- **−** Text is in Chinese only; the README mentions no English edition
- **−** License is CC BY-NC-SA 4.0, which bars commercial use
- **−** Last tagged release is from 2023-07-25
- **−** Chapters 8, 10 and 11 have no companion code listed

<sub>[Repo](https://github.com/datawhalechina/easy-rl) · [📖 Docs ↗](https://datawhalechina.github.io/easy-rl/) · [🌐 Site ↗](https://datawhalechina.github.io/easy-rl/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/easy-rl/)</sub>

<a name="ml-nlp"></a>
### #&#8288;47 [ml-nlp](https://github.com/nlp-love/ml-nlp) <sub>score [23](../README.md#-how-we-rank "Score 23/100. Adoption: known (47) · Freshness: quiet (29) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 18k · no license · Jan 2026</sub>

**Chinese-language ML and NLP interview study notes with code examples.**

A set of Markdown chapters, with Jupyter notebook code, covering topics commonly asked in machine learning and NLP interviews. Chapters run from linear regression, tree ensembles (GBDT, XGBoost, LightGBM) and SVM through CNN/RNN/LSTM, word embeddings, seq2seq, Transformer, BERT and XLNet. Two project chapters (recommendation system, customer service) exist; knowledge graph and review analysis are listed but empty.

- **+** Covers classical ML, deep learning and NLP in one chapter index
- **+** Chapters end with practical code examples, per the README
- **+** Includes Transformer, BERT and XLNet chapters alongside older RNN-era models
- **+** Each chapter is a standalone Markdown page, easy to skim for review
- **−** Written in Chinese only; no English version noted
- **−** No license file detected, so reuse terms are unclear
- **−** Nothing on modern LLMs, fine-tuning or serving
- **−** Knowledge graph and review analysis chapters are listed but empty

<sub>[Repo](https://github.com/nlp-love/ml-nlp) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ml-nlp/)</sub>

<a name="homemade-machine-learning"></a>
### #&#8288;48 [homemade-machine-learning](https://github.com/trekhleb/homemade-machine-learning) <sub>score [22](../README.md#-how-we-rank "Score 22/100. Adoption: popular (63) · Freshness: quiet (12) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 25k · MIT · Nov 2025</sub>

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

<a name="transformer-explainer"></a>
### #&#8288;49 [transformer-explainer](https://github.com/poloclub/transformer-explainer) <sub>score [22](../README.md#-how-we-rank "Score 22/100. Adoption: niche (16) · Freshness: recent (58) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.0k · MIT · Jun 2026</sub>

**Interactive browser visualization of how GPT-2 predicts the next token.**

Transformer Explainer runs a live GPT-2 model in the browser and shows the internal operations of the Transformer as you type your own text. It visualizes how the components work together to predict next tokens. It can be tried on a hosted page or run locally with Node.js 20+ and npm.

- **+** Runs GPT-2 in the browser, so no server or API key is needed
- **+** Accepts your own input text and updates the visualization live
- **+** Short local setup: npm install, npm run dev on port 5173
- **+** Backed by a CHI 2026 paper and a YouTube walkthrough video
- **−** Only GPT-2 is mentioned; no other models are listed
- **−** Educational visualizer, not a tool for running or serving models
- **−** No Docker image or compose file provided
- **−** Last tagged release is from June 2024

<sub>no GPU · Needs Node.js 20+, npm 10+ · Models: GPT-2 · port 5173 · [Repo](https://github.com/poloclub/transformer-explainer) · [▶️ Demo ↗](http://poloclub.github.io/transformer-explainer) · [🌐 Site ↗](http://poloclub.github.io/transformer-explainer) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/transformer-explainer/)</sub>

<a name="notebooks"></a>
### #&#8288;50 [notebooks](https://github.com/roboflow/notebooks) <sub>score [21](../README.md#-how-we-rank "Score 21/100. Adoption: niche (20) · Freshness: recent (70) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 9.7k · no license · Aug 2026</sub>

**Jupyter notebooks for computer vision models, with Colab and Kaggle links.**

A collection of 61 Jupyter notebooks from Roboflow covering computer vision tasks: object detection, segmentation, tracking, OCR, keypoints and JSON data extraction. Each notebook targets a specific model such as RF-DETR, YOLO26, YOLOv12, SAM3, Qwen2.5-VL, Qwen3-VL, PaliGemma 2 or Gemini, and links to Colab, Kaggle, a paper and often a video or blog post.

- **+** Each notebook opens directly in Colab or Kaggle, so no local setup is needed
- **+** Covers fine-tuning and zero-shot use for detection, segmentation, OCR and tracking
- **+** Many entries link to the upstream repo, arXiv paper, blog post or YouTube walkthrough
- **+** Recent additions include RF-DETR keypoints, YOLO26, SAM3 and Qwen3-VL
- **−** No license detected in the repository metadata
- **−** Last tagged release is from 2022-12, so versions are not pinned by release
- **−** Some notebooks call hosted APIs such as Gemini, which need external keys
- **−** Centered on Roboflow's ecosystem and datasets; not a general ML course

<sub>GPU optional · Needs Google Colab or Kaggle, Google Gemini API (some notebooks) · Models: RF-DETR, YOLO26, YOLOv12, YOLOE, SAM3 · [Repo](https://github.com/roboflow/notebooks) · [📖 Docs ↗](https://docs.roboflow.com) · [🌐 Site ↗](https://roboflow.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/notebooks/)</sub>

<a name="fun-rec"></a>
### #&#8288;51 [fun-rec](https://github.com/datawhalechina/fun-rec) <sub>score [19](../README.md#-how-we-rank "Score 19/100. Adoption: niche (6) · Freshness: active (90) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 7.4k · no license · Jun 2026</sub>

**Chinese-language textbook on recommender systems, from cascades to generative models.**

An online book (小麦书) on recommender algorithms in two parts. The first covers the cascade pipeline: collaborative filtering, vector and sequence recall, feature crossing, multi-task and multi-scenario ranking, and re-ranking. The second covers generative recommendation (HSTU, OneRec, reasoning and diffusion models) and ends with a production system project. The README gives no setup or run instructions.

- **+** Covers the path from collaborative filtering to generative recommenders such as HSTU and OneRec
- **+** Final chapter walks through building a production recommender system
- **+** Re-ranking, multi-objective and multi-scenario ranking are covered alongside recall
- **−** Main README is in Chinese; English version is a separate file
- **−** Under active development, and Pull Requests are not accepted
- **−** CC BY-NC-SA 4.0 license bars commercial use
- **−** README does not list code requirements, datasets or how to run examples

<sub>[Repo](https://github.com/datawhalechina/fun-rec) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fun-rec/)</sub>

<a name="llama-cookbook"></a>
### #&#8288;52 [llama-cookbook](https://github.com/meta-llama/llama-cookbook) <sub>score [16](../README.md#-how-we-rank "Score 16/100. Adoption: popular (51) · Freshness: quiet (3) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 19k · MIT · Nov 2025</sub>

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

<a name="pyprobml"></a>
### #&#8288;53 [pyprobml](https://github.com/probml/pyprobml) <sub>score [16](../README.md#-how-we-rank "Score 16/100. Adoption: niche (4) · Freshness: slowing (32) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.2k · MIT · Feb 2026</sub>

**Notebooks that reproduce figures from the Probabilistic Machine Learning books.**

Python 3 Jupyter notebooks that regenerate the figures in "Probabilistic Machine Learning: An Introduction" (book 1) and "Advanced Topics" (book 2). Code uses numpy, scipy, matplotlib and sklearn, with JAX in much of book 2 and TensorFlow 2 or Torch in parts of book 1. The repo has been in maintenance mode since September 2022.

- **+** Notebooks organized by chapter for both book 1 and book 2
- **+** Runs in Colab with free GPU/TPU; Colab intro notebook included
- **+** Status dashboards show which figure notebooks currently run
- **+** Shared plotting helpers live in the separate probml-utils package
- **−** Maintenance mode since September 2022; last release 2022-05-05
- **−** Tied to the books; not a standalone library or course
- **−** JAX, TensorFlow and Torch must be installed manually first
- **−** No Docker setup; local install is a requirements.txt plus manual steps

<sub>GPU optional · Needs JAX, TensorFlow 2, Torch, numpy, scipy, matplotlib, scikit-learn · [Repo](https://github.com/probml/pyprobml) · [📖 Docs ↗](https://probml.github.io/notebooks) · [🌐 Site ↗](https://probml.github.io/pml-book/book1.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pyprobml/)</sub>

<a name="langchain-chinese-getting-started-guide"></a>
### #&#8288;54 [langchain-chinese-getting-started-guide](https://github.com/liaokongvfx/langchain-chinese-getting-started-guide) <sub>score [15](../README.md#-how-we-rank "Score 15/100. Adoption: niche (17) · Freshness: recent (66) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Penalty: no license. Click for how we rank.") · ⭐ 9.1k · no license · Apr 2026</sub>

**Chinese-language LangChain tutorial with runnable OpenAI examples.**

A Chinese-language tutorial that teaches LangChain through worked Python examples: Q&A, Google search agents, long-text summarization, local-document Q&A with Chroma and Pinecone, YouTube Q&A, and Zapier tool use. It also covers sequential chains, structured output parsing and web scraping to JSON. The author warns it was written in early April 2023 and some Colab code is outdated.

- **+** Examples run in order and build on each other, from one Q&A call to agents
- **+** Covers RAG with both local Chroma and hosted Pinecone persistence
- **+** Explains summarize chain types (stuff, map_reduce, refine) and chunk_overlap with diagrams
- **+** Gitbook edition and a CHANGELOG are provided for reading and tracking updates
- **−** Written in April 2023; the author says some code is outdated against current LangChain
- **−** Uses legacy APIs such as text-davinci-003, initialize_agent and ChatVectorDBChain
- **−** Most examples need an OpenAI key, plus SerpAPI, Pinecone or Zapier accounts
- **−** No license declared; the text is Chinese only

<sub>no GPU · Needs OpenAI API, SerpAPI, Pinecone, Chroma, Zapier NLA · Models: text-davinci-003, gpt-3.5-turbo, text-embedding-ada-002 · [Repo](https://github.com/liaokongvfx/langchain-chinese-getting-started-guide) · [📖 Docs ↗](https://python.langchain.com/en/latest/) · [🌐 Site ↗](https://liaokong.gitbook.io/llm-kai-fa-jiao-cheng/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/langchain-chinese-getting-started-guide/)</sub>

<a name="introtodeeplearning"></a>
### #&#8288;55 [introtodeeplearning](https://github.com/mitdeeplearning/introtodeeplearning) <sub>score [10](../README.md#-how-we-rank "Score 10/100. Adoption: niche (14) · Freshness: quiet (19) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.8k · MIT · Jan 2026</sub>

**Jupyter notebook labs for MIT's Introduction to Deep Learning course.**

Code and software labs (lab1, lab2, lab3) for the MIT Introduction to Deep Learning course, written as Jupyter notebooks with #TODO cells to fill in. They run in Google Colab with a GPU runtime and use the companion `mitdeeplearning` pip package for helper functions. Lecture slides and videos are hosted on the course website and YouTube.

- **+** Self-paced labs with #TODO cells to complete, tied to public lecture videos
- **+** Runs in Google Colab, so no local install or local GPU is needed
- **+** Helper package `mitdeeplearning` is on PyPI and reusable outside the course
- **+** Code is MIT licensed
- **−** Requires a Google account to run the labs in Colab
- **−** Only three labs; covers course material, not a general cookbook
- **−** Reuse of code and slides must carry the MIT Introduction to Deep Learning attribution
- **−** Last release is 2025-01-08, older than the 2026 lab update

<sub>GPU optional · Needs Google Colab, Google account, mitdeeplearning (pip) · [Repo](https://github.com/mitdeeplearning/introtodeeplearning) · [🌐 Site ↗](http://introtodeeplearning.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/introtodeeplearning/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
