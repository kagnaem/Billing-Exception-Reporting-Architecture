# Reporting Architecture and Modelling Focus

## Enterprise Reporting Context

The project is based on a large telecom-style reporting environment where billing and exception reporting depends on multiple platforms working together. The main source domains include:

- CRM for customer and commercial context
- ServiceNow for service and operational context
- Datagate for billing and usage-related billing logic
- SAP for invoice and finance outputs
- SharePoint and file-based sources for extracts, mappings, and reference inputs
- additional API or supplier-side feeds where relevant

## Architecture Pattern

The architecture follows a layered design:

1. Upstream source systems and file-based inputs
2. Fabric ingestion and orchestration layer
3. Lakehouse storage and reusable transformed data
4. Power BI transformation, modelling, and semantic reporting layer
5. Billing and exception reporting outputs

This layered view makes the reporting flow easier to govern and easier to explain than a purely dashboard-centric design.

## Why Fabric Becomes Central

Microsoft Fabric is used here not just as a reporting host, but as the core integration and preparation layer. In this design it is responsible for:

- orchestrating ingestion from multiple platforms
- supporting Dataflow Gen2 for source-specific extraction and transformation
- centralising reusable data in a Lakehouse
- creating a more controlled handoff into Power BI modelling

## Power BI Modelling Role

Power BI remains an important part of the architecture, but its role becomes more focused. Instead of carrying too much multi-source transformation inside individual reports, Power BI is used to:

- connect to curated Fabric outputs
- apply lighter reporting transformations where needed
- model fact and dimension relationships across multiple source systems
- support billing and exception reporting through clearer import-mode models

## Design Goal

The design goal is to improve traceability from ingestion to reporting so that billing and exception reports are built on a more understandable and reusable data foundation.
