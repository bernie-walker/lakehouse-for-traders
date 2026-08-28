---
title: "Module 4: The Business Layer"
nav_order: 5
permalink: /module-4-the-business-layer/
layout: default
---

# Module 4 — The Business Layer: Turning Raw Data Into Something Traders Trust (4-5 hrs)

**What you'll learn:** How raw feeds get organized into "facts" (things that happened — trades, prices) and "dimensions" (context — instrument, counterparty, desk), what "single source of truth" / "golden source" means in practice, and the data quality checks that actually earn that trust — completeness, accuracy, timeliness, and consistency.

**Why it matters:** This is the core of what you're building — the layer front-office traders actually query. Getting this modeled well is the difference between a dashboard people trust and one they double-check against Excel. "Trust" isn't just the model being right on day one, either — it's knowing what quality checks run on the data and what happens when one fails, and it's whether the resulting dashboards and reports are something traders actually adopt, rather than quietly rebuilding in a spreadsheet because they don't trust or can't make sense of what they're given.

**Resources:**
- Blog (clearest intro to facts/dimensions): [Dimensional Modeling: Facts, Dimensions, and Grains — DEV Community](https://dev.to/alexmercedcoder/dimensional-modeling-facts-dimensions-and-grains-3obm)
- Blog: [A Complete Guide to Dimensional Modeling — dbt Labs](https://www.getdbt.com/blog/guide-to-dimensional-modeling)
- Reference: [Single Source of Truth — Wikipedia](https://en.wikipedia.org/wiki/Single_source_of_truth)
- Blog (the raw→refined pattern most lakehouses use): [What is Medallion Architecture? — Databricks](https://www.databricks.com/blog/what-is-medallion-architecture)
- Blog (what "trustworthy data" actually breaks down into): [What Are Data Quality Dimensions? — IBM](https://www.ibm.com/think/topics/data-quality-dimensions)
- Blog (treating the output as something people adopt, not just correct data): [What Is Data as a Product (DaaP)? — IBM](https://www.ibm.com/think/topics/data-as-a-product)

---

[← Previous: Module 3](/module-3-batch-vs-real-time/) · [Back to course overview](/) · [Next: Module 5 →](/module-5-back-office-and-recalibration/)
