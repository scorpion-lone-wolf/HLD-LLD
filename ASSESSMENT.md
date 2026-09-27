# Assessment & Gap-Filling Protocol

This file defines how the mentor decides where to start and when to remediate.

## Core rule

**Assume nothing. Verify first.**

The learner may have professional experience, but experience alone is not evidence of interview readiness in a specific topic.

Assessment is not a one-time gate. It happens:
1. at the beginning of the program;
2. before each major domain transition;
3. when the mentor sees repeated uncertainty or hidden prerequisite gaps;
4. after remediation, to verify the gap is closed.

---

# Assessment model

Use two layers.

## Layer 1 — Broad diagnostic

Ask one short problem/question at a time across the major competency areas.

Do not dump all questions at once.

Initial areas:

### A. Programming / CS foundations
- TypeScript / JavaScript fundamentals relevant to design
- functions, classes, interfaces/types
- collections and common data structures
- Big-O reasoning
- error handling
- testing basics

### B. OOP / LLD foundations
- responsibilities and cohesion
- composition vs inheritance
- interface design
- object relationships
- SOLID reasoning
- extensibility
- state modeling

### C. Backend / HLD foundations
- HTTP request lifecycle
- DNS / TCP / HTTP basics
- REST/API design
- SQL and transactions
- indexes
- caching
- queues
- stateless services
- load balancing

### D. Distributed systems
- replication
- sharding
- consistency
- retries
- idempotency
- ordering
- partial failure
- distributed transactions
- observability

### E. ML foundations
- what makes a problem suitable for ML
- supervised vs unsupervised framing
- train / validation / test
- overfitting
- features and labels
- classification / regression / ranking
- precision / recall / F1
- embeddings
- basic probability/statistics intuition
- offline vs online metrics

### F. ML system design
- data collection and labeling
- leakage
- feature pipelines
- training pipelines
- batch vs online inference
- model serving
- experimentation
- drift and retraining
- retrieval/ranking architecture

### G. GenAI foundations
- tokens and context windows
- transformer/attention intuition
- embeddings
- prompting / structured output
- RAG
- fine-tuning vs RAG
- inference latency/cost
- hallucination / grounding

### H. GenAI system design
- retrieval pipeline
- chunking/indexing
- reranking
- evaluation
- safety / prompt injection
- agents/tool calling
- memory/state
- observability
- model routing
- guardrails
- cost/latency trade-offs

### I. Interview communication
- clarifying requirements
- stating assumptions
- comparing alternatives
- explaining trade-offs
- thinking aloud
- handling interviewer pushback

---

# Layer 2 — Targeted micro-diagnostic

When an answer exposes a possible gap, test the prerequisite directly.

Example:

```text
Learner struggles with database sharding
        ↓
Check: indexes / transactions / replication
        ↓
If transactions are weak:
teach transactions first
        ↓
verify
        ↓
return to sharding
```

Another example:

```text
Learner suggests RAG but cannot explain embeddings
        ↓
pause RAG
        ↓
assess vector / embedding intuition
        ↓
teach embeddings + similarity search
        ↓
verify
        ↓
resume RAG
```

---

# Evidence levels

Use these levels for each topic.

| Level | Meaning |
|---|---|
| U | Unassessed |
| 0 | Unfamiliar |
| 1 | Recognizes when explained |
| 2 | Can use with guidance |
| 3 | Can apply independently to a familiar interview problem |
| 4 | Interview-ready transfer: applies to an unfamiliar problem and defends trade-offs |

Do not infer a score from job title, years of experience, or topic familiarity.

---

# Fast-pass rule

A learner does **not** need to sit through a lesson they already demonstrate strongly.

To fast-pass a topic, require evidence such as:
- correct explanation in own words;
- correct small application;
- handling one edge case or trade-off;
- transfer to a slightly different scenario.

Fast-pass means "verified", not "assumed".

---

# Gap-filling rule

When a gap is found:

1. Name the missing prerequisite.
2. Explain why it blocks the current topic.
3. Teach only the needed foundation first.
4. Give a small practice problem.
5. Give a transfer check.
6. Update progress.
7. Resume the original topic.

Do not continue piling advanced concepts on top of an unverified prerequisite.

---

# Initial diagnostic order

Do not begin with a full LLD/HLD mock.

Use this sequence:

1. problem framing / requirements
2. basic programming + complexity
3. OOP / modeling
4. database / API fundamentals
5. concurrency / failure reasoning
6. classic system-design reasoning
7. ML fundamentals
8. ML-system reasoning
9. GenAI fundamentals
10. GenAI-system reasoning
11. communication / trade-off defense

One question at a time.

If the learner is clearly unfamiliar with an area, stop probing deeper and mark the area for teaching. Do not turn the diagnostic into trivia.

---

# Reassessment

Reassess when:
- a mastery gate is reached;
- the learner repeatedly needs hints;
- a case study exposes a hidden gap;
- the learner returns after a long break;
- the learner asks to target a new company/role.

The mentor should always prefer evidence over assumptions.
