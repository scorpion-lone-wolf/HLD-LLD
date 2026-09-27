# Unified Design Interview Curriculum

This is the canonical step-by-step curriculum for **design interviews**:

- OOD / LLD / machine coding
- HLD / distributed systems
- Machine Learning System Design
- Generative AI / LLM System Design
- cross-domain AI systems
- resume / production-system deep dives
- realistic mocks

The curriculum is comprehensive, but it is **adaptive**: assessment can fast-pass verified material or temporarily route into a foundation-repair topic.

Every teachable concept has a stable ID so `PROGRESS.md` can store evidence precisely.

---

# STAGE 0 — Interview Operating System

## INT-01 Interview families
Understand expected outputs for:
- OOD/LLD
- machine coding
- HLD
- ML system design
- GenAI system design
- resume/production deep dive

## INT-02 Requirements and scope
- functional vs non-functional requirements
- constraints
- assumptions
- success criteria
- examples / counterexamples
- in-scope vs out-of-scope

## INT-03 Communication
- structured thinking aloud
- concise assumptions
- trade-off narration
- handling pushback
- avoiding premature technology/model selection

## INT-04 Universal answer structures

### LLD
`requirements → use cases → responsibilities → entities → relationships → contracts → flow → code → tests → extension`

### HLD
`requirements → NFRs → scale → APIs → data model → simple architecture → bottlenecks → failures → observability → trade-offs`

### ML
`product goal → ML suitability → baseline → metrics → data/labels → representation/model → offline eval → serving → online eval → monitoring/retraining`

### GenAI
`product goal → suitability → quality criteria → data/knowledge → approach choice → architecture → evaluation → serving → safety → observability/cost`

### Stage gate
Given a vague prompt, clarify before proposing implementation.

---

# STAGE 1 — Foundation Repair Layer

These are not mandatory lectures. Assessment activates only the gaps that matter.

## Programming / CS

### FND-01 TypeScript/JavaScript essentials
- values/references
- functions
- classes
- interfaces/types
- generics at interview-useful depth
- async/Promise basics

### FND-02 Core collections
- array
- map/hash map
- set
- stack
- queue/deque
- heap/priority queue
- tree/graph recognition

### FND-03 Complexity
- O(1), O(log n), O(n), O(n log n), O(n²)
- time vs space
- amortized intuition
- common collection operation costs

### FND-04 Errors and testing
- validation
- exceptions/result-style errors
- unit-test basics
- dependency boundaries
- deterministic tests

### FND-05 Concurrency basics
- race condition
- critical section
- lock/mutex intuition
- optimistic vs pessimistic coordination
- atomicity
- idempotency intuition

## Backend foundations

### FND-06 Networking
- DNS
- TCP connection intuition
- HTTP/HTTPS
- request/response lifecycle
- latency vs throughput
- WebSocket concept
- gRPC concept

### FND-07 API fundamentals
- resources
- methods
- status/error contracts
- pagination
- versioning
- idempotency keys
- synchronous vs asynchronous API

### FND-08 Database fundamentals
- relational model
- primary/foreign keys
- normalization intuition
- SQL vs NoSQL decision basics
- read/write access patterns

### FND-09 Indexes and transactions
- index purpose/cost
- composite indexes
- ACID
- isolation intuition
- locks
- lost update / double booking

### FND-10 Interview communication baseline
- ask clarifying questions
- state assumptions
- explain decision → reason → trade-off
- verify success

### Stage gate
All critical prerequisites for the next domain are Level 3+ or explicitly scheduled for repair.

---

# STAGE 2 — LLD / OOD Foundations

## LLD-01 Responsibilities and cohesion
- identify actors/use cases
- responsibilities
- high cohesion
- low coupling

## LLD-02 OOP for design
- encapsulation
- abstraction
- polymorphism
- interface-driven design

## LLD-03 Relationships
- association
- aggregation
- composition
- inheritance
- composition vs inheritance
- multiplicity/cardinality
- lifecycle ownership

## LLD-04 SOLID in practice
- SRP
- OCP
- LSP
- ISP
- DIP
- refactor before/after examples

## LLD-05 TypeScript design mechanics
- interfaces
- abstract classes
- dependency injection
- modules
- domain vs infrastructure boundaries
- value objects
- immutable state where useful

## LLD-06 Testability and invalid states
- test behavior
- dependency substitution
- deterministic core
- validation
- state invariants

## LLD-07 Design patterns as tools

Required recognition/application:
- Strategy
- Factory / Factory Method
- Observer
- State
- Adapter
- Decorator

Conditional/deeper when problems require them:
- Command
- Chain of Responsibility
- Builder
- Facade
- Proxy
- Composite

Recognition only unless target interviews demand more:
- Abstract Factory
- Prototype
- Visitor
- Singleton trade-offs

## LLD-08 Persistence boundary
- repository abstraction
- domain vs persistence objects
- transaction boundary intuition

## LLD-09 Concurrency in LLD
- shared mutable state
- race conditions
- locks
- idempotent operations
- double booking / inventory decrement

## LLD-10 Extensibility under curveballs
- adding new types/behaviors
- avoiding switch explosion
- preserving contracts
- backwards-compatible changes

### LLD foundation gate
Model a small domain, write testable TypeScript, and handle one requirement change without forced patterns.

---

# STAGE 3 — LLD Case-Study Ladder

Use the easiest case whose prerequisites are verified.

## Tier L1 — modeling and state

| Problem | Requires | Primary focus |
|---|---|---|
| Parking Lot | LLD-01..06 | entities, relationships, extensibility |
| Vending Machine | LLD-01..07 | state, inventory, payment behavior |
| Tic-Tac-Toe | FND-02/03, LLD-01..06 | modeling + algorithmic operations |
| Deck of Cards / Blackjack | LLD-01..06 | composition, rules |
| Unix File Search | LLD-01..07 | composite/specification-style filtering |
| Library Management | LLD-01..06 | entities, borrowing state |

## Tier L2 — workflows / concurrency / integrations

| Problem | Requires | Primary focus |
|---|---|---|
| Movie Ticket Booking | LLD-08/09 | booking concurrency |
| Elevator | LLD-07/09 | state + scheduling |
| ATM | LLD-07..10 | state, transactions, extensibility |
| Shipping Locker | LLD-01..10 | assignment + state |
| Restaurant Management | LLD-01..10 | workflows |
| Grocery Store | LLD-01..10 | inventory, checkout, extensibility |
| Notification System | LLD-07/10 | strategy/observer |
| Splitwise | FND-02/03, LLD-01..10 | balances, extensibility |
| Logging Framework | LLD-07/10 | chain/strategy, sinks |
| Task Scheduler | FND-02/05, LLD-07..10 | scheduling, concurrency |

## Tier L3 — interview-depth / machine coding

| Problem | Requires | Primary focus |
|---|---|---|
| Food Ordering / Assignment | LLD-01..10 | workflows + policies |
| Ride Sharing core | LLD-01..10 | state + matching contracts |
| Wallet / BNPL | FND-09, LLD-01..10 | money, idempotency |
| In-memory Order Matching Engine | FND-02/03/05, LLD-01..10 | data structures + concurrency |
| LRU Cache | FND-02/03 | data-structure implementation |
| Hash Map | FND-02/03 | hashing + resizing |
| Chat Server core | LLD-01..10 | sessions/messages |
| Call Center | LLD-07/10 | routing policies |

### LLD readiness gate
Complete at least two unfamiliar LLD mocks, including one timed and one with runnable code/tests.

---

# STAGE 4 — HLD Foundations

## HLD-01 Scale and stateless services
- vertical vs horizontal scaling
- stateless application tier
- session state

## HLD-02 Estimation
- users/DAU
- average/peak QPS
- read/write ratio
- storage
- bandwidth
- cache sizing
- order-of-magnitude reasoning

## HLD-03 API + data model
- APIs from use cases
- data access patterns
- schema choice
- relational vs NoSQL reasoning

## HLD-04 Load balancing
- health checks
- algorithms
- sticky sessions trade-off
- L4/L7 intuition

## HLD-05 Caching
- cache-aside
- read/write strategies
- TTL
- invalidation
- stale data
- eviction
- hot keys
- cache stampede

## HLD-06 Replication
- leader/follower
- read replicas
- replication lag
- failover
- consistency implications

## HLD-07 Partitioning / sharding
- shard key
- range/hash partitioning
- rebalancing
- hotspots
- cross-shard operations

## HLD-08 Consistent hashing
- ring intuition
- virtual nodes
- rebalancing use cases

## HLD-09 Unique ID generation
- UUID
- database sequence
- timestamp/worker approaches
- ordering/collision trade-offs

## HLD-10 Storage / CDN / search
- object/blob storage
- CDN
- search indexes
- full-text vs transactional DB

## HLD-11 Queues and pub-sub
- async decoupling
- queue vs pub-sub
- consumer groups
- backpressure

## HLD-12 Delivery, retries, ordering
- at-most-once
- at-least-once
- effectively-once through idempotency
- exponential backoff
- poison messages / DLQ
- ordering scope

## HLD-13 Consistency models
- strong/eventual
- read-your-writes intuition
- CAP correctly scoped
- quorum intuition

## HLD-14 Distributed transactions
- why 2PC is difficult
- saga
- compensating action
- transactional outbox

## HLD-15 Reliability patterns
- timeout
- retry
- circuit breaker
- bulkhead intuition
- rate limiting
- load shedding
- backpressure

## HLD-16 Availability / DR
- redundancy
- failover
- RPO/RTO intuition
- multi-AZ / multi-region trade-offs

## HLD-17 Observability
- metrics
- logs
- traces
- SLIs/SLOs/SLAs
- alert quality
- debugging distributed latency

## HLD-18 Security
- authentication
- authorization
- encryption in transit/at rest
- secrets
- least privilege
- abuse/rate controls

## HLD-19 Cost-aware design
- storage/compute/network cost
- managed vs self-hosted
- overprovisioning vs autoscaling
- hot path cost

### HLD foundation gate
Given requirements, produce API + data model + simple architecture and justify every major component.

---

# STAGE 5 — HLD Case-Study Ladder

## Tier H1 — foundational

| Problem | Key prerequisites |
|---|---|
| URL Shortener | HLD-02/03/05/09 |
| Rate Limiter | HLD-04/05/11/15 |
| Key-Value Store | HLD-05/06/07/13 |
| Unique ID Generator | HLD-02/09 |
| Notification System | HLD-03/11/12/17 |
| Search Autocomplete | HLD-05/10 |
| Web Crawler | HLD-10/11/12 |

## Tier H2 — distributed product systems

| Problem | Key prerequisites |
|---|---|
| Chat System | HLD-03/06/11/12/13 |
| News Feed | HLD-05/07/11 |
| Google Drive | HLD-06/07/10/13 |
| YouTube / Video Streaming | HLD-02/05/10/16 |
| Proximity Service / Nearby Friends | HLD-03/07/10 |
| Hotel / Ticket Reservation | FND-09, HLD-07/13/14 |
| Distributed Email | HLD-11/12/17 |
| Distributed Message Queue | HLD-06/07/11/12/13/17 |
| Metrics / Alerting | HLD-11/17 |
| Ad Click Aggregation | HLD-07/11/12 |
| Job Scheduler | HLD-11/12/15/17 |

## Tier H3 — advanced

| Problem | Key prerequisites |
|---|---|
| Payment System | HLD-12/13/14/17/18 |
| Digital Wallet | HLD-12/13/14/18 |
| Stock Exchange | FND-05/09, HLD-07/12/13 |
| S3-like Storage | HLD-06/07/10/16 |
| Google Maps | HLD-07/10 |
| Gaming Leaderboard | HLD-05/07 |
| Food Delivery | HLD-03/07/11/13 |
| Ride Sharing | HLD-03/07/10/11 |
| Collaborative Documents | HLD-12/13 + OT/CRDT concept when needed |
| Distributed Cache | HLD-05/06/07/08 |

Additional public practice titles:
- Pastebin
- Twitter timeline/search
- Search engine
- Social graph
- Recommendation platform

### HLD readiness gate
Complete at least two unfamiliar HLD mocks, including one timed, and defend at least two deep dives.

---

# STAGE 6 — ML Foundation Repair

These foundations support ML system-design interviews. Depth is calibrated to role.

## MLF-01 Probability / statistics intuition
- mean/variance
- probability
- conditional probability
- distributions intuition
- sampling bias
- correlation vs causation

## MLF-02 Vector intuition
- vector
- dot product
- norm
- cosine similarity
- distance intuition

## MLF-03 ML problem types
- regression
- binary/multiclass classification
- multilabel
- ranking
- clustering
- anomaly detection
- recommendation
- forecasting

## MLF-04 Data / features / labels
- examples
- features
- labels
- target definition
- label quality

## MLF-05 Splits and leakage
- train/validation/test
- time splits
- leakage
- duplicates
- distribution mismatch

## MLF-06 Training objective intuition
- loss/objective
- gradient descent intuition
- learning rate
- training vs inference

## MLF-07 Model families
Interview-level intuition for:
- linear/logistic models
- trees / boosted trees
- nearest neighbors
- neural networks
- embeddings
- when simple models are preferable

## MLF-08 Generalization
- overfitting/underfitting
- bias/variance intuition
- regularization
- early stopping

## MLF-09 Classification metrics
- confusion matrix
- precision
- recall
- F1
- ROC-AUC / PR-AUC intuition
- threshold choice
- calibration

## MLF-10 Ranking/recommendation metrics
- precision@k / recall@k
- MAP/MRR intuition
- NDCG
- CTR/conversion as online metrics
- diversity/novelty guardrails

## MLF-11 Embeddings / representation learning
- dense vectors
- similarity
- semantic representation
- embedding training intuition
- vector retrieval limitations

### ML foundation gate
Explain an ML problem, metric, data split and baseline without hand-waving.

---

# STAGE 7 — ML System Design

## MLS-01 Product goal → ML framing
- prediction unit
- objective
- constraints
- when ML is not appropriate

## MLS-02 Baseline + success metrics
- heuristic baseline
- offline metric
- product metric
- guardrail metric

## MLS-03 Data/label pipeline
- collection
- labeling
- weak/implicit labels
- delayed labels
- sampling
- imbalance
- privacy

## MLS-04 Feature/representation pipeline
- feature engineering
- embeddings
- feature stores
- offline/online consistency

## MLS-05 Training pipeline
- dataset versioning
- training jobs
- model registry
- reproducibility
- hyperparameter strategy at interview depth

## MLS-06 Serving
- batch vs online
- model server
- latency/throughput
- batching
- autoscaling
- shadow/canary
- fallback

## MLS-07 Experimentation
- A/B testing
- guardrails
- novelty effects
- sample-ratio mismatch intuition

## MLS-08 Monitoring / drift / retraining
- data quality
- feature drift
- label drift
- performance decay
- retraining triggers
- feedback loops

## MLS-09 Retrieval and ranking
- candidate generation
- ANN/vector retrieval
- two-stage ranking
- reranking
- negative sampling intuition
- freshness

## MLS-10 ML platform architecture
- feature store
- training platform
- model serving platform
- experimentation platform
- monitoring platform

### ML system-design gate
Design end-to-end without skipping data, metrics, serving, experimentation or monitoring.

---

# STAGE 8 — ML Case-Study Ladder

## Level M1 — prediction / classification
- Harmful Content Detection
- Spam / Abuse Detection
- Fraud Detection
- Ad Click Prediction
- Churn / Conversion Prediction
- ETA Prediction
- Demand Forecasting
- Dynamic Pricing

## Level M2 — retrieval / recommendation / ranking
- People You May Know
- Event Recommendation
- Video Recommendation
- Personalized News Feed
- Similar Listings
- Movie/Game/Place Recommendation
- Replacement Product Recommendation
- Search Ranking
- Ads Retrieval and Ranking

Requires: MLF-10/11 + MLS-09.

## Level M3 — semantic / multimodal search
- Visual Search
- YouTube Video Search
- Semantic Document Search
- Image / Video Search
- Multimodal Search
- Named Entity Linking

Requires: MLF-11 + MLS-09.

## Level M4 — ML infrastructure
- Feature Store
- Training Pipeline
- Model Serving Platform
- Experimentation Platform
- ML Monitoring / Drift Detection

### ML readiness gate
Two unfamiliar ML system-design mocks, one timed, with explicit metrics/data/model/serving/monitoring.

---

# STAGE 9 — GenAI / Deep-Learning Foundations

## GAI-01 Tokens / tokenization / context
- tokens
- context window
- truncation
- input/output token cost

## GAI-02 Neural-network intuition
- layers
- activations
- training/inference intuition
- representation learning

## GAI-03 Attention + transformer intuition
- query/key/value intuition
- self-attention
- positional information
- transformer blocks
- decoder-only intuition

## GAI-04 Autoregressive generation
- next-token prediction
- temperature
- top-k/top-p intuition
- deterministic vs creative generation

## GAI-05 Embeddings + vector search
- reuse MLF-11
- vector index/ANN intuition
- metadata filters
- recall vs latency

## GAI-06 Prompting / structured output
- system/user/tool roles
- few-shot examples
- schema/JSON output
- prompt versioning
- prompt injection awareness

## GAI-07 Multimodal representation
- text/image encoders
- shared embedding spaces
- captioning/retrieval intuition

## GAI-08 Diffusion-model intuition
- noise → denoising
- latent diffusion intuition
- conditioning
- sampling cost
- text-to-image/video conceptual pipeline

## GAI-09 Generative-media evaluation
- human evaluation
- quality/alignment
- diversity
- safety
- task-specific automated metrics limitations

### GenAI foundation gate
Explain tokens, transformer/attention intuition, embeddings and inference trade-offs before advanced LLM systems.

---

# STAGE 10 — GenAI System Design

## GSD-01 Choose the right approach
Compare:
- deterministic code
- classical ML
- prompt-only LLM
- RAG
- fine-tuning
- agent/tool use

## GSD-02 Retrieval pipeline
- document ingestion
- parsing
- chunking
- embedding
- indexing
- hybrid search
- reranking
- metadata filtering

## GSD-03 RAG architecture
- retrieval
- context assembly
- generation
- citations
- freshness
- permissions/ACLs
- failure/fallback

## GSD-04 Fine-tuning / adaptation
- when prompting is enough
- when RAG is enough
- SFT
- LoRA/PEFT intuition
- preference tuning concepts
- risks of fine-tuning stale facts

## GSD-05 Inference serving
- hosted vs self-hosted
- streaming
- batching
- KV-cache intuition
- quantization intuition
- autoscaling
- model routing
- semantic/prompt caching
- fallback
- token/compute cost

## GSD-06 Evaluation
- golden datasets
- task correctness
- retrieval recall/precision
- groundedness
- citation quality
- human evaluation
- LLM-as-judge strengths/limitations
- online experiments

## GSD-07 Safety / guardrails
- prompt injection
- jailbreaks
- content moderation
- PII
- tenant isolation
- permissions
- output validation
- policy checks

## GSD-08 Agents / tools
- tool schemas
- planning
- state/memory
- retries
- idempotency
- verification
- permissions
- human-in-the-loop
- runaway cost/loop controls

## GSD-09 Observability
- traces
- prompts/responses with privacy controls
- retrieval diagnostics
- tool calls
- token/cost metrics
- quality regressions
- safety incidents

## GSD-10 Long context / memory
- context stuffing trade-offs
- summarization
- episodic/profile memory concepts
- retrieval vs persistent memory
- freshness/deletion

### GenAI system-design gate
Select the correct approach and define evaluation, safety, serving, cost and failure handling—not just architecture.

---

# STAGE 11 — GenAI Case-Study Ladder

## Level G1 — language applications
- Gmail Smart Compose
- Google Translate
- Content Generation / Summarization
- Structured Document Extraction

## Level G2 — retrieval / RAG
- Enterprise RAG over Internal Documents
- Semantic Enterprise Search with Cited Answers
- Customer Support Chatbot
- Long-context Q&A
- Code Assistant over a Repository
- Retrieval-Augmented Generation

Requires: GSD-02/03/06/07/09.

## Level G3 — agents
- Coding Agent with Tools and Verification
- Personal Assistant / Agentic Workflow
- Support Agent with Human Escalation
- Payment/Operations Assistant

Requires: GSD-08 plus HLD-12/15/18.

## Level G4 — GenAI infrastructure
- Multi-tenant LLM Gateway
- Cost-aware Model Router
- LLM Evaluation Platform
- Safety / Guardrail Platform
- LLM Observability Platform
- Model Serving / Inference Platform
- Realtime Streaming Chat

Requires: GSD-05/06/07/09.

## Level G5 — multimodal / generative media
- Image Captioning
- Visual/Multimodal Assistant
- Realistic Face Generation
- High-Resolution Image Synthesis
- Text-to-Image Generation
- Personalized Headshot Generation
- Text-to-Video Generation

Requires: GAI-07/08/09 plus relevant serving/evaluation concepts.

### GenAI readiness gate
Two unfamiliar GenAI mocks, one timed, with explicit evaluation/safety/latency/cost/failure reasoning.

---

# STAGE 12 — Cross-Domain Systems

Use only after relevant domain foundations are verified.

- Product Search: HLD + retrieval/ranking ML
- Social Feed: HLD + recommendation ML
- Fraud Platform: event architecture + ML
- Customer Support: HLD + RAG + agents + human escalation
- Payment Assistant: payment HLD + GenAI permissions/safety
- Marketplace: transactions + search + recommendation
- Content Platform: moderation + recommendation + GenAI creation
- Developer Platform: code search + RAG + agents

Goal: distinguish which subsystem is ordinary software, ML, or GenAI and choose the simplest appropriate technique.

---

# STAGE 13 — Resume / Production Deep Dive

Prepare 2–3 real systems.

For each:
- business problem
- users/scale
- requirements
- constraints
- architecture
- API/data model
- personal contribution
- key decisions
- alternatives rejected
- failures/incidents
- observability
- measured result
- cost
- what would change now

For ML/AI systems also:
- dataset/labels
- metrics
- model/evaluation
- serving
- experimentation
- drift
- safety
- cost

Practice interviewer pushback:
- Why X?
- Why not Y?
- What broke?
- How did you know?
- What happens at 10x?
- What would you redesign today?

---

# STAGE 14 — Mock Interview Loop

Modes:

1. Guided
2. Semi-independent
3. Realistic untimed mock
4. Timed mock

Rotate:
- LLD / machine coding
- HLD
- ML system design
- GenAI system design
- resume deep dive

After every mock:
1. grade against `INTERVIEW_READINESS_RUBRIC.md`;
2. identify 1–2 highest-impact weaknesses;
3. route back to the exact prerequisite IDs;
4. retrain with a different problem;
5. retry later.

---

# Retention loop

Do not rely on one-time understanding.

- after 2–4 related concepts: one short recall
- before case study: prerequisite recall
- during mock: natural verification
- after long break: targeted reassessment

A previously verified topic can move to `revisit`.

---

# Question-bank policy

Problem titles provide coverage, not memorized solutions.

For each problem:
- start from a short interview-style prompt;
- learner drives first;
- use references only after the attempt;
- compare alternatives rather than memorizing one canonical diagram.

Publicly visible topic coverage has been informed by ByteByteGo's OOD, System Design, ML System Design and GenAI System Design curricula plus open interview repositories. Proprietary chapter text/solutions are not copied.

---

# Legacy Coverage Guarantee — Do Not Remove

This section preserves the exact interview-problem titles that existed in the earlier unified curriculum. The structured ladders above may rename/group problems for learning order, but **every title below remains part of the required practice bank**.

Future curriculum revisions must be a **strict superset** of this bank: topics/questions may be added, regrouped, or aliased, but not removed.

1. Parking Lot
2. Vending Machine
3. Tic-Tac-Toe
4. Blackjack / Deck of Cards
5. Unix File Search
6. Movie Ticket Booking
7. Elevator
8. Shipping Locker
9. ATM
10. Grocery Store
11. Restaurant Management
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
25. Rate Limiter
26. Key-Value Store
27. Unique ID Generator
28. URL Shortener
29. Web Crawler
30. News Feed
31. Chat System
32. Search Autocomplete
33. YouTube
34. Google Drive
35. Proximity Service
36. Nearby Friends
37. Google Maps
38. Distributed Message Queue
39. Metrics Monitoring and Alerting
40. Ad Click Event Aggregation
41. Hotel Reservation
42. Distributed Email Service
43. S3-like Object Storage
44. Real-time Gaming Leaderboard
45. Payment System
46. Digital Wallet
47. Stock Exchange
48. Pastebin
49. Twitter timeline/search
50. Search engine
51. Social graph
52. Distributed cache
53. Recommendation platform
54. Collaborative document editing
55. Distributed Job Scheduler
56. Food Delivery Platform
57. Ride Sharing Platform
58. Visual Search System
59. Google Street View Blurring System
60. YouTube Video Search
61. Harmful Content Detection
62. Video Recommendation System
63. Event Recommendation System
64. Ad Click Prediction on Social Platforms
65. Similar Listings on Vacation Rental Platforms
66. Personalized News Feed
67. People You May Know
68. Movie / Video Recommendation
69. Friend / Follower Recommendation
70. Game Recommendation
71. Replacement Product Recommendation
72. Rental Recommendation
73. Place Recommendation
74. Candidate Retrieval for a Large Catalog
75. Search Ranking over Hundreds of Millions of Documents
76. Ads Retrieval and Ranking
77. Full-text Document Search
78. Semantic Document Search
79. Image / Video Search
80. Multimodal Search
81. Named Entity Linking
82. Autocomplete / Typeahead
83. Sentiment Analysis
84. Language Identification
85. Spam / Abuse Detection
86. Fraud Detection
87. ETA Prediction
88. Demand Forecasting
89. Dynamic Pricing
90. Churn / Conversion Prediction
91. Feature Store
92. Model Serving Platform
93. Training Pipeline
94. Experimentation Platform
95. ML Monitoring / Drift Detection
96. Gmail Smart Compose
97. Google Translate
98. ChatGPT / Personal Assistant Chatbot
99. Image Captioning
100. Retrieval-Augmented Generation
101. Realistic Face Generation
102. High-Resolution Image Synthesis
103. Text-to-Image Generation
104. Personalized Headshot Generation
105. Text-to-Video Generation
106. Enterprise RAG over Internal Documents
107. Customer Support Chatbot with Human Escalation
108. Semantic Enterprise Search with Cited Answers
109. Code Assistant over a Large Repository
110. Coding Agent with Tools and Verification
111. Agentic Workflow / Personal Assistant
112. Content Generation / Summarization at Scale
113. LLM-based Recommendation / Personalization
114. Multi-tenant LLM Gateway
115. Document Processing / Extraction Pipeline
116. Content Moderation with LLM + classifiers
117. Realtime Streaming Chat
118. Semantic Search / Embedding Service
119. Multimodal Assistant
120. LLM Evaluation Platform
121. Safety / Guardrail Platform
122. LLM Observability Platform
123. Cost-aware Model Router
124. Long-context Q&A System
125. Model Serving / Inference Platform
