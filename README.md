# Cameron Morreale — Data Engineering Portfolio

Building financial data systems, repairing broken pipelines, and transforming complex, undocumented data environments into scalable decision infrastructure.

![Python](https://img.shields.io/badge/Python-Data%20Engineering-blue)
![SQL](https://img.shields.io/badge/SQL-Advanced-green)
![Oracle](https://img.shields.io/badge/Database-Oracle-red)
![AWS](https://img.shields.io/badge/AWS-Lambda-orange)
![Focus](https://img.shields.io/badge/Focus-Financial%20Data%20Systems-black)

Data Engineer specializing in **financial data systems, data architecture, and pipeline reconstruction**, with experience restoring production-critical pipelines and enabling decision systems in complex, undocumented environments.

**MS Data Science — Worcester Polytechnic Institute**
**Wellington Management — Data Engineering / Data Architecture**

📎 [LinkedIn](https://www.linkedin.com/in/cam-morreale99)

---

## 🧠 Core Focus

* Data Architecture & Schema Reconstruction
* SQL Pipeline Debugging & Recovery
* Scalable Data Ingestion (Async / API-driven systems)
* Financial Data Systems & Investment Workflows
* End-to-End Data → Decision Infrastructure

---

## 🔥 Professional Work

**Flagship Project — Reconstructed a broken data architecture and restored pipeline execution for a $153B investment platform (~$8.06M annual impact)**

### Wellington Management — Data Engineering & Data Architecture Intern

*June 2025 – August 2025 | Boston, MA*

Reconstructed the data architecture powering a **$153B investment decision platform** used by ~160 investment professionals across 23 countries, enabling migration from a legacy Excel workflow to a production Python system.

#### Key Contributions

* Reverse-engineered an **undocumented Oracle database (~250 tables)** to identify relational structure, key datasets, and data dependencies
* Diagnosed a **critical SQL pipeline failure** by tracing execution dependencies and identifying a missing upstream dataset
* Restored **end-to-end pipeline execution**, enabling development of the production decision platform
* Reconstructed the **relational schema supporting analytics workflows**, aligning SQL transformations with the underlying data model
* Co-engineered an **analytics override framework** enabling controlled parameter adjustments with validation and auditability

#### Impact

* Supported a platform associated with **$8.06M in annual operational efficiency gains**
* Replaced spreadsheet-driven workflows with structured, production-grade data pipelines
* Established a coherent map of system-wide data dependencies

📄 [Full Technical Writeup](./wellington/technical-writeup.md)

---

## ⚙️ Projects

### BoardGameGeek Data Platform

**Async Data Pipeline + Relational Modeling for Marketplace & Ratings Data**

End-to-end system integrating **asynchronous data ingestion, relational modeling, and transaction workflows** across a full-stack architecture.

#### Data Engineering

* Developed an **async Python ELT pipeline (aiohttp)** to collect marketplace data for ~150 games
* Implemented **rate-limit handling, retry logic, and concurrent execution** to ensure reliable ingestion
* Structured preprocessing workflows for **data cleaning, normalization, and schema alignment**
* Reindexed ranking systems and validated data integrity across merged datasets

#### Data Modeling

* Designed a **recursive relational schema** to represent game reimplementations
* Generated preprocessing pipelines to produce **parent–child entity relationships**

#### Backend + Frontend

* Engineered an **AWS Lambda serverless function** for account balance updates
* Built a React-based checkout workflow with cart state management, validation, and transaction handling

📄 [Full Technical Writeup](./bgg/technical-writeup.md)

---

## 📊 Research

### Quantitative Market Modeling — WPI IQP

**Trading Strategy Development & Performance Evaluation**

Developed and evaluated trading strategies using live simulation environments.

* Speculative strategy: **+24.73% return**
* Fundamentals-driven strategy: **+9.20% return**
* Benchmark (S&P 500): **+1.36%**

Demonstrates applied understanding of market behavior, risk management, and strategy evaluation.

📄 [Co-Authored Paper](./research/quantitative-market-modeling.pdf)

---

### Decentralized IoT Data Architecture — WPI MQP (Embue)

**Secure, Verifiable Data Pipelines using Blockchain + ML**

Designed and implemented system architecture for **secure, verifiable IoT data pipelines** combining blockchain and machine learning.

* Implemented **GnuPG encryption workflows**
* Integrated **IPFS + Filecoin** for decentralized storage
* Designed architecture for **immutable, timestamped data verification**

📄 [Co-Authored Paper](./research/decentralized-iot-architecture.pdf)

---

## 🧠 How I Think

### Debugging Approach

* Trace systems **end-to-end before modifying components**
* Identify **upstream dependencies first**
* Validate assumptions against actual data behavior

### System Design Philosophy

* Data integrity > short-term convenience
* Prefer **simple, explainable architectures**
* Build for **observability and failure detection**

### Engineering Principles

* Schema clarity is foundational to reliable systems
* Pipelines should be reproducible and auditable
* Most failures originate from **hidden data dependencies**

---

## 🎯 Career Focus

Targeting roles in:

* Data Engineering (Finance / Asset Management)
* Data Infrastructure & Platform Engineering
* Financial Data Systems & Decision Platforms

