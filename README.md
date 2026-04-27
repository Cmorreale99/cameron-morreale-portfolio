# Cameron Morreale — Data Engineering Portfolio

Building financial data systems, repairing broken pipelines, and transforming complex, undocumented data environments into scalable decision infrastructure.

![Python](https://img.shields.io/badge/Python-Data%20Engineering-blue)
![SQL](https://img.shields.io/badge/SQL-Advanced-green)
![Oracle](https://img.shields.io/badge/Database-Oracle-red)
![AWS](https://img.shields.io/badge/AWS-Lambda-orange)
![Focus](https://img.shields.io/badge/Focus-Financial%20Data%20Systems-black)

# Cameron Morreale: Business Logic Into Reliable Data Systems

I operate at the business-data boundary: ambiguous workflows, undocumented systems, and unreliable data paths into structured, auditable data systems. I build pipelines, data models, validation layers, and analytics interfaces that help stakeholders trust the numbers they use to make decisions.

My strongest signal is translating fragmented business logic into reliable architecture: reverse-engineering source systems, diagnosing pipeline failures, structuring messy inputs, and delivering analytics-ready outputs.

**MS Data Science: Worcester Polytechnic Institute**  
**Wellington Management: Data Engineering / Data Architecture**

[LinkedIn](https://www.linkedin.com/in/cam-morreale99)

---

## Flagship Project

### Wellington Management: Data Architecture and Pipeline Recovery

Reconstructed the data architecture behind an investment decision platform supporting ~$153B in assets and ~160 investment professionals.

- **Problem:** A legacy Excel-driven investment workflow was being migrated into a production Python platform, but the Oracle data environment had ~250 tables, no schema, no documented relationships, and no clear lineage. The SQL pipeline failed before the new system could run.
- **Intervention:** Reverse-engineered SQL and embedded Excel business logic, narrowed the environment to ~25 prioritized core tables, inferred relationships, and traced the execution path that exposed a missing upstream dataset.
- **Impact:** Restored pipeline execution with minimal modification, enabled the team to continue building the production decision platform, and supported an analytics override framework with validation and auditability.
- **Business signal:** Platform supported ~$153B in assets and was associated with ~$8M in annual operational efficiency gains.
- **Useful tools:** Oracle SQL, Python, Pandas, ipywidgets.

[Full technical writeup](./wellington/technical-writeup.md)

---

## Selected Projects

### Wellington Management

Data architecture and pipeline recovery for a production investment decision platform.

- **Problem:** Fragmented Oracle environment, undocumented lineage, spreadsheet-derived SQL, and a missing upstream dependency that broke pipeline execution.
- **System built:** Reconstructed relational structure from SQL and Excel logic, mapped core dependencies, restored access to the missing dataset, and contributed to controlled analytics overrides.
- **Impact:** Enabled a reliable Python decision platform for ~160 investment professionals supporting ~$153B in assets, with ~$8M estimated annual operational efficiency gain.
- **Key technologies:** Oracle SQL, Python, Pandas, ipywidgets.

### MassDEP

LLM-based document intelligence system for environmental reporting workflows.

- **Problem:** PFAS metrics, shipment quantities, and environmental report data were embedded in inconsistent free-text PDFs, forcing manual and error-prone extraction.
- **System built:** On a team, I architected a multi-stage pipeline for retrieval, entity extraction, validation, and post-generation verification. Outputs were integrated into a Power BI analytics layer with page-level inspection, readability tracking, and system performance visualization.
- **Impact:** Transformed unstructured environmental reports into structured, validated datasets with ~97.4% document processing coverage and an estimated ~40% manual reporting effort reduction.
- **Key technologies:** RAG, vector embeddings, constrained generation, validation logic, Power BI.

### Embue

Distributed IoT data infrastructure for secure telemetry storage and verification.

- **Problem:** Centralized IoT storage created single points of failure and weak guarantees around integrity, confidentiality, and auditability.
- **System built:** Designed a layered architecture where telemetry is encrypted, stored through IPFS, verified through Filecoin/blockchain infrastructure, and governed through access-control smart contracts.
- **Impact:** Separated storage from verification so blockchain handled integrity and auditability while bulk sensor data stayed off-chain for scalability.
- **Key technologies:** GnuPG, IPFS, Web3.Storage, Filecoin, Lotus, smart contracts.

### BoardGameGeek

Async data platform combining marketplace prices, ratings, metadata, and checkout workflows.

- **Problem:** Marketplace prices, ratings, and game metadata came from heterogeneous sources with rate-limited APIs and inconsistent formats.
- **System built:** Built a three-stage async ingestion pipeline with bounded concurrency, rate-limit handling, retries, progress tracking, normalization, validation, and a recursive relational model for board game relationships.
- **Impact:** Produced queryable, integrated board game data and connected it to backend and frontend workflows through AWS Lambda account updates and a React checkout flow.
- **Key technologies:** Python, aiohttp, relational modeling, AWS Lambda, React.

### OneWorld

Tokenized carbon market infrastructure for programmable emissions permits.

- **Problem:** Traditional cap-and-trade systems suffer from opaque permit allocation, weak enforcement, double-counting risk, and market manipulation.
- **System built:** Hackathon system that modeled emissions permits as programmable financial assets, with deterministic supply decay, time-period constraints, tiered pricing, and blockchain-based auditability.
- **Impact:** Placed Top 3 out of 100+ teams and translated policy constraints into enforceable market infrastructure.
- **Key technologies:** Blockchain infrastructure, token design, incentive modeling, oracle-ready architecture.

### Oasis

Decentralized social platform with DAO governance and tokenized incentives.

- **Problem:** Centralized social platforms concentrate moderation power, weaken user ownership, and misalign incentives between users and platform operators.
- **System built:** Built in a 48-hour hackathon environment using DAO-based voting, smart contracts, decentralized storage, staking, rewards pools, and token incentives for content participation.
- **Impact:** Placed 1st out of 100+ teams and showed rapid end-to-end architecture, product thinking, and incentive design under tight constraints.
- **Key technologies:** Smart contracts, DAO governance, decentralized storage, staking, token rewards.

---

## Technical Strengths

- **Data systems and architecture:** Reverse-engineer fragmented systems, identify core dependencies, separate storage from verification, and design controlled workflows.
- **SQL and data modeling:** Infer relational structure, prioritize core tables, map lineage, design recursive models, and align transformations with business logic.
- **Pipeline engineering:** Diagnose root causes, restore failed execution paths, build async ingestion, handle rate limits, implement retries, and validate merged datasets.
- **BI and stakeholder analytics:** Turn processed data into decision interfaces through Power BI dashboards, inspection views, performance tracking, and analytics-ready outputs.
- **RAG and document intelligence:** Extract structured data from inconsistent PDFs using retrieval, entity extraction, constrained generation, validation, and post-generation verification.
- **Distributed systems and blockchain infrastructure:** Design architectures where encryption, storage, verification, access control, incentives, and auditability have clear boundaries.

---

## How I Work

- Ambiguous workflow to structured system.
- Business logic to data model.
- Broken pipeline to diagnosed dependency and restored execution.
- Raw documents to validated datasets and stakeholder-usable analytics.
- Experimental architecture to controlled, auditable workflow.

I start by tracing how the business process actually works, then map the data dependencies that support it. I prefer systems that are explainable, testable, and usable by the people responsible for decisions.

---

## Links

- [LinkedIn](https://www.linkedin.com/in/cam-morreale99)
- [Wellington technical writeup](./wellington/technical-writeup.md)
- [Wellington project folder](./wellington/)
- [BoardGameGeek project folder](./bgg/)
- [Oasis project folder](./oasis/)

