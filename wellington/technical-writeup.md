# Wellington Management — Reverse-Engineering a $153B Investment Data Platform

## Overview

At Wellington Management, I reconstructed the application-level data architecture behind a Python-based investment decision platform supporting **$153B in insurance assets across 23 countries**, used by approximately **160 investment professionals globally**.

The platform was being migrated from a legacy Excel-driven workflow into a production decision system. The underlying Oracle data environment was undocumented at the application level, structurally opaque, and partially non-functional.

I reverse-engineered the data architecture by partnering with the primary stakeholder/PM to understand the Excel-based business logic, map spreadsheet functions to database fields and table patterns, decompose a large multi-nested SQL pipeline, diagnose a missing upstream table dependency, restore pipeline execution, and document the relational data model needed for the platform to function reliably.

---

## System Overview

<img width="750" height="500" alt="architecture" src="https://github.com/user-attachments/assets/23c612b6-2000-48d9-9e9a-f072d247d65d" />

*Reconstructed the data architecture behind a $153B investment decision platform, restored a blocked SQL pipeline, and supported an estimated ~$8.05M in annual workflow efficiency gains.*

---

## Technical Problem

The system’s data layer originated from spreadsheet-based business logic translated into a large, deeply nested SQL query.

The query contained multiple nested subqueries, joins, aggregations, and window functions, but it did not execute because one required upstream table dependency was unavailable. Because there was no usable application-level schema documentation, the team did not initially know whether the failure came from flawed SQL logic, missing source data, invalid join paths, incomplete table access, or misunderstood business rules.

Although the Oracle environment contained approximately **250 tables**, there was no reliable map of:

* Which tables were relevant to the application workflow
* How Excel functions and business rules mapped to database tables and fields
* How tables linked together through valid join paths
* What cardinalities existed between entities
* Which join types were required for downstream outputs
* Which fields drove calculations, filters, window functions, and aggregations
* How source data flowed through SQL transformations into the Python application layer

As a result, the platform’s data layer was structurally opaque. Core queries could not execute reliably until the application-level data architecture, dependencies, and lineage were reconstructed.

---

## Environment & Constraints

* **Database:** Oracle SQL
* **Application Layer:** Python, Pandas, ipywidgets
* **Source Workflow:** Legacy Excel-based investment workflow
* **Initial SQL Logic:** Large multi-nested query translated from Excel-based business logic
* **Primary Stakeholder:** Product manager responsible for the platform workflow and business requirements
* **Users:** Approximately 160 investment professionals
* **Business Scope:** $153B in insurance asset workflows across 23 countries
* **Primary Constraints:** No usable application-level schema documentation, unclear lineage, unknown table relevance, broken pipeline execution, missing upstream dependency

---

## My Role

* Partnered with the primary stakeholder/PM to understand the Excel-based business workflow, calculation logic, and output requirements
* Mapped spreadsheet functions and business rules to Oracle table names, fields, joins, and transformation patterns
* Reconstructed application-level data architecture across an undocumented Oracle environment with approximately 250 tables
* Reduced the working data scope from ~250 tables to approximately **25 core datasets** by mapping Excel logic to the data layer
* Mapped relevant tables, fields, joins, cardinalities, and transformation dependencies
* Decomposed a large nested SQL query into interpretable transformation layers
* Diagnosed and resolved a critical pipeline execution failure caused by a missing upstream table dependency
* Reconstructed the relational data model supporting downstream Python analytics
* Formalized system architecture, lineage, and data flow documentation

---

## Business-to-Data Layer Mapping

A central part of the work was translating stakeholder knowledge into a usable data architecture.

I met with the primary stakeholder/PM to understand what the legacy Excel workflow was doing: which spreadsheet functions mattered, how calculations were structured, what intermediate outputs meant, and how investment users interpreted the final results.

That business context became the key to narrowing the technical search space. Instead of treating the Oracle environment as 250 undifferentiated tables, I used the Excel workflow as a map for identifying likely data sources, relevant fields, table naming patterns, joins, and transformation dependencies.

This process involved:

* Translating spreadsheet functions into data requirements
* Mapping Excel-derived business concepts to Oracle table and field patterns
* Identifying which fields were likely to drive calculations, filters, aggregations, and outputs
* Comparing business terminology against database object names and column names
* Using stakeholder context to distinguish relevant tables from unrelated database objects
* Connecting business outputs back to upstream data dependencies

This business-to-data mapping reduced the working search space from approximately **250 Oracle tables** to approximately **25 core datasets** that appeared to drive the platform workflow.

---

## Reverse-Engineering the Data Architecture

To reconstruct the system, I combined stakeholder-driven business context with SQL decomposition and database inspection.

The core challenge was not simply writing SQL. It was translating business logic into data architecture: determining which tables mattered, how spreadsheet calculations mapped to Oracle objects, which fields controlled downstream outputs, which join paths were valid, what cardinalities existed between entities, and where the pipeline failure originated.

I approached the reverse-engineering process by:

* Eliciting business logic from the PM and translating spreadsheet behavior into data requirements
* Mapping Excel functions, intermediate calculations, and output fields to Oracle table and column patterns
* Breaking down nested SQL logic into smaller transformation layers
* Identifying implicit joins, filters, aggregations, and window-function logic
* Reducing scope from approximately 250 Oracle tables to approximately 25 core datasets
* Mapping primary-key and foreign-key patterns where explicit documentation was unavailable
* Inferring cardinalities between entities based on join behavior, field usage, and output requirements
* Tracing end-to-end data flow from source inputs through SQL transformations into Python analytics outputs

By aligning stakeholder knowledge, spreadsheet-derived calculations, SQL transformation logic, and Oracle metadata, I reconstructed the relational foundation required to support the platform’s analytics layer. This established a coherent map of system-wide data dependencies and made the previously opaque data environment interpretable.

---

## Pipeline Failure Diagnosis & Recovery

The initial SQL logic was delivered as one large, multi-nested query translated from Excel-based business logic. It included complex joins, aggregations, and window functions, but failed during execution because a required upstream table dependency was unavailable.

I diagnosed the failure by:

* Decomposing the nested SQL into interpretable transformation layers
* Tracing table dependencies across subqueries, joins, aggregations, and window functions
* Identifying the missing upstream dataset referenced by downstream logic
* Verifying the dependency gap through targeted Oracle SQL inspection queries
* Coordinating access restoration with the team

Once access was restored, the SQL pipeline executed successfully with minimal modification. This confirmed the failure originated from a missing data dependency rather than defective transformation logic.

This distinction mattered because it prevented unnecessary rewriting of valid SQL logic and redirected the recovery effort toward the actual system-level blocker: incomplete access to a required upstream dataset.

---

## Reconstructed Application-Level Data Architecture

With the missing dependency identified and pipeline execution restored, I reconstructed the application-level data architecture underlying the platform workflow.

The work centered on understanding how the existing Oracle environment functioned: how core tables connected, how SQL transformations depended on upstream datasets, how spreadsheet-derived business logic mapped to database objects, and how outputs fed the Python analytics layer.

I reconstructed the model by:

* Mapping inferred relationships between core Oracle tables
* Identifying primary-key and foreign-key patterns used by downstream SQL logic
* Documenting relevant fields, valid join paths, and observed cardinalities
* Linking source datasets, SQL transformations, and application-layer outputs
* Aligning the reconstructed model with the business logic inherited from Excel workflows

This moved the system from fragmented, spreadsheet-derived query logic toward a coherent, interpretable data architecture that developers and analysts could use to reason about downstream computation.

---

## Analytics Override Framework

To support investment decision-making, I co-engineered a controlled override framework that allowed users to adjust parameters without bypassing validation, traceability, or downstream calculation integrity.

* Implemented override functionality using **Python, Pandas, Oracle SQL, and ipywidgets**
* Enforced validation constraints on user inputs
* Preserved auditability of parameter modifications
* Integrated override logic into downstream calculations

This provided flexibility for investment users while maintaining the reliability and traceability of the data system.

---

## System Architecture & Documentation

To improve system clarity and maintainability, I formalized platform architecture and data flow documentation.

* Produced architecture diagrams for both legacy and production workflows
* Documented relevant tables, joins, dependencies, transformation layers, and pipeline structure
* Mapped interactions between the UI, Python application logic, SQL transformations, and Oracle data layer
* Created a shared reference point for developers, analysts, and stakeholders working on the platform

This documentation converted implicit institutional and spreadsheet-based logic into an explicit technical model of the platform.

---

## Business Impact

* Enabled a production-bound investment decision platform supporting **$153B in insurance asset workflows across 23 countries**
* Restored a critical SQL pipeline, unblocking core application functionality
* Supported reliable usage by approximately **160 investment professionals globally**
* Helped replace spreadsheet-based workflows with a structured decision system
* Contributed to approximately **$8.05M–$8.06M in estimated annual operational efficiency gains**, calculated as:

  * 160 users × 10 hours/week × 48 weeks × approximately $105/hour

---

## Technical Skills Demonstrated

* Application-level data architecture reconstruction
* Business-to-data layer mapping
* Stakeholder requirements translation
* Oracle SQL pipeline debugging
* Complex SQL decomposition across nested subqueries, joins, aggregations, and window functions
* Data lineage analysis and dependency tracing
* Relational data modeling under incomplete documentation
* Cardinality and join-path inference
* Business-logic translation from Excel workflows into SQL/Python analytics systems
* SQL-to-Python application integration
* Production workflow documentation under ambiguity

---

## Key Takeaway

This work followed a consistent engineering pattern:

* **Elicited** business logic from the primary stakeholder/PM
* **Mapped** Excel-based workflows to the Oracle data layer
* **Reduced** the technical search space from ~250 tables to ~25 core datasets
* **Reverse-engineered** an undocumented application-level data architecture
* **Decomposed** complex SQL translated from Excel business logic
* **Diagnosed** a missing upstream dependency blocking execution
* **Restored** critical pipeline functionality
* **Reconstructed** the relational data model and lineage required for reliable downstream analytics
* **Documented** the system architecture so future developers and analysts could understand the platform

The result was a transition from a non-functional, opaque data environment to a coherent, interpretable decision infrastructure capable of supporting real-world investment workflows.
