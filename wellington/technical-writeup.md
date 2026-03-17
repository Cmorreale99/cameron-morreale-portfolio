# Wellington Management — Data Architecture & Pipeline Recovery

## Overview

At Wellington Management, I rebuilt the data foundation of a Python-based investment decision platform supporting ~$153B in insurance assets across 23 countries, used by ~160 investment professionals. The platform was being migrated from a legacy Excel-driven workflow into a production system.

The underlying data environment was undocumented, structurally opaque, and partially non-functional. I reverse-engineered the data architecture, restored a broken SQL pipeline, and established a reliable data model that enabled the application to function as a production decision system.

---

## Problem

The system’s data layer originated from spreadsheet-based logic translated into SQL without a formal schema or documentation.

This resulted in:

- An Oracle database (~250 tables) with **no defined schema or relational structure**
- A **non-functional SQL pipeline** due to missing upstream dependencies  
- Business logic embedded in spreadsheets, obscuring data lineage  
- No clear mapping between source data, transformations, and outputs  

The application could not execute core queries until the data architecture and dependencies were reconstructed.

---

## Environment & Constraints

- **Database:** Oracle SQL  
- **Application Layer:** Python (Pandas, ipywidgets)  
- **Users:** ~160 investment professionals  
- **Scope:** $153B in insurance asset workflows  
- **Constraints:** No documentation, unclear lineage, broken pipeline  

---

## My Role

- Reverse-engineered an undocumented Oracle database (~250 tables)  
- Identified and reconstructed critical data dependencies (~25 core tables)  
- Diagnosed and resolved pipeline execution failure  
- Rebuilt a usable data model supporting application-layer analytics  
- Documented system architecture and data flow  

---

## Reverse-Engineering the Data Architecture

To reconstruct the system, I:

1. **Decomposed SQL logic derived from Excel workflows**
   - Analyzed query structure and referenced tables  
   - Identified implicit join patterns and transformation logic  

2. **Identified core datasets**
   - Reduced scope from ~250 tables to ~25 key tables  
   - Prioritized datasets driving critical business outputs  

3. **Reconstructed schema relationships**
   - Inferred primary and foreign key relationships  
   - Mapped dependencies across transformations  

4. **Rebuilt data lineage**
   - Traced end-to-end data flow from source inputs to final outputs  
   - Aligned SQL outputs with financial metrics used by investment professionals  

This process transformed an unstructured database into a **coherent, production-usable data model**.

---

## Pipeline Failure Diagnosis & Recovery

A critical SQL pipeline failed to execute, blocking the application from generating required datasets.

I:

- Traced query execution dependencies step-by-step  
- Identified a **missing upstream dataset** referenced in SQL logic  
- Confirmed the dependency gap through targeted SQL inspection queries  
- Escalated the issue and worked with the team to obtain access  

Once access was restored, the pipeline executed successfully with minimal changes, re-enabling the full data workflow.

---

## Analytics Override Framework

To support investment decision-making, I co-engineered a controlled override system allowing users to adjust model inputs while maintaining integrity.

- Built override functionality using **Python (Pandas), Oracle SQL, and ipywidgets**  
- Enforced validation constraints on user inputs  
- Ensured auditability of all modifications  
- Integrated overrides into downstream calculations  

This enabled flexible analysis without compromising the reliability of the underlying data system.

---

## System Architecture & Documentation

I developed system-level documentation to clarify the platform structure:

- Created architecture diagrams for both the legacy Excel workflow and new system  
- Documented data dependencies, transformations, and pipeline structure  
- Mapped interactions between UI, application logic, and data layer  

This established a foundation for maintainability and future development.

---

## Business Impact

- Enabled a production platform supporting **~$153B in insurance assets**  
- Restored a **critical broken pipeline**, unblocking application functionality  
- Enabled reliable usage by **~160 investment professionals globally**  
- Replaced manual Excel workflows with a structured application system  

- Drove approximately **$8M in annual operational efficiency gains**, calculated as:  
  - 160 users × 10 hours/week × 48 weeks × ~$105/hour average compensation

---

## Technical Skills Demonstrated

- Data modeling and schema reconstruction  
- SQL pipeline debugging and dependency tracing  
- Reverse-engineering undocumented systems  
- Data lineage analysis  
- Integration of SQL and Python analytics workflows  
- Building production-grade data systems under ambiguity  

---
