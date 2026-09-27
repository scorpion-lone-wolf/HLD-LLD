# Interview Readiness Rubric

The learner is interview-ready only when performance is repeatable across unfamiliar prompts.

# Universal dimensions

| Dimension | Ready behavior |
|---|---|
| Requirements | Clarifies scope before solutioning |
| Communication | Thinks aloud with structure |
| Assumptions | States and validates assumptions |
| Trade-offs | Compares realistic alternatives |
| Simplicity | Starts simple, adds complexity only when needed |
| Verification | Defines how correctness/success will be checked |
| Adaptability | Handles interviewer curveballs without collapsing the design |

# LLD readiness

The learner can:
- clarify scope;
- identify core objects/responsibilities;
- model relationships correctly;
- choose appropriate collections/data structures;
- write clean TypeScript;
- produce runnable/testable core logic;
- handle errors and invalid states;
- adapt to new requirements;
- identify concurrency issues when relevant;
- use patterns because they fit, not to show them off.

# HLD readiness

The learner can:
- define functional and non-functional requirements;
- estimate scale when useful;
- design APIs;
- model data around access patterns;
- start from a simple architecture;
- introduce caching/queues/sharding/etc. only when justified;
- reason about consistency and partial failure;
- discuss reliability and observability;
- identify bottlenecks;
- defend trade-offs;
- evolve the design under 10x/100x constraints.

# ML system-design readiness

The learner can:
- translate product goal into ML task;
- decide whether ML is appropriate;
- establish heuristic/baseline;
- choose product + offline metrics;
- explain data/label strategy;
- prevent leakage;
- choose reasonable feature/representation and model family;
- design training pipeline;
- design online/batch serving;
- plan A/B testing;
- monitor data/model drift;
- define retraining strategy;
- reason about feedback loops and bias.

# GenAI system-design readiness

The learner can:
- decide whether LLMs are appropriate;
- choose prompt-only vs RAG vs fine-tuning vs agents;
- explain retrieval/indexing/chunking/reranking;
- design quality evaluation;
- address hallucination/grounding;
- address prompt injection/permissions/PII;
- reason about context limits;
- design serving with latency/cost considerations;
- reason about caching/model routing/fallbacks;
- design tool/agent failure handling;
- include observability;
- define human escalation where needed.

# Mock-interview graduation rule

Do not call a domain interview-ready based on one strong mock.

Require:
- at least two unfamiliar prompts;
- independent structure;
- no critical prerequisite gap;
- reasonable trade-off defense;
- one curveball handled;
- communication that would be understandable to an interviewer.

The purpose is not a numerical badge. It is evidence that the performance transfers.
