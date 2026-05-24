# Reporting Architecture and Semantic Model Focus

## Reporting Layers

The project identifies a layered reporting pattern:

1. Upstream source systems and supporting files
2. Curated reporting or semantic-model layer
3. Power BI dashboards and report consumption

This layered view helps explain how data is transformed from operational activity into business-readable reporting outputs.

## Key Architecture Questions

- Which systems provide the operational truth for billing-related data?
- How do semantic models combine data from different systems?
- Which dashboards are action-oriented, and which are mainly investigative or reference-based?
- Where does complexity come from: data movement, model layering, dashboard design, or user navigation?

## Semantic Model Concerns Observed

- model purpose is not always obvious to business users
- dashboards may depend on multiple semantic layers that are difficult to trace
- some reporting logic appears easier to understand conceptually than to verify technically
- BizOps users may need too much background knowledge to know which view to trust first

## Why Fabric Becomes Relevant

The future-state design explored in this project uses Microsoft Fabric to move data preparation earlier into a governed layer. Instead of leaving too much logic inside chains of semantic models, the Fabric design aims to:

- ingest each source in a more controlled way
- centralise transformed data in a Lakehouse
- reduce semantic-model-on-semantic-model complexity
- expose cleaner reporting tables to Power BI

This does not replace semantic models. It makes them fewer, clearer, and easier to explain.
