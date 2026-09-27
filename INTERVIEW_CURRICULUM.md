# Interview Curriculum — HLD + LLD

## Learning model

Follow the order below. Do not skip prerequisites merely because a topic name sounds familiar.

For each topic:
- explain;
- ask the learner to explain it back;
- practice;
- give a transfer question;
- produce Notion-ready notes;
- update progress.

A topic is **complete** only when the learner can use it, not merely recognize it.

---

# Stage 0 — Interview Operating System

## 0.1 HLD vs LLD
Learn:
- what each round evaluates;
- typical deliverables;
- how to narrate thinking;
- how to clarify scope before designing.

## 0.2 Requirements first
Learn:
- functional vs non-functional requirements;
- constraints;
- assumptions;
- success criteria;
- scope negotiation.

## 0.3 Design-answer structure
LLD:
`requirements → entities → relationships → interfaces → flows → code → tests → extension`

HLD:
`requirements → scale → API/data model → architecture → deep dives → failures → trade-offs → observability`

### Mastery gate
Given a vague prompt, learner can spend the first few minutes clarifying instead of proposing technologies.

---

# Stage 1 — LLD Foundations

## 1.1 OOP for design
Only interview-relevant depth:
- encapsulation;
- abstraction;
- composition vs inheritance;
- interfaces;
- polymorphism.

## 1.2 Object relationships
- association;
- aggregation;
- composition;
- cardinality;
- ownership and lifecycle.

## 1.3 SOLID through code
Prioritize:
- SRP;
- OCP;
- DIP;
then LSP and ISP.

Do not memorize definitions only. Refactor small TypeScript examples.

## 1.4 TypeScript design mechanics
- interfaces;
- abstract classes;
- dependency injection;
- enums vs objects;
- error types;
- immutable/value objects where useful.

## 1.5 Testability
- dependency boundaries;
- unit-testable services;
- deterministic logic;
- fakes/mocks only when justified.

### Mastery gate
Learner can model a small domain and write clean, testable TypeScript without forcing design patterns.

---

# Stage 2 — LLD Patterns by Problem

Patterns are learned because a design problem demands them.

## 2.1 Strategy
When behavior varies independently.

## 2.2 Factory
When object creation varies or should be hidden.

## 2.3 Observer / pub-sub
When multiple consumers react to events.

## 2.4 State
When valid behavior depends on lifecycle state.

## 2.5 Adapter
When integrating incompatible interfaces.

## 2.6 Decorator
When behavior is layered dynamically.

## 2.7 Command / Chain of Responsibility
Teach when a case study genuinely needs them.

Defer unless needed:
- Prototype;
- Visitor;
- Abstract Factory as a standalone memorization topic.

### Mastery gate
Given a requirement change, learner can decide whether a pattern helps and explain why—not merely name one.

---

# Stage 3 — LLD Engineering Depth

## 3.1 Error handling and validation
## 3.2 Extensibility under changing requirements
## 3.3 Concurrency and race conditions
## 3.4 Idempotency in object/service design
## 3.5 Persistence boundary and repository abstraction
## 3.6 API and schema basics inside LLD rounds
## 3.7 Complexity of important operations
## 3.8 Runnable code and focused tests

### Mastery gate
Learner can implement a working solution, handle edge cases, and adapt it when the interviewer adds a requirement.

---

# Stage 4 — LLD Case Studies

Do progressively, not all at once.

### Tier 1
1. Vending Machine
2. Parking Lot
3. Tic-Tac-Toe
4. Notification System

### Tier 2
5. Splitwise
6. Movie Ticket Booking
7. ATM
8. Elevator

### Tier 3
9. Food Ordering / Restaurant Assignment
10. Ride Sharing
11. Task Scheduler
12. BNPL / Wallet / Payment-oriented system

For each:
- clarify requirements;
- model entities;
- define contracts;
- implement core flow in TypeScript;
- write tests;
- handle interviewer curveball;
- discuss concurrency/persistence where applicable.

### LLD readiness gate
Solve an unseen medium LLD prompt with runnable code and explain trade-offs without instructor-led structure.

---

# Stage 5 — HLD Foundations

## 5.1 Back-of-the-envelope estimation
- users;
- QPS;
- peak traffic;
- storage;
- bandwidth.

## 5.2 Networking essentials
- DNS;
- HTTP/HTTPS;
- TCP basics;
- WebSocket;
- REST vs gRPC only to interview-useful depth.

## 5.3 API design
- resources;
- pagination;
- idempotency;
- versioning;
- error contracts.

## 5.4 Data modeling
- access patterns first;
- SQL vs NoSQL;
- normalization/denormalization;
- indexes;
- transactions.

### Mastery gate
Learner can convert requirements into APIs and data model before drawing architecture.

---

# Stage 6 — HLD Scaling Building Blocks

Prerequisite order matters.

## 6.1 Stateless services
## 6.2 Load balancing
## 6.3 Caching
- cache-aside;
- invalidation;
- eviction;
- hot keys.

## 6.4 Replication
## 6.5 Partitioning / sharding
## 6.6 Consistent hashing
## 6.7 CDN/object storage where relevant
## 6.8 Search/indexing concepts where relevant

### Mastery gate
For each component, learner must answer:
- what problem does it solve?
- what new failure mode does it introduce?
- when should we NOT use it?

---

# Stage 7 — Async + Distributed-System Reasoning

## 7.1 Queues and pub-sub
## 7.2 Delivery semantics
- at-most-once;
- at-least-once;
- effectively-once via idempotency.

## 7.3 Ordering
## 7.4 Retries and backoff
## 7.5 Idempotency
## 7.6 Distributed transactions
- saga at interview depth;
- transactional outbox concept.

## 7.7 Consistency models
## 7.8 CAP theorem
## 7.9 Quorums where useful

### Mastery gate
Learner can reason about duplicates, ordering, partial failure, consistency, and recovery.

---

# Stage 8 — Reliability, Production, Security

## 8.1 Timeouts
## 8.2 Retries
## 8.3 Circuit breakers
## 8.4 Rate limiting
## 8.5 Backpressure
## 8.6 High availability and failover
## 8.7 SLI / SLO / SLA
## 8.8 Logs, metrics, traces
## 8.9 Authentication vs authorization
## 8.10 Encryption and secrets
## 8.11 Cost-aware design

### Mastery gate
For a proposed architecture, learner can explain how it fails, how we detect it, and how we recover.

---

# Stage 9 — HLD Case Studies

### Tier 1
1. URL Shortener
2. Notification System
3. Rate Limiter

### Tier 2
4. Ticket Booking
5. Chat / Messaging
6. Search Autocomplete
7. Distributed Job Scheduler

### Tier 3
8. Payment System
9. Food Delivery Platform
10. Ride Sharing
11. Social Feed
12. Video Streaming / media delivery

Case-study method:
1. scope;
2. functional requirements;
3. non-functional requirements;
4. estimate;
5. APIs;
6. data model;
7. simple architecture;
8. identify bottleneck;
9. evolve architecture;
10. failures;
11. observability;
12. trade-offs.

### HLD readiness gate
Solve an unseen HLD prompt in interview format and defend two deep dives without being handed the architecture.

---

# Stage 10 — Resume / Production Deep Dive

Prepare 2–3 real systems from work.

For each:
- business problem;
- scale;
- constraints;
- architecture;
- your contribution;
- key decision;
- trade-off;
- failure/incident;
- measurement;
- what you would change now.

Practice:
- “Why did you choose X?”
- “Why not Y?”
- “What failed?”
- “How did you know?”
- “What happened at 10x scale?”

---

# Stage 11 — Mock Interview Loop

Run alternating:
- LLD / machine coding;
- HLD;
- resume deep dive.

Feedback dimensions:

### LLD
- requirements;
- modeling;
- code quality;
- testability;
- extensibility;
- edge cases;
- concurrency;
- communication.

### HLD
- requirements;
- estimation;
- API/data model;
- architecture;
- deep dives;
- reliability;
- trade-offs;
- observability;
- communication.

A weak dimension is retrained before another full mock.

---

# Optional / Role-dependent topics

Study only when target roles justify them:
- GenAI/RAG system design;
- CRDT/OT;
- deep consensus algorithms;
- Kubernetes internals;
- deep streaming internals;
- advanced CQRS/event sourcing;
- multi-region active-active architectures.

These are not prerequisites for the core path.
