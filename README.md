# Hi there, I'm Kader Beevi 👋

**Lead Software Engineer**  
Full‑Stack & Distributed Systems | Software Architecture | AI/LLM Engineering | Cloud Infrastructure & Backend Design

*Specializing in High-Concurrency OLTP Systems, Distributed Database Architectures, Scalable Low-Latency Backend Engines, Enterprise RAG Workflows, AI Governance, and Stateful Multi-Agent Systems.*

✉️ kaderbv@gmail.com | 💼 [LinkedIn](https://linkedin.com/in/kaderbeevi) | 💻 [GitHub](https://github.com/Kaderbv)

---

## 🚀 About Me

With over **17 years of hands-on engineering experience**, I build high-availability backend systems, low-latency transaction processing layers, and enterprise AI orchestration frameworks. My technical focus bridges core database engine performance with cutting-edge agentic workflows and retrieval-augmented generation (RAG) platforms.

* ⚙️ **Core Expertise:** Distributed Systems Architecture, OLTP Query Optimization, Microservices, and Event-Driven Pipelines.
* 🤖 **AI Infrastructure:** Stateful Multi-Agent Orchestration, Vector DB Integration (Qdrant/Milvus), and AI Security/Governance.
* 🛠️ **Impact Highlights:**
  * Architected an in-house PaaS OLTP system across 700+ retail stores handling real-time payments via ISO 8583 standards.
  * Migrated 5.45 million loyalty accounts with zero data loss using scalable distributed pipelines.
  * Designed end-to-end multimodal computer vision and stateful RAG frameworks.

---

## 📂 Featured Open-Source & AI Projects

### 🛡️ [Aegis AI Platform](https://github.com/Kaderbv/aegis-platform-showcase)
**Role:** Independent Developer & AI Architect  
*Enterprise AI Security, Governance, and Agentic Guardrail Framework*

A production-grade platform to build, deploy, observe, evaluate, and operate reliable AI agents at scale. **Current release: v0.2.0 (Agent + RAG Foundation)**, with PostgreSQL persistence in progress.
> 🔒 Source code is private. The [showcase repo](https://github.com/Kaderbv/aegis-platform-showcase) has the case study, architecture, measured results, and design record. Reviewers can request access there.

* **Agent engine:** Built an async agent API with **FastAPI** and **LangGraph** that routes each request to a sandboxed calculator, the LLM, or the knowledge base, with real **SSE streaming** and typed API error mapping.
* **Multi-provider LLM layer:** Wrote a provider abstraction with **NVIDIA** (default) and **OpenAI** adapters, bounded retries with exponential backoff, request deadlines, and streaming-safe failure handling.
* **Grounded RAG:** Built configurable chunking (recursive / markdown), **OpenAI and NVIDIA embeddings**, **Qdrant** storage, and file upload (.txt/.md/.pdf/.docx). Agent answers are grounded in retrieved context, with source citations.
* **Retrieval safety (fail-closed):** Added query guardrails, role- and tenant-based access control, LLM query expansion, cross-encoder reranking, **Presidio** PII masking, and hallucination-risk scoring.
* **Multi-tenant data integrity:** Found and fixed cross-tenant overwrite and injection paths by scoping document identity to `(organization, doc_id)`. Added tenant-safe delete and content-hash change detection, so unchanged documents skip re-embedding.
* **Observability and operations:** Built LLM and RAG metrics (latency, failures by pipeline stage, guardrail rejections), correlation-ID middleware, startup model warm-up behind readiness probes, and an app factory.
* **Persistence (in progress, v0.3.0):** Added async **PostgreSQL** (asyncpg) settings, pooled engine lifecycle, and database-aware readiness checks, with Postgres 16 integration tests in CI.
* **Engineering rigor:** Documentation-first process (PRD, SRS, C4, **10 RFCs**, **18 ADRs**). **900+ unit, integration, and smoke tests** run without API keys, and GitHub Actions gates every change on Ruff, mypy, pytest, and pre-commit.

### 👁️ [LocateMe AI: Voice-Assisted Object Finder](https://github.com/Kaderbv/LocateMeAI-Showcase)
**Role:** Lead Creator & Architect  
*Multimodal Computer Vision & Natural Language Query Engine*
> 🔒 Source code is private. The [showcase repo](https://github.com/Kaderbv/LocateMeAI-Showcase) has the case study, [demo video](https://youtu.be/C4aFTRYnjs0), architecture, and evaluation results. Reviewers can request access there.

* Built a full-stack voice and text object finder ("where's my phone?") that combines **YOLOv8** detection, **ByteTrack / BoT-SORT** multi-object tracking, a local **LLaVA** vision-language model via Ollama, and **MiniLM** intent routing, using **FastAPI** and **Streamlit**.
* Designed **tracklet stitching** and a static-object rule that count each object once instead of once per frame. This cut video counting error **8×** (MAE 5.33 → 0.67), turning "1,916 detections" into "3 motorcycles".
* Built a **privacy blur** layer and tested it adversarially by re-running the detector on blurred output. Bystander leakage dropped from **24 % to 0 %**.
* Raised LLM class extraction from **86.7 % to 100 %** exact match by tracing every failure to the deterministic parser, then locking each fix in with a regression test.
* Runs fully **on-device**: **21 ms** per image and **45–47 FPS** video on CPU. Images never leave the machine.
* Wrote a **six-stage evaluation suite** (intent, extraction, detection mAP, counting MAE/MAPE, latency, blur leakage) and 53 pytest unit tests, with GitHub Actions gating Docker Compose deploys to AWS EC2.

### 🧠 [WIKIRAG - Stateful Multi-Agent RAG System](https://github.com/Kaderbv/WIKIRAG)
**Role:** Lead Creator & Architect  
*Stateful Retrieval-Augmented Generation Architecture*
* Designed a low-latency, stateful RAG pipeline utilizing **LangChain**, **LangGraph**, and **Qdrant/Milvus** vector databases.
* Integrated multi-agent orchestration to dynamically process unstructured queries and validate retrieval accuracy before LLM synthesis.

### 📊 [Classic Machine Learning & Anomaly Detection Workflows](https://github.com/Kaderbv)
**Role:** Lead Developer  
*Production-Ready ML Pipelines & Predictive Classification*
* Built end-to-end production pipelines using **Python**, **Scikit-Learn**, **Pandas**, and **NumPy** for tabular classification algorithms and real-time anomaly detection.
* Implemented feature selection, automated hyperparameter optimization, and strict cross-validation strategies to eliminate model drift.

---

## 🛠 CORE TECHNICAL SKILLS

* **Languages:** C#, Python, SQL, JavaScript, C++
* **Backend & Distributed Systems:** .NET Core, ASP.NET Core / Web API, Microservices, Distributed Systems, REST APIs, CQRS, MediatR, Event-Driven Architecture, Pub/Sub, Distributed Caching, Multi-Tenant Systems, High Availability
* **Cloud & Infrastructure:** Microsoft Azure, Azure Functions, Azure App Services, Azure Storage, Azure Service Bus, Azure AD/B2C, Azure DevOps, AKS, AWS
* **Containers & DevOps:** Docker, Kubernetes, OpenShift, Rancher, CI/CD, Git, Production Automation
* **Databases & Messaging:** SQL Server, PostgreSQL, MongoDB, Cassandra, Redis, Elasticsearch, LiteDB, Entity Framework, Dapper, RabbitMQ, Kafka, Hangfire, ISO 8583, TCP Socket Communication
* **AI/ML & RAG:** Retrieval-Augmented Generation (RAG), Vector Search, Vector Databases (Qdrant / Milvus / Chroma), Text Embeddings, Semantic Search, Dense Passage Retrieval, Chunking Strategies, Context Expansion, Prompt Engineering, Hallucination Reduction, Python, FastAPI, Scikit-Learn, Pandas, NumPy, Feature Engineering, Classification, Anomaly Detection, Model Evaluation
* **LLM & AI Orchestration:** LangChain, LangGraph, LlamaIndex, Agentic Workflows & Multi-Agent Orchestration, OpenAI API, Ollama, HuggingFace Embeddings, Claude Code, GitHub Copilot
* **AI-Assisted Engineering:** OpenAI API, Claude Code, GitHub Copilot, Repository-wide Refactoring, Automated PR Generation, Automated Test Generation
* **Testing & Observability:** xUnit, Moq, FluentAssertions, Integration Testing, OpenTelemetry, Dynatrace, Splunk

---

## 📈 GitHub Stats

<p align="left">
  <img src="https://github-readme-stats.vercel.app/api?username=Kaderbv&show_icons=true&theme=nord" alt="Kaderbv GitHub Stats" height="150" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Kaderbv&layout=compact&theme=nord" alt="Top Languages" height="150" />
</p>

---

📫 **Let's Connect:** Feel free to reach out via [LinkedIn](https://linkedin.com/in/kaderbeevi) or [Email](mailto:kaderbv@gmail.com) for technical discussions on distributed database engine design, AI governance, or system architecture!
