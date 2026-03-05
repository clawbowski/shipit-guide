# Ship It: Building LLM-Powered Search in Production
## Product Outline — Draft 1

**Subtitle:** The architecture, patterns, and hard-won lessons for shipping AI search that actually works

**Target reader:** Backend/ML engineers at startups building AI products who are struggling to go from "demo works" to "this runs in production."

**Core promise:** Save 6–12 months of painful trial and error by learning what a senior eng who shipped LLM search at Dropbox scale figured out the hard way.

---

## Part 1: The Foundation Nobody Talks About

### Chapter 1: Why LLM Search Is Different
- The illusion of "just call the API"
- Why semantic search breaks down in production (and how to prevent it)
- The three failure modes: relevance, latency, cost

### Chapter 2: Data Source Architecture
- Heterogeneous data: the real problem
- Designing abstraction layers so new data types don't require service changes
- Schema design for searchable AI content
- Chunking strategies that actually work

### Chapter 3: The Authorization Problem
- ACL filtering at query time vs. index time — tradeoffs
- Building a reusable auth library instead of bespoke per-source hacks
- The patterns that scale; the ones that blow up

---

## Part 2: The Query Layer

### Chapter 4: Query Semantics That Don't Suck
- Boolean query composition — why bespoke filter logic is a trap
- Building a composable query interface reused across product teams
- Handling hybrid search (semantic + keyword) cleanly

### Chapter 5: Retrieval Strategies
- When to use vector search, BM25, or both
- Re-ranking: when it helps, when it's overkill
- Metadata stores for offloading index traffic (latency + cost wins)

### Chapter 6: LLM Integration Patterns
- RAG done right vs. RAG done naively
- Prompt architecture for search result synthesis
- Streaming responses without making your backend a mess

---

## Part 3: Making It Production-Ready

### Chapter 7: Observability for AI Search
- What to measure (hint: not just latency)
- Relevance metrics you can actually track
- Logging for debugging retrieval failures

### Chapter 8: Cost Control
- The billing surprises nobody warns you about
- Caching strategies for LLM calls
- When to use smaller models for parts of the pipeline

### Chapter 9: API Design for AI Products
- Versioning AI endpoints (harder than it sounds)
- Documentation standards that help other teams integrate
- Designing for testability from day one

---

## Part 4: The Operational Reality

### Chapter 10: On-Call for AI Services
- Incident patterns unique to LLM-powered systems
- Runbooks that actually help during outages
- Systematic improvement vs. whack-a-mole

### Chapter 11: Testing Strategies
- Unit testing search pipelines
- Integration testing with live vs. mock LLMs
- Evaluation sets and how to build them

### Chapter 12: Scaling Up
- When your architecture needs to change
- Multi-tenancy challenges
- Lessons from 0→1 to production traffic

---

## Appendices
- A: Reference architecture diagram (annotated)
- B: Code templates (Go + Python)
- C: Vendor comparison matrix (embedding models, vector DBs)
- D: Checklist: "Is my search production-ready?"

---

**Estimated length:** 80–120 pages
**Format:** PDF + code repo with templates
**Price point:** $79 early bird / $97 regular
**Upsell:** Monthly community/Q&A tier at $19/mo
