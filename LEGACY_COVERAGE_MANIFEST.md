# Legacy Coverage Manifest

Purpose: prevent future curriculum cleanup from silently deleting useful interview depth.

The repository's superset guarantee covers both:
1. **concepts/capabilities** in this file;
2. **problem titles** in the legacy bank inside `INTERVIEW_CURRICULUM.md`.

A concept may move or be renamed, but its prior wording should remain discoverable here.

---

## LLD / machine coding concepts to preserve

- three LLD variants: design discussion, greenfield machine coding, existing-codebase extension/refactor
- OOP interview framing
- SOLID
- association / aggregation / composition / multiplicity
- creational patterns
- structural patterns
- behavioral patterns
- concurrency / race conditions / producer-consumer intuition
- testing
- extensibility under surprise requirements
- runnable code as an interview deliverable
- communication while coding
- TypeScript / Node.js as current default
- Python as a valid alternate when a target interview requires/allows it

---

## HLD concepts to preserve

### Estimation / networking
- back-of-the-envelope estimation
- DNS
- HTTP/HTTPS
- TCP vs UDP intuition
- REST
- gRPC
- GraphQL
- WebSocket
- WebRTC

### Scaling / databases
- vertical vs horizontal scaling
- statelessness
- load balancing
- SQL vs NoSQL
- indexing
- normalization vs denormalization
- query optimization intuition
- ACID
- LSM trees vs B-trees
- replication
- sharding/partitioning
- consistent hashing
- erasure coding

### Consistency / caching
- CAP scoped correctly
- strong vs eventual consistency
- quorum
- cache-aside
- write-through/write-back
- eviction
- CDN
- cache stampede / thundering herd

### Async / processing
- queues
- pub-sub
- event-driven architecture
- batch vs stream processing
- MapReduce intuition
- backpressure

### API / architecture
- API gateway
- rate limiting
- idempotency
- BFF
- connection pooling
- microservices vs monolith
- service discovery
- saga
- circuit breaker
- strangler pattern

### Deployment / reliability
- blue-green
- canary
- feature flags
- bulkhead
- retries with backoff/jitter
- timeouts
- load shedding
- redundancy
- failover
- disaster recovery
- SLA/SLO/SLI
- RPO/RTO

### Distributed coordination
- leader election
- distributed locks
- distributed transactions
- consensus
- Paxos/Raft conceptual understanding

### Observability / security
- metrics/logs/traces
- distributed tracing
- correlation IDs
- secrets management
- authentication/authorization
- encryption
- deserialization risks
- cost-aware design

---

## India / fintech capabilities to preserve

- payment/ledger reasoning
- wallet/BNPL
- ATM/banking domain modeling
- order matching / stock exchange
- double-entry bookkeeping
- booking/calendar
- food delivery / assignment
- company-reported question mapping as **directional**, not authoritative

---

## Interview-operating capabilities to preserve

- explicit communication traps
- numerical estimation reference
- resume/production deep dive
- guided → semi-independent → untimed → timed mock progression
- current-format awareness
- AI-assisted interview adaptation when permitted
- exact session resume
- retention/revisit loop
- evidence-based readiness, not completion-based readiness

---

## ML concepts to preserve

- ML suitability + non-ML baseline
- classification/regression/ranking/recommendation/forecasting/anomaly detection
- features/labels
- train/validation/test
- leakage
- objective/loss intuition
- generalization
- classification/ranking metrics
- embeddings
- data/label pipeline
- feature/representation pipeline
- training pipeline
- serving
- experimentation
- monitoring/drift/retraining
- retrieval/ranking
- feature store / model serving / ML platform concepts

---

## GenAI concepts to preserve

- tokens/context
- transformer/attention intuition
- embeddings/vector retrieval
- prompting/structured output
- multimodal representation
- diffusion intuition
- deterministic vs ML vs prompt-only vs RAG vs fine-tune vs agent selection
- RAG ingestion/chunking/retrieval/reranking/permissions/freshness
- inference serving
- evaluation
- safety/guardrails
- agents/tools
- observability
- long context/memory
- generative-media systems

---

## Revision checklist

Before declaring a curriculum refactor complete:

- [ ] compare this manifest against the new curriculum;
- [ ] verify every concept is still explicit or mapped;
- [ ] verify all 125 legacy problem titles remain;
- [ ] verify no prerequisite ID referenced elsewhere was orphaned;
- [ ] verify README/source-of-truth order remains accurate;
- [ ] verify readiness gates still require unfamiliar transfer;
- [ ] verify progress/session continuity still works.
