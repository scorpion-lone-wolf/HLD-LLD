# Unified Design Interview Curriculum

This is the single canonical learning path for:
- Object-Oriented / Low-Level Design (OOD / LLD)
- classic High-Level / Distributed System Design (HLD)
- Machine Learning System Design
- Generative AI / LLM System Design

It is intentionally **one sequence**, not four separate courses.

The order is prerequisite-based: software design foundations first, then distributed systems, then ML systems, then GenAI systems. Later topics reuse earlier ones.

---

# How to use this curriculum

For every topic:

1. Why it matters in interviews
2. Core explanation
3. Example / diagram
4. Learner attempt
5. Feedback
6. Transfer question
7. Notion-ready notes
8. Mastery check
9. Update progress and exact resume point

## Advancement rule

Do not move forward because a topic was read.

Move forward only when the learner can explain or apply the idea with reasonable independence.

---

# PHASE 0 — Interview Operating System

## 0.1 The four design interview families

Understand the distinction and overlap between:

- OOD / LLD: objects, responsibilities, contracts, code quality, extensibility
- Classic HLD: APIs, data model, scale, storage, distributed systems, reliability
- ML System Design: classic HLD + data, features, model, offline/online evaluation, serving, drift
- GenAI System Design: classic HLD + LLM/RAG/agents, retrieval, evaluation, safety, latency/cost

## 0.2 Requirements and scope

Learn:
- functional requirements
- non-functional requirements
- constraints
- assumptions
- success criteria
- examples and edge cases
- scope negotiation

## 0.3 Communication

Practice:
- think aloud
- state assumptions
- compare alternatives
- make a decision and defend it
- invite interviewer clarification
- avoid premature technology selection

## 0.4 Universal design framework

### LLD
`requirements → entities → responsibilities → relationships → contracts → flow → code → tests → extensibility`

### Classic HLD
`requirements → NFRs → scale → API → data model → simple architecture → bottlenecks → reliability → observability → trade-offs`

### ML
`requirements → ML framing → metrics → data → features/representations → model → offline eval → serving → online eval → monitoring/retraining`

### GenAI
`requirements → task framing → data/knowledge → model/RAG/agent choice → evaluation → architecture → serving → safety → monitoring/cost`

### Mastery gate
Given a vague prompt, the learner clarifies before proposing architecture/model/code.

---

# PHASE 1 — Software Modeling Foundations

## 1.1 OOP for design
- encapsulation
- abstraction
- composition vs inheritance
- polymorphism
- interfaces/contracts

## 1.2 Object relationships
- association
- aggregation
- composition
- multiplicity/cardinality
- lifecycle ownership

## 1.3 SOLID in practice
Prioritize:
- SRP
- OCP
- DIP
Then:
- LSP
- ISP

Use refactoring exercises rather than definition memorization.

## 1.4 TypeScript design mechanics
- interfaces
- abstract classes
- dependency injection
- error types
- immutable/value objects where useful
- modules/packages
- domain vs infrastructure boundaries

## 1.5 Testability
- unit-testable services
- dependency boundaries
- deterministic logic
- fakes/mocks/stubs
- test behavior rather than implementation

### Mastery gate
Model a small domain and implement clean, testable TypeScript without forcing design patterns.

---

# PHASE 2 — Design Patterns as Tools

Learn patterns only by the problem they solve.

## 2.1 Strategy
Vary behavior independently.

## 2.2 Factory
Separate creation from use.

## 2.3 Observer / Pub-Sub
Notify multiple interested consumers.

## 2.4 State
Behavior changes with lifecycle/state.

## 2.5 Adapter
Integrate incompatible interfaces.

## 2.6 Decorator
Add behavior without rewriting the wrapped object.

## 2.7 Command
Represent operations/actions explicitly.

## 2.8 Chain of Responsibility
Pass a request through ordered handlers.

### Deferred unless a real problem needs them
- Prototype
- Visitor
- Abstract Factory as a memorization topic

### Mastery gate
Given a design change, decide whether a pattern helps and explain the trade-off.

---

# PHASE 3 — LLD Engineering Depth

## 3.1 Validation and error handling
## 3.2 Extensibility under new requirements
## 3.3 Persistence boundaries
## 3.4 API/schema thinking in LLD
## 3.5 Concurrency and race conditions
## 3.6 Idempotency
## 3.7 Complexity of key operations
## 3.8 Runnable code + focused tests

### Mastery gate
Implement a working solution, test it, and adapt it when the interviewer changes a requirement.

---

# PHASE 4 — OOD / LLD Case-Study Ladder

The following includes every publicly listed case-study title from ByteByteGo's Object-Oriented Design Interview course, plus selected open-source supplements.

## Tier A — first modeling problems
1. Parking Lot
2. Vending Machine
3. Tic-Tac-Toe
4. Blackjack / Deck of Cards
5. Unix File Search

## Tier B — state, workflows, and integrations
6. Movie Ticket Booking
7. Elevator
8. Shipping Locker
9. ATM
10. Grocery Store
11. Restaurant Management

## Supplemental public OOD problems
12. LRU Cache
13. Hash Map
14. Call Center
15. Chat Server
16. Notification System
17. Splitwise / Expense Sharing
18. Logging Framework
19. Library Management
20. Task Scheduler
21. Food Ordering / Restaurant Assignment
22. Ride Sharing core classes
23. Wallet / BNPL core classes
24. In-memory Order Matching Engine

### LLD readiness gate
Solve a fresh medium LLD prompt with runnable TypeScript, tests, edge cases, and one interviewer curveball.

---

# PHASE 5 — Classic System Design Foundations

## 5.1 Scale from one server to many
- stateless application servers
- horizontal vs vertical scaling
- load balancers

## 5.2 Back-of-the-envelope estimation
- users
- QPS
- peak QPS
- storage
- bandwidth
- memory/cache sizing

## 5.3 Networking
- DNS
- TCP basics
- HTTP/HTTPS
- REST
- WebSocket
- gRPC when appropriate

## 5.4 API design
- resources
- pagination
- idempotency
- versioning
- error contracts

## 5.5 Data modeling
- access-pattern-first design
- SQL vs NoSQL
- normalization / denormalization
- indexes
- transactions

## 5.6 Caching
- cache-aside
- write-through / write-back concepts
- TTL
- invalidation
- eviction
- hot keys

## 5.7 Replication
## 5.8 Partitioning / sharding
## 5.9 Consistent hashing
## 5.10 Unique ID generation
## 5.11 Object/blob storage and CDN
## 5.12 Search / indexing basics

### Mastery gate
Turn requirements into API + data model + a simple architecture before adding distributed-system complexity.

---

# PHASE 6 — Distributed Systems and Production Reliability

## 6.1 Queues and pub-sub
## 6.2 At-most-once / at-least-once / effectively-once
## 6.3 Ordering
## 6.4 Retries and exponential backoff
## 6.5 Idempotency
## 6.6 Distributed transactions
- saga
- transactional outbox concept

## 6.7 Consistency models
## 6.8 CAP theorem
## 6.9 Quorums
## 6.10 Timeouts
## 6.11 Circuit breakers
## 6.12 Rate limiting
## 6.13 Backpressure
## 6.14 High availability / failover
## 6.15 SLI / SLO / SLA
## 6.16 Logs, metrics, traces
## 6.17 AuthN / AuthZ
## 6.18 Encryption / secrets
## 6.19 Cost-aware design

### Mastery gate
For each major component, explain:
- what problem it solves
- when not to use it
- what failure modes it introduces
- how failures are detected and recovered

---

# PHASE 7 — Classic HLD Case-Study Ladder

This bank includes every publicly listed design case from ByteByteGo's System Design Interview course.

## Foundational
1. Rate Limiter
2. Key-Value Store
3. Unique ID Generator
4. URL Shortener
5. Web Crawler
6. Notification System
7. News Feed
8. Chat System
9. Search Autocomplete
10. YouTube
11. Google Drive

## Advanced
12. Proximity Service
13. Nearby Friends
14. Google Maps
15. Distributed Message Queue
16. Metrics Monitoring and Alerting
17. Ad Click Event Aggregation
18. Hotel Reservation
19. Distributed Email Service
20. S3-like Object Storage
21. Real-time Gaming Leaderboard
22. Payment System
23. Digital Wallet
24. Stock Exchange

## Supplemental open-source HLD problems
25. Pastebin
26. Twitter timeline/search
27. Search engine
28. Social graph
29. Distributed cache
30. Recommendation platform
31. Collaborative document editing
32. Distributed Job Scheduler
33. Food Delivery Platform
34. Ride Sharing Platform

### HLD readiness gate
Solve an unseen HLD problem and defend two deep dives without being handed the architecture.

---

# PHASE 8 — Machine Learning Foundations for System Design

ML system design is not "HLD with a model box." It adds an entire data/model/evaluation lifecycle.

## 8.1 When ML is appropriate
- business objective
- heuristic/baseline first
- ML task formulation
- input/output
- prediction unit

## 8.2 Metrics
- offline vs online
- precision / recall / F1
- ranking metrics
- calibration
- business/product metrics
- guardrail metrics

## 8.3 Data
- collection
- labels
- leakage
- sampling
- class imbalance
- train/validation/test splits
- time-based splits

## 8.4 Feature/representation layer
- feature engineering
- embeddings
- feature stores
- offline/online consistency

## 8.5 Model development
- baselines
- architecture choice
- loss/objective
- hyperparameters
- offline evaluation

## 8.6 Serving
- batch vs online
- model server
- latency
- throughput
- batching
- autoscaling
- shadow/canary

## 8.7 Experimentation
- A/B testing
- guardrails
- feedback loops

## 8.8 Monitoring
- feature/data drift
- label drift
- model-performance decay
- data quality
- retraining triggers

### Mastery gate
Design an ML system end-to-end without skipping metrics, data, evaluation, serving, or monitoring.

---

# PHASE 9 — ML System Design Case-Study Ladder

Every publicly listed ByteByteGo ML System Design case is included here.

1. Visual Search System
2. Google Street View Blurring System
3. YouTube Video Search
4. Harmful Content Detection
5. Video Recommendation System
6. Event Recommendation System
7. Ad Click Prediction on Social Platforms
8. Similar Listings on Vacation Rental Platforms
9. Personalized News Feed
10. People You May Know

## Supplemental open-source ML interview bank

### Recommendation / retrieval / ranking
11. Movie / Video Recommendation
12. Friend / Follower Recommendation
13. Game Recommendation
14. Replacement Product Recommendation
15. Rental Recommendation
16. Place Recommendation
17. Candidate Retrieval for a Large Catalog
18. Search Ranking over Hundreds of Millions of Documents
19. Ads Retrieval and Ranking

### Search
20. Full-text Document Search
21. Semantic Document Search
22. Image / Video Search
23. Multimodal Search

### NLP / classification
24. Named Entity Linking
25. Autocomplete / Typeahead
26. Sentiment Analysis
27. Language Identification
28. Spam / Abuse Detection
29. Fraud Detection

### Forecasting / prediction
30. ETA Prediction
31. Demand Forecasting
32. Dynamic Pricing
33. Churn / Conversion Prediction

### ML platform
34. Feature Store
35. Model Serving Platform
36. Training Pipeline
37. Experimentation Platform
38. ML Monitoring / Drift Detection

### ML readiness gate
Solve a new ML design prompt with explicit product metric, offline metric, data strategy, baseline/model, serving path, online evaluation, and monitoring.

---

# PHASE 10 — GenAI / LLM Foundations

## 10.1 LLM application landscape
- generation vs discriminative ML
- hosted models vs self-hosting
- quality / latency / cost triangle

## 10.2 Prompt/context design
- system instructions
- structured outputs
- context windows
- prompt injection risk

## 10.3 Embeddings and semantic retrieval
## 10.4 Chunking and indexing
## 10.5 RAG
- ingestion path
- retrieval path
- hybrid search
- reranking
- freshness
- citations / grounding

## 10.6 Fine-tuning / adaptation
- when prompt/RAG is enough
- SFT / LoRA concepts
- preference tuning concepts

## 10.7 Inference serving
- tokens
- KV cache
- batching
- streaming
- autoscaling
- model routing
- caching
- quantization concepts

## 10.8 Evaluation
- golden datasets
- retrieval metrics
- answer correctness
- groundedness
- LLM-as-judge limitations
- human evaluation
- online experiments

## 10.9 Safety and guardrails
- moderation
- jailbreak/prompt injection
- PII
- permissions
- policy routing

## 10.10 Agents
- tool calling
- planning
- state/memory
- retries
- verification
- human-in-the-loop
- cost/latency control

## 10.11 Observability
- traces
- tool calls
- token/cost metrics
- retrieval quality
- hallucination/regression monitoring

### Mastery gate
Given an AI feature, decide whether it needs prompt-only, RAG, fine-tuning, classical ML, agents, or no AI at all—and justify it.

---

# PHASE 11 — GenAI System Design Case-Study Ladder

Every publicly listed ByteByteGo GenAI System Design case is included here.

1. Gmail Smart Compose
2. Google Translate
3. ChatGPT / Personal Assistant Chatbot
4. Image Captioning
5. Retrieval-Augmented Generation
6. Realistic Face Generation
7. High-Resolution Image Synthesis
8. Text-to-Image Generation
9. Personalized Headshot Generation
10. Text-to-Video Generation

## Supplemental public LLM/AI interview bank
11. Enterprise RAG over Internal Documents
12. Customer Support Chatbot with Human Escalation
13. Semantic Enterprise Search with Cited Answers
14. Code Assistant over a Large Repository
15. Coding Agent with Tools and Verification
16. Agentic Workflow / Personal Assistant
17. Content Generation / Summarization at Scale
18. LLM-based Recommendation / Personalization
19. Multi-tenant LLM Gateway
20. Document Processing / Extraction Pipeline
21. Content Moderation with LLM + classifiers
22. Realtime Streaming Chat
23. Semantic Search / Embedding Service
24. Multimodal Assistant
25. LLM Evaluation Platform
26. Safety / Guardrail Platform
27. LLM Observability Platform
28. Cost-aware Model Router
29. Long-context Q&A System
30. Model Serving / Inference Platform

### GenAI readiness gate
Design a new LLM system with explicit quality evaluation, grounding/safety strategy, latency/cost budget, failure handling, and monitoring.

---

# PHASE 12 — Cross-Domain Interview Practice

Now mix the layers.

Examples:
- Product search: HLD + retrieval/ranking ML
- Social feed: HLD + recommendation ML
- Fraud system: event architecture + ML
- Customer support: HLD + RAG + agent + human escalation
- Payment assistant: payments HLD + GenAI permissions/safety
- Marketplace: transactional HLD + search + recommendations

Goal:
Recognize which parts are ordinary software engineering and which genuinely require ML/GenAI.

---

# PHASE 13 — Resume / Production Deep Dive

Prepare 2–3 systems from real work.

For each:
- business problem
- users and scale
- requirements
- constraints
- architecture
- data model
- your contribution
- trade-offs
- incidents/failures
- observability
- measured outcome
- what you would change now

For ML/AI systems additionally:
- dataset
- metrics
- model/evaluation
- serving
- drift/monitoring
- cost

---

# PHASE 14 — Mock Interview Loop

Alternate:
1. LLD / machine coding
2. classic HLD
3. ML system design
4. GenAI system design
5. resume deep dive

The learner drives. The interviewer does not reveal the framework.

## Weakness loop

After each mock:
- identify the weakest 1–2 dimensions
- return to prerequisite topic
- do targeted exercises
- retry with a different problem

---

# Canonical question-bank policy

The case-study titles above are an index of publicly visible prompts/topics. They are not copies of proprietary solution chapters.

When practicing a problem:
- start from a short interview-style prompt;
- solve it independently;
- use public references only after the attempt;
- never memorize one source's architecture as the only correct solution.

---

# Source coverage used to build this bank

Publicly visible course/index material was used from:
- ByteByteGo Object-Oriented Design Interview
- ByteByteGo System Design Interview
- ByteByteGo Machine Learning System Design Interview
- ByteByteGo Generative AI System Design Interview
- System Design Primer
- AIMLInterviews
- awesome-ml-system-design
- awesome-llm-system-design

The question bank should evolve as new relevant public interview patterns appear.
