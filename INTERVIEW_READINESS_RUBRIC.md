# Interview Readiness Rubric

Interview-ready means **repeatable performance on unfamiliar prompts**, not lesson completion.

## Evidence levels

| Level | Meaning |
|---:|---|
| U | unassessed |
| 0 | unfamiliar |
| 1 | learning |
| 2 | practicing with guidance |
| 3 | verified on a familiar problem independently |
| 4 | transfer-verified on an unfamiliar problem with trade-off defense |
| R | revisit |

A domain cannot be interview-ready while a critical prerequisite is below Level 3.

## Universal dimensions

| Dimension | Ready behavior |
|---|---|
| Requirements | Clarifies scope before solutioning |
| Communication | Explains reasoning in a structured way |
| Assumptions | States and validates assumptions |
| Trade-offs | Compares plausible alternatives |
| Simplicity | Starts simple and adds complexity only when needed |
| Verification | Defines correctness/success signals |
| Adaptability | Handles requirement changes without losing structure |
| Time management | Reaches important deep dives within the interview window |

## LLD / OOD readiness

The learner can:
- clarify use cases and scope;
- identify responsibilities and entities;
- model relationships and ownership;
- choose appropriate data structures;
- write clean TypeScript;
- produce runnable/testable logic when required;
- model invalid states and errors;
- adapt to a new requirement;
- identify race conditions when relevant;
- justify patterns rather than force them;
- reason about complexity of important operations.

Practice all three formats:
1. class/design discussion;
2. design + working code/tests;
3. extend/refactor an existing codebase.

## HLD readiness

The learner can:
- negotiate functional and non-functional scope;
- estimate scale when useful;
- define API contracts;
- choose a data model from access patterns;
- start with a simple viable architecture;
- justify caching/queues/replication/sharding;
- reason about consistency, duplicates and partial failure;
- discuss reliability, security and observability;
- identify bottlenecks;
- defend trade-offs;
- evolve under increased scale or new constraints.

## ML system-design readiness

The learner can:
- decide whether ML is appropriate;
- translate product goals into an ML task;
- establish a heuristic/non-ML baseline;
- choose product, offline and guardrail metrics;
- define data and labeling strategy;
- prevent leakage;
- reason about sampling/imbalance;
- choose a reasonable representation/model family;
- explain training and offline evaluation;
- design batch/online serving;
- plan online experiments;
- detect train/serve skew and drift;
- define monitoring/retraining;
- identify feedback loops, bias and failure modes.

## GenAI system-design readiness

The learner can:
- decide whether GenAI is appropriate;
- choose among deterministic logic, classical ML, prompt-only, RAG, fine-tuning and agents;
- explain tokens/context/embeddings at interview depth;
- design retrieval/chunking/indexing/reranking;
- handle freshness and access permissions;
- define answer/retrieval quality evaluation;
- reason about hallucination and grounding;
- address prompt injection, PII and guardrails;
- design inference with latency/cost constraints;
- reason about caching, batching, routing and fallbacks;
- design agent/tool failure handling and human escalation;
- include observability/regression monitoring;
- for generative-media prompts, explain relevant model/evaluation pipeline at appropriate depth.

## Mock progression

1. Guided
2. Semi-independent
3. Realistic untimed mock
4. Timed mock

## Domain graduation rule

A domain is interview-ready only when all are true:

1. critical prerequisites are Level 3+;
2. core reasoning skills include multiple Level 4 transfer checks;
3. at least two unfamiliar mocks are completed;
4. at least one mock is timed;
5. one meaningful interviewer curveball is handled;
6. no unresolved critical gap remains;
7. communication is understandable without the mentor reconstructing intent.

Do not average away a critical weakness with strengths elsewhere.
