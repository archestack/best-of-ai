# 📖 Learning and cookbooks reviews · Best of Open-Source AI

Courses, cookbooks and guides with runnable code, for learning to build with AI. Back to the [leaderboard](../README.md#-learning-and-cookbooks).

<sub>🌐 Also on the web: [Learning and cookbooks on archestack.com](https://archestack.com/best-of-ai/learning/), each project on its own page.</sub>

<a name="ai-engineering-from-scratch"></a>
### 🥇 [ai-engineering-from-scratch](https://github.com/rohitg00/ai-engineering-from-scratch) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 69k · MIT · Oct 2026</sub>

**Hands-on curriculum for building AI systems from math to agents.**

A course of 528 lessons across 20 phases, covering math foundations, ML fundamentals, LLM engineering, agents, tools and protocols, and production infrastructure. Lessons are runnable code in Python, TypeScript, Rust and Julia, with three graded projects: retrieval evaluation, agent trace debugging and a tool-call firewall. It can be followed on the website, from a local clone, or through tutor skills installed into a coding agent.

- **+** Lessons ship runnable code; the first ones need only python3 and no extra dependencies
- **+** Three staged projects with local graders (project_test.py --strict) and reference solutions
- **+** Tutor skills install via npx skills and save progress to LEARNING.md
- **+** Code in Python, TypeScript, Rust and Julia; README translated into 30+ languages
- **−** 528 lessons is a large scope; total study time is not stated in the visible README
- **−** Project starters fail by design until you implement the stages
- **−** Tutor skills need Node.js, npx and a skill-capable coding agent host
- **−** GPU and RAM needs for later phases are not stated in the visible README

<sub>Needs Python 3.10+, Node.js 22.18+ (TypeScript project), Rust (Tool Call Firewall project), npx (optional, tutor skills) · [Repo](https://github.com/rohitg00/ai-engineering-from-scratch) · [🌐 Site ↗](https://aiengineeringfromscratch.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai-engineering-from-scratch/)</sub>

<a name="generative-ai-for-beginners"></a>
### 🥈 [generative-ai-for-beginners](https://github.com/microsoft/generative-ai-for-beginners) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: fair (62) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 121k · MIT · Oct 2026</sub>

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

<a name="llms-from-scratch"></a>
### 🥉 [llms-from-scratch](https://github.com/rasbt/llms-from-scratch) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: fair (58) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 107k · custom license · Oct 2026</sub>

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

<a name="hello-agents"></a>
### #&#8288;4 [hello-agents](https://github.com/datawhalechina/hello-agents) <sub>score [76](../README.md#-how-we-rank "Score 76/100. Adoption: widely used (82) · Freshness: active (100) · Maintenance: fair (70) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 83k · custom license · Oct 2026</sub>

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

<a name="ml-for-beginners"></a>
### #&#8288;5 [ml-for-beginners](https://github.com/microsoft/ml-for-beginners) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: fair (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 91k · MIT · Sep 2026</sub>

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

<a name="ai-agents-for-beginners"></a>
### #&#8288;6 [ai-agents-for-beginners](https://github.com/microsoft/ai-agents-for-beginners) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: fair (60) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 77k · MIT · Oct 2026</sub>

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

<a name="ai-for-beginners"></a>
### #&#8288;7 [ai-for-beginners](https://github.com/microsoft/ai-for-beginners) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: fair (59) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 70k · MIT · Sep 2026</sub>

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

<a name="ai-agent-book"></a>
### #&#8288;8 [ai-agent-book](https://github.com/bojieli/ai-agent-book) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (57) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 54k · Apache-2.0 · Sep 2026</sub>

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

<a name="openai-cookbook"></a>
### #&#8288;9 [openai-cookbook](https://github.com/openai/openai-cookbook) <sub>score [71](../README.md#-how-we-rank "Score 71/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: fair (51) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 77k · MIT · Oct 2026</sub>

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

<a name="claude-cookbooks"></a>
### #&#8288;10 [claude-cookbooks](https://github.com/anthropics/claude-cookbooks) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: patchy (36) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 53k · MIT · Oct 2026</sub>

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

<a name="rag-techniques"></a>
### #&#8288;11 [rag_techniques](https://github.com/nirdiamant/rag_techniques) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: minimal (45) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · custom license · Oct 2026</sub>

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

<a name="self-llm"></a>
### #&#8288;12 [self-llm](https://github.com/datawhalechina/self-llm) <sub>score [50](../README.md#-how-we-rank "Score 50/100. Adoption: niche (28) · Freshness: active (100) · Maintenance: patchy (40) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 32k · Apache-2.0 · Sep 2026</sub>

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

<a name="ai-engineering-hub"></a>
### #&#8288;13 [ai-engineering-hub](https://github.com/patchy631/ai-engineering-hub) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: known (40) · Freshness: active (100) · Maintenance: weak (24) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 38k · MIT · Oct 2026</sub>

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

<a name="happy-llm"></a>
### #&#8288;14 [happy-llm](https://github.com/datawhalechina/happy-llm) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: known (33) · Freshness: active (93) · Maintenance: weak (13) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 34k · custom license · Aug 2026</sub>

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

<a name="llm-course"></a>
### #&#8288;15 [llm-course](https://github.com/mlabonne/llm-course) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: widely used (85) · Freshness: slowing (41) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 84k · Apache-2.0 · Feb 2026</sub>

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
### #&#8288;16 [made-with-ml](https://github.com/gokumohandas/made-with-ml) <sub>score [33](../README.md#-how-we-rank "Score 33/100. Adoption: known (50) · Freshness: recent (62) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 50k · MIT · Mar 2026</sub>

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

<a name="annotated-deep-learning-paper-implementations"></a>
### #&#8288;17 [annotated_deep_learning_paper_implementations](https://github.com/labmlai/annotated_deep_learning_paper_implementations) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: popular (64) · Freshness: slowing (36) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 68k · MIT · Jan 2026</sub>

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

<a name="hands-on-large-language-models"></a>
### #&#8288;18 [hands-on-large-language-models](https://github.com/handsonllm/hands-on-large-language-models) <sub>score [26](../README.md#-how-we-rank "Score 26/100. Adoption: niche (18) · Freshness: recent (69) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Apr 2026</sub>

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

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
