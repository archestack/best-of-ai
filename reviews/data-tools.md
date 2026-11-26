# 🕸️ Data and scraping for AI reviews · Best of Open-Source AI

Tools that turn web pages, PDFs and documents into clean text or structured data that models can use. Back to the [leaderboard](../README.md#%EF%B8%8F-data-and-scraping-for-ai).

<sub>🌐 Also on the web: [Data and scraping for AI on archestack.com](https://archestack.com/best-of-ai/data-tools/), each project on its own page.</sub>

<a name="opendataloader-pdf"></a>
### 🥇 [opendataloader-pdf](https://github.com/opendataloader-project/opendataloader-pdf) <sub>score [93](../README.md#-how-we-rank "Score 93/100. Adoption: widely used (88) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Nov 2026</sub>

**PDF parser that outputs Markdown, JSON with bounding boxes, and Tagged PDF.**

Java-based PDF parser with Python, Node.js and Java SDKs. It extracts Markdown, JSON with per-element bounding boxes, and HTML, using XY-Cut++ reading order in a deterministic local mode. An optional hybrid mode sends complex pages to a Docling-based backend for OCR, borderless tables, LaTeX formulas and chart descriptions. It also auto-tags untagged PDFs into Tagged PDF.

- **+** Bounding boxes and element types for every extracted item, usable for source citations
- **+** Local mode needs no GPU; README reports 0.015 s/page
- **+** Hybrid mode adds OCR, LaTeX formulas and chart descriptions; OCR engine is selectable
- **+** Reports 0.907 overall on its own 200-PDF benchmark, ahead of docling and marker
- **−** Requires Java 11+ on the host, even when using the Python package
- **−** Each convert() call spawns a JVM, so calls must be batched
- **−** PDF/UA export and accessibility studio are enterprise-only
- **−** Does not process Word, Excel or PowerPoint; benchmark is run by the project itself

<sub>no GPU · Needs Java 11+, Python 3.10+ (Python SDK), Docling backend (hybrid mode) · Models: Docling, EasyOCR, RapidOCR, Tesseract, SmolVLM (256M) · port 5002 · [Repo](https://github.com/opendataloader-project/opendataloader-pdf) · [📖 Docs ↗](https://opendataloader.org/docs/quick-start-python) · [🌐 Site ↗](https://opendataloader.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/opendataloader-pdf/)</sub>

<a name="docling"></a>
### 🥈 [docling](https://github.com/docling-project/docling) <sub>score [92](../README.md#-how-we-rank "Score 92/100. Adoption: widely used (95) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 71k · MIT · Nov 2026</sub>

**Python library that converts PDFs, Office files and more into structured text.**

Docling parses PDF, DOCX, PPTX, XLSX, HTML, EPUB, images, audio and other formats into a unified DoclingDocument, then exports to Markdown, HTML or lossless JSON. PDF handling covers layout, reading order, tables, code and formulas, with OCR and VLM options such as GraniteDocling. It runs locally via a Python API or CLI, and also ships an MCP server and a docling-serve API server.

- **+** Handles a wide format list: PDF, Office, ODF, EPUB, email, calendar, audio and video
- **+** PDF layout, table structure, formula and reading-order extraction with OCR for scans
- **+** Runs locally, usable in air-gapped setups; MIT licensed
- **+** Integrates with LangChain, LlamaIndex, CrewAI and Haystack; has MCP server and API server
- **−** Model weights carry their own licenses, separate from the MIT code
- **−** Metadata extraction and chemistry understanding are listed as not yet available
- **−** Requires Python 3.10 or higher; Python 3.9 dropped in 2.70.0

<sub>GPU optional · Docker · Models: GraniteDocling, VLMs, ASR models, OCR engines · [Repo](https://github.com/docling-project/docling) · [📖 Docs ↗](https://docling-project.github.io/docling/) · [🌐 Site ↗](https://docling-project.github.io/docling/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/docling/)</sub>

<a name="mineru"></a>
### 🥉 [mineru](https://github.com/opendatalab/mineru) <sub>score [91](../README.md#-how-we-rank "Score 91/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 84k · custom license · Nov 2026</sub>

**Parses PDFs, images and Office files into Markdown and structured JSON.**

MinerU converts PDFs, scanned images, Office, OpenDocument, EPUB, OFD, HTML and CSV files into Markdown, HTML, LaTeX, DOCX and structured content lists. It offers four parsing tiers (flash, basic, standard, advanced), a Python SDK, a /v1/tasks HTTP API, a multi-service router and a Gradio WebUI. It also ships an agent skill and a local document library with stable page and block locators.

- **+** Handles PDF, images, DOC/DOCX, PPT/PPTX, XLS/XLSX, EPUB, OFD, HTML and CSV inputs
- **+** Four parsing tiers trade speed against layout and OCR quality
- **+** Runs on CPU, with automatic ONNX acceleration on Intel, AMD, NVIDIA and Apple GPUs
- **+** VLM backends include llama.cpp, vLLM and LMDeploy
- **−** 4.1 replaced the /v1/uploads and /v1/parse/jobs APIs, a breaking change for existing clients
- **−** Requires Python 3.11 to 3.14; older interpreters are unsupported
- **−** HuggingFace demo offers only the flash and basic tiers
- **−** License is detected as NOASSERTION, so terms need manual review

<sub>GPU optional · Docker + Compose · Needs Python 3.11-3.14, uv · Models: ONNX, Torch, llama.cpp, vLLM, LMDeploy · [Repo](https://github.com/opendatalab/mineru) · [▶️ Demo ↗](https://huggingface.co/spaces/opendatalab/MinerU) · [📖 Docs ↗](https://opendatalab.github.io/MinerU/) · [🌐 Site ↗](https://mineru.net/OpenSourceTools/Extractor?source=github) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mineru/)</sub>

<a name="agent-reach"></a>
### #&#8288;4 [agent-reach](https://github.com/panniantong/agent-reach) <sub>score [88](../README.md#-how-we-rank "Score 88/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 115k · MIT · Nov 2026</sub>

**CLI that gives coding agents read access to login-gated and Chinese web platforms.**

Agent Reach is a Python CLI that wraps upstream tools such as bili-cli, yt-dlp, Jina Reader and Exa behind one command format: `agent-reach <channel> <action>`. It covers Bilibili, V2EX, GitHub, YouTube, Xiaohongshu, Xueqiu, Reddit, Twitter and others, trying an ordered list of tools per action with fallbacks. It is read-only, and login-gated sites use a dedicated background browser that copies your Chrome session for that site.

- **+** Covers Chinese platforms (Bilibili, Xiaohongshu, V2EX, Xueqiu) that generic agent search handles poorly
- **+** Per-action ordered tool list with automatic fallback when an upstream tool breaks
- **+** Read-only by design: no posting, commenting, liking or messaging
- **+** All tools, logins and settings live in `~/.agent-reach/`, so removal is contained
- **−** Twitter, Facebook and Instagram channels are labeled experimental and may break at any time
- **−** Login-gated channels copy your Chrome session, usually the main account; README advises a spare account
- **−** YouTube and Xiaoyuzhou transcription needs a Groq or OpenAI key
- **−** README is mainly in Chinese; the English docs are a separate file

<sub>no GPU · Needs uv, Python 3.10+, bili-cli, yt-dlp, Jina Reader, Exa, Groq or OpenAI API key (transcription) · [Repo](https://github.com/panniantong/agent-reach) · [📖 Docs ↗](https://github.com/Panniantong/Agent-Reach/blob/main/docs/README_en.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agent-reach/)</sub>

<a name="markitdown"></a>
### #&#8288;5 [markitdown](https://github.com/microsoft/markitdown) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (99) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 199k · MIT · Nov 2026</sub>

**Python library and CLI that converts office files, PDFs and audio to Markdown.**

MarkItDown converts PDF, Word, PowerPoint, Excel, images, audio, HTML, CSV/JSON/XML, ZIP, EPub and YouTube URLs into Markdown that keeps headings, lists, tables and links. It runs as a Python library or the `markitdown` CLI. It can optionally call an OpenAI-compatible LLM for image descriptions, or Azure Document Intelligence and Content Understanding for higher-quality extraction. Output targets LLM pipelines, not human-facing fidelity.

- **+** Covers many formats (PDF, DOCX, PPTX, XLSX, EPub, ZIP, YouTube) through one convert call
- **+** Built-in converters run offline; install only needed formats via extras like [pdf,docx,pptx]
- **+** Plugin system, plus a markitdown-ocr plugin that uses an LLM vision client for embedded images
- **+** Optional Azure Document Intelligence and Content Understanding backends with YAML front matter fields
- **−** Not meant for high-fidelity conversion for human reading, per the README
- **−** Runs with the calling process's privileges; untrusted input must be sanitized by the caller
- **−** Azure backends are billable; Content Understanding is the only route for video
- **−** Repo accepts no web server, REST API or GUI; those must be separate projects

<sub>no GPU · Docker · Needs Python 3.10-3.14, Azure Document Intelligence (optional), Azure Content Understanding (optional), OpenAI-compatible client (optional) · Models: OpenAI-compatible vision models (gpt-4o in examples) · [Repo](https://github.com/microsoft/markitdown) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/markitdown/)</sub>

<a name="marker"></a>
### #&#8288;6 [marker](https://github.com/datalab-to/marker) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: healthy (98) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · Apache-2.0 · Nov 2026</sub>

**Converts PDFs, Office files and images to markdown, JSON, HTML or chunks.**

Marker is a Python library and CLI that converts PDF, image, PPTX, DOCX, XLSX, HTML and EPUB files into markdown, JSON, HTML or chunks. It handles tables, equations, code blocks and image extraction, and strips headers and footers. OCR and layout run through a surya VLM served locally by vLLM or llama.cpp, with an optional LLM pass (Gemini, Claude, OpenAI-compatible, Ollama and others) for higher accuracy.

- **+** Outputs markdown, JSON with block polygons, HTML or chunks from one pipeline
- **+** Fast mode and --disable_ocr allow CPU-only, text-layer extraction
- **+** Extensible processors, converters and block API for custom logic
- **+** Batch CLI with worker pool, multi-GPU and multi-node sharding options
- **−** Model weights use a modified OpenRAIL-M license with revenue limits for commercial use
- **−** Needs Docker with NVIDIA Container Toolkit, or llama.cpp, for the VLM server
- **−** Non-PDF formats require the extra marker-pdf[full] install
- **−** README points to the paid hosted platform as more accurate than Marker

<sub>GPU optional · Needs PyTorch, Python 3.10+, vLLM via Docker (NVIDIA GPU), llama.cpp llama-server (CPU/Apple Silicon) · Models: surya VLM, Gemini, Claude, OpenAI-compatible, Azure · [Repo](https://github.com/datalab-to/marker) · [▶️ Demo ↗](https://www.datalab.to/playground) · [📖 Docs ↗](https://documentation.datalab.to) · [🌐 Site ↗](https://www.datalab.to) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/marker/)</sub>

<a name="cvat"></a>
### #&#8288;7 [cvat](https://github.com/cvat-ai/cvat) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: widely used (80) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · MIT · Nov 2026</sub>

**Self-hosted annotation tool for image, video, audio and 3D point cloud datasets.**

CVAT is a web-based labeling platform for computer vision datasets. It supports boxes, polygons, masks, keypoints and cuboids on images, video, audio and point clouds, organized into projects, tasks and jobs with roles and review. Auto-annotation runs through Nuclio serverless functions (SAM, YOLO v7, RetinaNet and others), and data exports in 20+ formats such as COCO and YOLO.

- **+** Covers image, video, audio and 3D point cloud annotation in one tool
- **+** Exports and imports 20+ formats including COCO, YOLO, Pascal VOC and KITTI
- **+** Python SDK, CLI and REST API for scripting task creation and exports
- **+** Multi-user organizations with roles, task assignment, comments and review workflows
- **−** Auto-annotation needs a separate Nuclio serverless stack and manual nuctl function deployment
- **−** Built-in SAM 2/SAM 3 labeling, SSO and quality control UI are paid-only
- **−** Serverless model code may use third-party assets with non-commercial licenses
- **−** Safari is unsupported and Firefox has caveats; testing targets Chromium browsers

<sub>Docker + Compose · Needs Docker Engine, Docker Compose, Git, Nuclio (for auto-annotation), Grafana (for analytics) · Models: SAM, IOG, RetinaNet R101, HRNet32, TransT · port 8080 · [Repo](https://github.com/cvat-ai/cvat) · [▶️ Demo ↗](https://app.cvat.ai) · [📖 Docs ↗](https://docs.cvat.ai/docs/) · [🌐 Site ↗](https://www.cvat.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cvat/)</sub>

<a name="cocoindex"></a>
### #&#8288;8 [cocoindex](https://github.com/cocoindex-io/cocoindex) <sub>score [87](../README.md#-how-we-rank "Score 87/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: healthy (90) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Nov 2026</sub>

**Incremental Python pipelines that keep vector indexes and agent context fresh.**

CocoIndex is a Python framework with a Rust core for declaring how source data (files, code, PDFs, Slack, databases) maps to a target such as Postgres/pgvector or LanceDB. It memoizes by input and code hash, so after a change only the affected rows are recomputed and re-embedded. It also tracks lineage from each target row back to its source.

- **+** Memoization keyed on input and code hash re-embeds only changed files
- **+** Pipelines are plain Python functions, not a DAG or YAML config
- **+** Per-row lineage traces target vectors back to source content
- **+** Rust core with retries, back-off and dead-letter queues, per the README
- **−** Library only: no UI, you write and run the pipeline code yourself
- **−** Python 3.10-3.13 supported; other languages are not mentioned
- **−** Quickstart needs an external target store such as Postgres
- **−** README is marketing-heavy; connector and scale details are only in the docs

<sub>Needs Python 3.10-3.13, Postgres (pgvector) or LanceDB as target · Models: sentence-transformers · [Repo](https://github.com/cocoindex-io/cocoindex) · [📖 Docs ↗](https://cocoindex.io/docs) · [🌐 Site ↗](https://cocoindex.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cocoindex/)</sub>

<a name="crawl4ai"></a>
### #&#8288;9 [Crawl4AI](https://github.com/unclecode/crawl4ai) <sub>score [86](../README.md#-how-we-rank "Score 86/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 88k · Apache-2.0 · Nov 2026</sub>

**Async Python web crawler that outputs LLM-ready Markdown and structured JSON.**

Crawl4AI drives Playwright browsers (Chromium, Firefox, WebKit) to fetch pages and convert them to filtered Markdown or JSON, using CSS/XPath schemas or an LLM. It ships as a pip library, a `crwl` CLI and a Docker REST server with MCP, a dashboard and a playground on port 11235. A separate hosted cloud adds search, SERP and answer endpoints.

- **+** Schema-based CSS/XPath extraction works without any LLM call
- **+** Fit Markdown filters (pruning, BM25, LLM) strip menus and boilerplate
- **+** Deep crawl with BFS, DFS and score-ordered strategies, resumable after crashes
- **+** Docker server has REST endpoints, MCP and token auth by default
- **−** Search, SERP and answer endpoints exist only in the hosted cloud
- **−** Self-hosted bot-wall handling relies on your own proxies and settings
- **−** Needs a Playwright browser install, so heavier than plain HTTP scrapers
- **−** LLM extraction requires an external provider key or a local model endpoint

<sub>no GPU · Docker + Compose · Needs Playwright browsers (Chromium), Docker (optional), LLM provider via LiteLLM (optional) · Models: any LiteLLM provider (OpenAI, Ollama) · port 11235 · [Repo](https://github.com/unclecode/crawl4ai) · [📖 Docs ↗](https://docs.crawl4ai.com) · [🌐 Site ↗](https://crawl4ai.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/crawl4ai/)</sub>

<a name="labelme"></a>
### #&#8288;10 [labelme](https://github.com/wkentaro/labelme) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · GPL-3.0 · Nov 2026</sub>

**Desktop image annotation tool with polygon labeling and SAM-assisted masks.**

Labelme is a Qt (PySide6) desktop app for annotating images with polygon, rectangle, circle, line and point shapes, saved as JSON files. It exports VOC and COCO datasets and offers AI-assisted annotation: SAM and EfficientSAM for point-to-polygon, YOLO-world and SAM3 for text-to-annotation. It is an application, not a library, with no stable Python API.

- **+** Supports polygon, rectangle, circle, line, point shapes plus image-level flags
- **+** Exports VOC and COCO datasets for segmentation and detection
- **+** Built-in SAM, EfficientSAM, YOLO-world and SAM3 assisted labeling
- **+** Installs with pip; UI translated into 20 languages
- **−** v7 requires Python 3.12+ and PySide6; Qt5 users must pin labelme<7
- **−** No stable Python API; internal modules were made private in v7
- **−** Standalone no-Python app is a paid one-time purchase
- **−** Single-user desktop GUI; no team or review workflow described

<sub>Needs Python 3.12+, PySide6 (Qt6) · Models: SAM, EfficientSAM, YOLO-world, SAM3 · [Repo](https://github.com/wkentaro/labelme) · [📖 Docs ↗](https://www.labelme.io/docs/install-labelme-terminal) · [🌐 Site ↗](https://labelme.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/labelme/)</sub>

<a name="liteparse"></a>
### #&#8288;11 [liteparse](https://github.com/run-llama/liteparse) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: popular (75) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Nov 2026</sub>

**Local PDF and Office document parser with bounding boxes and Markdown output.**

LiteParse extracts spatially laid-out text from PDFs using PDFium, at roughly 2-5 ms per page, and converts DOCX, XLSX, PPTX and images through LibreOffice or Rust image crates. It outputs Markdown, JSON with bounding boxes, or plain text, and can run Tesseract or an HTTP OCR server on pages that need it. A Rust core ships with a `lit` CLI plus Node.js, Python and WASM bindings.

- **+** No ML model or GPU required; ~2-5 ms per page text extraction via PDFium
- **+** Bindings for Rust, Node.js, Python and browser WASM, with one `lit` CLI
- **+** Pluggable OCR: bundled Tesseract or any server following its OCR HTTP API spec
- **+** Worker pool mode gives parallel parsing and hard per-parse timeouts
- **−** Markdown is heuristic and rule-based; complex layouts may render imperfectly
- **−** Charts score near zero in its own ParseBench results
- **−** Math is not output as LaTeX; olmOCR-bench math categories score 0%
- **−** Office formats depend on LibreOffice for conversion

<sub>no GPU · Docker · Needs LibreOffice (for DOCX/XLSX/PPTX), Optional HTTP OCR server (EasyOCR, PaddleOCR, RapidOCR) · Models: Tesseract OCR (bundled), PaddleOCR PP-OCRv5 via HTTP, EasyOCR via HTTP · [Repo](https://github.com/run-llama/liteparse) · [📖 Docs ↗](https://developers.llamaindex.ai/liteparse/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/liteparse/)</sub>

<a name="langextract"></a>
### #&#8288;12 [langextract](https://github.com/google/langextract) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (92) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · Apache-2.0 · Nov 2026</sub>

**Python library that extracts grounded structured data from text using LLMs.**

LangExtract is a Python library that takes a prompt and a few examples and uses an LLM to pull structured entities and attributes out of unstructured text. Each extraction is mapped to its character span in the source, and results can be rendered as an interactive HTML review page. Long documents are handled with chunking, parallel workers and multiple passes, using Gemini, OpenAI or local Ollama models.

- **+** Each extraction carries a char_interval into the source; ungrounded results get None
- **+** Long-document handling via chunking, max_workers and extraction_passes for recall
- **+** Supports Gemini, OpenAI (with Batch API), Vertex AI batch and local Ollama models
- **+** Plugin system for custom model providers, plus a community provider registry
- **−** Needs few-shot examples; misaligned examples trigger prompt alignment warnings
- **−** Ollama provider does not support output_schema
- **−** Controlled generation is described for supported models like Gemini; quality depends on the LLM
- **−** Library only, no server or UI; visualization is a static HTML file

<sub>no GPU · Docker · Needs Gemini, OpenAI or Vertex AI API key, or a local Ollama server · Models: Gemini, OpenAI, Ollama, Vertex AI, OpenAI-compatible endpoints · [Repo](https://github.com/google/langextract) · [▶️ Demo ↗](https://google-langextract.hf.space/) · [📖 Docs ↗](https://github.com/google/langextract/blob/main/docs/examples/longer_text_example.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/langextract/)</sub>

<a name="moli"></a>
### #&#8288;13 [moli](https://github.com/lexmount/moli) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (85) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · Apache-2.0 · Nov 2026</sub>

**Rust headless browser for AI agents with CLI, CDP and WebDriver access.**

Moli is a standalone browser kernel written in Rust (V8, Stylo, Taffy, Parley), not a Chromium wrapper. It fetches pages as HTML, Markdown, JSON or a semantic tree, and serves CDP, WebDriver Classic and WebDriver BiDi from one endpoint. Layout and painting run only on demand with `--layout`, so DOM-only work skips them.

- **+** One binary serves CDP, WebDriver Classic and BiDi; no ChromeDriver or Chrome install needed
- **+** README reports median peak memory of 92 MiB versus 697 MiB for Chrome on 557 tasks
- **+** Layout, screenshots and PDF are opt-in via --layout, so DOM-only fetches skip rendering
- **+** Playwright connects directly over CDP at port 9222; prebuilt installers for Linux, macOS, Windows
- **−** Passes 81.9% of 1,308 comparable Lexbench tasks; Chrome passes 99.8%
- **−** Trails other browsers on text, formula and table extraction in WebMainBench
- **−** No Docker image or compose file detected
- **−** Visual output is software-rendered on CPU, with no GPU compositor or persistent window

<sub>no GPU · Needs libcurl, V8 · port 9222 · [Repo](https://github.com/lexmount/moli) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/moli/)</sub>

<a name="surya"></a>
### #&#8288;14 [surya](https://github.com/datalab-to/surya) <sub>score [83](../README.md#-how-we-rank "Score 83/100. Adoption: widely used (83) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 22k · Apache-2.0 · Nov 2026</sub>

**Document OCR, layout and table recognition VLM with a lightweight Python client.**

Surya is a 689M-parameter vision-language model that does page OCR, layout analysis with reading order, and table recognition (HTML with colspan/rowspan). The surya-ocr package is a thin client that spawns or attaches to a vllm, llama.cpp or MLX server. It ships CLI commands, a Python API and a local web viewer (surya_gui). Code is Apache-2.0; model weights use a modified OpenRAIL-M license.

- **+** One VLM handles OCR, layout, reading order, tables and inline math (KaTeX LaTeX)
- **+** Backends: vllm on NVIDIA, llama.cpp on CPU, mlx_vlm on Apple Silicon
- **+** Reports 85.9 on OmniParseBench and 4.5 pages/s on one H100 at 192 DPI
- **+** Can attach to any OpenAI-compatible server via SURYA_INFERENCE_URL
- **−** Model weights are not Apache: free only for research, personal use, and startups under $5M
- **−** NVIDIA GPU path needs Docker or Podman plus the NVIDIA Container Toolkit
- **−** Outputs blocks and HTML only; full Markdown or RAG conversion needs the separate Marker project
- **−** Self-hosted servers must return special tokens (llama-server needs --special)

<sub>GPU optional · Needs vllm (Docker/Podman + NVIDIA Container Toolkit), llama.cpp llama-server, mlx_vlm · Models: Surya 2.5 (689M VLM), OpenAI-compatible servers · port 8000 · [Repo](https://github.com/datalab-to/surya) · [▶️ Demo ↗](https://www.datalab.to/playground) · [📖 Docs ↗](https://documentation.datalab.to) · [🌐 Site ↗](https://www.datalab.to) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/surya/)</sub>

<a name="rerun"></a>
### #&#8288;15 [rerun](https://github.com/rerun-io/rerun) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Nov 2026</sub>

**Multimodal data logging, viewer and query engine for robotics.**

Rerun logs multi-rate data such as images, point clouds, transforms, time series, joint states and video through Python, Rust and C++ SDKs. A built-in viewer renders the streams in sync on a timeline. The stored data can be queried with dataframes or SQL and streamed into training. It reads MCAP, rrd and LeRobot, and the storage layer is written in Rust.

- **+** SDKs for Python, Rust and C++; pip install rerun-sdk bundles the viewer
- **+** Ingests MCAP, rrd and LeRobot alongside direct SDK logging
- **+** Time-aware viewer with scrubbing; in-memory buffer size is configurable
- **+** Viewer also runs in the browser at rerun.io/viewer
- **−** API still evolving; README warns to expect breaking changes
- **−** Viewer slows down with too many entities
- **−** Multi-million point clouds can be slow
- **−** Rerun Hub catalog for teams is commercial, limited to design partners

<sub>Needs nasm (optional, for faster video decoding when building the CLI) · [Repo](https://github.com/rerun-io/rerun) · [▶️ Demo ↗](https://www.rerun.io/viewer) · [📖 Docs ↗](https://rerun.io/docs) · [🌐 Site ↗](https://www.rerun.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rerun/)</sub>

<a name="scrapegraph-ai"></a>
### #&#8288;16 [scrapegraph-ai](https://github.com/scrapegraphai/scrapegraph-ai) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: widely used (89) · Freshness: active (100) · Maintenance: fair (69) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 33k · MIT · Oct 2026</sub>

**Python library that builds LLM-driven scraping pipelines from a prompt and a URL.**

ScrapeGraphAI is a Python library that extracts structured data from websites and local files (XML, HTML, JSON, Markdown) given a natural-language prompt. It provides graph pipelines such as SmartScraperGraph, SearchGraph and ScriptCreatorGraph, with multi-page variants that call the LLM in parallel. It works with OpenAI, Groq, Azure, Gemini, MiniMax or local models through Ollama, and uses Playwright to fetch pages.

- **+** Prompt plus URL returns a JSON dict; no per-site selectors to write
- **+** Runs against local Ollama models or hosted APIs by changing the llm config
- **+** Several pipelines: single page, multi-page, search results, Python script generation
- **+** Multi-page graph variants run LLM calls in parallel
- **−** Proxies, anti-bot handling and scaling are left to the user in the open-source version
- **−** Needs a separate `playwright install` step to fetch page content
- **−** Anonymous telemetry is on by default; opt out via SCRAPEGRAPHAI_TELEMETRY_ENABLED=false
- **−** README steers users to the paid managed API for crawl and monitor features

<sub>GPU optional · Docker + Compose · Needs Playwright, Ollama (for local models), LLM provider API key (for hosted models) · Models: Ollama, OpenAI, Groq, Azure, Gemini · [Repo](https://github.com/scrapegraphai/scrapegraph-ai) · [📖 Docs ↗](https://docs.scrapegraphai.com/introduction) · [🌐 Site ↗](https://scrapegraphai.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/scrapegraph-ai/)</sub>

<a name="unstructured"></a>
### #&#8288;17 [unstructured](https://github.com/unstructured-io/unstructured) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: healthy (87) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Nov 2026</sub>

**Python library that parses PDFs, Office files and HTML into typed elements.**

The unstructured library parses documents such as PDF, HTML, Word, email and images into typed elements (titles, narrative text, tables). A single `partition` function detects the file type and routes it to a format-specific parser. It installs from PyPI with per-format extras or runs from a Docker image, and some formats need system packages such as poppler, tesseract and libreoffice.

- **+** One `partition` call auto-detects file type and dispatches to format-specific parsers
- **+** Per-format pip extras (docx, pptx, pdf) keep installs smaller for narrow use cases
- **+** Apache-2.0 licensed; multi-platform Docker images for x86_64 and Apple silicon
- **+** Batch ingestion and connectors are available through the separate unstructured-ingest project
- **−** README's own benchmark lists table cell content accuracy of 0.426 versus 0.866 for the paid API
- **−** PDF, image and Office parsing needs system packages: poppler, tesseract, libreoffice
- **−** Sends anonymous telemetry by default; opt out with DO_NOT_TRACK or SCARF_NO_ANALYTICS
- **−** Highest-quality output is only in the hosted Transform API, not this library

<sub>Docker · Needs poppler-utils, tesseract-ocr, libmagic-dev, libreoffice · [Repo](https://github.com/unstructured-io/unstructured) · [📖 Docs ↗](https://docs.unstructured.io) · [🌐 Site ↗](https://unstructured.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/unstructured/)</sub>

<a name="firecrawl"></a>
### #&#8288;18 [Firecrawl](https://github.com/firecrawl/firecrawl) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: widely used (100) · Freshness: active (100) · Maintenance: patchy (42) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 210k · AGPL-3.0 · Nov 2026</sub>

**Web API that turns sites and searches into markdown or JSON for LLMs.**

Firecrawl exposes REST endpoints to search the web, scrape a URL, crawl a site, map its URLs, batch-scrape, parse documents (PDF, DOCX) and run page actions such as click and scroll. Output is markdown, HTML, screenshots or schema-based JSON. SDKs cover Python, Node.js, Go, Java, Elixir, Rust and Ruby, plus a CLI and an MCP server. The README examples use the hosted API with a key; self-hosting details are not in the excerpt.

- **+** Endpoints for search, scrape, crawl, map, batch scrape and document parsing
- **+** Official SDKs for seven languages, plus a CLI and MCP server
- **+** Outputs markdown, HTML, screenshots or schema-based structured JSON
- **+** Page actions and an interact endpoint for JS-heavy pages
- **−** README examples target the hosted API and require an API key
- **−** AGPL-3.0 license restricts use in closed-source network services
- **−** Agent endpoint runs the spark-2 model; self-hosted availability is unknown

<sub>Compose · Needs Firecrawl API key (hosted service) · Models: spark-2 · [Repo](https://github.com/firecrawl/firecrawl) · [▶️ Demo ↗](https://firecrawl.dev/playground) · [📖 Docs ↗](https://docs.firecrawl.dev) · [🌐 Site ↗](https://firecrawl.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/firecrawl/)</sub>

<a name="tesseract"></a>
### #&#8288;19 [tesseract](https://github.com/tesseract-ocr/tesseract) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: widely used (96) · Freshness: active (100) · Maintenance: fair (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 78k · Apache-2.0 · Nov 2026</sub>

**OCR engine and command-line tool with LSTM recognition for 100+ languages.**

Tesseract is a C++ OCR engine (libtesseract) with a tesseract command-line program. Version 4 and later use an LSTM line-recognition engine, and the legacy Tesseract 3 engine is available with --oem 0. It reads PNG, JPEG and TIFF through Leptonica and writes plain text, hOCR, PDF, TSV, ALTO and PAGE.

- **+** Recognizes more than 100 languages with UTF-8 support using downloadable traineddata files
- **+** Outputs plain text, hOCR, PDF, invisible-text PDF, TSV, ALTO and PAGE
- **+** C and C++ APIs plus a CLI; wrappers for other languages are listed in the docs
- **+** Can be trained for additional languages; Apache-2.0 licensed
- **−** No GUI included; third-party front-ends are needed
- **−** Accuracy depends on input image quality; preprocessing is often required
- **−** Leptonica opens images only, not documents like PDF
- **−** Legacy engine mode needs separate legacy-compatible traineddata files

<sub>no GPU · Needs Leptonica, traineddata files · Models: LSTM traineddata, legacy Tesseract 3 traineddata · [Repo](https://github.com/tesseract-ocr/tesseract) · [📖 Docs ↗](https://tesseract-ocr.github.io/tessdoc/) · [🌐 Site ↗](https://tesseract-ocr.github.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tesseract/)</sub>

<a name="skill-seekers"></a>
### #&#8288;20 [skill_seekers](https://github.com/yusufkaraaslan/skill_seekers) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (78) · Freshness: active (100) · Maintenance: fair (64) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 15k · MIT · Nov 2026</sub>

**CLI that turns docs, repos, PDFs and videos into AI skills and RAG data.**

Skill Seekers is a Python CLI that scrapes 18 source types (doc sites, GitHub repos, PDFs, Word, Jupyter, OpenAPI, YouTube, Confluence, Notion and others) and packages the result for 22 targets. Targets include Claude/Gemini/OpenAI skills, LangChain and LlamaIndex documents, and vector stores such as Chroma, Qdrant and Pinecone. It also ships an MCP server with 40 tools and can install skills into 19 coding agents.

- **+** Handles 18 source types and exports to 22 targets from one scrape
- **+** AI enhancement runs via API providers or local agents such as Claude Code, no API cost
- **+** Ships an MCP server (40 tools) with stdio and HTTP transports
- **+** Doc scraper checks sitemap.xml and llms.txt, and falls back to headless browser rendering
- **−** Quality of SKILL.md depends on an external LLM agent or API for enhancement
- **−** Video visual extraction needs extra installs, including GPU-specific PyTorch and easyocr
- **−** Large doc sets (10K+ pages) need a separate streaming mode and take long
- **−** Speed and quality claims like '99% faster' are not backed by published benchmarks

<sub>GPU optional · Docker + Compose · Needs Python 3.10+, Git, Anthropic/Gemini/OpenAI API or local agent (optional), Whisper, PyTorch, easyocr (video extras) · Models: Claude, Gemini, OpenAI, Kimi, MiniMax · port 8765 · [Repo](https://github.com/yusufkaraaslan/skill_seekers) · [📖 Docs ↗](https://github.com/yusufkaraaslan/Skill_Seekers/blob/main/docs/README.md) · [🌐 Site ↗](https://skillseekersweb.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/skill-seekers/)</sub>

<a name="x-anylabeling"></a>
### #&#8288;21 [x-anylabeling](https://github.com/cvhub520/x-anylabeling) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (70) · Freshness: active (100) · Maintenance: healthy (94) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · GPL-3.0 · Nov 2026</sub>

**Desktop app for AI-assisted annotation of images, video, text and point clouds.**

X-AnyLabeling is a cross-platform desktop annotation tool for building datasets for detection, segmentation, pose, OCR, tracking, VQA and 3D point clouds. It integrates models such as YOLO variants, SAM 1/2/3, Grounding DINO and several VLMs for auto-labeling, run locally via ONNX Runtime, TensorRT or OpenCV DNN, or remotely via vLLM, SGLang or its own server. It imports and exports COCO, VOC, YOLO, DOTA, MOT and others.

- **+** Wide model library: YOLO family, SAM 1/2/3, Grounding DINO, RF-DETR, PP-OCR, Qwen3-VL
- **+** Exports COCO, VOC, YOLO, DOTA, MOT, PPOCR, ShareGPT and other formats
- **+** Covers many tasks in one tool: boxes, polygons, rotated boxes, tracking, OCR, VQA, 3D point clouds
- **+** Runs on Windows, Linux and macOS; remote inference via X-AnyLabeling-Server, vLLM or SGLang
- **−** GPL-3.0 license imposes copyleft terms on derived or redistributed code
- **−** Requires Python 3.11+ for source or PyPI install
- **−** Contributions require signing a Contributor License Agreement

<sub>GPU optional · Needs ONNX Runtime, TensorRT, OpenCV DNN, vLLM, SGLang · Models: ONNX, YOLO, SAM, Grounding DINO, Qwen3-VL · [Repo](https://github.com/cvhub520/x-anylabeling) · [📖 Docs ↗](https://xanylabeling.com/docs/x-anylabeling/user_guide) · [🌐 Site ↗](https://xanylabeling.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/x-anylabeling/)</sub>

<a name="trafilatura"></a>
### #&#8288;22 [trafilatura](https://github.com/adbar/trafilatura) <sub>score [79](../README.md#-how-we-rank "Score 79/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.2k · Apache-2.0 · Nov 2026</sub>

**Python library and CLI that extracts main text and metadata from web pages.**

Trafilatura downloads web pages, crawls sitemaps and feeds, and extracts main text, metadata and comments from HTML while dropping headers, footers and boilerplate. It uses its own rule-based extractor with jusText and readability-lxml as fallbacks, and outputs TXT, Markdown, CSV, JSON, HTML, XML or XML-TEI. It runs as a Python package or command-line tool and needs no database.

- **+** Reports top results in ScrapingHub and Bevendorff et al. 2023 extraction benchmarks
- **+** Handles discovery too: sitemaps (TXT, XML), feeds (ATOM, JSON, RSS), URL filtering and deduplication
- **+** Outputs TXT, Markdown, CSV, JSON, HTML, XML and XML-TEI, with metadata fields
- **+** Works on live URLs or already downloaded HTML; no database required
- **−** Rule-based extraction with fallbacks; no LLM or JavaScript rendering mentioned
- **−** Versions before v1.8.0 are GPLv3+, which matters when pinning old releases
- **−** Not an AI-native tool; LLM or RAG pipeline integration is left to the user

<sub>no GPU · Needs jusText, readability-lxml · [Repo](https://github.com/adbar/trafilatura) · [📖 Docs ↗](https://trafilatura.readthedocs.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/trafilatura/)</sub>

<a name="label-studio"></a>
### #&#8288;23 [label-studio](https://github.com/humansignal/label-studio) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 29k · Apache-2.0 · Nov 2026</sub>

**Multi-user data labeling tool for audio, text, images, video and time series.**

Label Studio is a web-based annotation tool for preparing and correcting ML training data across images, audio, text, HTML, video and time series. Labeling interfaces are defined in a configuration language, with included templates, and results export to various model formats. It can connect to an ML backend for pre-labeling, online learning and active learning, and has a REST API for pipelines.

- **+** Handles images, audio, text, HTML, video and time series in one instance
- **+** Installs via pip, Docker, or a Compose stack with Nginx and PostgreSQL
- **+** ML backend SDK supports pre-labeling, online learning and active learning
- **+** Imports from S3, GCS and files; REST API for pipeline integration
- **−** Default install stores data in SQLite; PostgreSQL needs the Compose setup
- **−** Some features are tied to paid editions; README links a comparison page
- **−** ML integration needs a separately run backend server
- **−** Windows install requires manually downloading a prebuilt lxml wheel

<sub>no GPU · Docker + Compose · Needs PostgreSQL (optional, Compose), Nginx (optional, Compose), MinIO (optional) · Models: Custom ML backends via Label Studio ML SDK · port 8080 · [Repo](https://github.com/humansignal/label-studio) · [📖 Docs ↗](https://labelstud.io/guide/) · [🌐 Site ↗](https://labelstud.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/label-studio/)</sub>

<a name="rea-video"></a>
### #&#8288;24 [rea-video](https://github.com/juneyaooo/rea-video) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: popular (76) · Freshness: active (100) · Maintenance: fair (76) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Nov 2026</sub>

**Agent skill and CLI that breaks a video into shots and judges how each was made.**

rea-video splits a video into shots and decides for each whether it was filmed, AI-generated or built in code, using frame cadence, sensor noise, metadata AIGC tags and audio analysis. It outputs a remake plan and a report.html with per-shot evidence, prompts, camera and lighting notes, and an audio breakdown. It is designed to be driven by Claude Code, Codex or a similar agent, and can optionally use Gemini or Doubao for better accuracy.

- **+** Offline tools-only mode needs no paid model; README reports 98–99% accuracy on original files
- **+** Judges each shot separately as live, AI, 3D or code, then reassembles on the original timeline
- **+** Exports captions to SRT/ASS and reports BPM, cuts and sound effect placement
- **+** Remake plan batches shots by target video model limits such as clip length and reference images
- **−** Accuracy on re-encoded platform videos drops to 88.6% without a vision model or agent review
- **−** Does not render video; automatic regeneration needs the separate capsule-cinema project
- **−** Docs are in Chinese only for now
- **−** Built around an agent workflow; no standalone UI or hosted demo

<sub>Needs ffmpeg, Python 3.10+ · Models: Gemini, Doubao · [Repo](https://github.com/juneyaooo/rea-video) · [🌐 Site ↗](https://www.reavideo.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/rea-video/)</sub>

<a name="kordoc"></a>
### #&#8288;25 [kordoc](https://github.com/chrisryugj/kordoc) <sub>score [78](../README.md#-how-we-rank "Score 78/100. Adoption: known (32) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.1k · MIT · Nov 2026</sub>

**Parses HWP, HWPX, PDF and Office files into Markdown, as library, CLI and MCP server.**

kordoc converts Korean government document formats (HWP 3.x/5.x, HWPX, HWPML) plus PDF, XLS/XLSX, DOCX, PPTX and images into Markdown and structured blocks. It also writes HWPX from Markdown, converts HWP to HWPX, fills forms and lints documents. It runs as a Node.js library, a CLI, and an MCP server with 22 tools, with local CPU OCR and an offline mode.

- **+** Reads HWP/HWPX without Hancom Office; 10,342/10,342 tables matched on 2,424 HWPX files
- **+** Local OCR on CPU with no API key; KORDOC_OFFLINE=1 blocks all external network calls
- **+** Emits RAG chunks with heading paths, plus Python and Java SDKs
- **+** Also generates HWPX from Markdown, converts HWP to HWPX, and fills forms
- **−** README is written in Korean; an English version is linked separately
- **−** OCR table structure matched only 33 of 65 tables in its own benchmark
- **−** Parallel batch conversion with --jobs increases memory use
- **−** HWP to HWPX conversion fully matches only 69 of 232 compared pairs

<sub>no GPU · Needs Node.js 20+ · Models: HWP 3.x/5.x, HWPX, HWPML, PDF, XLS/XLSX · [Repo](https://github.com/chrisryugj/kordoc) · [📖 Docs ↗](https://github.com/chrisryugj/kordoc/blob/main/docs/usage.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kordoc/)</sub>

<a name="dataflow"></a>
### #&#8288;26 [dataflow](https://github.com/opendcai/dataflow) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (64) · Freshness: active (100) · Maintenance: healthy (93) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.7k · Apache-2.0 · Nov 2026</sub>

**Operator-based Python pipelines for generating and cleaning LLM training data.**

DataFlow is a Python framework that turns noisy sources (PDFs, plain text, low-quality QA pairs) into datasets for pre-training, SFT and RL, using composable operators grouped into pipelines. It ships ready-made pipelines for text, reasoning, Text2SQL, knowledge-base cleaning and agentic RAG, plus a visual WebUI started with `dataflow webui` and an agent that assembles pipelines.

- **+** Pipeline → Operator → Prompt structure, with custom operators packaged via GitHub or PyPI
- **+** Ready-made pipelines for text, reasoning, Text2SQL, knowledge-base cleaning and agentic RAG
- **+** Works with API LLMs or local vLLM inference (`open-dataflow[vllm]`)
- **+** Visual WebUI via `dataflow webui`, plus a DataFlow Agent that builds pipelines
- **−** Output quality depends on the LLM backend you configure; API use needs a DF_API_KEY
- **−** Local GPU inference needs the vllm extra and a CUDA Docker image (cu124)
- **−** Several pieces (WebUI, Skills, RayOrch, MM) live in separate repos
- **−** Some tutorials are hosted on Bilibili and Feishu, with a Chinese-language focus

<sub>GPU optional · Docker · Needs OpenAI-compatible LLM API or vLLM, uv · Models: OpenAI-compatible APIs, vLLM local models · [Repo](https://github.com/opendcai/dataflow) · [▶️ Demo ↗](https://colab.research.google.com/drive/1haosl2QS4N4HM7u7HvSsz_MnLabxexXl?usp=sharing) · [📖 Docs ↗](https://OpenDCAI.github.io/DataFlow-Doc/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/dataflow/)</sub>

<a name="openmed"></a>
### #&#8288;27 [openmed](https://github.com/maziyarpanahi/openmed) <sub>score [74](../README.md#-how-we-rank "Score 74/100. Adoption: popular (54) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · Apache-2.0 · Nov 2026</sub>

**Clinical NER and PII de-identification SDK that runs locally on CPU, GPU, Apple, mobile.**

OpenMed is a Python SDK with a registry of clinical NER and PII models. It extracts diseases, drugs, anatomy and genes from medical text and de-identifies it by mask, replace, hash or date shift. It runs on CPU, CUDA, Apple MLX, Android via ONNX Runtime Mobile and browsers via Transformers.js, and also offers a REST service, an MCP server and agent skills.

- **+** Same extract_pii and deidentify API across PyTorch, MLX, ONNX, Swift, Kotlin and Transformers.js
- **+** Runs offline from a local model directory without contacting the Hugging Face Hub
- **+** PII support for 42 language codes, 35 of them model-backed
- **+** Ships REST endpoints, an MCP server and agent skills
- **−** Only the SDK source is Apache-2.0; model and dataset licenses vary
- **−** SDK use alone does not establish HIPAA compliance; expert review is required
- **−** Clinical brief demo uses synthetic test doubles, not validated models
- **−** Mobile, MLX and browser paths need per-model exported artifacts

<sub>GPU optional · Docker + Compose · Needs Hugging Face Hub (model download), PyTorch, MLX (optional, Apple Silicon), ONNX Runtime (optional) · Models: Hugging Face PyTorch, MLX, ONNX, CoreML, Transformers.js · port 8080 · [Repo](https://github.com/maziyarpanahi/openmed) · [📖 Docs ↗](https://openmed.life/docs) · [🌐 Site ↗](https://openmed.life/docs) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/openmed/)</sub>

<a name="chandra"></a>
### #&#8288;28 [chandra](https://github.com/datalab-to/chandra) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (74) · Freshness: active (100) · Maintenance: fair (67) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · Apache-2.0 · Nov 2026</sub>

**OCR model that converts PDFs and images to Markdown, HTML or JSON with layout.**

Chandra OCR 2 is a vision-language OCR model and Python CLI that turns images and PDFs into Markdown, HTML or JSON while keeping layout, tables, math, forms and handwriting. It runs locally through HuggingFace or against a vLLM server, and ships a Streamlit demo app. Weights use a modified OpenRAIL-M license, separate from the Apache-2.0 code.

- **+** Outputs Markdown, HTML and JSON with layout, extracted images and captions
- **+** Supports 90+ languages; README reports 77.8% average on its own 43-language benchmark
- **+** Two backends: local HuggingFace or vLLM server with parallel workers
- **+** Handles handwriting, math, tables and checkbox forms; CLI takes page ranges and directories
- **−** Weights are OpenRAIL-M: free only for research, personal use and startups under $2M
- **−** Hosted Datalab API is stated to be more accurate than the open weights
- **−** Benchmarks are mostly self-published; throughput is 1.44 pages/s on an H100
- **−** The chandra_vllm launcher depends on Docker; VRAM and RAM requirements are unknown

<sub>GPU required · Needs vLLM, Docker, HuggingFace Transformers, PyTorch · Models: datalab-to/chandra-ocr-2, HuggingFace, vLLM · port 8000 · [Repo](https://github.com/datalab-to/chandra) · [▶️ Demo ↗](https://www.datalab.to/playground) · [📖 Docs ↗](https://documentation.datalab.to) · [🌐 Site ↗](https://www.datalab.to) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chandra/)</sub>

<a name="unstract"></a>
### #&#8288;29 [unstract](https://github.com/zipstack/unstract) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (61) · Freshness: active (100) · Maintenance: fair (78) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.5k · AGPL-3.0 · Nov 2026</sub>

**Extracts structured JSON from PDFs and scans using LLM prompts.**

Unstract extracts structured JSON from documents such as PDFs, images and scans. Extraction schemas are defined as natural-language prompts in Prompt Studio, then deployed as a REST API or an ETL pipeline that loads results into a warehouse. It also offers an MCP server and an n8n node, and works with OpenAI, Anthropic, Bedrock, Ollama and other LLM providers.

- **+** Prompt Studio defines extraction schemas in natural language instead of per-vendor templates
- **+** Deploys as a REST API or ETL pipeline from S3, GCS, Drive, SFTP to Snowflake, BigQuery, Postgres
- **+** Supports many LLMs, including local Ollama, and vector DBs such as Qdrant, Weaviate, Milvus
- **+** Ships an MCP server and an n8n custom node for agent and workflow integration
- **−** Heavy stack: Django, Celery, FastAPI, Redis, RabbitMQ and PostgreSQL; 8 GB RAM minimum
- **−** LLMChallenge, SinglePass extraction, human review and SSO/RBAC are cloud or enterprise only
- **−** README lists Linux or macOS only; no Windows setup is documented
- **−** Default login unstract/unstract must be changed; losing ENCRYPTION_KEY locks adapter credentials

<sub>RAM ≥ 8 GB · no GPU · Docker + Compose · Needs Docker, Docker Compose, PostgreSQL, Redis, RabbitMQ, LLM provider, Vector database, Text extractor (LLMWhisperer, Unstructured.io or LlamaIndex Parse) · Models: OpenAI, Azure OpenAI, OpenAI Compatible, Anthropic Claude, AWS Bedrock · [Repo](https://github.com/zipstack/unstract) · [📖 Docs ↗](https://docs.unstract.com) · [🌐 Site ↗](https://unstract.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/unstract/)</sub>

<a name="data-juicer"></a>
### #&#8288;30 [data-juicer](https://github.com/datajuicer/data-juicer) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: popular (60) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.3k · Apache-2.0 · Nov 2026</sub>

**Operator-based pipelines for cleaning and deduplicating multimodal training data.**

Data-Juicer is a Python library and CLI (dj-process) that runs YAML-defined pipelines of 200+ operators over text, image, audio and video data, covering filtering, mapping, deduplication and analysis. It runs locally or on Ray clusters, and the README cites 70B samples in 2h on 50 Ray nodes and 5TB deduplicated in 2.8h on 1280 cores. It also ships LLM-based operators and a natural-language refinement model, Juicer.

- **+** 200+ operators across text, image, audio, video and multimodal data
- **+** Reproducible YAML recipes, plus a Python API for composing operators
- **+** Ray-based distributed execution with partitioning, checkpoints and OP fusion
- **+** Supports S3 and HDFS I/O, and loads Hugging Face datasets and gz JSONL
- **−** Many operators need extra dependencies or GPUs; the install is split into extras
- **−** Large-scale performance figures come from big clusters (1280 to 6400 cores)
- **−** Frequent releases with many operator behavior fixes; pin versions for reproducibility
- **−** Docs and several tools are spread across separate repos (hub, agents, sandbox)

<sub>GPU optional · Docker · Needs Ray (distributed mode), S3 or HDFS (optional), Hugging Face / ModelScope models (optional) · Models: Hugging Face models, OpenAI-compatible API, LiteLLM, Juicer-35B-A3B · [Repo](https://github.com/datajuicer/data-juicer) · [▶️ Demo ↗](http://8.138.149.181/) · [📖 Docs ↗](https://datajuicer.github.io/data-juicer/en/main/docs_index.html) · [🌐 Site ↗](https://datajuicer.github.io/data-juicer/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/data-juicer/)</sub>

<a name="sumy"></a>
### #&#8288;31 [sumy](https://github.com/miso-belica/sumy) <sub>score [73](../README.md#-how-we-rank "Score 73/100. Adoption: known (39) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · Apache-2.0 · Nov 2026</sub>

**Extractive text summarizer for web pages and plain text, as library and CLI.**

Sumy is a Python library and command line tool that summarizes HTML pages (by URL) or plain text by selecting key sentences with classic extractive algorithms such as LexRank, Luhn, LSA and Edmundson. It also includes a small evaluation framework for scoring summaries against a reference. It uses no neural or LLM models.

- **+** Installs with pip or uv; usable as a library or via sumy and sumy_eval commands
- **+** Several extractive algorithms (LexRank, Luhn, LSA, Edmundson) with per-language tokenizers
- **+** Built-in evaluation commands compare summaries against a reference text
- **+** Docker image and a Hugging Face Space allow trying it without installing
- **−** Extractive only: picks existing sentences, cannot rewrite or abstract
- **−** Language coverage depends on tokenizers; unsupported languages need manual additions
- **−** Python API example still carries legacy Python 2 compatibility imports

<sub>no GPU · Docker · [Repo](https://github.com/miso-belica/sumy) · [▶️ Demo ↗](https://huggingface.co/spaces/issam9/sumy_space) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sumy/)</sub>

<a name="doctr"></a>
### #&#8288;32 [doctr](https://github.com/mindee/doctr) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (56) · Freshness: active (100) · Maintenance: fair (73) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.4k · Apache-2.0 · Nov 2026</sub>

**Two-stage OCR library for PDFs and images, built on PyTorch.**

docTR is a Python library that extracts text from PDFs and images by running a text detection model, then a text recognition model on each detected word. It returns a structured Document (pages, blocks, lines, words) that can be exported as JSON, and also offers a KIE predictor, optional layout detection and a FastAPI template. Detection and recognition architectures are selectable, with pretrained weights.

- **+** Swappable detection (DBNet, LinkNet, FAST) and recognition (CRNN, SAR, MASTER, ViTSTR, PARSeq, VIPTR) models
- **+** Handles rotated pages and returns nested page/block/line/word output exportable to JSON
- **+** Includes KIE predictor, layout detection and a FastAPI template with OCR and KIE routes
- **+** Hosted Hugging Face Space and Streamlit demo for trying it before installing
- **−** Python 3.11 or higher required; PyTorch is the only supported framework
- **−** API template is minimal; README example uses port 8080 while the server runs on 8002
- **−** Docker GPU images need host CUDA 12.2 or newer
- **−** Default pipeline is OCR only; table structure and layout models are listed but sparsely documented in README

<sub>GPU optional · Docker · Needs PyTorch, Streamlit (demo), FastAPI (API template), weasyprint (URL input) · Models: DBNet, LinkNet, FAST, CRNN, SAR · port 8002 · [Repo](https://github.com/mindee/doctr) · [▶️ Demo ↗](https://huggingface.co/spaces/mindee/doctr) · [📖 Docs ↗](https://mindee.github.io/doctr/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/doctr/)</sub>

<a name="contextgem"></a>
### #&#8288;33 [contextgem](https://github.com/shcherbak-ai/contextgem) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: niche (20) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.1k · Apache-2.0 · Nov 2026</sub>

**Python library for extracting typed, source-referenced data from documents.**

ContextGem is a Python library that extracts structured data from documents using declarative aspects and concepts instead of hand-written prompts. It generates the prompts, validates output into typed items (text, numbers, dates, booleans, labels, ratings, JSON), and maps each item back to source paragraphs or sentences. LLMs run through LiteLLM, and version 1.0 adds decision models that return probabilities for closed questions.

- **+** Items carry references to source paragraphs or sentences, with optional justifications
- **+** Works with any LLM supported by LiteLLM, including Ollama and LM Studio
- **+** Decision models return per-answer probabilities with configurable thresholds
- **+** Optional Docling extra converts PDF, DOCX, PPTX, XLSX, HTML and many other formats
- **−** Tested with hosted LLMs; smaller local models may not follow extraction instructions
- **−** Decision models need an external provider such as TypeSafe Jev or OpenAI Decisions API
- **−** Some formats need LibreOffice (DOC, PPT, XLS, RTF) when converting through Docling
- **−** 1.0 renamed or removed classes and dropped Python 3.10, so 0.x code needs migration

<sub>GPU optional · Needs LiteLLM, Docling (optional), LibreOffice (some formats) · Models: OpenAI, Anthropic, Google, Azure OpenAI, xAI · [Repo](https://github.com/shcherbak-ai/contextgem) · [📖 Docs ↗](https://contextgem.shcherbak.ai/) · [🌐 Site ↗](https://contextgem.shcherbak.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/contextgem/)</sub>

<a name="deeppapernote"></a>
### #&#8288;34 [deeppapernote](https://github.com/917dhj/deeppapernote) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: niche (6) · Freshness: active (100) · Maintenance: healthy (100) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.4k · MIT · Nov 2026</sub>

**Agent skill that turns one paper into an illustrated Obsidian note.**

DeepPaperNote is a skill for Claude Code, Codex and other skill-capable agents. Given a title, DOI, arXiv ID, URL or PDF, it reads the full text, crops figures and tables from the PDF, and saves a structured note into an Obsidian vault with links to related papers. It uses 10 paper-type templates and runs an independent review before saving. Three companion skills handle research memory, vault organization and glossary notes.

- **+** Ten paper-type templates, each with its own note structure and reading criteria
- **+** Crops figures and tables from the PDF and places them beside the discussion
- **+** Stops and asks for the paper when only the abstract is available
- **+** Regenerating a note keeps the My Notes section; existing notes are not silently overwritten
- **−** Needs a skill-capable agent such as Claude Code or Codex; not standalone
- **−** Scanned PDFs need Tesseract and pytesseract for OCR
- **−** Browser Connector extension currently supports only Chrome on macOS
- **−** Quality claims rest on the authors' own rubric and 34 test papers

<sub>no GPU · Needs Python 3.10+, PyMuPDF, Claude Code or Codex (skill-capable agent), Obsidian, Zotero (optional), Tesseract and pytesseract (optional), Semantic Scholar API key (optional) · Models: Claude Code, Codex · [Repo](https://github.com/917dhj/deeppapernote) · [🌐 Site ↗](https://917dhj.github.io/DeepPaperNote/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deeppapernote/)</sub>

<a name="anydoc"></a>
### #&#8288;35 [anydoc](https://github.com/firecrawl/anydoc) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: widely used (84) · Freshness: active (100) · Maintenance: patchy (41) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · MIT · Nov 2026</sub>

**Rust library converting Office, EPUB, CSV and PDF files to Markdown.**

anydoc parses Word, PowerPoint, Excel, OpenDocument, RTF, EPUB, CSV and text-based PDF files into a shared document model and renders GitHub-Flavored Markdown. It ships as a Rust crate with Node.js, Python and WebAssembly bindings, a CLI, and an Agent Skill. Scanned PDFs need an opt-in call to the hosted Firecrawl Parse API.

- **+** Covers 14 formats through one Markdown serializer, so tables and footnotes render consistently
- **+** Pure Rust with no ML models; README reports 4.4 ms median conversion per document
- **+** Detects format from file content, so mislabeled extensions still convert
- **+** Bindings for Node, Python and browser WASM; the demo page converts files locally
- **−** No local OCR; scanned PDFs fail with NeedsOcr unless sent to hosted Firecrawl Parse
- **−** Hosted OCR uploads the whole document, since Parse has no page selection
- **−** Benchmark corpus is not redistributable, so published scores cannot be reproduced
- **−** CSV needs an explicit format or extension because it has no content signature

<sub>no GPU · Needs Firecrawl Parse API (optional, for OCR) · [Repo](https://github.com/firecrawl/anydoc) · [▶️ Demo ↗](https://firecrawl.github.io/anydoc/) · [🌐 Site ↗](https://firecrawl.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/anydoc/)</sub>

<a name="datachain"></a>
### #&#8288;36 [datachain](https://github.com/datachain-ai/datachain) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (29) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.8k · Apache-2.0 · Nov 2026</sub>

**Python library that indexes cloud files into versioned, typed datasets.**

DataChain indexes files in S3, GCS, Azure or local disk into named, versioned datasets with Pydantic schemas, stored as metadata and file pointers in a local SQLite Dataset DB. Pipelines use map/filter/join/save with checkpoint recovery and delta updates that skip unchanged files. An optional skill lets Claude Code, Cursor, Codex, Copilot and Pi build and query these datasets; distributed compute, MCP and the Knowledge Base need the hosted Studio.

- **+** Checkpoint recovery resumes a failed UDF from the last uncommitted batch
- **+** delta=True reprocesses only new or changed files and drops results for deleted ones
- **+** Pydantic return types become queryable columns; vectors stored in the same rows for similarity search
- **+** Data stays in your storage; only metadata and file pointers are indexed locally in SQLite
- **−** Distributed compute, shared registry, MCP endpoint and Knowledge Base require Studio
- **−** Agent skill targets only Claude Code, Cursor, Codex, Copilot and Pi
- **−** Scale claims (hundreds of millions of records) apply to Studio, not the local SQLite DB
- **−** Python-only API; pipelines are written as UDFs with typed signatures

<sub>GPU optional · Needs SQLite (local Dataset DB), S3, GCS or Azure storage (optional), DataChain Studio (optional, for distributed compute and MCP) · Models: open_clip embeddings (example), LLM-enriched summaries via Studio Knowledge Base · [Repo](https://github.com/datachain-ai/datachain) · [📖 Docs ↗](https://www.datachain.ai/docs) · [🌐 Site ↗](https://studio.datachain.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/datachain/)</sub>

<a name="webclaw"></a>
### #&#8288;37 [webclaw](https://github.com/0xmassi/webclaw) <sub>score [68](../README.md#-how-we-rank "Score 68/100. Adoption: niche (26) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · AGPL-3.0 · Nov 2026</sub>

**Rust CLI and MCP server that turns web pages into clean markdown or JSON.**

webclaw fetches a URL and returns main-content markdown, LLM-optimized text, JSON, tables, or CSS/XPath selections. It also offers query-based filtering, token-sized chunks for RAG, numbered citations, crawling, caching and WARC archiving. It ships as a CLI, MCP server, Python wrapper and self-hostable server, with a hosted API at webclaw.io.

- **+** Many output modes: markdown, llm text, tables JSON, selectors, query filtering, and RAG chunks
- **+** Prebuilt binaries for macOS, Linux and Windows, plus Homebrew, Cargo and Docker installs
- **+** npx create-webclaw configures MCP for Claude, Cursor, Windsurf, Codex CLI and others
- **+** Crawl output can be archived to WARC files or cached on disk
- **−** JavaScript rendering needs a build with the browser feature and local Chrome
- **−** AGPL-3.0 license restricts use in closed-source network services
- **−** Chunk token counts are estimates, with 4.5% of chunks over the size in cl100k
- **−** --warc refuses --cache, --cloud and browser render modes such as --render always

<sub>no GPU · Docker + Compose · Needs Chrome (optional, for JavaScript rendering) · [Repo](https://github.com/0xmassi/webclaw) · [📖 Docs ↗](https://webclaw.io/docs) · [🌐 Site ↗](https://webclaw.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/webclaw/)</sub>

<a name="babeldoc"></a>
### #&#8288;38 [babeldoc](https://github.com/funstory-ai/babeldoc) <sub>score [67](../README.md#-how-we-rank "Score 67/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: fair (57) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.9k · AGPL-3.0 · Nov 2026</sub>

**PDF paper translator that keeps layout and outputs bilingual PDFs.**

BabelDOC translates scientific PDFs through an OpenAI-compatible LLM endpoint and rebuilds the layout, producing monolingual and bilingual PDFs. It ships a CLI and a Python API and is mainly meant to be embedded in other programs. It supports glossary CSVs with automatic term extraction, page selection, split translation for large files, and an OCR workaround for scanned documents.

- **+** Outputs monolingual and bilingual PDFs, side by side or on alternating pages
- **+** Glossary CSV support plus automatic term extraction for consistent terminology
- **+** Works with any OpenAI-compatible endpoint, including local servers such as Ollama
- **+** Offline asset package for air-gapped installs; TOML config file
- **−** Only OpenAI-compatible LLMs supported; not optimized for Bing or Google engines
- **−** Mainly tested on English-to-Chinese; other language pairs untested
- **−** README says the CLI is for debugging and gets no end-user support
- **−** No built-in web UI; self-hosted WebUI is in PDFMathTranslate-next

<sub>Needs OpenAI-compatible LLM API, uv, Python 3.12 · Models: OpenAI-compatible APIs, gpt-4o-mini (default), glm-4-flash, deepseek-chat, Ollama · [Repo](https://github.com/funstory-ai/babeldoc) · [▶️ Demo ↗](https://app.immersivetranslate.com/babel-doc/) · [📖 Docs ↗](https://funstory-ai.github.io/BabelDOC/supported_languages/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/babeldoc/)</sub>

<a name="paddleocr"></a>
### #&#8288;39 [paddleocr](https://github.com/paddlepaddle/paddleocr) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: widely used (98) · Freshness: active (100) · Maintenance: weak (23) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 93k · Apache-2.0 · Sep 2026</sub>

**OCR and document parsing toolkit that outputs Markdown and JSON from PDFs and images.**

PaddleOCR runs text recognition (PP-OCRv6) and document parsing (PaddleOCR-VL 0.9B VLM, PP-StructureV3) on PDFs and images, producing Markdown or JSON for RAG pipelines. It runs on CPU, NVIDIA GPU, Kunlunxin XPU and other accelerators, with ONNX, OpenVINO, TensorRT and Transformers backends. Models are on HuggingFace and ModelScope.

- **+** Three PP-OCRv6 tiers (1.5M, 7.7M, 34.5M params) cover edge to server
- **+** One PP-OCRv6 model handles 50 languages; PaddleOCR-VL covers 111
- **+** Outputs Markdown, JSON and DOCX; PP-StructureV3 returns table cell and text coordinates
- **+** Multiple inference backends: Paddle, Transformers, ONNX Runtime, OpenVINO, TensorRT, plus C++ deployment
- **−** Depends on the PaddlePaddle framework; GPU installs need matching CUDA builds
- **−** Benchmark claims such as 96.3% on OmniDocBench are the authors' own
- **−** Python support listed as 3.8 to 3.12 only
- **−** Several pipelines and models, so choosing between PP-OCR, VL and StructureV3 takes reading

<sub>GPU optional · Needs PaddlePaddle · Models: PP-OCRv6, PaddleOCR-VL-1.6, PP-StructureV3, HPD-Parsing, ONNX · [Repo](https://github.com/paddlepaddle/paddleocr) · [▶️ Demo ↗](https://www.paddleocr.com) · [📖 Docs ↗](https://www.paddleocr.ai/latest/en/version3.x/pipeline_usage/pipeline_overview.html) · [🌐 Site ↗](https://www.paddleocr.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paddleocr/)</sub>

<a name="textract"></a>
### #&#8288;40 [textract](https://github.com/deanmalmgren/textract) <sub>score [65](../README.md#-how-we-rank "Score 65/100. Adoption: known (48) · Freshness: active (100) · Maintenance: fair (68) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.7k · MIT · Oct 2026</sub>

**Python library and CLI that extracts text from many document formats.**

textract extracts plain text from documents through a single Python interface and command line. The README gives only a one-line description and a link to the full documentation on Read the Docs, so supported formats and system dependencies are not listed there. It does not use models itself; it prepares document text for downstream use.

- **+** Published on PyPI, so installation is a standard pip install
- **+** MIT license
- **+** Full documentation hosted on Read the Docs
- **+** Latest release dated 2026-09-01, with recent commits
- **−** README has no usage example or install instructions
- **−** README badges point to Travis CI, which suggests dated CI config
- **−** Plain text extraction only per README; no layout or table output described

<sub>no GPU · Docker · [Repo](https://github.com/deanmalmgren/textract) · [📖 Docs ↗](http://textract.readthedocs.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/textract/)</sub>

<a name="tesserocr"></a>
### #&#8288;41 [tesserocr](https://github.com/sirfz/tesserocr) <sub>score [63](../README.md#-how-we-rank "Score 63/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: healthy (91) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · MIT · Nov 2026</sub>

**Python wrapper around the Tesseract OCR C++ API, Pillow-friendly.**

tesserocr binds directly to Tesseract's C++ API through Cython and exposes it to Python as PyTessBaseAPI plus helpers like image_to_text and file_to_text. It accepts PIL images or file paths, releases the GIL during recognition, and supports free-threaded CPython. Pre-built wheels for Linux, macOS and 64-bit Windows bundle Tesseract and Leptonica.

- **+** Calls the C++ API directly via Cython, avoiding subprocess calls to the tesseract CLI
- **+** Releases the GIL during recognition, so threads run OCR concurrently
- **+** Wheels bundle Tesseract and Leptonica; no separate install needed
- **+** Exposes layout iterators, word confidences, orientation/script detection and symbol choices
- **−** Language .traineddata files must be installed separately and match the Tesseract version
- **−** Each worker needs its own PyTessBaseAPI instance; instances have no internal lock
- **−** Some Tesseract parameters are process-wide and cannot change during parallel OCR
- **−** Source builds need libtesseract, libleptonica and Cython >=3.1.8,<3.4

<sub>no GPU · Docker · Needs Tesseract (libtesseract >=3.04), Leptonica (>=1.71), Cython (build only), Pillow (optional), tessdata language files · Models: Tesseract traineddata, LSTM engine · [Repo](https://github.com/sirfz/tesserocr) · [🌐 Site ↗](https://pypi.python.org/pypi/tesserocr) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tesserocr/)</sub>

<a name="pdfmathtranslate"></a>
### #&#8288;42 [pdfmathtranslate](https://github.com/pdfmathtranslate/pdfmathtranslate) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: widely used (91) · Freshness: recent (73) · Maintenance: patchy (42) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · AGPL-3.0 · Nov 2026</sub>

**Translates scientific PDFs while keeping formulas, figures and layout intact.**

pdf2zh translates scientific PDFs and writes a translated-only and a bilingual (dual) PDF, preserving formulas, charts, table of contents and annotations. It runs as a CLI, a Gradio web UI on port 7860, a Python or HTTP API, or an MCP server, and calls a configurable translation service (Google by default). Layout detection uses a DocLayout-YOLO ONNX model, with optional OCR and an --ultrafast mode.

- **+** Outputs both translated-only and side-by-side bilingual PDFs from one command
- **+** Many interfaces: CLI, Gradio GUI, Docker, Python API, HTTP API, MCP stdio/SSE
- **+** Selectable translation backends via -s, with Google as the default
- **+** Optional OCR for scanned pages and --ultrafast mode for native-text PDFs
- **−** Python limited to 3.11 to 3.12
- **−** OCR is experimental and targets white-background scans; handwriting may fail
- **−** Last release is 2025-07-11; v2 work lives in a separate PDFMathTranslate-next repo
- **−** --ultrafast is CLI fast mode only and is weaker on complex tables or formulas

<sub>no GPU · Docker + Compose · Needs DocLayout-YOLO ONNX model (Hugging Face download), Translation service (Google default, others configurable) · Models: ONNX · port 7860 · [Repo](https://github.com/pdfmathtranslate/pdfmathtranslate) · [▶️ Demo ↗](https://pdf2zh.com/) · [📖 Docs ↗](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pdfmathtranslate/)</sub>

<a name="datatrove"></a>
### #&#8288;43 [datatrove](https://github.com/huggingface/datatrove) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: known (36) · Freshness: active (100) · Maintenance: fair (60) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.4k · Apache-2.0 · Nov 2026</sub>

**Python library for filtering and deduplicating large text datasets.**

DataTrove is a Python library for building pipelines that read, extract, filter, deduplicate, tokenize and write text data at LLM-training scale. Pipelines are lists of blocks operating on a Document (text, id, metadata) and run unchanged on a local machine, Slurm, Ray, or the experimental Hugging Face Jobs executor. Task completion markers let you relaunch a failed job and rerun only unfinished tasks.

- **+** Same pipeline runs on local multiprocessing, Slurm, or Ray without code changes
- **+** Resumable jobs: completion markers mean relaunch only reruns failed tasks
- **+** Prebuilt readers, extractors, filters, minhash and sentence dedup; FineWeb reproduction included
- **+** fsspec paths cover local disk, S3 and Hugging Face Hub datasets and buckets
- **−** Each input file goes to one task; large single files are not split
- **−** Changing task count when relaunching breaks input sharding
- **−** Hugging Face Jobs executor is experimental and may be removed
- **−** ExactSubstr dedup depends on Google's separate deduplicate-text-datasets repo

<sub>GPU optional · Needs Slurm (optional), Ray (optional), fsspec, S3 (optional) · [Repo](https://github.com/huggingface/datatrove) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/datatrove/)</sub>

<a name="new-term-radar"></a>
### #&#8288;44 [new-term-radar](https://github.com/zhuyansen/new-term-radar) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: niche (22) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.2k · MIT · Nov 2026</sub>

**Daily report of new AI model, tool and repo names, with keyword demand.**

A Python CLI that reads X, Hugging Face trending, GitHub breakout repos, directory sitemaps, new sites and payment-link signals each day to find AI names starting to surge. It then builds a keyword table per name with search volume, Trends shape, page-one difficulty and a prioritize/watch/skip decision. It also ships as Agent Skills and an MCP server.

- **+** Combines many early signals (X, HF, GitHub, sitemaps, new domains), not only Google Trends
- **+** Keyword table adds volume, markets, page-one shape and a decision per term
- **+** Hugging Face, GitHub and sitemap signals are free and need no key; per-run costs are listed
- **+** Checks each lead against DataForSEO Trends 14 days later and reports hit rate
- **−** Most signals and the keyword table need a paid AIsa key; GoAnyAPI adds more
- **−** Example config costs about $15 a month, mostly X reads
- **−** Aimed at SEO and content work, not general AI development
- **−** No Docker or compose files provided

<sub>no GPU · Needs AIsa API key, GoAnyAPI key (optional), GitHub token (optional), TrustMRR key (optional), Google Search Console token (optional) · [Repo](https://github.com/zhuyansen/new-term-radar) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/new-term-radar/)</sub>

<a name="jionlp"></a>
### #&#8288;45 [jionlp](https://github.com/dongrixinyu/jionlp) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: known (42) · Freshness: active (100) · Maintenance: fair (63) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.9k · Apache-2.0 · Nov 2026</sub>

**Python toolkit for Chinese text cleaning, extraction and parsing.**

JioNLP is a pip-installable Python library of Chinese NLP preprocessing functions. It covers regex cleaning and extraction (URLs, phone numbers, ID cards), parsing of time expressions, addresses and license plates, pinyin and traditional/simplified conversion, plus NER, classification and word-segmentation dataset helpers. Most functions are rule- and dictionary-based rather than model-based.

- **+** Wide set of Chinese-specific parsers: time, address, ID card, plate, phone region
- **+** Bundled dictionaries: idioms, xiehouyu, China and world place names, Xinhua
- **+** NER and classification dataset helpers: tag conversion, splitting, entity diffing
- **+** Installs with a single pip command
- **−** Chinese only; no support for other languages
- **−** Documentation lives in a GitHub wiki and the README is mostly a function table
- **−** No tagged releases on GitHub
- **−** Back-translation augmentation depends on third-party cloud translation APIs

<sub>Needs Cloud machine-translation APIs (BackTranslation only) · [Repo](https://github.com/dongrixinyu/jionlp) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/jionlp/)</sub>

<a name="indra"></a>
### #&#8288;46 [indra](https://github.com/datalab-to/indra) <sub>score [61](../README.md#-how-we-rank "Score 61/100. Adoption: niche (17) · Freshness: active (100) · Maintenance: healthy (86) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.0k · Apache-2.0 · Nov 2026</sub>

**CPU-only OCR model that converts PDFs and images to markdown or JSON.**

Indra OCR is a small ONNX Runtime OCR pipeline (about 76 MB of default models, no PyTorch) that converts PDFs and images into markdown, text, or JSON with line boxes, layout blocks and reading order. It covers 80+ languages through four script-specific recognizers, and for digital PDFs it reads the text layer and OCRs only what is missing. It ships a CLI, a Python API and a local web viewer.

- **+** Runs on CPU via ONNX Runtime; about 212 ms median per page on 4 vCPUs
- **+** Scores 66.7 on OmniParseBench vs 58.4 for PP-StructureV3, per the README
- **+** Outputs markdown, text, or JSON with boxes, layout labels and reading order
- **+** Handles rotated, tilted and vertical pages; uses the PDF text layer when it passes checks
- **−** Handwriting scores 25.2% and degraded scans 29.5% on OmniParseBench
- **−** Complex tables with merged cells or no ruling lines often misplace cells
- **−** Math is plain text unless --math is set; it is slower and lowers table score
- **−** Weights use modified OpenRAIL-M; commercial use above $20M funding or revenue needs a license

<sub>no GPU · Needs onnxruntime, opencv, pypdfium2, Hugging Face (model download) · Models: ONNX, indra-ocr · port 8765 · [Repo](https://github.com/datalab-to/indra) · [▶️ Demo ↗](https://www.datalab.to/playground) · [📖 Docs ↗](https://documentation.datalab.to) · [🌐 Site ↗](https://www.datalab.to) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/indra/)</sub>

<a name="ai-youtube-shorts-generator"></a>
### #&#8288;47 [ai-youtube-shorts-generator](https://github.com/anil-matcha/ai-youtube-shorts-generator) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: popular (57) · Freshness: active (100) · Maintenance: patchy (39) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.6k · MIT · Nov 2026</sub>

**CLI that cuts long YouTube videos into ranked vertical shorts.**

Python CLI and library that downloads a YouTube video or local file, transcribes it with Whisper, and has an LLM score highlight candidates for virality. The top N are cropped to 9:16 or another ratio. API mode runs everything through the MuAPI hosted service; local mode uses yt-dlp, faster-whisper, ffmpeg and OpenCV face tracking, with OpenAI or Gemini for ranking.

- **+** Local mode runs download, Whisper, and cropping on your machine; only the LLM call is remote
- **+** Each clip returns a score, hook line, and reason; --output-json dumps full results
- **+** Highlight prompt and virality criteria are editable in shorts_generator/highlights.py
- **+** Chunks videos over 30 minutes and dedupes overlapping candidates by score
- **−** Default API mode depends on a paid MuAPI key for download, transcription, and cropping
- **−** Local mode still needs an OpenAI or Gemini API key for highlight ranking
- **−** README promotes a hosted clipping API as giving better quality than this repo
- **−** No Dockerfile, web UI, or tagged release; CLI and Python library only

<sub>GPU optional · Needs MuAPI (API mode), ffmpeg (local mode), yt-dlp, faster-whisper, OpenCV, OpenAI or Gemini API key (local mode) · Models: OpenAI gpt-4o-mini, Gemini gemini-2.5-flash, faster-whisper tiny to large-v3, MuAPI gpt-5-mini · [Repo](https://github.com/anil-matcha/ai-youtube-shorts-generator) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ai-youtube-shorts-generator/)</sub>

<a name="grobid"></a>
### #&#8288;48 [grobid](https://github.com/grobidorg/grobid) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: popular (52) · Freshness: active (100) · Maintenance: patchy (48) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.2k · Apache-2.0 · Nov 2026</sub>

**Extracts structured TEI/XML from scientific PDFs, including metadata and references.**

GROBID parses scientific and technical PDFs into structured XML/TEI using a cascade of sequence-labelling models. CRF models are the default, and DeLFT deep learning models can be enabled via JEP. It extracts headers, references, citation contexts, full-text structure, funders and PDF coordinates, and exposes them through a web service, batch commands and a Java API.

- **+** Reference parsing around .87 F1 on a PubMed Central set with the deep learning model
- **+** Returns PDF bounding-box coordinates for extracted structures
- **+** Reported 10.6 PDF/s full-text on one 16-CPU, 32 GB machine with the Node.js client
- **+** Default CRF models run on commodity CPUs without a GPU
- **−** Deep learning models are off by default and need Python/JEP, ideally a GPU
- **−** Windows is not currently supported
- **−** Aimed at scholarly PDFs, not general document-to-markdown conversion
- **−** Batch command lines are single-threaded; clients are needed for scale

<sub>GPU optional · Docker · Needs OpenJDK 21 (source builds), Python 3.10-3.11 with JEP (deep learning models), DeLFT, pdfalto, biblio-glutton or CrossRef API (optional consolidation) · Models: CRF, RNN, transformers (via DeLFT) · port 8080 · [Repo](https://github.com/grobidorg/grobid) · [▶️ Demo ↗](https://grobidOrg-grobid.hf.space/) · [📖 Docs ↗](https://grobid.readthedocs.io/en/latest/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/grobid/)</sub>

<a name="docetl"></a>
### #&#8288;49 [docetl](https://github.com/ucbepic/docetl) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: known (45) · Freshness: active (100) · Maintenance: patchy (50) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · MIT · Nov 2026</sub>

**Declarative LLM map-reduce pipelines over documents, with automatic optimization.**

DocETL runs LLM operators (map, reduce, filter, resolve, split, gather, extract) over large collections of structured or unstructured data, with each step written as a natural-language prompt. Pipelines are defined in Python or YAML and produce tables. An optimizer (MOAR) rewrites prompts, swaps models and decomposes operations to trade accuracy against cost. DocWrangler is a visual playground for developing prompts.

- **+** Python API and YAML config both supported, run with `docetl run pipeline.yaml`
- **+** Optimizer rewrites prompts, swaps models and replaces subtasks with code
- **+** Configurable rate limits and per-run cost reporting via pipeline.total_cost
- **+** Backed by peer-reviewed papers (VLDB 2025, UIST 2025) from UC Berkeley
- **−** Examples assume hosted providers such as OpenAI; local model setup is not shown
- **−** Optimization runs add extra LLM calls, which adds cost up front
- **−** Output is tables; no serving layer or long-running agent runtime
- **−** Prompt-authoring help points to Claude Code skill or hosted prompts

<sub>no GPU · Docker + Compose · Needs LLM provider API key (OpenAI or other) · Models: OpenAI, other LLM providers via API key · [Repo](https://github.com/ucbepic/docetl) · [▶️ Demo ↗](https://docetl.org/playground) · [📖 Docs ↗](https://ucbepic.github.io/docetl) · [🌐 Site ↗](https://docetl.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/docetl/)</sub>

<a name="deepdoctection"></a>
### #&#8288;50 [deepdoctection](https://github.com/deepdoctection/deepdoctection) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: known (34) · Freshness: active (100) · Maintenance: fair (65) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.3k · Apache-2.0 · Oct 2026</sub>

**Python library for PDF layout analysis, table recognition and OCR pipelines.**

deepdoctection is a Python library that builds pipelines for scanned and PDF documents. It combines layout and table detection (Detectron2, Transformers), OCR (Tesseract, DocTr, AWS Textract) and document or token classification with LayoutLM, LiLT and BERT-style models. It also supports fine-tuning and evaluating whole pipelines. Version 1.0 is PyTorch-only.

- **+** Layout analysis, table recognition, OCR and classification in one configurable pipeline
- **+** Several OCR backends: Tesseract, DocTr and AWS Textract
- **+** Reads native PDF text with pdfplumber instead of running OCR
- **+** Includes fine-tuning and pipeline evaluation, plus a Hugging Face Space demo and notebooks
- **−** Detectron2 is not on PyPI and needs a separate install for the full setup
- **−** PyTorch must be installed separately; v1.0 dropped other deep learning backends
- **−** Docker container exposes no endpoint, so there is no built-in HTTP service
- **−** Library only, with no bundled UI; used from Python or notebooks

<sub>GPU optional · Docker + Compose · Needs Python >= 3.10, PyTorch >= 2.6, Detectron2, Tesseract, python-doctr, AWS Textract · Models: Detectron2, Hugging Face Transformers, LayoutLM, LiLT, BERT-style · [Repo](https://github.com/deepdoctection/deepdoctection) · [▶️ Demo ↗](https://huggingface.co/spaces/deepdoctection/deepdoctection) · [📖 Docs ↗](https://deepdoctection.readthedocs.io/en/latest/install/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepdoctection/)</sub>

<a name="chubbyskills"></a>
### #&#8288;51 [chubbyskills](https://github.com/chubbyguan/chubbyskills) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (5) · Freshness: active (100) · Maintenance: healthy (95) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.4k · MIT · Oct 2026</sub>

**Agent skills and CLI that save videos, podcasts and articles as searchable Markdown.**

Chubby Skills is a set of 14 Agent Skills plus a Python CLI (`chubby`) that ingests video, podcast, article and local Markdown/TXT/PDF sources into a local Markdown vault. It builds a keyword index, optional semantic search and a 6-tool MCP server, and exports source-cited briefs with line numbers and file SHA-256. The core path uses only the Python standard library; platform scraping and transcription need extra packages.

- **+** Core import, search and brief export use only the Python standard library
- **+** Briefs include verbatim excerpts, line numbers, source links and SHA-256 for fact-checking
- **+** Local transcription via SenseVoice-Small; cloud DashScope and Groq backends are optional
- **+** Output is plain Markdown with frontmatter, usable in Obsidian or any editor
- **−** Platform scraping is fragile; X and Xiaohongshu are marked manual fallback, no anti-bot handling
- **−** Requires Python 3.11+ for subscribe; macOS system Python 3.9 fails there
- **−** PDF import reads the text layer only, with no OCR
- **−** Cloud transcription is not yet validated against real services; docs are mainly in Chinese

<sub>GPU optional · Needs Python 3.11+, yt-dlp, ffmpeg, funasr, beautifulsoup4, pymupdf, DashScope API (optional), Groq API (optional), DeepSeek API (optional), OpenAI API (optional) · Models: SenseVoice-Small, Qwen3-ASR-0.6B, qwen3-asr-flash, whisper-large-v3-turbo, DeepSeek · [Repo](https://github.com/chubbyguan/chubbyskills) · [📖 Docs ↗](https://github.com/chubbyguan/chubbyskills/blob/main/docs/introduction.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chubbyskills/)</sub>

<a name="claude-real-video"></a>
### #&#8288;52 [claude-real-video](https://github.com/huangchihhungleo/claude-real-video) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (24) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · MIT · Nov 2026</sub>

**Extracts scene-change keyframes and a timestamped transcript from videos for LLMs.**

claude-real-video (crv) takes a URL or local file, keeps frames at scene changes with sliding-window dedup, transcribes audio with Whisper, and writes frames, frames.json, transcript and MANIFEST.txt that any LLM can read. It runs locally through a CLI, a local web page, a Python API, an agent skill and an MCP server, and indexes past analyses in a local SQLite file for search. The free edition omits on-screen text recognition and shot analysis, which are sold in paid add-ons.

- **+** Scene-change selection with dedup: a 58 s clip gives 26 frames instead of 58 at 1 fps
- **+** Processing is local; the source video is not uploaded anywhere
- **+** Several Whisper backends: openai-whisper, faster-whisper with VAD, and mlx-whisper on Apple Silicon
- **+** Ships as CLI, Python API, agent skill and MCP server with five tools
- **−** On-screen text recognition and shot or emotion analysis are paid add-ons, not in this edition
- **−** Requires a separately installed ffmpeg; no speech-to-text without the whisper extra
- **−** Frames are pasted into an LLM afterwards; vision understanding depends on that model
- **−** Default 640 px frames lose small text unless --frame-width is raised

<sub>GPU optional · Needs ffmpeg, ffprobe, yt-dlp, whisper · Models: openai-whisper, faster-whisper, mlx-whisper, Silero VAD, speaker diarization (45 MB) · [Repo](https://github.com/huangchihhungleo/claude-real-video) · [▶️ Demo ↗](https://youtu.be/QRuh1oByT3M) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/claude-real-video/)</sub>

<a name="curator"></a>
### #&#8288;53 [curator](https://github.com/bespokelabsai/curator) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: niche (12) · Freshness: active (100) · Maintenance: healthy (85) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · Apache-2.0 · Nov 2026</sub>

**Python library for bulk LLM inference and synthetic data generation.**

Curator is a Python library for building synthetic data pipelines. You subclass curator.LLM, define prompt and parse methods, and run it over a list or HuggingFace Dataset with Pydantic structured outputs. It handles parallelism, retries and response caching, and routes to OpenAI-compatible APIs, LiteLLM providers, Ollama or vLLM, with batch mode for several providers. Tinker and Fireworks trainers cover LoRA fine-tuning on the curated data.

- **+** Batch mode via batch=True for OpenAI, Anthropic, Gemini, kluster.ai and Mistral
- **+** One LLM class over OpenAI-compatible APIs, LiteLLM, Ollama and vLLM backends
- **+** Caching and retries on by default; rerunning the same prompt returns from cache
- **+** Pydantic structured outputs and chainable LLM blocks for multi-step generation
- **−** Anonymized telemetry is on by default; opt out with TELEMETRY_ENABLED=False
- **−** Hosted providers need API keys, so most runs send data to third-party APIs
- **−** Fine-tuning goes through external services (Tinker, Fireworks), not local training
- **−** Library only: no UI or server, pipelines are written in Python

<sub>GPU optional · Needs Provider API keys (OpenAI, Anthropic, etc.) or local Ollama/vLLM, LiteLLM, HuggingFace datasets, Tinker or Fireworks AI for fine-tuning (optional) · Models: OpenAI, Anthropic, Gemini, Mistral, kluster.ai · [Repo](https://github.com/bespokelabsai/curator) · [📖 Docs ↗](https://docs.bespokelabs.ai/bespoke-curator/getting-started) · [🌐 Site ↗](https://bespokelabs.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/curator/)</sub>

<a name="oxen"></a>
### #&#8288;54 [oxen](https://github.com/oxen-ai/oxen) <sub>score [58](../README.md#-how-we-rank "Score 58/100. Adoption: niche (2) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · Apache-2.0 · Nov 2026</sub>

**Git-style version control for large datasets and model weights.**

Oxen is a Rust version control system with git-like commands (init, add, commit, push) built for repositories with millions of files and terabytes of data. It is used through a CLI, a Python package (oxenai), an HTTP API or the embeddable liboxen crate. Repositories can be hosted on Oxen.ai or on a self-hosted oxen-server.

- **+** Git-like command set, so existing git users need little retraining
- **+** Handles any blob type; indexes csv, parquet and jsonl for querying
- **+** Self-hostable oxen-server with Prometheus metrics and OpenTelemetry tracing
- **+** CLI, Python package, HTTP API and Rust crate share one core
- **−** oxen-server does not run on Windows; Linux, macOS or Docker only
- **−** Video thumbnails need a build with the ffmpeg feature and FFmpeg libraries
- **−** Some visualization features are tied to the hosted Oxen.ai service
- **−** Self-hosted upgrades may require running manual migration steps

<sub>no GPU · Docker + Compose · Needs FFmpeg libraries (optional, thumbnails), cmake (build only) · [Repo](https://github.com/oxen-ai/oxen) · [📖 Docs ↗](https://docs.oxen.ai) · [🌐 Site ↗](https://oxen.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/oxen/)</sub>

<a name="easyocr"></a>
### #&#8288;55 [easyocr](https://github.com/jaidedai/easyocr) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: widely used (87) · Freshness: recent (70) · Maintenance: weak (29) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Nov 2026</sub>

**Python OCR library for 80+ languages using CRAFT detection and CRNN recognition.**

EasyOCR is a Python package that detects and reads text in images with a CRAFT detector and a CRNN recognizer (ResNet/VGG, LSTM, CTC), built on PyTorch. It returns bounding boxes, text and confidence per region, accepts file paths, URLs, numpy arrays or bytes, and also has a CLI. Model weights download per language on first use, and it runs on GPU or CPU.

- **+** Supports 80+ languages and major scripts, including Latin, Chinese, Arabic, Devanagari and Cyrillic
- **+** Two-line Python API: Reader(langs) then readtext() returns boxes, text and confidence
- **+** Runs on CPU with gpu=False; also ships a command-line tool and a Dockerfile
- **+** Documents training of custom recognition models and the CRAFT detector
- **−** Handwritten text support is still listed as upcoming
- **−** Not every language combination works in one Reader; only English pairs with all
- **−** Last release 1.7.2 in September 2024, despite later commits
- **−** Optional DBNet detector compiles C++/CUDA ops on first use and needs Ninja

<sub>GPU optional · Docker · Needs PyTorch, torchvision, Ninja (optional, for DBNet) · Models: CRAFT detector, CRNN recognizer, DBNet detector (optional) · [Repo](https://github.com/jaidedai/easyocr) · [▶️ Demo ↗](https://huggingface.co/spaces/tomofi/EasyOCR) · [📖 Docs ↗](https://www.jaided.ai/easyocr/documentation) · [🌐 Site ↗](https://www.jaided.ai/easyocr) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/easyocr/)</sub>

<a name="subtitle-translator"></a>
### #&#8288;56 [subtitle-translator](https://github.com/rockbenben/subtitle-translator) <sub>score [56](../README.md#-how-we-rank "Score 56/100. Adoption: niche (2) · Freshness: active (100) · Maintenance: healthy (83) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · MIT · Nov 2026</sub>

**Browser-based batch subtitle translator for SRT, ASS, VTT and LRC files.**

Parses .srt, .ass, .vtt and .lrc files locally, strips timecodes and headers, and sends only dialogue text to one of 8 machine-translation APIs or 27 LLM providers and gateways. It handles whole seasons in batch, multiple target languages per pass, and bilingual output including two-style ASS. A `yarn cli` command runs the same engine headlessly, and it can be self-hosted with Node.js 24 or newer.

- **+** Timecodes and cue numbers never reach the model, so timing cannot be rewritten
- **+** Free GTX and Edge engines work with no key or setup
- **+** Local models work through any OpenAI-compatible URL, e.g. Ollama at localhost:11434
- **+** CLI shares engine and cache with the web app, and runs resume after interruption
- **−** Complex inline ASS effect tags are simplified during translation
- **−** Context mode with models under 70B parameters may produce misaligned output
- **−** CORS-blocked providers go through a relay, built-in or self-deployed Worker
- **−** Free GTX and Edge engines are rate-limited and rated lower for stability

<sub>no GPU · Docker · Needs Node.js >= 24, Yarn · Models: DeepL, Google Translate, Azure Translate, DeepLX, Qwen-MT · port 3000 · [Repo](https://github.com/rockbenben/subtitle-translator) · [▶️ Demo ↗](https://tools.newzone.top/en/subtitle-translator) · [📖 Docs ↗](https://docs.newzone.top/en/guide/translation/subtitle-translator/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/subtitle-translator/)</sub>

<a name="chonkie"></a>
### #&#8288;57 [chonkie](https://github.com/feyninc/chonkie) <sub>score [55](../README.md#-how-we-rank "Score 55/100. Adoption: known (49) · Freshness: active (99) · Maintenance: weak (29) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.9k · MIT · Aug 2026</sub>

**Python library that chunks text and code for RAG ingestion pipelines.**

Chonkie is a Python library that splits text, code and markdown tables into chunks using token, sentence, recursive, semantic, late, neural and LLM-based strategies. Chunks can be refined with overlap and embeddings, then written to JSON, HuggingFace datasets or vector stores such as Chroma, Qdrant, pgvector, Pinecone and Milvus. It also ships a REST API server (`chonkie serve`) that stores reusable pipelines in SQLite.

- **+** Small base install: 505KB wheel, 49MB installed, per the project's own benchmarks
- **+** Many chunkers: token, sentence, recursive, semantic, late, code, neural, LLM-driven, table
- **+** Ten vector DB handshakes and 16 embedding providers, each as an optional extra
- **+** Pipeline API with async support, plus a self-hosted REST server with Docker compose
- **−** Ingestion only; no retrieval, query or answer generation layer
- **−** Semantic, neural and slumber chunkers need extra installs and embedding or LLM models
- **−** Speed and size comparisons come from the project's own benchmarks
- **−** README advises against the `all` install in production, so extras are picked by hand

<sub>GPU optional · Docker + Compose · Needs Python, SQLite (API server pipelines), Optional: embedding/LLM providers and vector DBs · Models: sentence-transformers, Model2Vec, OpenAI, Azure OpenAI, Cohere · port 8000 · [Repo](https://github.com/feyninc/chonkie) · [📖 Docs ↗](https://docs.chonkie.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chonkie/)</sub>

<a name="quant-mind"></a>
### #&#8288;58 [quant-mind](https://github.com/llmquant/quant-mind) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: known (33) · Freshness: active (95) · Maintenance: weak (24) · Agent-ready: ready (85) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.1k · MIT · Aug 2026</sub>

**Python library turning financial papers and news into typed, cited knowledge records.**

QuantMind refines financial sources such as arXiv papers and PR Newswire news into typed records that carry their own text, an as_of timestamp and a source reference. It ships PaperFlow, collect_news and batch_run, plus rag/, library/ and mind/ modules for retrieval over the output. The repo also includes AGENTS.md and CLAUDE.md contracts, skills, hooks and a verify script so a coding agent can build new pipelines inside the checkout.

- **+** Every artifact stores text, as_of timestamp and citation, so it persists and time-queries standalone
- **+** Deterministic preprocess with no model in the loop gives replayable provenance
- **+** batch_run fans any flow across inputs with concurrency, error skipping and progress callbacks
- **+** scripts/verify.sh runs lint, types, import boundaries and tests; CI runs the same script
- **−** Only arXiv paper and PR Newswire news flows ship today; SEC filings flow is roadmap
- **−** Evaluation benchmarks are still in design; no results are published
- **−** Needs an external LLM; supported providers are not listed in the README
- **−** Agent-first workflow centers on Claude Code and Codex; no separate docs site

<sub>no GPU · Needs uv, LLM API (model set in config) · Models: gpt-5.6-luna (README example) · [Repo](https://github.com/llmquant/quant-mind) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/quant-mind/)</sub>

<a name="paper2poster"></a>
### #&#8288;59 [paper2poster](https://github.com/paper2poster/paper2poster) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: known (43) · Freshness: active (100) · Maintenance: patchy (32) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.1k · MIT · Nov 2026</sub>

**Turns a scientific paper PDF into an editable PowerPoint poster.**

PosterAgent takes a paper.pdf and produces an editable poster.pptx through a parser, a binary-tree layout planner, and a painter-commentor loop that uses VLM feedback to fix overflow and alignment. It runs with API models such as GPT-4o or with local Qwen-2.5 models served by vLLM. The repo also includes the Paper2Poster benchmark and evaluation scripts (PaperQuiz, VLM-as-Judge, statistical metrics).

- **+** Outputs editable .pptx rather than a flat image
- **+** Mixes LLM and VLM backends: GPT-4o, or Qwen-2.5 via vLLM
- **+** Ships evaluation suite: PaperQuiz, VLM-as-Judge, statistical metrics
- **+** Auto-adds conference logos; YAML style config; parallel section generation
- **−** Needs LibreOffice and poppler installed alongside Python requirements
- **−** Local vLLM models require editing the port in get_agent_config()
- **−** CLI scripts only; the README documents no packaged API or web UI
- **−** No tagged releases

<sub>GPU optional · Docker · Needs LibreOffice, poppler, OpenAI API key (for GPT-4o), vLLM (for local models), Google Custom Search API (optional) · Models: GPT-4o, Qwen-2.5-7B-Instruct (vLLM), Qwen VL (vLLM) · [Repo](https://github.com/paper2poster/paper2poster) · [▶️ Demo ↗](https://huggingface.co/spaces/camel-ai/Paper2Poster) · [🌐 Site ↗](https://paper2poster.github.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/paper2poster/)</sub>

<a name="humanize-text"></a>
### #&#8288;60 [humanize-text](https://github.com/lynote-ai/humanize-text) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: known (37) · Freshness: active (100) · Maintenance: patchy (39) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.5k · MIT · Oct 2026</sub>

**Rewrites AI-generated text through LLM passes and a translation chain, with step traces.**

Python CLI that rewrites AI-drafted text in four steps: two high-temperature LLM rewrites (Chinese, then Japanese), then Google Translate to Finnish and Niutrans back to English. Every intermediate step can be printed or dumped as JSON. Advanced and focus tiers add multi-round rewriting and a detection-guided loop. The repo also ships an n8n workflow, a FastAPI app, and a training-data pipeline for SFT and KTO.

- **+** Every step is readable code, and --json returns the full step-by-step trace
- **+** Works with DeepSeek, OpenRouter, Atlas Cloud, OrcaRouter, or any OpenAI-compatible endpoint
- **+** Runs as Python CLI, n8n workflow import, or a Docker REST endpoint
- **+** Includes a documented SFT and KTO data pipeline with demo records and tests
- **−** Needs both an LLM key and a Niutrans key, plus Google Translate access
- **−** Translation hops can change technical terms and citations, per the README
- **−** No detection guarantee; showcase verdicts come from one detector at one time
- **−** Own trained model and weights are not included; they are only in the hosted Lynote.ai

<sub>no GPU · Docker + Compose · Needs LLM API (DeepSeek default), Niutrans API, Google Translate, n8n (optional) · Models: DeepSeek, OpenRouter, Atlas Cloud, OrcaRouter, LiteLLM · [Repo](https://github.com/lynote-ai/humanize-text) · [▶️ Demo ↗](https://lynote.ai/ai-humanizer) · [📖 Docs ↗](https://github.com/lynote-ai/humanize-text/blob/main/docs/installation.md) · [🌐 Site ↗](https://lynote.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/humanize-text/)</sub>

<a name="oxr"></a>
### #&#8288;61 [oxr](https://github.com/somarkai/oxr) <sub>score [51](../README.md#-how-we-rank "Score 51/100. Adoption: known (38) · Freshness: active (100) · Maintenance: patchy (30) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.7k · custom license · Nov 2026</sub>

**1.3B document parsing model that turns PDFs and images into Markdown or JSON.**

OXR is a 1.3B-parameter model from SoMark that parses PDFs and document images into Markdown or JSON with layout coordinates, covering 13 element types such as formulas, tables, chemical structures and code blocks. Layout analysis runs as a separate, replaceable model, while OXR handles recognition and reading order. It serves a SoMark-compatible parsing API and a demo page on port 8000, using vLLM for the model.

- **+** Layout model is swappable while OXR keeps recognition and reading order
- **+** Outputs Markdown or JSON with bounding boxes for 13 element types
- **+** API works with somark-py and somark-js CLIs by changing the base URL
- **+** Local demo at /demo plus a free hosted API for trying it
- **−** Needs Linux and an NVIDIA BF16 GPU; 24GB VRAM minimum, 48GB recommended
- **−** Custom license based on Apache 2.0 with extra terms
- **−** Official vLLM lacks OXR support; an out-of-tree plugin is required
- **−** Benchmark rankings are self-reported; technical report not yet published

<sub>GPU required · Docker · Needs NVIDIA driver (CUDA 13.0 compatible), vLLM 0.25.1, PyTorch 2.11.0, Python 3.12, Docker · Models: OXR-1.0 (BF16, 1.3B), D-FINE layout analysis model · port 8000 · [Repo](https://github.com/somarkai/oxr) · [▶️ Demo ↗](https://free-oxr.somark.ai) · [📖 Docs ↗](https://docs.somark.ai/api-reference) · [🌐 Site ↗](https://somark.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/oxr/)</sub>

<a name="glm-ocr"></a>
### #&#8288;62 [glm-ocr](https://github.com/zai-org/glm-ocr) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: popular (62) · Freshness: active (96) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.6k · Apache-2.0 · Oct 2026</sub>

**0.9B OCR model and SDK that parses documents into Markdown and JSON.**

GLM-OCR is a 0.9B-parameter document OCR model (CogViT encoder, GLM-0.5B decoder) paired with a Python SDK. The SDK runs layout analysis with PP-DocLayout-V3, then recognizes regions in parallel and returns Markdown and JSON. It can call the Zhipu hosted API or a self-hosted vLLM, SGLang, Ollama or MLX server, and ships a CLI and a Flask service.

- **+** Small 0.9B model; README lists deployment on vLLM, SGLang, Ollama and Apple Silicon via mlx-vlm
- **+** Reports 94.62 on OmniDocBench V1.5, ranked #1 overall by the authors
- **+** CLI, Python API and Flask endpoint (port 5002) with swappable pipeline modules
- **+** Cloud mode needs no GPU; layout model can be placed on CPU or a chosen GPU
- **−** Self-hosted pipeline needs a separate vLLM or SGLang server plus transformers>=5.3.0
- **−** Hosted mode depends on a Zhipu API key from open.bigmodel.cn
- **−** Code is Apache-2.0 but model is MIT, and PP-DocLayoutV3 adds a third license to follow

<sub>GPU optional · Needs vLLM or SGLang or Ollama (self-hosted), PP-DocLayout-V3, Zhipu MaaS API (cloud mode) · Models: zai-org/GLM-OCR (BF16) · port 5002 · [Repo](https://github.com/zai-org/glm-ocr) · [📖 Docs ↗](https://docs.z.ai/guides/vlm/glm-ocr) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/glm-ocr/)</sub>

<a name="mnbvc"></a>
### #&#8288;63 [mnbvc](https://github.com/esbatmop/mnbvc) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: known (45) · Freshness: active (100) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.3k · MIT · Oct 2026</sub>

**Chinese text corpus of 63 TB plus the crawlers and cleaning scripts behind it.**

MNBVC is a community-collected corpus of Chinese internet text (news, books, forums, code, Q&A, papers), with a stated target of 253 TB and 63,441 GB collected so far. The repo is mainly a landing page: it links download routes (Verysync P2P, Baidu Netdisk, cleaned subsets on ModelScope and Hugging Face) and many separate repos for encoding detection, deduplication, PDF parsing and per-source cleaning. The data is only roughly processed (html to txt, csv to json).

- **+** Very large Chinese corpus: 63,441 GB collected, target 253 TB
- **+** Covers many text types: forums, novels, papers, code, Q&A, parallel text
- **+** Companion repos for crawling GitHub, Bitbucket and arXiv, and for PDF parsing
- **+** Cleaned subsets are published on Hugging Face and ModelScope
- **−** Archive data is only roughly processed, with mixed txt, json, jsonl and parquet formats
- **−** No index or classification of archive contents; copyright review was not done
- **−** Full download goes through Verysync P2P or Baidu Netdisk; part1 needs 10 TB+ of disk
- **−** README is a link hub; tools live in many separate repos of varying maintenance

<sub>Needs Verysync (P2P sync), Baidu Netdisk, Hugging Face, ModelScope · [Repo](https://github.com/esbatmop/mnbvc) · [📖 Docs ↗](https://wiki.mnbvc.org) · [🌐 Site ↗](http://mnbvc.253874.net/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/mnbvc/)</sub>

<a name="tesseract-js"></a>
### #&#8288;64 [tesseract.js](https://github.com/naptha/tesseract.js) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: widely used (91) · Freshness: recent (60) · Maintenance: weak (5) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 39k · Apache-2.0 · May 2026</sub>

**JavaScript OCR library that runs Tesseract in the browser and Node.js.**

Tesseract.js wraps a WebAssembly port of the Tesseract OCR engine and extracts text from images in the browser or on Node.js. It exposes a worker API (createWorker, recognize, terminate) plus schedulers for parallel processing, and supports a long list of languages. It does not read PDFs or change Tesseract's recognition model.

- **+** Runs client-side in browsers via webpack, ESM or CDN script tag, so images can stay local
- **+** Also runs on Node.js (v7 needs v16 or newer) with the same worker API
- **+** Schedulers allow parallel recognition across multiple workers
- **+** Supports almost any language through Tesseract language data, chosen in createWorker
- **−** No PDF support; the README points to Scribe.js for that
- **−** Does not modify the Tesseract model, so accuracy is that of upstream Tesseract
- **−** Since v6, output formats other than text (e.g. hocr) are off by default
- **−** Breaking API changes across v4, v5 and v6 complicate upgrades

<sub>no GPU · Docker · Needs Node.js 16+ (v7, server use), tesseract.js-core (WebAssembly port of Tesseract) · Models: Tesseract traineddata language files · [Repo](https://github.com/naptha/tesseract.js) · [▶️ Demo ↗](http://tesseract.projectnaptha.com/) · [📖 Docs ↗](https://github.com/naptha/tesseract.js/blob/master/docs/api.md) · [🌐 Site ↗](https://tesseract.projectnaptha.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tesseract-js/)</sub>

<a name="jina-reader"></a>
### #&#8288;65 [Jina Reader](https://github.com/jina-ai/reader) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: popular (73) · Freshness: recent (64) · Maintenance: weak (6) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · May 2026</sub>

**Converts any URL or search query into LLM-friendly markdown.**

Open-source branch of the service behind r.jina.ai and s.jina.ai: fetches a page with headless Chrome or curl-impersonate, parses PDFs and Office files, and returns markdown, text, HTML, screenshots or JSON controlled by request headers (engine, timeout, token limits). The ghcr.io image bundles Chrome, LibreOffice and CJK fonts, serves HTTP/1.1 on 8081 and h2c on 8080, and runs stateless or with S3-compatible caching.

- **+** Prebuilt image with Chrome, LibreOffice and CJK fonts; stateless by default
- **+** Fine-grained headers: x-respond-timing, x-max-tokens, x-token-budget, x-target-selector
- **+** Optional VLM captions for images without alt text
- **+** Semantic markdown chunking by heading or block level
- **−** Hosted proxy pool, rate limiting and MongoDB storage layer are not in the OSS branch
- **−** Needs non-redistributable assets (MaxMind GeoLite2, Source Han Sans) fetched at build
- **−** Last commit May 2026; the SaaS resync was April 2026
- **−** Default h2c port 8080 needs --http2-prior-knowledge from curl; use 8081 otherwise

<sub>no GPU · Docker + Compose · Needs Headless Chrome and LibreOffice (bundled in image), S3-compatible bucket (optional cache), VLM endpoint for image captions (optional) · port 8081 · [Repo](https://github.com/jina-ai/reader) · [▶️ Demo ↗](https://jina.ai/reader#demo) · [📖 Docs ↗](https://r.jina.ai/docs) · [🌐 Site ↗](https://jina.ai/reader) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/jina-reader/)</sub>

<a name="tavily-python"></a>
### #&#8288;66 [tavily-python](https://github.com/tavily-ai/tavily-python) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: niche (5) · Freshness: active (100) · Maintenance: fair (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.4k · MIT · Oct 2026</sub>

**Python client for the Tavily search, extract, crawl, map and research API.**

Official Python SDK for the hosted Tavily API. It wraps search, content extraction (up to 20 URLs per call), crawl, map, research reports and a feedback endpoint, with sync and async clients. A keyless mode allows search and extract without an API key, rate-limited; the other endpoints need a key.

- **+** Sync TavilyClient and async AsyncTavilyClient cover search, extract, crawl, map and research
- **+** Keyless mode lets you try search and extract without signing up
- **+** Accepts a custom requests.Session or httpx.AsyncClient for routing through an API gateway
- **+** get_search_context returns a context string ready to feed into a RAG prompt
- **−** Only a client: every call goes to the hosted Tavily API, nothing runs locally
- **−** Crawl is invite-only according to the README
- **−** Free tier is limited to 1,000 credits per month; paid beyond that
- **−** Keyless mode is rate-limited and excludes crawl, map and research

<sub>no GPU · Needs Tavily API (hosted), Tavily API key (except keyless search/extract) · [Repo](https://github.com/tavily-ai/tavily-python) · [📖 Docs ↗](https://docs.tavily.com/sdk/python/reference) · [🌐 Site ↗](https://tavily.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/tavily-python/)</sub>

<a name="keybert"></a>
### #&#8288;67 [keybert](https://github.com/maartengr/keybert) <sub>score [46](../README.md#-how-we-rank "Score 46/100. Adoption: known (44) · Freshness: recent (70) · Maintenance: patchy (40) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.2k · MIT · Nov 2026</sub>

**Python library that extracts keywords and keyphrases using sentence embeddings.**

KeyBERT embeds a document and its candidate n-grams, then ranks phrases by cosine similarity to the document. It supports Sentence-Transformers, Flair, spaCy, Gensim and USE embeddings, with Max Sum and MMR options for diversifying results. A separate KeyLLM class sends text to an LLM such as OpenAI for keyword extraction.

- **+** Uses pretrained embeddings, so no training step; extraction takes a few lines of Python
- **+** Max Sum Distance and MMR options reduce near-duplicate keywords
- **+** Several embedding backends: Sentence-Transformers, Flair, spaCy, Gensim, USE
- **+** Light install without PyTorch is possible via Model2Vec
- **−** Library only: no UI, server or API; you write Python to use it
- **−** Max Sum Distance has super-exponential time cost with large top_n
- **−** KeyLLM example needs the openai package and an API key
- **−** Last release is 2025-02-07, older than the latest commit

<sub>GPU optional · Needs Python 3.10+, scikit-learn, sentence-transformers, openai (for KeyLLM) · Models: Sentence-Transformers, Flair, spaCy, Gensim, Universal Sentence Encoder · [Repo](https://github.com/maartengr/keybert) · [📖 Docs ↗](https://maartengr.github.io/KeyBERT/guides/embeddings.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/keybert/)</sub>

<a name="anakin"></a>
### #&#8288;68 [anakin](https://github.com/anakin-inc/anakin) <sub>score [44](../README.md#-how-we-rank "Score 44/100. Adoption: known (40) · Freshness: active (92) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.8k · AGPL-3.0 · Aug 2026</sub>

**Self-hosted scraping API that returns LLM-ready markdown or JSON.**

AnakinScraper OSS is a Go server exposing sync, async and batch REST endpoints that fetch a URL and return HTML, cleaned HTML and markdown. Each job runs a handler chain: plain HTTP fetch, then a Camoufox anti-detect Firefox service, then an optional external API such as anakin.io. Per-domain configs, failure-pattern detection, Thompson Sampling proxy selection and optional Gemini JSON extraction are included, plus a React dashboard.

- **+** Runs as a single Go binary with in-memory jobs; PostgreSQL is optional
- **+** Handler chain falls back from HTTP to Camoufox browser to external API automatically
- **+** Per-domain configs with failure and required patterns trigger retries on the next handler
- **+** Includes React dashboard, CLI support and an OpenClaw skill wrapper
- **−** AGPL-3.0 license requires open-sourcing modifications offered as a hosted service
- **−** JavaScript-heavy sites need the separate Python Camoufox browser service
- **−** Structured JSON extraction depends on a Google Gemini API key
- **−** Anonymous telemetry is on by default and must be disabled with TELEMETRY=off

<sub>no GPU · Compose · Needs PostgreSQL (optional), Camoufox browser service (optional), Gemini API (optional), anakin.io API (optional), Go 1.25+ · Models: Google Gemini (JSON extraction) · port 8080 · [Repo](https://github.com/anakin-inc/anakin) · [🌐 Site ↗](https://anakin.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/anakin/)</sub>

<a name="agentql"></a>
### #&#8288;69 [agentql](https://github.com/tinyfish-io/agentql) <sub>score [43](../README.md#-how-we-rank "Score 43/100. Adoption: niche (7) · Freshness: active (100) · Maintenance: patchy (37) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.5k · MIT · Nov 2026</sub>

**Natural-language queries to extract data and automate live web pages.**

AgentQL is a query language with Python and JavaScript SDKs that locates elements and extracts structured data on live web pages from natural-language queries. It integrates with Playwright and also offers a REST API, a Chrome debugger extension, a web playground and an MCP server. Queries are meant to work across similar sites and survive UI changes.

- **+** Python and JavaScript SDKs on Playwright, with many example scripts for both
- **+** Same query can run across different sites with similar content
- **+** Output structure follows the shape of the query
- **+** Browser debugger extension and web playground for testing queries
- **−** README does not describe self-hosting the query resolution; REST API suggests a hosted service
- **−** No tagged releases on the repository
- **−** SDK use requires a Playwright-controlled browser
- **−** Self-healing and cross-site claims come with no benchmarks in the README

<sub>Needs Playwright, AgentQL REST API · [Repo](https://github.com/tinyfish-io/agentql) · [▶️ Demo ↗](https://playground.agentql.com/) · [📖 Docs ↗](https://docs.agentql.com) · [🌐 Site ↗](https://agentql.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/agentql/)</sub>

<a name="olmocr"></a>
### #&#8288;70 [olmocr](https://github.com/allenai/olmocr) <sub>score [42](../README.md#-how-we-rank "Score 42/100. Adoption: widely used (82) · Freshness: recent (54) · Maintenance: weak (5) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 20k · Apache-2.0 · Mar 2026</sub>

**PDF and image to Markdown converter built on a 7B vision-language model.**

olmOCR converts PDFs, PNGs and JPEGs into Markdown using a 7B vision-language model served through vLLM. It handles equations, tables, handwriting and multi-column layouts, and strips headers and footers. It runs on a local NVIDIA GPU, against a remote OpenAI-compatible server, or across many nodes coordinated through an S3 workspace.

- **+** Scores 82.4 on olmOCR-Bench (v0.4.0), near the top of the README table
- **+** Accepts any OpenAI-compatible server via --server, so no local GPU is required
- **+** Multi-node batch mode with an S3 work queue for millions of PDFs
- **+** Ships benchmark suite and trainer code for reproducing or fine-tuning the model
- **−** Local inference needs an NVIDIA GPU with at least 12 GB VRAM and 30 GB disk
- **−** README advises a clean conda environment because dependencies are hard to install
- **−** System setup needs poppler-utils and extra fonts; instructions cover only Ubuntu/Debian
- **−** Docker image with the model is about 30 GB

<sub>GPU required · Docker · Needs vLLM, poppler-utils, NVIDIA GPU (12 GB+ VRAM), AWS S3 (optional, multi-node) · Models: olmOCR-2-7B-1025-FP8, olmOCR-7B-0825-FP8, olmOCR-7B-0725-FP8 · [Repo](https://github.com/allenai/olmocr) · [▶️ Demo ↗](https://olmocr.allenai.org/) · [🌐 Site ↗](https://olmocr.allenai.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/olmocr/)</sub>

<a name="zingg"></a>
### #&#8288;71 [zingg](https://github.com/zinggai/zingg) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: niche (4) · Freshness: active (100) · Maintenance: patchy (32) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.3k · AGPL-3.0 · Oct 2026</sub>

**Spark-based entity resolution and record matching trained with active learning.**

Zingg matches and deduplicates records that refer to the same entity (customer, patient, supplier, product) across one or many data sources. It learns a blocking model and a similarity classifier from a small set of labels collected in an interactive CLI, and runs on Spark. Connectors cover Snowflake, Cassandra, S3, Azure, Elastic, relational databases and common file formats.

- **+** Active-learning labeler builds models from small training samples
- **+** Learned blocking cuts comparisons to roughly 0.05-1% of possible pairs
- **+** Reads and writes Snowflake, Cassandra, S3, Azure, Elastic, RDBMS, Parquet, Avro, JSON, CSV
- **+** Handles English plus Chinese, Thai, Japanese and Hindi out of the box
- **−** Runs on Spark, so a Spark environment is needed at scale
- **−** AGPL-3.0 license; other licensing requires contacting the vendor
- **−** Labeling happens in a CLI; no web UI is mentioned
- **−** Pretrained models ship only for the Febrl demo dataset

<sub>no GPU · Docker · Needs Apache Spark · [Repo](https://github.com/zinggai/zingg) · [▶️ Demo ↗](https://www.youtube.com/watch?v=zOabyZxN9b0) · [📖 Docs ↗](https://docs.zingg.ai/) · [🌐 Site ↗](https://www.zingg.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/zingg/)</sub>

<a name="llm-scraper"></a>
### #&#8288;72 [llm-scraper](https://github.com/mishushakov/llm-scraper) <sub>score [39](../README.md#-how-we-rank "Score 39/100. Adoption: popular (58) · Freshness: recent (73) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.0k · MIT · Jun 2026</sub>

**TypeScript library that extracts structured data from web pages with LLMs.**

LLM Scraper loads a page through Playwright and asks an LLM to fill a Zod or JSON Schema, returning typed objects. It runs on the Vercel AI SDK, so OpenAI, Anthropic, Google, Groq and Ollama models plug in. It can also stream partial objects or generate a reusable Playwright script for a schema.

- **+** Schemas in Zod or JSON Schema give type-safe output in TypeScript
- **+** Six input formats: html, raw_html, markdown, text, image, custom
- **+** Code generation produces a reusable Playwright script, avoiding an LLM call per page
- **+** Works with hosted providers and local models via Ollama
- **−** Library only: no CLI, server or UI
- **−** Needs Playwright and a separately installed AI SDK provider package
- **−** README gives no cost, token-limit or accuracy guidance for large pages
- **−** No tagged release published

<sub>no GPU · Needs Playwright, Zod, Vercel AI SDK provider package, LLM provider API or Ollama · Models: OpenAI GPT, Anthropic Claude, Google Gemini, Groq Llama, Ollama · [Repo](https://github.com/mishushakov/llm-scraper) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/llm-scraper/)</sub>

<a name="video-subtitle-extractor"></a>
### #&#8288;73 [video-subtitle-extractor](https://github.com/yaofanguk/video-subtitle-extractor) <sub>score [38](../README.md#-how-we-rank "Score 38/100. Adoption: popular (67) · Freshness: recent (59) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.8k · Apache-2.0 · Apr 2026</sub>

**Desktop tool that OCRs hard-coded video subtitles into SRT files.**

Extracts burned-in subtitles from video by sampling key frames, locating text regions, running local PaddlePaddle-based OCR, and removing duplicate lines to write an srt or txt file. It has a GUI (gui.py) and a CLI (backend/main.py), supports batch extraction, and covers 87 languages. Fast, auto and accurate modes trade speed against missed lines and typos; CUDA, DirectML and CPU backends are supported.

- **+** OCR runs locally; no online OCR API keys or services needed
- **+** Supports 87 languages including Chinese, Japanese, Korean, Arabic and Russian
- **+** Batch extraction, plus typoMap.json to replace or strip specific recognized text
- **+** Runs on CPU, NVIDIA CUDA, or DirectML; prebuilt release archives available
- **−** Accurate mode is described as very slow; fast mode may drop some subtitles
- **−** Paths to videos and program must avoid Chinese characters and spaces
- **−** ONNX path for macOS/ROCm is untested and the README says not to file issues
- **−** README is Chinese-first and CUDA setup targets 11.8; RTX 50 series needs DirectML

<sub>GPU optional · Needs PaddlePaddle 3.3.1, VideoSubFinder, CUDA 11.8 and cuDNN 8.6.0 (NVIDIA GPU), ONNX Runtime DirectML (AMD/Intel GPU) · Models: PaddleOCR-based mini and large OCR models · [Repo](https://github.com/yaofanguk/video-subtitle-extractor) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/video-subtitle-extractor/)</sub>

<a name="watercrawl"></a>
### #&#8288;74 [watercrawl](https://github.com/watercrawl/watercrawl) <sub>score [36](../README.md#-how-we-rank "Score 36/100. Adoption: niche (23) · Freshness: active (96) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.3k · custom license · Aug 2026</sub>

**Web crawling and search API that extracts page data for LLM pipelines.**

WaterCrawl is a Django, Scrapy and Celery application that crawls websites and runs web searches through a REST API with OpenAPI docs. Crawl depth, speed and content targeting are configurable, and progress streams over Server-Sent Events. It ships client SDKs and plugins for Dify and n8n, so scraped content can feed AI workflows.

- **+** Client SDKs for Python, Node.js, Go and PHP
- **+** Dify plugin and n8n node for wiring into AI workflows
- **+** Real-time crawl and search progress via Server-Sent Events
- **+** Search supports multiple depths plus language and country targeting
- **−** WaterCrawl License is MIT with extra restrictions, not a standard OSI license
- **−** Needs MinIO and other services; non-localhost deploys require editing MinIO URLs
- **−** Rust client and Flowise integration are not released; Langflow PR unmerged
- **−** Output formats and JavaScript rendering support are not described

<sub>no GPU · Docker + Compose · Needs MinIO, Celery, database · port 80 · [Repo](https://github.com/watercrawl/watercrawl) · [📖 Docs ↗](https://docs.watercrawl.dev/intro) · [🌐 Site ↗](https://watercrawl.dev) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/watercrawl/)</sub>

<a name="json2yolo"></a>
### #&#8288;75 [json2yolo](https://github.com/ultralytics/json2yolo) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: niche (3) · Freshness: recent (70) · Maintenance: weak (20) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.2k · AGPL-3.0 · Oct 2026</sub>

**Scripts that convert COCO and LabelMe JSON annotations to YOLO labels.**

JSON2YOLO is a set of Python scripts that convert COCO detection, segmentation and keypoint annotations, plus LabelMe JSON, into the Ultralytics YOLO dataset layout (images/, labels/, YAML of class names). The README states the standalone scripts are no longer actively updated and points to convert_coco() in the ultralytics package instead.

- **+** Handles COCO boxes, segments and keypoints via --use-segments and --use-keypoints flags
- **+** Also reads LabelMe polygon, rectangle, circle, linestrip and mask annotations
- **+** Runs on Linux, macOS and Windows with Python 3.8+ and a requirements.txt
- **+** Maintained equivalent exists as convert_coco() in the ultralytics package
- **−** Standalone scripts are no longer actively updated, per the README
- **−** --save-dir is deleted and recreated on every run
- **−** Labelbox mask-only objects are skipped with a warning
- **−** AGPL-3.0 license; commercial use needs a separate enterprise license

<sub>no GPU · Needs Python 3.8+, ultralytics (for convert_coco) · Models: COCO JSON, LabelMe JSON, Labelbox JSON, YOLO format · [Repo](https://github.com/ultralytics/json2yolo) · [📖 Docs ↗](https://docs.ultralytics.com/reference/data/converter) · [🌐 Site ↗](https://www.ultralytics.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/json2yolo/)</sub>

<a name="extractthinker"></a>
### #&#8288;76 [extractthinker](https://github.com/enoch3712/extractthinker) <sub>score [34](../README.md#-how-we-rank "Score 34/100. Adoption: niche (9) · Freshness: recent (70) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · Apache-2.0 · Sep 2026</sub>

**Python library that extracts Pydantic-typed data from documents using LLMs.**

ExtractThinker is a Python library that loads documents (PDF, images, tables, spreadsheets, text), then classifies, splits and extracts fields into validated Pydantic contracts using a configurable LLM. Loaders include PyPdf, PyMuPDF, Camelot, Tabula and Adobe; local models work through Ollama. Recent additions on main, such as SQLite page retrieval, parallel field extraction and an MCP service, are not in the latest PyPI release.

- **+** Pydantic contracts give typed, validated output with field constraints and post-validation
- **+** Classification and splitting handle mixed document bundles
- **+** Pluggable loaders and LLM providers, including local models via Ollama
- **+** Completion strategies for long inputs and incomplete responses
- **−** 2026 features (MCP service, SQLite retrieval) need install from a checkout, not PyPI
- **−** Scanned documents need OCR or a vision-capable model
- **−** System MIME detection requires libmagic installed on the host
- **−** Schema validity does not ensure accuracy; hosted providers may incur charges

<sub>GPU optional · Docker + Compose · Needs LLM provider API or Ollama, libmagic, pypdf (for PDFs) · Models: Ollama local models, Hosted LLM providers via EXTRACT_THINKER_MODEL · [Repo](https://github.com/enoch3712/extractthinker) · [📖 Docs ↗](https://enoch3712.github.io/ExtractThinker/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/extractthinker/)</sub>

<a name="doccano"></a>
### #&#8288;77 [doccano](https://github.com/doccano/doccano) <sub>score [32](../README.md#-how-we-rank "Score 32/100. Adoption: popular (69) · Freshness: slowing (32) · Maintenance: weak (7) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 11k · MIT · Jan 2026</sub>

**Web-based text annotation tool for labeling NLP datasets.**

doccano is a web application for annotating text for classification, sequence labeling (such as named entity recognition) and sequence-to-sequence tasks like summarization. Teams create a project, upload data, and label it collaboratively, with a REST API for automation. It runs from pip with SQLite by default, or with PostgreSQL, Docker or Docker Compose.

- **+** Covers text classification, sequence labeling and seq2seq annotation in one tool
- **+** Installs with pip and uses SQLite by default, so no database setup to start
- **+** Collaborative annotation with multiple users per project and a RESTful API
- **+** Deploy options include pip, Docker, Docker Compose, AWS CloudFormation and Heroku
- **−** Text only; the README lists no image, audio or video annotation
- **−** README mentions no built-in model-assisted pre-labeling
- **−** Compose setup needs RabbitMQ and PostgreSQL; pip setup needs a separate task queue process
- **−** Admin password is passed in plain environment variables or CLI arguments in the examples

<sub>no GPU · Docker + Compose · Needs SQLite (default), PostgreSQL (optional), RabbitMQ (Docker Compose) · port 8000 · [Repo](https://github.com/doccano/doccano) · [📖 Docs ↗](https://doccano.github.io/doccano/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/doccano/)</sub>

<a name="deepke"></a>
### #&#8288;78 [deepke](https://github.com/zjunlp/deepke) <sub>score [32](../README.md#-how-we-rank "Score 32/100. Adoption: known (47) · Freshness: recent (58) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.5k · MIT · Jul 2026</sub>

**Toolkit for extracting entities, relations and attributes to build knowledge graphs.**

DeepKE is a PyTorch toolkit that trains and runs models for named entity recognition, relation extraction, attribute extraction and event extraction. It covers standard, few-shot, document-level and multimodal settings, with Hydra-configured run.py and predict.py scripts per task. A separate DeepKE-LLM environment adds LLM-based extraction, and an MCP tool service is also provided.

- **+** Covers NER, relation, attribute and event extraction in one framework
- **+** Supports few-shot, document-level and multimodal settings, with Chinese and English data
- **+** Includes several published models (W2NER, LightNER, KnowPrompt, PRGC, PURE, ASP)
- **+** Provides an online demo, docs, Colab notebook and a hosted MCP service
- **−** Pinned to Python 3.8, torch<=1.11 and transformers 4.26.0, which conflicts with newer stacks
- **−** Last release 2023-09-21; pip package is marked not recommended
- **−** Each task needs its own dataset download and config editing before training
- **−** Separate environment needed for DeepKE-LLM; dataset links use a bare IP over HTTP

<sub>Docker · Needs PyTorch, transformers, hydra-core, wandb (optional) · Models: BERT-style encoders, W2NER, LightNER, KnowPrompt, PRGC · [Repo](https://github.com/zjunlp/deepke) · [▶️ Demo ↗](http://deepke.zjukg.cn/) · [📖 Docs ↗](https://zjunlp.github.io/DeepKE/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepke/)</sub>

<a name="cleanlab"></a>
### #&#8288;79 [cleanlab](https://github.com/cleanlab/cleanlab) <sub>score [31](../README.md#-how-we-rank "Score 31/100. Adoption: popular (71) · Freshness: slowing (31) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Jan 2026</sub>

**Python library that finds label errors and outliers in ML datasets.**

cleanlab uses predictions and embeddings from your existing model to detect label errors, outliers, duplicates and other issues in text, image, audio and tabular datasets. It is based on confident learning and also offers CleanLearning, a wrapper that trains a classifier on the cleaned data, plus tools for multi-annotator consensus and active learning.

- **+** Model-agnostic: works with outputs from PyTorch, TensorFlow, JAX, HuggingFace, XGBoost, scikit-learn
- **+** Dedicated support for multi-label, token classification, regression, segmentation and object detection
- **+** Datalab API reports issues in a few lines: find_issues() then report()
- **+** Algorithms are backed by published peer-reviewed papers
- **−** Needs pred_probs or embeddings from a trained model; it does not train a base model for you
- **−** Aimed at supervised ML datasets; not a general document or web data cleaner
- **−** Other ML tasks beyond the listed ones require adapting the methods
- **−** Library only; no hosted UI or web app in the open-source package

<sub>no GPU · Needs Python 3.10+ · Models: PyTorch, TensorFlow, Keras, JAX, HuggingFace · [Repo](https://github.com/cleanlab/cleanlab) · [📖 Docs ↗](https://docs.cleanlab.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/cleanlab/)</sub>

<a name="video-analyzer"></a>
### #&#8288;80 [video-analyzer](https://github.com/byjlw/video-analyzer) <sub>score [30](../README.md#-how-we-rank "Score 30/100. Adoption: niche (9) · Freshness: recent (61) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.6k · Apache-2.0 · Apr 2026</sub>

**CLI that describes videos using key frames, a vision LLM and Whisper.**

Extracts key frames from a video with OpenCV, transcribes audio with Whisper, and sends each frame to a vision model, by default Llama 3.2 Vision through Ollama. Each frame analysis includes context from earlier frames, and a final pass combines them with the transcript into a written description. It can also use any OpenAI-compatible API such as OpenRouter or OpenAI, and writes results to a JSON file.

- **+** Runs fully locally with Ollama, or against any OpenAI-compatible endpoint
- **+** Each frame analysis is given context from previous frames
- **+** Cascading config: CLI arguments, config/config.json, then defaults
- **+** Optional prompt tuning with DSPy MIPROv2 via video-analyzer-tune
- **−** Local mode needs a 12GB VRAM GPU or Apple Silicon with 32GB
- **−** Command-line tool only, no web UI or API server
- **−** Requires separate FFmpeg and Ollama installs
- **−** No Docker image provided

<sub>RAM ≥ 16 GB · GPU optional · Needs Python 3.11+, FFmpeg, Ollama, OpenCV, Whisper · Models: Llama 3.2 Vision 11B (Ollama), OpenAI-compatible APIs (OpenRouter, OpenAI), Whisper · [Repo](https://github.com/byjlw/video-analyzer) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/video-analyzer/)</sub>

<a name="kubric"></a>
### #&#8288;81 [kubric](https://github.com/google-research/kubric) <sub>score [28](../README.md#-how-we-rank "Score 28/100. Adoption: niche (29) · Freshness: recent (64) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.9k · Apache-2.0 · May 2026</sub>

**Synthetic multi-object video generator with segmentation, depth and optical flow labels.**

Kubric generates semi-realistic synthetic videos of multiple objects, using pybullet for physics and Blender 2.93 for rendering. Each scene comes with ground-truth annotations such as instance segmentation masks, depth maps and optical flow. It also hosts dataset challenges from the CVPR'22 paper (MOVi, point tracking, NeRF variants), stored in a public Google Cloud bucket.

- **+** Emits instance masks, depth maps and optical flow alongside rendered video
- **+** Physics simulation via pybullet produces object interactions automatically
- **+** Prebuilt kubruntu Docker image runs the hello-world example in one command
- **+** Ships ten dataset challenges, including MOVi and point tracking, in a public bucket
- **−** Pinned to Blender 2.93, so inspecting .blend files needs that exact version
- **−** Rendering is Blender-based; other backends are only a possible future option
- **−** No tagged releases; usage is by cloning the repository
- **−** Aimed at vision research datasets, not general-purpose image or video generation

<sub>Docker · Needs Blender 2.93, pybullet, Docker · [Repo](https://github.com/google-research/kubric) · [📖 Docs ↗](https://kubric.readthedocs.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/kubric/)</sub>

<a name="fastdup"></a>
### #&#8288;82 [fastdup](https://github.com/visual-layer/fastdup) <sub>score [26](../README.md#-how-we-rank "Score 26/100. Adoption: niche (16) · Freshness: recent (69) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · custom license · Aug 2026</sub>

**Python library that finds duplicates, outliers and mislabels in image datasets.**

fastdup is a pip-installable Python package with a C++ engine that analyzes image and video datasets for duplicates and near-duplicates, outliers, mislabels, broken images and blurry or dark images. It can delete duplicates from disk in one call (default similarity above 0.96, with a dry-run option) and renders static galleries of the findings. It also accepts custom embeddings, such as TIMM or ONNX models like DINOv2.

- **+** README claims 400M images processed on a single CPU machine
- **+** Runs locally; data stays on your own host or cloud
- **+** Accepts custom embeddings from TIMM or ONNX models such as DINOv2
- **+** remove_duplicates has a dry_run preview and an adjustable distance threshold
- **−** License badge says CC BY-NC-ND 4.0, which bars commercial use and derivatives
- **−** Last release was 2024-06-14, while commits continue
- **−** Output is static galleries; hosted Visual Layer Cloud is the upsell for more
- **−** Windows is supported only through WSL2

<sub>GPU optional · Docker · Models: TIMM, ONNX, DINOv2 · [Repo](https://github.com/visual-layer/fastdup) · [📖 Docs ↗](https://visual-layer.readme.io/) · [🌐 Site ↗](https://www.visual-layer.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fastdup/)</sub>

<a name="scattertext"></a>
### #&#8288;83 [scattertext](https://github.com/jasonkessler/scattertext) <sub>score [24](../README.md#-how-we-rank "Score 24/100. Adoption: niche (25) · Freshness: recent (56) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.4k · Apache-2.0 · Jul 2026</sub>

**Python library that plots distinguishing terms between text corpora as interactive HTML.**

Scattertext is a Python library that scores which words and phrases are characteristic of one document category versus another, then writes a standalone interactive HTML scatter plot with non-overlapping point labels. It includes scoring methods such as Scaled F-Score, Cohen's d, Cliff's Delta and Bi-Normal Separation, plus dispersion metrics. A `scattertext` command-line tool handles CSV input without writing Python.

- **+** Outputs a self-contained HTML file with zoom, click-through term stats and non-overlapping labels
- **+** Many term scoring options: Scaled F-Score, Cohen's d, Cliff's Delta, BNS, dispersion measures
- **+** Runs without spaCy using a regex-based whitespace tokenizer
- **+** CLI analyzes a CSV with text and category columns, no Python needed
- **−** Classical corpus statistics; no LLM integration, so not an LLM-era tool
- **−** Last tagged release is 2017-03-13 although commits continue
- **−** Full feature set needs optional packages: spacy, gensim, empath, umap-learn, jieba, flashtext
- **−** README recommends Chrome or Safari for viewing output; docs are a work in progress

<sub>no GPU · Needs Python 3.11+, spacy (optional), gensim (optional), empath (optional), umap-learn (optional), jieba (optional), flashtext (optional), astropy (optional) · [Repo](https://github.com/jasonkessler/scattertext) · [▶️ Demo ↗](https://jasonkessler.github.io/demo_compact.html) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/scattertext/)</sub>

<a name="fg-data-synthetic"></a>
### #&#8288;84 [fg-data-synthetic](https://github.com/data-centric-ai-community/fg-data-synthetic) <sub>score [23](../README.md#-how-we-rank "Score 23/100. Adoption: niche (11) · Freshness: recent (65) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.7k · MIT · Apr 2026</sub>

**Python library for synthetic tabular and time-series data using GANs and Gaussian Mixture.**

fg-data-synthetic is a Python package, the renamed successor to ydata-synthetic, that trains generative models on tabular or sequential data and samples synthetic records. It includes GAN variants (CGAN, WGAN, WGAN-GP, DRAGAN, Cramer, CTGAN), a Gaussian Mixture model that needs no GPU, and TimeGAN and DoppelGANger for time series. A Streamlit app offers a low-code flow to train a synthesizer and profile the output.

- **+** Covers both tabular (CTGAN, WGAN-GP, Gaussian Mixture) and time-series (TimeGAN, DoppelGANger) synthesis
- **+** Gaussian Mixture model lets you start without a GPU
- **+** Optional Streamlit UI for training and profiling without writing code
- **+** Colab notebooks for adult census, stock and FCC MBA datasets
- **−** Deep learning models are built on TensorFlow 2, not PyTorch
- **−** README lists Python 3.9 and 3.10 only
- **−** Streamlit app does not run inside Jupyter notebooks
- **−** Streamlit app covers tabular data only; time-series models are code-only

<sub>GPU optional · Needs TensorFlow 2, Streamlit (optional extra) · Models: CGAN, WGAN, WGAN-GP, DRAGAN, Cramer GAN · [Repo](https://github.com/data-centric-ai-community/fg-data-synthetic) · [🌐 Site ↗](https://ydata.ai/products/synthetic_data) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/fg-data-synthetic/)</sub>

<a name="diffgram"></a>
### #&#8288;85 [diffgram](https://github.com/diffgram/diffgram) <sub>score [21](../README.md#-how-we-rank "Score 21/100. Adoption: niche (16) · Freshness: recent (53) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · custom license · Jun 2026</sub>

**Self-hosted data labeling platform and datastore for AI training data.**

Diffgram is a self-installed platform for storing AI data (schemas, blobs, predictions) and annotating it with human supervision. It supports labeling image, video, 3D, text, audio, geospatial and multi-modal data, plus conversational/LLM data in preview. It adds a data workflow layer and a UI catalog for browsing the datastore, under a custom commercial open source license (DLv2).

- **+** Annotation covers image, video, 3D, text, audio and geospatial in one tool
- **+** Self-installed, so data stays under your control
- **+** README cites 706 tests (E2E, unit) and commercial use since 2018
- **+** Supports pre-labels and ML program integrations for automation
- **−** Custom license (DLv2) rather than a standard OSS license; commercial terms apply
- **−** Last release was 2024-10-14, well behind recent commits
- **−** Document, HTML and DICOM annotation are roadmap only
- **−** Conversational/LLM annotation is still marked preview

<sub>Compose · [Repo](https://github.com/diffgram/diffgram) · [📖 Docs ↗](https://diffgram.readme.io/docs) · [🌐 Site ↗](https://diffgram.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/diffgram/)</sub>

<a name="blenderproc"></a>
### #&#8288;86 [blenderproc](https://github.com/dlr-rm/blenderproc) <sub>score [20](../README.md#-how-we-rank "Score 20/100. Adoption: known (41) · Freshness: quiet (11) · Maintenance: weak (17) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.8k · GPL-3.0 · Jan 2026</sub>

**Python pipeline for rendering synthetic training images with Blender.**

BlenderProc is a Python API and CLI that runs scripts inside Blender's Python environment to build or load 3D scenes, sample object, light and camera poses, and render images. It outputs RGB, stereo, depth, normal and segmentation data, written to .hdf5 containers or COCO and BOP annotations. It is aimed at generating labelled synthetic data for computer vision training.

- **+** Loads .obj, .ply, .blend, .fbx, BOP, ShapeNet, Haven and 3D-FRONT scenes
- **+** Writes .hdf5, COCO and BOP annotations directly from the render step
- **+** Physics simulation for object placement and sampling of poses, lights and materials
- **+** Installs with pip; debug subcommand opens the script in the Blender GUI
- **−** Scripts must run via the blenderproc CLI, not the normal Python interpreter
- **−** Breakpoint debugging needs remote debugpy or PyCharm setup inside Blender's Python
- **−** GPL-3.0 license may constrain use in proprietary code
- **−** Last tagged release is 2024-10-22, older than recent commits

<sub>Needs Blender · Models: obj, ply, blend, fbx, BOP · [Repo](https://github.com/dlr-rm/blenderproc) · [📖 Docs ↗](https://dlr-rm.github.io/BlenderProc) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/blenderproc/)</sub>

<a name="lingua-py"></a>
### #&#8288;87 [lingua-py](https://github.com/pemistahl/lingua-py) <sub>score [19](../README.md#-how-we-rank "Score 19/100. Adoption: niche (14) · Freshness: slowing (49) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.8k · Apache-2.0 · Mar 2026</sub>

**Offline language detector for Python, accurate on short text and single words.**

Python bindings to a Rust implementation that identifies which of 75 languages a text is written in. It combines a rule-based alphabet filter with a Naive Bayes model over character n-grams of size 1 to 5, with no neural networks and no external API. It returns a single language, a confidence value per language, or None below a set minimum relative distance.

- **+** Uses n-grams of size 1 to 5, aimed at short phrases and single words
- **+** Models are stored as FSTs, so runtime memory is a few dozen megabytes
- **+** Fully offline once installed; thread-safe, with models shared across detector instances
- **+** Can restrict candidate languages and set a minimum relative distance to reject ambiguous input
- **−** Supports only 75 languages, by design favoring quality over quantity
- **−** Requires Python 3.12 or newer for the 2.x line
- **−** Compiled extension, so unsupported platforms need the pure-Python 1.x branch
- **−** Single-word accuracy is lower; the German example scores 74.2% on words

<sub>no GPU · [Repo](https://github.com/pemistahl/lingua-py) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lingua-py/)</sub>

<a name="deepseek-ocr-app"></a>
### #&#8288;88 [deepseek_ocr_app](https://github.com/rdumasia303/deepseek_ocr_app) <sub>score [18](../README.md#-how-we-rank "Score 18/100. Adoption: niche (15) · Freshness: slowing (45) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 1.9k · MIT · Mar 2026</sub>

**Web UI and API for running DeepSeek-OCR on images and PDFs.**

A React frontend and FastAPI backend that wrap the DeepSeek-OCR model from Hugging Face. It does image OCR in four modes (plain, describe, find with bounding boxes, freeform prompt) and multi-page PDF processing, exporting to Markdown, HTML, DOCX or JSON. It is started with docker compose and needs an NVIDIA GPU.

- **+** PDF input up to 100MB with Markdown, HTML, DOCX and JSON export
- **+** Find mode draws bounding boxes, rescaled from the model's 0-999 coordinates
- **+** REST endpoints /api/ocr and /api/process-pdf, with Swagger docs at /docs
- **+** Ports, upload limit, model name and crop sizes set through .env
- **−** Requires an NVIDIA GPU with CUDA and the NVIDIA Container Toolkit
- **−** Only 4 of the original 12 modes remain; tables, layout and PII modes are disabled
- **−** First run downloads about 5-10GB of weights; roughly 20GB disk needed
- **−** No authentication mentioned, and no tagged releases

<sub>RAM ≥ 16 GB · GPU required · Compose · Needs Docker Compose, NVIDIA Container Toolkit, NVIDIA driver · Models: deepseek-ai/DeepSeek-OCR · port 3000 · [Repo](https://github.com/rdumasia303/deepseek_ocr_app) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deepseek-ocr-app/)</sub>

<a name="libpostal"></a>
### #&#8288;89 [libpostal](https://github.com/openvenues/libpostal) <sub>score [16](../README.md#-how-we-rank "Score 16/100. Adoption: popular (50) · Freshness: quiet (3) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.9k · MIT · Dec 2025</sub>

**C library for parsing and normalizing street addresses worldwide.**

libpostal is a C library that parses free-form street addresses into components and normalizes them for matching and full-text indexing. The parser is a Conditional Random Field model trained on over 1 billion addresses from OpenStreetMap and OpenAddresses. It is not a geocoder, but works as a preprocessing step for one. Bindings exist for Python, Ruby, Go, Java, PHP and NodeJS.

- **+** Trained on over 1 billion addresses covering every inhabited country
- **+** Pure C core with officially supported bindings for six languages
- **+** Runs fully on CPU, offline, with pkg-config support
- **+** Optional Senzing model reports 4.3% better parsing on its test set
- **−** Model data needs a few GB of disk (about 1.8GB default, 2.2GB Senzing)
- **−** Last tagged release is from 2018, though commits continue
- **−** Not a geocoder; it only parses and normalizes address strings
- **−** Source build needs autotools; Windows requires MSys2/MinGW; M1 needs --disable-sse2

<sub>no GPU · Needs autoconf, automake, libtool, pkg-config, curl · Models: Conditional Random Field address parser, Senzing alternative model · [Repo](https://github.com/openvenues/libpostal) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/libpostal/)</sub>

<a name="gosseract"></a>
### #&#8288;90 [gosseract](https://github.com/otiai10/gosseract) <sub>score [14](../README.md#-how-we-rank "Score 14/100. Adoption: known (33) · Freshness: quiet (13) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.1k · MIT · Jan 2026</sub>

**Go bindings for the Tesseract OCR C++ library.**

gosseract is a Go package that wraps the Tesseract and Leptonica C++ libraries through cgo, so Go programs can extract text from images with a small client API (SetImage, Text). It needs Tesseract development headers and language data on the build host. Install steps are given for macOS, Debian/Ubuntu and Windows (vcpkg and MinGW-w64).

- **+** Minimal API: NewClient, SetImage, Text return recognized text in a few lines
- **+** CI runs on Go, Docker, BSD and Windows runtimes
- **+** MIT licensed, with a companion OCR server example (otiai10/ocrserver)
- **+** Prebuilt Docker image available as otiai10/gosseract
- **−** Requires cgo plus libtesseract-dev and libleptonica-dev at build time
- **−** Windows setup is manual: vcpkg, MinGW import libraries, several env variables
- **−** Last tagged release is 2023-09-06, though commits continue into 2026
- **−** Clear Linux and Arch Linux test runtimes were removed in January 2026

<sub>no GPU · Docker · Needs Tesseract, Leptonica, cgo, tessdata language files · Models: Tesseract traineddata · [Repo](https://github.com/otiai10/gosseract) · [📖 Docs ↗](https://pkg.go.dev/github.com/otiai10/gosseract/v2) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/gosseract/)</sub>

<a name="scispacy"></a>
### #&#8288;91 [scispacy](https://github.com/allenai/scispacy) <sub>score [9](../README.md#-how-we-rank "Score 9/100. Adoption: niche (18) · Freshness: quiet (12) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 2.0k · Apache-2.0 · Dec 2025</sub>

**spaCy pipelines, NER models and entity linking for biomedical text.**

scispaCy provides spaCy models trained on biomedical data: a tokenizer with extra rules, POS tagger, dependency parser and NER models (CRAFT, JNLPBA, BC5CDR, BIONLP13CG). It also ships pipeline components for abbreviation detection, Hearst-pattern hyponym extraction and entity linking to UMLS, MeSH, RxNorm, GO and HPO. Models install as pip packages and load with spacy.load.

- **+** Entity linker covers UMLS (~3M concepts), MeSH, RxNorm, GO and HPO
- **+** Model sizes from sm to lg, plus a scibert transformer pipeline
- **+** Adds to standard spaCy pipelines via nlp.add_pipe, no separate service
- **+** Linker can load other ontologies such as HGNC through pyobo
- **−** English biomedical text only; no other languages listed
- **−** Models must be re-downloaded on each scispaCy upgrade to match versions
- **−** First UMLS linker use downloads about 1GB and loads a large JSON file
- **−** Linking is char-3gram string overlap, not context-aware disambiguation

<sub>GPU optional · Docker · Needs spaCy, Python 3.6+, pyobo (optional, for custom ontologies) · Models: spaCy pipelines, en_core_sci_sm/md/lg, en_core_sci_scibert, en_ner_craft_md, en_ner_jnlpba_md · [Repo](https://github.com/allenai/scispacy) · [▶️ Demo ↗](https://scispacy.apps.allenai.org) · [🌐 Site ↗](https://allenai.github.io/scispacy/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/scispacy/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
