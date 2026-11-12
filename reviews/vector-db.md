# 🧮 Vector databases reviews · Best of Open-Source AI

Vector stores and hybrid search engines for embeddings. Back to the [leaderboard](../README.md#-vector-databases).

<sub>🌐 Also on the web: [Vector databases on archestack.com](https://archestack.com/best-of-ai/vector-db/), each project on its own page.</sub>

<a name="milvus"></a>
### 🥇 [Milvus](https://github.com/milvus-io/milvus) <sub>score [90](../README.md#-how-we-rank "Score 90/100. Adoption: widely used (94) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 47k · Apache-2.0 · Nov 2026</sub>

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

<a name="qdrant"></a>
### 🥈 [Qdrant](https://github.com/qdrant/qdrant) <sub>score [85](../README.md#-how-we-rank "Score 85/100. Adoption: widely used (87) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 36k · Apache-2.0 · Oct 2026</sub>

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

<a name="meilisearch"></a>
### 🥉 [Meilisearch](https://github.com/meilisearch/meilisearch) <sub>score [84](../README.md#-how-we-rank "Score 84/100. Adoption: widely used (97) · Freshness: active (100) · Maintenance: fair (74) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 60k · custom license · Nov 2026</sub>

**Rust search engine with typo tolerance, filtering and hybrid semantic search.**

Meilisearch is a search engine with a RESTful API for full-text, semantic and hybrid search, including typo tolerance, facets, sorting, synonyms and geosearch. It runs as a single binary or Docker image on port 7700, and ships an experimental MCP server at /mcp plus a LangChain vector store integration. The Community Edition is MIT licensed; sharding is in the Enterprise Edition.

- **+** Single binary or Docker image; quick start is one command on port 7700
- **+** Typo tolerance, facets, filters, sorting, synonyms and geosearch built in
- **+** Hybrid full-text plus semantic search through one REST API
- **+** SDKs for JavaScript, Python, PHP, Ruby, Go and Rust, plus a React integration
- **−** Sharding and other advanced features need the Enterprise Edition and a commercial agreement
- **−** README recommends Meilisearch Cloud over self-hosting
- **−** MCP server at /mcp is marked experimental

<sub>no GPU · Docker · Models: embedding models for semantic search (providers unknown) · port 7700 · [Repo](https://github.com/meilisearch/meilisearch) · [▶️ Demo ↗](https://where2watch.meilisearch.com/) · [📖 Docs ↗](https://www.meilisearch.com/docs) · [🌐 Site ↗](https://www.meilisearch.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/meilisearch/)</sub>

<a name="faiss"></a>
### #&#8288;4 [faiss](https://github.com/facebookresearch/faiss) <sub>score [81](../README.md#-how-we-rank "Score 81/100. Adoption: widely used (91) · Freshness: active (100) · Maintenance: healthy (80) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 42k · MIT · Nov 2026</sub>

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

<a name="leann"></a>
### #&#8288;5 [leann](https://github.com/startrail-org/leann) <sub>score [80](../README.md#-how-we-rank "Score 80/100. Adoption: popular (63) · Freshness: active (100) · Maintenance: healthy (84) · Agent-ready: partly (55) (each out of 100, weighted). Click for how we rank.") · ⭐ 14k · MIT · Oct 2026</sub>

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

<a name="weaviate"></a>
### #&#8288;6 [Weaviate](https://github.com/weaviate/weaviate) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (71) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: minimal (40) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · custom license · Nov 2026</sub>

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

<a name="lancedb"></a>
### #&#8288;7 [lancedb](https://github.com/lancedb/lancedb) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: popular (59) · Freshness: active (100) · Maintenance: healthy (89) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 12k · Apache-2.0 · Nov 2026</sub>

**Embedded vector database built on the Lance columnar format.**

LanceDB is a vector database written in Rust on top of the Lance columnar format. It stores vectors, metadata and multimodal data (text, images, video, point clouds) and supports vector similarity search, full-text search and SQL filtering. It runs locally or in your own cloud, with Python, TypeScript and Rust SDKs plus a REST API.

- **+** Runs embedded and locally, with no separate server required per the README
- **+** Combines vector search, full-text search and SQL in one store
- **+** Automatic data versioning and zero-copy access without extra infrastructure
- **+** Python, TypeScript and Rust SDKs; integrates with LangChain, LlamaIndex, Pandas, Polars, DuckDB
- **−** README gives no benchmarks or hardware figures to back the billion-vector claims
- **−** Managed Cloud and Enterprise tiers exist; feature split with open source is not detailed
- **−** README has little setup detail and defers to external docs

<sub>GPU optional · Docker + Compose · [Repo](https://github.com/lancedb/lancedb) · [📖 Docs ↗](https://docs.lancedb.com) · [🌐 Site ↗](https://lancedb.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lancedb/)</sub>

<a name="helix-db"></a>
### #&#8288;8 [HelixDB](https://github.com/helixdb/helix-db) <sub>score [77](../README.md#-how-we-rank "Score 77/100. Adoption: known (35) · Freshness: active (100) · Maintenance: healthy (97) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 6.3k · Apache-2.0 · Nov 2026</sub>

**Graph database with built-in vector and BM25 search, written in Rust.**

HelixDB is a transactional labeled-property graph database that also does approximate nearest-neighbor vector search, prefiltered by graph traversal, and BM25 full-text search over node and edge properties. Queries are written with Rust, TypeScript, Python or Go SDKs and sent as JSON to POST /v2/query on port 6969. It runs locally via the helix CLI, embedded in-process, or on the managed Helix Cloud.

- **+** Graph, vector and BM25 queries in one transactional engine
- **+** SDKs for Rust, TypeScript, Python and Go emit the same JSON request
- **+** No build or deploy step for queries; embedded mode runs in-process
- **+** Apache-2.0 licensed; durable storage on object storage
- **−** Local dev needs Docker or Podman; data is in memory unless started with --disk
- **−** Cypher support is only in source builds
- **−** Python SDK is at 0.3.4 and Go at v0.3.1, so pre-1.0
- **−** HA, auto-scaling readers are in the managed Helix Cloud, not the local server

<sub>no GPU · Docker · Needs Docker or Podman (local server) · port 6969 · [Repo](https://github.com/helixdb/helix-db) · [📖 Docs ↗](https://docs.helix-db.com) · [🌐 Site ↗](https://helix-db.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/helix-db/)</sub>

<a name="zvec"></a>
### #&#8288;9 [zvec](https://github.com/alibaba/zvec) <sub>score [75](../README.md#-how-we-rank "Score 75/100. Adoption: popular (68) · Freshness: active (100) · Maintenance: healthy (82) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 16k · Apache-2.0 · Nov 2026</sub>

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

<a name="chroma"></a>
### #&#8288;10 [Chroma](https://github.com/chroma-core/chroma) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: widely used (83) · Freshness: active (99) · Maintenance: patchy (36) · Agent-ready: partly (70) (each out of 100, weighted). Click for how we rank.") · ⭐ 30k · Apache-2.0 · Nov 2026</sub>

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

<a name="pgvector"></a>
### #&#8288;11 [pgvector](https://github.com/pgvector/pgvector) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: popular (79) · Freshness: active (100) · Maintenance: fair (61) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 24k · custom license · Nov 2026</sub>

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

<a name="lance"></a>
### #&#8288;12 [lance](https://github.com/lance-format/lance) <sub>score [72](../README.md#-how-we-rank "Score 72/100. Adoption: known (42) · Freshness: active (100) · Maintenance: healthy (88) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.3k · Apache-2.0 · Nov 2026</sub>

**Columnar table format for multimodal AI data with vector and full-text search.**

Lance is a file format, table format and catalog spec written in Rust, with Python (pylance) and Java bindings. It stores images, video, audio, text and embeddings in one dataset on local disk or object storage, with IVF_PQ vector indices, BM25 full-text search and versioned tables with time travel. It integrates with Arrow, Pandas, Polars, DuckDB, Spark, Ray, Trino and Flink.

- **+** Vector, BM25 full-text and SQL queries run on the same dataset with secondary indices
- **+** Reads and writes S3, Azure, GCS, Hugging Face Hub and other stores by URI scheme
- **+** Adds columns with backfilled values without rewriting the whole table
- **+** Built-in ACID versioning with tags, branches and time travel
- **−** Library and format, not a server; the README shows no network query API
- **−** Only stable data_storage_version values carry a compatibility guarantee; next is unstable
- **−** Mixed Lance versions require pinning data_storage_version for deterministic writes
- **−** Performance claims such as 100x vs Parquet come from the project's own benchmarks

<sub>Compose · [Repo](https://github.com/lance-format/lance) · [📖 Docs ↗](https://lance.org) · [🌐 Site ↗](https://lance.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/lance/)</sub>

<a name="turbovec"></a>
### #&#8288;13 [turbovec](https://github.com/ryancodrai/turbovec) <sub>score [69](../README.md#-how-we-rank "Score 69/100. Adoption: popular (73) · Freshness: active (100) · Maintenance: fair (50) · Agent-ready: none (15) (each out of 100, weighted). Click for how we rank.") · ⭐ 17k · MIT · Oct 2026</sub>

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
### #&#8288;14 [Vespa](https://github.com/vespa-engine/vespa) <sub>score [66](../README.md#-how-we-rank "Score 66/100. Adoption: known (40) · Freshness: active (100) · Maintenance: healthy (81) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 7.2k · Apache-2.0 · Nov 2026</sub>

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

<a name="infinity"></a>
### #&#8288;15 [infinity](https://github.com/infiniflow/infinity) <sub>score [60](../README.md#-how-we-rank "Score 60/100. Adoption: niche (18) · Freshness: active (100) · Maintenance: fair (72) · Agent-ready: minimal (30) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.8k · Apache-2.0 · Nov 2026</sub>

**Database for hybrid dense, sparse, tensor and full-text search.**

Infinity is a C++ database that runs hybrid search over dense vectors, sparse vectors, tensors and full-text, with filtering on structured columns. It supports RRF, weighted-sum and ColBERT rerankers, and is used from a Python SDK (embedded or over the network) or an HTTP API. The README reports 0.1 ms latency and 15K+ QPS on million-scale vector sets, and 1 ms latency on full-text search over 33M documents.

- **+** One query combines dense, sparse, tensor and full-text search with filters
- **+** Ships RRF, weighted-sum and ColBERT rerankers
- **+** Single binary with no external dependencies; also embeddable as a Python module
- **+** Python SDK and HTTP API available
- **−** Requires an x86_64 CPU with AVX2; no ARM support listed
- **−** Quickstart uses the nightly Docker tag rather than a pinned release
- **−** Benchmark figures are self-reported in the README
- **−** Windows use requires WSL/WSL2 with host networking

<sub>no GPU · Models: dense embeddings, sparse embeddings, tensors, ColBERT reranking · [Repo](https://github.com/infiniflow/infinity) · [📖 Docs ↗](https://infiniflow.org/docs/dev/category/get-started) · [🌐 Site ↗](https://infiniflow.org) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/infinity/)</sub>

<a name="hnswlib"></a>
### #&#8288;16 [hnswlib](https://github.com/nmslib/hnswlib) <sub>score [53](../README.md#-how-we-rank "Score 53/100. Adoption: niche (27) · Freshness: active (96) · Maintenance: fair (55) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.4k · Apache-2.0 · Sep 2026</sub>

**Header-only C++ library for approximate nearest neighbor search with HNSW graphs.**

Hnswlib implements the HNSW graph index for approximate nearest neighbor search as a header-only C++11 library with Python bindings. It supports L2, inner product and cosine distances, incremental inserts, updates, label filtering and marking elements as deleted. Indexes are saved to disk or pickled in Python, and C++ users can define custom distances.

- **+** Header-only with no dependencies beyond C++11; installs with pip install hnswlib
- **+** Supports incremental inserts, in-place updates, and deletion with slot reuse
- **+** Python index is picklable; C++ supports custom distances, multivector and epsilon search
- **+** Optional -fno-exceptions C++ API via *NoExceptions methods returning Status
- **−** Library only: no server, REST API or built-in metadata storage
- **−** Only l2, ip and cosine in Python; other spaces need nmslib
- **−** max_elements must be set up front; resizing is not thread-safe with add or query
- **−** Python filtered search is slow in multithreaded mode because of the GIL

<sub>no GPU · [Repo](https://github.com/nmslib/hnswlib) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/hnswlib/)</sub>

<a name="sptag"></a>
### #&#8288;17 [sptag](https://github.com/microsoft/sptag) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: niche (21) · Freshness: active (100) · Maintenance: patchy (44) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.0k · MIT · Sep 2026</sub>

**C++ library for approximate nearest neighbor search over large vector sets.**

SPTAG is a Microsoft Research and Bing library for approximate nearest neighbor search over vectors using L2 or cosine distance. It offers two index types: SPTAG-KDT (kd-tree plus relative neighborhood graph) and SPTAG-BKT (balanced k-means tree plus graph). It supports online insertion and deletion, and search across multiple machines.

- **+** Two index types: KDT for cheaper builds, BKT for accuracy on very high-dimensional data
- **+** Supports online vector insertion and deletion without a full rebuild
- **+** Distributed serving across multiple machines
- **+** Backed by published papers (SPANN, SPFresh, VBASE) and MIT licensed
- **−** Source build needs swig, cmake and boost; optional SPDK and RocksDB builds are involved
- **−** Only L2 and cosine distances are documented
- **−** No tagged releases; build from source or the Dockerfile
- **−** Library, not a standalone server; an online service needs the Python wrapper

<sub>Docker · Needs swig >= 4.0.2, cmake >= 3.12.0, boost >= 1.67.0, SPDK (optional), RocksDB (optional) · [Repo](https://github.com/microsoft/sptag) · [📖 Docs ↗](https://github.com/microsoft/SPTAG/blob/master/docs/GettingStart.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sptag/)</sub>

<a name="usearch"></a>
### #&#8288;18 [usearch](https://github.com/unum-cloud/usearch) <sub>score [49](../README.md#-how-we-rank "Score 49/100. Adoption: niche (13) · Freshness: active (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 4.4k · Apache-2.0 · Nov 2026</sub>

**Proximity-graph nearest-neighbor index with bindings for 14 languages.**

USearch is a header-only C++20 library for approximate nearest-neighbor search over dense vectors, with experimental engines for sequences, 3D shapes and geospatial sets. Indexes can live in RAM, GPU VRAM or NVMe and share one checkpoint format. It also offers MaxSim multi-vector scoring and graph-selected sparse products. ClickHouse, DuckDB, ScyllaDB and YugabyteDB embed it.

- **+** Header-only C++20 core with no external dependencies; one C ABI under all bindings
- **+** RAM, VRAM and NVMe residencies exchange portable SafeGraphs checkpoint files
- **+** Embedded in ClickHouse, DuckDB, ScyllaDB and YugabyteDB for vector search
- **+** Compiles up to 11 storage types (bf16, i8, u1, e4m3 and more) and uses 128-bit keys
- **−** Library only: no server, REST API or built-in clustering
- **−** Sequence, shape and geospatial engines are experimental and exposed only via C/C++
- **−** Filtered search is missing in the JavaScript and Java bindings
- **−** Geometry and storage types are fixed when the index opens

<sub>GPU optional · [Repo](https://github.com/unum-cloud/usearch) · [📖 Docs ↗](https://github.com/unum-cloud/USearch/blob/main/include/usearch/dense/README.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/usearch/)</sub>

<a name="deeplake"></a>
### #&#8288;19 [deeplake](https://github.com/activeloopai/deeplake) <sub>score [47](../README.md#-how-we-rank "Score 47/100. Adoption: popular (52) · Freshness: recent (71) · Maintenance: patchy (32) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 9.3k · Apache-2.0 · May 2026</sub>

**Serverless database for vectors and raw AI data, with versioning and ML dataloaders.**

Deep Lake is a Python-installed database that stores embeddings alongside raw data such as images, video, audio, text and PDFs in a chunked columnar format. It serves as a vector store for LLM apps (LangChain, LlamaIndex) and as a streaming dataset layer for PyTorch and TensorFlow training. Computation runs client-side, and data can live on S3, GCP, Azure, S3-compatible storage like MinIO, or local disk.

- **+** Stores raw media and embeddings together, not just vectors with light metadata
- **+** Built-in dataset version control and PyTorch/TensorFlow dataloaders
- **+** Serverless and client-side; works with S3, GCP, Azure, MinIO, local or in-memory storage
- **+** Integrates with LangChain, LlamaIndex, Weights & Biases and MMDetection
- **−** README says full features require registering in the hosted Deep Lake App
- **−** Visualizer and public dataset hub are tied to Activeloop's cloud service
- **−** No server mode; README gives no benchmarks for large-scale vector search
- **−** README links mix old and new docs sites, and comparisons look dated

<sub>no GPU · Needs Python (pip install deeplake), Deep Lake App account for full features, Optional S3/GCP/Azure storage · Models: PyTorch, TensorFlow, LangChain, LlamaIndex · [Repo](https://github.com/activeloopai/deeplake) · [📖 Docs ↗](https://docs.deeplake.ai/) · [🌐 Site ↗](https://www.deeplake.ai/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/deeplake/)</sub>

<a name="attu"></a>
### #&#8288;20 [attu](https://github.com/zilliztech/attu) <sub>score [45](../README.md#-how-we-rank "Score 45/100. Adoption: niche (5) · Freshness: active (100) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.2k · custom license · Sep 2026</sub>

**Management UI for Milvus clusters with data browsing, search and an AI agent.**

Attu is a management console for Milvus vector databases. One instance connects to several Milvus clusters or Zilliz Cloud, and lets you browse collections, edit data, run vector and BM25 searches, manage backups and RBAC, and view Prometheus metrics. A built-in agent with 50+ tools performs Milvus operations from chat, using OpenAI, Claude, DeepSeek, Gemini, OpenRouter or a custom endpoint.

- **+** Multiple Milvus clusters managed from one instance, each with its own workspace
- **+** Ships as Docker image, Linux server package, or desktop app for macOS, Linux, Windows
- **+** Local login, audit logs of write operations, TLS/mTLS and SSRF protection built in
- **+** Backup and restore to S3, MinIO, GCS or Azure Blob, plus CSV, JSON, Parquet import/export
- **−** Supports only Milvus 2.6.0+ and 3.x plus Zilliz Cloud; 2.5.x and earlier are unsupported
- **−** Works only with Milvus; no other vector stores
- **−** Desktop build is single-user and has no multi-user login
- **−** Desktop SSRF rules block local and LAN services unless allowlisted via environment variable

<sub>no GPU · Needs Milvus 2.6.0+ or 3.x, or Zilliz Cloud, SQLite (bundled), Node.js 24.x (standalone server package) · Models: OpenAI, Anthropic Claude, DeepSeek, Google Gemini, OpenRouter · port 3000 · [Repo](https://github.com/zilliztech/attu) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/attu/)</sub>

<a name="sqlite-vec"></a>
### #&#8288;21 [sqlite-vec](https://github.com/asg017/sqlite-vec) <sub>score [37](../README.md#-how-we-rank "Score 37/100. Adoption: known (48) · Freshness: recent (74) · Maintenance: weak (2) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 8.3k · Apache-2.0 · May 2026</sub>

**Vector search extension for SQLite, written in pure C.**

sqlite-vec adds vec0 virtual tables to SQLite for storing float, int8 and binary vectors and running KNN queries with a MATCH clause. It is pure C with no dependencies and runs wherever SQLite does, including WASM and Raspberry Pi. Metadata, auxiliary and partition key columns keep non-vector data in the same table. It is pre-v1 and succeeds sqlite-vss.

- **+** Pure C with no dependencies; loads as a normal SQLite extension
- **+** Bindings for Python, Node.js, Ruby, Go, Rust, Datasette, rqlite and sqlite-utils
- **+** Supports float, int8 and binary vectors, given as JSON or compact binary
- **+** Runs in the browser via WASM and on small devices like Raspberry Pi
- **−** Pre-v1, so the README warns to expect breaking changes
- **−** Described as 'fast enough'; README gives no benchmarks or index types
- **−** Does not generate embeddings; separate tools like sqlite-lembed are needed
- **−** Embedded library only; no standalone server mode

<sub>no GPU · Needs SQLite · Models: float vectors, int8 vectors, binary vectors · [Repo](https://github.com/asg017/sqlite-vec) · [📖 Docs ↗](https://alexgarcia.xyz/sqlite-vec/installation.html) · [🌐 Site ↗](https://alexgarcia.xyz/sqlite-vec/) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/sqlite-vec/)</sub>

<a name="ann-benchmarks"></a>
### #&#8288;22 [ann-benchmarks](https://github.com/erikbern/ann-benchmarks) <sub>score [35](../README.md#-how-we-rank "Score 35/100. Adoption: known (30) · Freshness: active (87) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 5.8k · MIT · Jul 2026</sub>

**Benchmark harness comparing approximate nearest neighbor libraries on recall versus speed.**

ANN-Benchmarks runs approximate nearest neighbor algorithms, each built in its own Docker container, against pre-split HDF5 datasets such as SIFT, GloVe, GIST and NYTimes. It sweeps hyperparameters, keeps the precision-performance frontier, and plots recall against queries per second. The README states the project is no longer actively maintained and points to VIBE as a successor.

- **+** Covers about 40 implementations including FAISS, hnswlib, Annoy, pgvector, Qdrant, Milvus and DiskANN
- **+** Datasets ship pre-split with top-100 ground truth in HDF5, with Euclidean, angular and Jaccard metrics
- **+** Each algorithm has a Dockerfile, config.yml and CI test, so results are reproducible
- **+** Adding an algorithm needs a Python wrapper, a Dockerfile and a config file
- **−** No longer actively maintained; README recommends VIBE instead
- **−** Published plots are from April 2025, and the README has a TODO to update the website plots
- **−** Full run can take days; the Docker image build alone takes 10-30 minutes
- **−** Single-CPU, in-RAM datasets only; GPU support exists just for FAISS and needs a local build

<sub>GPU optional · Needs Docker, Python 3.10 · Models: HDF5 datasets · [Repo](https://github.com/erikbern/ann-benchmarks) · [🌐 Site ↗](http://ann-benchmarks.com) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/ann-benchmarks/)</sub>

<a name="nmslib"></a>
### #&#8288;23 [nmslib](https://github.com/nmslib/nmslib) <sub>score [7](../README.md#-how-we-rank "Score 7/100. Adoption: niche (8) · Freshness: quiet (16) · Maintenance: weak (0) · Agent-ready: none (0) (each out of 100, weighted). Click for how we rank.") · ⭐ 3.6k · Apache-2.0 · Jan 2026</sub>

**Approximate nearest-neighbor search library for metric and non-metric spaces.**

NMSLIB is a C++ similarity search library with Python bindings and an Apache Thrift query server usable from Java. It implements HNSW, VP-tree, NAPP and inverted-file methods, and supports non-metric distance functions. It also serves as a toolkit for evaluating search methods. The core library has no third-party dependencies.

- **+** Core library has no third-party dependencies
- **+** Supports non-metric spaces, not only L2 or cosine
- **+** Prebuilt wheels for Python 3.8-3.13 on Linux, macOS, Windows, Intel and ARM
- **+** Extendible with new search methods and distance functions
- **−** Last release was 2021-02-03, though commits continue
- **−** Library only: no persistence layer or database features described
- **−** Standalone hnswlib is lighter if only HNSW is needed
- **−** Query server requires Apache Thrift 0.12, an old version

<sub>Needs Apache Thrift 0.12 (query server only) · [Repo](https://github.com/nmslib/nmslib) · [📖 Docs ↗](https://github.com/nmslib/nmslib/blob/master/manual/README.md) · [📊 Score breakdown ↗](https://archestack.com/best-of-ai/projects/nmslib/)</sub>

<sub>Written from each project README and checked facts; see [how this works](../README.md#-how-this-works). Wrong? [Tell us](https://github.com/archestack/best-of-ai/issues/new/choose).</sub>
