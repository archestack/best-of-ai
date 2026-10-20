# 🧮 Vector databases reviews · Best of Open-Source AI

Vector stores and hybrid search engines for embeddings. Back to the [leaderboard](../README.md#-vector-databases).

<sub>🌐 Also on the web: [Vector databases on archestack.com](https://archestack.com/best-of-ai/vector-db/), each project on its own page.</sub>

<a name="milvus"></a>
### 🥇 [Milvus](https://github.com/milvus-io/milvus) <sub>score [82](../README.md#-how-we-rank "Score 82/100. Adoption: widely used (86) · Freshness: active (100) · Maintenance: healthy (84) · Easy to run: easy (67) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 46k · Apache-2.0 · Oct 2026</sub>

**Distributed vector database with dense, sparse and hybrid search at scale.**

Milvus is a distributed vector database (Go and C++, LF AI & Data Foundation) that separates compute and storage on Kubernetes, with a Standalone Docker mode and pip-installable Milvus Lite. It offers HNSW, IVF, FLAT, SCANN and DiskANN indexes, GPU CAGRA, sparse BM25 and learned-sparse vectors for hybrid search, metadata filtering, multi-tenancy, hot/cold storage, auth, TLS and RBAC.

- **+** Index types HNSW, IVF, FLAT, SCANN, DiskANN plus GPU CAGRA
- **+** Dense, sparse (BM25, SPLADE, BGE-M3) and hybrid search in one collection
- **+** Multi-tenancy at database, collection, partition or partition-key level
- **+** Mandatory auth, TLS and RBAC; Milvus Lite via pip for local dev
- **−** Distributed mode is Kubernetes-native with several microservices to operate
- **−** No port, RAM or Docker command in the README; install lives in docs
- **−** Zilliz is the major contributor and promotes its managed cloud
- **−** Source build needs Go 1.21+, CMake, GCC 11+ and Python 3.8 to 3.11

<sub>GPU optional · Compose · Compose runs Milvus, MinIO · Models: any embedding model or service; pymilvus[model] wraps embedding and reranking models · [Repo](https://github.com/milvus-io/milvus) · [▶️ Demo ↗](https://milvus.io/milvus-demos) · [📖 Docs ↗](https://milvus.io/docs) · [🌐 Site ↗](https://milvus.io/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/milvus/)</sub>

<a name="meilisearch"></a>
### 🥈 [Meilisearch](https://github.com/meilisearch/meilisearch) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: widely used (93) · Freshness: active (100) · Maintenance: healthy (80) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 60k · custom license · Oct 2026</sub>

**Rust search engine API with full-text, vector and hybrid search.**

Meilisearch is a Rust search engine with a REST API that combines full-text search (typo tolerance, facets, geosearch) with vector and hybrid search, returning results as you type. It adds API keys with fine-grained permissions, tenant tokens for multi-tenancy, conversational search and MCP and LangChain integrations. The Community Edition is MIT; sharding and S3 snapshots require the Enterprise Edition.

- **+** Search-as-you-type under 50 ms with typo tolerance and faceting
- **+** Hybrid semantic plus full-text ranking in one engine
- **+** API keys with fine-grained permissions and tenant tokens for multi-tenancy
- **+** REST API with official SDKs; MCP and LangChain integrations
- **−** Sharding, S3 snapshots and search-rule previews are Enterprise Edition (BSL or commercial)
- **−** Anonymized telemetry is on by default and must be disabled
- **−** No port, RAM or install details in the README; docs only
- **−** Vector search is documented under experimental features

<sub>no GPU · Docker · [Repo](https://github.com/meilisearch/meilisearch) · [▶️ Demo ↗](https://where2watch.meilisearch.com/) · [📖 Docs ↗](https://www.meilisearch.com/docs) · [🌐 Site ↗](https://www.meilisearch.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/meilisearch/)</sub>

<a name="qdrant"></a>
### 🥉 [Qdrant](https://github.com/qdrant/qdrant) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (72) · Freshness: active (100) · Maintenance: healthy (81) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 35k · Apache-2.0 · Oct 2026</sub>

**Rust vector database with payload filtering, REST and gRPC.**

Qdrant is a Rust vector database exposing REST (OpenAPI 3.0) and gRPC on port 6333 for storing points (vectors plus JSON payload) and searching with dense, sparse and multivector (ColBERT) embeddings, rich payload filters and hybrid fusion (RRF, DBSF). It adds quantization, on-disk storage, sharding and replication, multitenancy, GPU-accelerated indexing and a web UI. Qdrant Edge runs the same engine embedded in-process.

- **+** Dense, sparse and multivector (ColBERT) search with RRF and DBSF fusion
- **+** Quantization cuts RAM up to 97 percent; on-disk storage and io_uring
- **+** REST with OpenAPI 3.0 spec plus gRPC; six official clients
- **+** Sharding and replication with zero-downtime collection resize
- **−** Default docker run has no auth and binds all interfaces
- **−** GPU acceleration covers indexing only; search runs on CPU
- **−** Qdrant Edge embedded mode is Python and Rust only
- **−** Sharding and tenant isolation require upfront design

<sub>GPU optional · Docker · Models: any embedding model; dense, sparse and late-interaction (ColBERT) vectors · port 6333 · [Repo](https://github.com/qdrant/qdrant) · [▶️ Demo ↗](https://qdrant.to/semantic-search-demo) · [📖 Docs ↗](https://qdrant.tech/documentation/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/qdrant/)</sub>

<a name="faiss"></a>
### #&#8288;4 [faiss](https://github.com/facebookresearch/faiss) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: popular (80) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: some setup (33) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 41k · MIT · Oct 2026</sub>

**C++ library for similarity search and clustering of dense vectors.**

Faiss is a C++ library with Python/numpy wrappers for nearest-neighbor search over dense vectors using L2 distance, dot product or cosine. It offers exact search, HNSW and NSG graph indexes, and compressed indexes that scale to billions of vectors in memory. Some indexes also run on GPU via CUDA or AMD ROCm, with optional NVIDIA cuVS backends.

- **+** Many index types trading off speed, accuracy, memory per vector and training time
- **+** Compressed and binary indexes handle sets that do not fit in RAM uncompressed
- **+** GPU indexes (CUDA, ROCm) replace CPU ones, single or multi-GPU
- **+** Only hard dependency is a BLAS implementation; MIT licensed
- **−** Library only: no server, REST API, auth or built-in persistence service
- **−** Vectors are identified by integers; metadata filtering must be built separately
- **−** Choosing and tuning an index type requires understanding the trade-offs
- **−** Builds with cmake; prebuilt packages are listed for Anaconda only

<sub>GPU optional · Needs BLAS, CUDA or ROCm (optional), NVIDIA cuVS (optional) · [Repo](https://github.com/facebookresearch/faiss) · [📖 Docs ↗](https://github.com/facebookresearch/faiss/wiki) · [🌐 Site ↗](https://faiss.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/faiss/)</sub>

<a name="chroma"></a>
### #&#8288;5 [Chroma](https://github.com/chroma-core/chroma) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: patchy (36) · Easy to run: easy (50) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Oct 2026</sub>

**Embedding database with a four-function API for Python and JavaScript.**

Chroma is an embedding database with a four-function API (create collection, add, query, get) that tokenizes, embeds and indexes documents itself or accepts your own vectors, with metadata and document filters. It runs in-memory or persisted from the Python or JavaScript client, or as a server via chroma run; the repo ships a Dockerfile and compose file. Chroma Cloud is the hosted serverless version.

- **+** Four-function API: create collection, add, query, get
- **+** Handles tokenization, embedding and indexing; own vectors optional
- **+** Python and JavaScript clients; chroma run for client-server mode
- **+** Weekly tagged releases on Mondays with hotfixes in between
- **−** README is thin: no port, resource or auth guidance
- **−** Hosted Chroma Cloud is the headline; self-hosting detail lives in docs
- **−** Row-based API marked coming soon
- **−** No multi-user auth described in the README

<sub>no GPU · Docker + Compose · Models: built-in embedding or user-supplied vectors · [Repo](https://github.com/chroma-core/chroma) · [📖 Docs ↗](https://docs.trychroma.com/) · [🌐 Site ↗](https://www.trychroma.com/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/chroma/)</sub>

<a name="weaviate"></a>
### #&#8288;6 [Weaviate](https://github.com/weaviate/weaviate) <sub>score [62](../README.md#-how-we-rank "Score 62/100. Adoption: known (36) · Freshness: active (100) · Maintenance: fair (71) · Easy to run: easy (50) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · custom license · Oct 2026</sub>

**Go vector database with built-in vectorizers, hybrid search and RAG.**

Weaviate is a Go vector database that stores objects with their vectors and serves hybrid BM25 plus semantic search, filtering, built-in RAG and reranking through REST, gRPC and GraphQL APIs. It can vectorize data at import using modules for OpenAI, Cohere, HuggingFace, Google or a local model2vec image, or accept precomputed vectors. Docker Compose runs it on ports 8080 and 50051; production adds multi-tenancy, replication and RBAC.

- **+** Vectorizes at import with OpenAI, Cohere, HuggingFace, Google or a local model2vec container
- **+** Hybrid BM25 plus vector, image search, filtering, RAG and reranking in one query
- **+** Multi-tenancy, replication, RBAC, horizontal scaling and vector compression
- **+** REST, gRPC and GraphQL with Python, TypeScript, Java, Go and C# clients
- **−** Enterprise features in wl/ need a commercial license key; one image mixes both
- **−** Vectorization needs a module container or external API keys
- **−** No RAM or sizing guidance in the README
- **−** Both REST 8080 and gRPC 50051 must be exposed

<sub>no GPU · Docker + Compose · Needs optional embedding inference container (e.g. model2vec) or external embedding APIs · Models: OpenAI, Cohere, HuggingFace, Google and other integrated model providers, local model2vec (minishlab/potion-base-32M), precomputed vectors · port 8080 · [Repo](https://github.com/weaviate/weaviate) · [▶️ Demo ↗](https://elysia.weaviate.io) · [📖 Docs ↗](https://docs.weaviate.io) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/weaviate/)</sub>

<a name="zvec"></a>
### #&#8288;7 [zvec](https://github.com/alibaba/zvec) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: known (31) · Freshness: active (100) · Maintenance: healthy (83) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Oct 2026</sub>

**In-process vector database library with hybrid and full-text search.**

Zvec is a C++ vector database that embeds in the application process instead of running as a server. It stores dense and sparse vectors with a write-ahead log, and combines vector similarity, full-text search and structured filters in one query. SDKs exist for Python, Node.js, Go, Rust and Dart/Flutter.

- **+** Runs in-process: pip or npm install, no server or config to operate
- **+** Dense and sparse vectors, full-text search and filters in a single hybrid query
- **+** WAL-based durability; multiple processes can read the same collection concurrently
- **+** SDKs for Python, Node.js, Go, Rust, Dart; Linux glibc/musl, macOS, Windows builds
- **−** Writes are single-process exclusive, limiting multi-writer setups
- **−** No standalone server mode or HTTP API described in the README
- **−** Python SDK requires 64-bit Python 3.10 to 3.14
- **−** Benchmark results are only linked or charted; no figures in the README text

<sub>no GPU · [Repo](https://github.com/alibaba/zvec) · [📖 Docs ↗](https://zvec.org/en/docs/db/) · [🌐 Site ↗](https://zvec.org/en/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/zvec/)</sub>

<a name="leann"></a>
### #&#8288;8 [leann](https://github.com/startrail-org/leann) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: fair (72) · Easy to run: easy (50) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 13k · MIT · Oct 2026</sub>

**Vector index that recomputes embeddings on demand to cut storage.**

LEANN is a Python vector database that stores a pruned graph and recomputes embeddings at query time instead of storing them. The README claims 97% less storage, for example 60M chunks in 6GB versus 201GB. It ships HNSW and DiskANN backends, a CLI, RAG examples for files, mail and chat history, and an MCP server for Claude Code.

- **+** Graph-based selective recomputation avoids storing embeddings; README claims 97% less storage
- **+** HNSW and DiskANN backends, selectable with --backend-name
- **+** Works with Ollama, LM Studio, vLLM, llama.cpp and any OpenAI-compatible endpoint
- **+** Includes ready RAG loaders for PDFs, Apple Mail, WeChat, iMessage, ChatGPT and Claude history
- **−** Recomputing embeddings at query time adds latency compared with stored vectors
- **−** DiskANN needs a native toolchain (Boost, protobuf, MKL) when built from source
- **−** GPU acceleration is only a survey item for a future version
- **−** Linux uv hardlink installs can fail with a nltk pathsec error without a workaround

<sub>GPU optional · Docker · Needs uv, Ollama or OpenAI-compatible API (optional, for generation) · Models: HuggingFace, Ollama, OpenAI-compatible APIs, Anthropic, sentence-transformers · [Repo](https://github.com/startrail-org/leann) · [▶️ Demo ↗](https://colab.research.google.com/github/yichuan-w/LEANN/blob/main/demo.ipynb) · [📖 Docs ↗](https://github.com/yichuan-w/LEANN/blob/main/docs/configuration-guide.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/leann/)</sub>

<a name="helix-db"></a>
### #&#8288;9 [HelixDB](https://github.com/helixdb/helix-db) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (8) · Freshness: active (100) · Maintenance: healthy (95) · Easy to run: easy (50) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.2k · Apache-2.0 · Oct 2026</sub>

**Rust graph database with native vector and BM25 search.**

HelixDB is a Rust database that combines a labeled property graph, approximate nearest-neighbor vector search and BM25 full-text search in one transactional engine. A CLI starts a local instance in Docker or Podman on port 6969 (in-memory by default, --disk to persist) or the engine runs embedded, and Rust, TypeScript, Python and Go SDKs send the same JSON queries to POST /v2/query.

- **+** Graph traversal, vector ANN and BM25 in one transactional engine
- **+** Vector search prefiltered by graph traversal
- **+** SDKs for Rust, TypeScript, Python and Go sending the same JSON query
- **+** Embedded mode runs inside your process without a server
- **−** Local data is in-memory unless started with --disk
- **−** Python and Go SDKs are 0.x while Rust and TypeScript are 3.x
- **−** Cypher support only in source builds
- **−** Install is a curl piped to bash script

<sub>no GPU · Docker · Needs Docker or Podman for the local instance · Models: any embedding model; stores precomputed vectors · port 6969 · [Repo](https://github.com/helixdb/helix-db) · [📖 Docs ↗](https://docs.helix-db.com) · [🌐 Site ↗](https://helix-db.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/helix-db/)</sub>

<a name="pgvector"></a>
### #&#8288;10 [pgvector](https://github.com/pgvector/pgvector) <sub>score [59](../README.md#-how-we-rank "Score 59/100. Adoption: popular (53) · Freshness: active (100) · Maintenance: fair (57) · Easy to run: easy (50) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 23k · custom license · Oct 2026</sub>

**PostgreSQL extension for vector similarity search with HNSW and IVFFlat.**

pgvector is a PostgreSQL extension (Postgres 13+) that adds vector, halfvec, bit and sparsevec column types with L2, inner product, cosine, L1, Hamming and Jaccard distance operators, exact search by default and HNSW or IVFFlat indexes for approximate search. Vectors sit beside ordinary rows with ACID, joins and backups, and Postgres full-text search can be combined for hybrid retrieval. It installs via make, Docker or OS packages.

- **+** Vectors live next to relational data with ACID, joins and point-in-time recovery
- **+** HNSW and IVFFlat indexes with six distance operators
- **+** Half-precision, binary and sparse vector types plus binary quantization
- **+** Installs via make, Docker, Homebrew, APT, Yum; preinstalled on many hosted Postgres
- **−** vector type capped at 2,000 dimensions (halfvec 4,000)
- **−** Approximate indexes filter after scanning; filtered recall needs iterative scan tuning
- **−** HNSW builds slow down sharply once the graph exceeds maintenance_work_mem
- **−** No server of its own; capacity depends on your Postgres tuning

<sub>no GPU · Docker · Needs PostgreSQL 13+ · Models: any embedding model; stores precomputed vectors · [Repo](https://github.com/pgvector/pgvector) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/pgvector/)</sub>

<a name="turbovec"></a>
### #&#8288;11 [turbovec](https://github.com/ryancodrai/turbovec) <sub>score [54](../README.md#-how-we-rank "Score 54/100. Adoption: known (41) · Freshness: active (100) · Maintenance: fair (64) · Easy to run: some setup (33) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · MIT · Oct 2026</sub>

**In-process quantized vector index for Python and Rust using TurboQuant.**

turbovec is a library that stores embeddings at 2 or 4 bits per dimension using Google Research's TurboQuant and searches the compressed form with SIMD kernels. It needs no training step, supports single-vector add and remove, and persists incrementally with sync(). It does a brute-force scan rather than graph search, and ships LangChain, LlamaIndex, Haystack and Agno integrations.

- **+** README reports 4.4× faster than FAISS FastScan at 4-bit, at matching recall
- **+** 7.8× smaller than float32 at 4-bit, 15.5× at 2-bit
- **+** No training or rebuild; add and remove cost microseconds per vector
- **+** Allowlist filtering and crash-safe incremental sync(); drop-in stores for four frameworks
- **−** Scans every vector, so query cost grows linearly with corpus size
- **−** Lossy: top-1 matches float ground truth 96–98% at 4-bit on OpenAI embeddings
- **−** Library only: no network API, replication or multi-tenant service
- **−** Dimension must be a multiple of 8 and at most 16,384; only 2 or 4 bits

<sub>no GPU · [Repo](https://github.com/ryancodrai/turbovec) · [📖 Docs ↗](https://github.com/RyanCodrai/turbovec/blob/main/docs/api.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/turbovec/)</sub>

<a name="vespa"></a>
### #&#8288;12 [Vespa](https://github.com/vespa-engine/vespa) <sub>score [41](../README.md#-how-we-rank "Score 41/100. Adoption: niche (13) · Freshness: active (100) · Maintenance: healthy (81) · Easy to run: hard (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.1k · Apache-2.0 · Oct 2026</sub>

**Serving engine for vectors, tensors, text and ML ranking at scale.**

Vespa is a serving platform that indexes vectors, tensors, text and structured data, selects a subset at query time, evaluates machine-learned ranking models over it and returns results in under 100 ms while the corpus changes, across many nodes. The Java and C++ engine builds from this repo with a release every morning Monday to Thursday. Getting started and self-hosting live in docs.vespa.ai; Vespa Cloud is the hosted option.

- **+** Vectors, tensors, text and structured data queried and ranked together
- **+** Machine-learned ranking models evaluated at serving time
- **+** Runs hundreds of thousands of queries per second on large internet services
- **+** Sample applications repo plus detailed docs
- **−** README covers building, not running; install details live in docs
- **−** Heavy platform (Java and C++ engine) sized for multi-node clusters
- **−** C++ builds require AlmaLinux 8; Java needs JDK 17 and Maven
- **−** A new release every weekday morning Monday to Thursday; versions churn

<sub>no GPU · Models: machine-learned ranking models evaluated in Vespa · [Repo](https://github.com/vespa-engine/vespa) · [📖 Docs ↗](https://docs.vespa.ai) · [🌐 Site ↗](https://vespa.ai) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/vespa/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
