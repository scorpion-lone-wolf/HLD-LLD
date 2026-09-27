# Prerequisite Map

This is one curriculum with explicit dependency gates. The mentor follows the canonical order in `INTERVIEW_CURRICULUM.md` and uses this map for remediation and no-jump enforcement.

# Shared repair nodes

- FND-01 TypeScript/JavaScript essentials
- FND-02 Core collections
- FND-03 Complexity
- FND-04 Errors/testing
- FND-05 Concurrency basics
- FND-06 Networking
- FND-07 API fundamentals
- FND-08 Database fundamentals
- FND-09 Indexes/transactions
- FND-10 Interview communication

Strong evidence can fast-pass any repair node.

# LLD chain

```text
FND-01/02/03/04
      ↓
LLD-01 responsibilities
      ↓
LLD-02 OOP
      ↓
LLD-03 relationships
      ↓
LLD-04 SOLID
      ↓
LLD-05 TypeScript design mechanics
      ↓
LLD-06 testability / invalid states
      ↓
LLD-07 relevant patterns
      ↓
LLD-08/09/10 persistence + concurrency + extensibility
      ↓
LLD case studies
```

Patterns are not prerequisites unless the problem actually depends on them.

# HLD chain

```text
FND-05/06/07/08/09
      ↓
HLD-01/02/03 single-service + estimation + API/data model
      ↓
HLD-04/05 load balancing + caching
      ↓
HLD-06/07/08/09 replication + partitioning + hashing + IDs
      ↓
HLD-10/11 storage/search + queues
      ↓
HLD-12/13/14 delivery + consistency + transactions
      ↓
HLD-15/16/17/18/19 reliability + DR + observability + security + cost
      ↓
HLD-20 service architecture / evolution
      ↓
HLD-21 coordination / leadership / consensus
      ↓
HLD case studies
```

# ML foundation chain

```text
MLF-01 probability/statistics
MLF-02 vector intuition
      ↓
MLF-03 problem types
      ↓
MLF-04 data/features/labels
      ↓
MLF-05 splits/leakage
      ↓
MLF-06 objective/optimization intuition
      ↓
MLF-07 model families
      ↓
MLF-08 generalization
      ↓
MLF-09/10 metrics
      ↓
MLF-11 embeddings
```

Depth is role-calibrated; conceptual understanding is still verified.

# ML system-design chain

```text
ML foundations
 + HLD-03/11/17
      ↓
MLS-01 framing
      ↓
MLS-02 baseline/metrics
      ↓
MLS-03 data/labels
      ↓
MLS-04 representations
      ↓
MLS-05 training
      ↓
MLS-06 serving
      ↓
MLS-07 experimentation
      ↓
MLS-08 monitoring/retraining
      ↓
MLS-09 retrieval/ranking
      ↓
MLS-10 platform concepts
      ↓
ML case studies
```

# GenAI foundation chain

```text
MLF-02 + MLF-06 + MLF-11
      ↓
GAI-01 tokens/context
      ↓
GAI-02 neural-net intuition
      ↓
GAI-03 attention/transformer
      ↓
GAI-04 generation/sampling
      ↓
GAI-05 vector retrieval
      ↓
GAI-06 prompting/structured output
```

Generative-media branch:
```text
GAI-02
  ↓
GAI-07 multimodal representations
  ↓
GAI-08 diffusion intuition
  ↓
GAI-09 media evaluation
```

# GenAI system-design chain

```text
HLD-12/15/17/18 reliability + observability + security
 + GAI foundations
      ↓
GSD-01 approach choice
      ↓
GSD-02 retrieval
      ↓
GSD-03 RAG
      ↓
GSD-04 adaptation/fine-tuning
      ↓
GSD-05 inference serving
      ↓
GSD-06 evaluation
      ↓
GSD-07 safety
      ↓
GSD-08 agents/tools
      ↓
GSD-09 observability
      ↓
GSD-10 long context/memory
      ↓
GenAI case studies
```

# Case-study routing

Before selecting a case:
1. read its prerequisites in `INTERVIEW_CURRICULUM.md`;
2. check those IDs in `PROGRESS.md`;
3. repair any critical missing prerequisite;
4. choose the easiest case that exercises the intended skill.

Never pick a random problem merely because it is famous.
