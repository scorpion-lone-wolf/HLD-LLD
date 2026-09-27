# Prerequisite Map

This map prevents topic jumping.

## Foundation chain

```text
Programming / CS basics
        ↓
OOP + modeling
        ↓
LLD principles + patterns
        ↓
LLD case studies
```

```text
Networking + APIs + databases
        ↓
single-service architecture
        ↓
scaling primitives
        ↓
distributed systems
        ↓
HLD case studies
```

```text
ML fundamentals + metrics + data
        ↓
model development
        ↓
serving + experimentation
        ↓
ML system design
```

```text
ML foundations
        +
distributed-system foundations
        ↓
LLM/Transformer intuition
        ↓
embeddings + retrieval
        ↓
RAG / fine-tuning / inference
        ↓
agents + safety + evaluation
        ↓
GenAI system design
```

---

# Dependency rules

## Before LLD case studies, verify
- basic TypeScript
- OOP
- object relationships
- SOLID reasoning
- testing
- error handling
- basic complexity
- extensibility

## Before advanced LLD, verify
- concurrency basics
- race conditions
- idempotency
- persistence boundary
- API/schema basics

## Before HLD case studies, verify
- HTTP/API basics
- SQL/NoSQL basics
- transactions
- indexes
- caching
- load balancing
- replication
- sharding
- queues
- consistency
- failure handling
- observability

## Before ML system design, verify
- ML problem framing
- supervised-learning intuition
- train/validation/test
- overfitting
- core evaluation metrics
- data leakage
- features/labels
- embeddings where relevant
- offline vs online evaluation

## Before recommendation/search ML problems, verify
- retrieval vs ranking
- embeddings / similarity
- ranking metrics
- negative sampling intuition
- candidate generation
- online feedback loops

## Before GenAI system design, verify
- tokens/context
- transformer/attention intuition
- embeddings
- vector search
- prompting
- RAG fundamentals
- classical ML evaluation concepts
- distributed serving fundamentals

## Before agent-system design, verify
- tool calling
- state
- retries/idempotency
- permissions
- failure recovery
- evaluation
- observability
- cost/latency control

---

# Remediation examples

### "I know caching"
Do not accept the statement alone.

Check:
- cache-aside flow;
- invalidation;
- stale data;
- hot key;
- when caching makes things worse.

### "I know ML"
Check:
- data split;
- leakage;
- metric choice;
- baseline;
- serving;
- monitoring.

### "I know RAG"
Check:
- ingestion;
- chunking;
- embedding;
- retrieval;
- reranking;
- grounding;
- evaluation;
- permissions/freshness.

The goal is to reveal hidden gaps before they appear in a mock interview.
