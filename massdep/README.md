# MassDEP — Document Intelligence & Analytics System

## Overview

Built an AI-assisted document intelligence pipeline for environmental construction reports, converting unstructured PDF/report content into structured datasets ready for analytics and Power BI reporting.

Designed a multi-stage extraction and validation workflow to identify key environmental reporting fields such as PFAS metrics, shipment quantities, site conditions, and project-level details across inconsistent report formats.

**Impact: ~40% reduction in manual reporting effort across 50+ projects, with ~97% extraction success through page-level validation and failure detection.**

---

## Key Contributions

- Built an **LLM-driven extraction pipeline** to convert unstructured environmental construction reports into structured tabular outputs  
- Designed a **generator/discriminator validation architecture** to reduce hallucinations and improve extraction reliability  
- Used a generator model to produce structured outputs from report pages and a discriminator model to validate semantic consistency  
- Implemented **page-level validation** to detect unreadable pages, incomplete extractions, and failure states  
- Structured outputs into **CSV / analytics-ready datasets** for downstream reporting and dashboard integration  
- Designed the pipeline around **Power BI-ready data outputs**, enabling scalable reporting across environmental project data  
- Extracted and organized fields such as **PFAS metrics, shipment quantities, site conditions, project identifiers, and reporting attributes**  
- Reduced manual review burden by automating repetitive document interpretation and data structuring workflows  

---

## Business Impact

- Reduced manual environmental reporting effort by approximately **40%**  
- Supported scalable analysis across **50+ environmental construction projects**  
- Achieved approximately **97% extraction success** using page-level validation and failure handling  
- Converted inconsistent report formats into structured datasets usable for analytics and stakeholder reporting  
- Improved transparency by surfacing unreadable pages, extraction gaps, and validation failures rather than silently producing unreliable outputs  
- Enabled environmental project data to move from manual document review toward repeatable analytics infrastructure  

---

## Tech Stack

- **AI / NLP:** LLM-based extraction, semantic validation, entailment-style verification  
- **Python:** Data processing, extraction orchestration, validation workflows  
- **Data Outputs:** CSV, structured tabular datasets, Power BI-ready outputs  
- **Analytics:** Power BI integration pathway  
- **Focus Areas:** Document intelligence, unstructured data extraction, validation, data quality, reporting automation  

---

## Deep Dive

➡️ [Read Full Technical Writeup](./technical-writeup.md)

---

## Navigation

⬅️ [Back to Portfolio Home](../README.md)
