---
title: "Module 3: Batch vs. Real-Time"
nav_order: 4
permalink: /module-3-batch-vs-real-time/
layout: default
---

# Module 3 — Batch vs. Real-Time, Demystified (3-4 hrs)

**What you'll learn:** The difference between scheduled batch jobs and continuous streaming, which one fits which business need, and the operational risks specific to real-time systems — what happens when a message gets processed twice, when a stream processor crashes and has to recover, or when data arrives later than expected.

**Why it matters:** Your product needs both — front-office pricing/risk wants near-real-time, back-office settlement and reporting is fine on a batch cycle. Knowing which is which prevents both over-spending on unnecessary real-time infrastructure and under-delivering on latency traders actually need. And once you do commit to real-time, the useful question shifts from "is it fast enough" to "what's the failure behavior" — that's what actually separates a lead who can evaluate a real-time pricing feed proposal from one who can't.

**Resources:**
- Blog (simplest, "photo vs. video" analogy): [Big Data 101: Dummy's Guide to Batch vs. Streaming Data — Precisely](https://www.precisely.com/blog/big-data/big-data-101-batch-process-streams/)
- Blog: [Real Time vs. Batch Processing vs. Stream Processing — BMC](https://www.bmc.com/blogs/batch-processing-stream-processing-real-time/)
- Blog: [Batch vs Stream Processing: When to Use Each and Why It Matters — DataCamp](https://www.datacamp.com/blog/batch-vs-stream-processing)
- Blog (delivery guarantees, and why they're genuinely hard): [What is Exactly-Once Delivery and Why It's So Hard to Achieve — Estuary](https://estuary.dev/blog/exactly-once-delivery/)

**Practical add-on:** When a vendor or engineer pitches you a real-time pipeline, ask three questions: what happens if a message is processed twice (at-least-once vs. exactly-once delivery), how does it recover if the stream processor crashes (checkpointing), and what happens to data that arrives after its expected window (late data handling). These aren't rare edge cases — they're the actual, everyday failure modes of real-time systems, and a serious vendor should have a clear answer for each.

---

[← Previous: Module 2](/module-2-where-the-data-comes-from/) · [Back to course overview](/) · [Next: Module 4 →](/module-4-the-business-layer/)
