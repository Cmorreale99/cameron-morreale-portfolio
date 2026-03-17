# Wellington Management — Data Architecture & Pipeline Recovery

---

## Overview

At Wellington Management, I reconstructed the data foundation of a Python-based investment decision platform supporting **$153B in insurance assets across 23 countries**, used by ~160 investment professionals.

The platform was being migrated from a legacy Excel-driven workflow into a production system. The underlying data environment was undocumented, structurally opaque, and partially non-functional.

I reverse-engineered the data architecture, diagnosed and restored a critical SQL pipeline failure, and engineered a coherent data model that enabled the platform to function as a production decision system.

---

## System Overview

<img width="750" height="500" alt="architecture" src="https://github.com/user-attachments/assets/23c612b6-2000-48d9-9e9a-f072d247d65d" />

*Reconstructed a broken data architecture and restored pipeline execution for a $153B investment platform, enabling ~$8.05M in annual efficiency gains.*

---

## Problem

The system’s data layer originated from spreadsheet-based logic translated into SQL without a formal schema or documentation.

This resulted in:

* An Oracle database (~250 tables) with **no defined schema or relational structure**
* A **non-functional SQL pipeline** due to missing upstream dependencies
* Business logic embedded in spreadsheets, obscuring data lineage
* No explicit mapping between source data, transformations, and outputs

The application could not execute core queries until the data architecture and dependencies were reconstructed.

---

## Environment & Constraints

* **Database:** Oracle SQL
* **Application Layer:** Python (Pandas, ipywidgets)
* **Users:** ~160 investment professionals
* **Scope:** $153B in insurance asset workflows
* **Constraints:** No documentation, unclear lineage, broken pipeline

---

## My Role

* Reverse-engineered an undocumented Oracle database (~250 tables)
* Mapped and reconstructed critical data dependencies (~25 core tables)
* Diagnosed and resolved pipeline execution failure
* Designed a relational data model supporting application-layer analytics
* Formalized system architecture and data flow documentation

---

## Reverse-Engineering the Data Architecture

To reconstruct the system, I decomposed SQL logic derived from Excel workflows and analyzed query structures to infer the true organization of the data layer.

* Identified implicit joins, transformations, and aggregation logic embedded in SQL
* Reduced scope from ~250 tables to ~25 core datasets driving business outputs
* Mapped primary and foreign key relationships across datasets
* Traced end-to-end data flow from source inputs to final outputs

By aligning database structure with spreadsheet-derived calculations, I reconstructed the relational foundation required to support the platform’s analytics layer. This established the first coherent map of system-wide data dependencies.

---

## Pipeline Failure Diagnosis & Recovery

A critical SQL pipeline failed to execute, blocking generation of required datasets.

I diagnosed the failure by:

* Tracing execution dependencies across SQL transformations
* Identifying a **missing upstream dataset** referenced in downstream logic
* Verifying the dependency gap through targeted SQL inspection queries
* Coordinating access restoration with the team

Once access was restored, the pipeline executed successfully with minimal modification, confirming the failure originated from missing data dependencies rather than flawed transformation logic.

---

## Relational Schema Construction

With dependencies identified and the pipeline restored, I designed a structured relational schema aligned with the reconstructed data architecture.

* Defined relationships between core datasets identified during reverse-engineering
* Structured SQL transformations to align with the inferred schema
* Ensured consistency between database outputs and application-layer analytics

This enabled the transition from fragmented query logic to a **coherent, interpretable data model** supporting reliable downstream computation.

---

## Analytics Override Framework

To support investment decision-making, I co-engineered a controlled override system enabling parameter adjustments while preserving system integrity.

* Implemented override functionality using **Python (Pandas), Oracle SQL, and ipywidgets**
* Enforced validation constraints on user inputs
* Ensured auditability of parameter modifications
* Integrated override logic into downstream calculations

This provided flexibility for users while maintaining the reliability and traceability of the data system.

---

## System Architecture & Documentation

To improve system clarity and maintainability, I formalized platform architecture and data flow documentation.

* Produced architecture diagrams for both legacy and production workflows
* Documented data dependencies, transformation layers, and pipeline structure
* Mapped interactions between UI, application logic, and data layer

This established a shared system understanding and enabled more efficient development and onboarding.

---

## Business Impact

* Enabled a production platform supporting **$153B in insurance assets**

* Restored a **critical pipeline**, unblocking core application functionality

* Supported reliable usage by **~160 investment professionals globally**

* Replaced spreadsheet-based workflows with a structured decision system

* Contributed to approximately **$8.05M–$8.06M in annual operational efficiency gains**, calculated as:

  * 160 users × 10 hours/week × 48 weeks × ~$105/hour

---

## Technical Skills Demonstrated

* Data modeling and schema reconstruction
* SQL pipeline debugging and dependency tracing
* Reverse-engineering undocumented systems
* Data lineage analysis and validation
* Integration of SQL and Python analytics workflows
* Designing production-grade systems under ambiguity

---

## Key Takeaway

This work followed a consistent engineering pattern:

* **Reverse-engineered** an undocumented system
* **Diagnosed** a critical failure blocking execution
* **Reconstructed** the data architecture and dependencies
* **Engineered** a reliable foundation for production use

The result was a transition from a non-functional, opaque data environment to a structured, interpretable system capable of supporting real-world investment decision workflows.

