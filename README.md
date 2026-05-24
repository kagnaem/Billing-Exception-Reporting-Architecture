# Billing Exception Reporting Architecture

An anonymized portfolio project based on enterprise-style billing, exception reporting, semantic model review, and Microsoft Fabric architecture design.

## Overview

This project documents how a complex billing and exception reporting environment can be understood, reviewed, and redesigned in a more structured way. It focuses on the relationship between upstream operational systems, semantic models, Power BI dashboards, and a trial future-state architecture in Microsoft Fabric.

The work is presented in anonymized form to protect organisational privacy while still showing the analytical approach, documentation methods, and architecture thinking used in the project.

## Project Focus

- reporting architecture review across Power BI, semantic models, and Microsoft Fabric
- end-to-end data flow mapping from upstream systems into billing reports
- dashboard navigation and semantic model mapping
- scenario-based exception and revenue leakage analysis
- trial Fabric architecture using Dataflow Gen2, Lakehouse storage, and Power BI star-schema modelling

## What This Project Covers

### 1. Reporting Architecture Review
- mapped the relationship between SharePoint, semantic models, OneLake/Fabric, and the Billing Reports app
- documented how the reporting environment is structured and where dashboard complexity creates user friction

### 2. Semantic Model and Dashboard Analysis
- reviewed how dashboard navigation connects users to reports, files, systems, and semantic models
- documented model purpose, likely lineage, and areas where interpretation becomes difficult for BizOps users

### 3. Billing and Exception Scenarios
- created realistic operating scenarios that show when key dashboards are used
- explained how billing changes, Datagate exceptions, and supplier reconciliation support investigation and revenue assurance

### 4. Future-State Fabric Design
- designed a trial architecture using one Dataflow Gen2 per source system
- centralised transformed outputs in a Lakehouse
- proposed Power BI consumption through Import mode and star-schema modelling

## Portfolio-Safe Deliverables

- architecture diagrams
- end-to-end data flow diagrams
- dashboard and semantic model review documents
- scenario-based process flows
- trial Fabric architecture notes

## Tools and Platforms

- Microsoft Fabric
- OneLake
- Power BI
- Dataflow Gen2
- Power BI semantic models
- SharePoint
- Dataverse
- API and file-based source integration

## Privacy Note

This repository is intentionally anonymized. System names, dashboard examples, and reporting flows have been simplified where needed to protect organisational confidentiality while preserving the analytical and architecture design approach.

## Repository Structure

- [`docs/project-summary.md`](docs/project-summary.md) - high-level project summary
- [`docs/reporting-architecture.md`](docs/reporting-architecture.md) - architecture and semantic model focus
- [`docs/scenario-driven-reporting.md`](docs/scenario-driven-reporting.md) - practical billing and exception scenarios
- [`assets/`](assets/) - supporting diagrams for the portfolio version
