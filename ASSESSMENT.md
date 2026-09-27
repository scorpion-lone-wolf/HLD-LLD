# Assessment & Gap-Filling Protocol

## Principle

**Assume nothing. Verify first.**

Experience, confidence, and previous courses are context, not mastery evidence. Assessment is progressive; do not turn the beginning of the program into one giant exam.

# 1. Profile calibration — not scored

At program start, establish:
- target role(s)
- target seniority
- target companies if known
- expected interview families
- primary implementation language
- interview date only if pacing help is wanted
- 2–3 real systems/projects worth using later in resume deep dives

This changes depth and priority, not prerequisite rules.

# 2. Unified evidence scale

| Level | Status | Meaning |
|---:|---|---|
| U | unassessed | no evidence |
| 0 | unfamiliar | cannot yet explain/use |
| 1 | learning | recognizes after explanation |
| 2 | practicing | uses with guidance |
| 3 | verified | independently applies to a familiar problem |
| 4 | transfer-verified | independently applies to an unfamiliar problem and defends trade-offs |
| R | revisit | prior knowledge needs refresh |

Topic verification is not the same as domain interview readiness.

# 3. Initial baseline — lightweight

Ask one question at a time across only the shared foundations:

1. problem framing / requirements
2. programming + data structures / complexity
3. OOP / modeling
4. API + database/backend fundamentals
5. concurrency / failure reasoning
6. basic system-design reasoning
7. communication / trade-off explanation

When a clear gap appears, stop probing deeper in that branch. Record it and route to the relevant foundation-repair topic.

Do **not** test the whole ML and GenAI curriculum before learning begins.

# 4. Domain-entry assessments

Run only when the learner reaches that domain.

## LLD entry
Check:
- TypeScript essentials
- classes/interfaces/types
- collections
- common Big-O
- OOP responsibilities
- composition vs inheritance
- testing basics

## HLD entry
Check:
- request/response lifecycle
- HTTP/API basics
- SQL basics
- indexes/transactions
- concurrency intuition
- latency vs throughput
- basic cache/queue intuition

## ML entry
Check:
- classification/regression/ranking
- features/labels
- train/validation/test
- overfitting
- probability/statistics intuition
- precision/recall
- baseline thinking

## GenAI entry
Check:
- tokens/context
- vectors/embeddings
- similarity search
- neural-network/transformer intuition
- training vs inference
- evaluation thinking

# 5. Targeted micro-diagnostic

When a later answer exposes a hidden gap, test that prerequisite directly.

Example:
```text
sharding unclear
  ↓
check indexes + transactions + replication
  ↓
teach missing prerequisite
  ↓
practice + transfer
  ↓
resume sharding
```

Example:
```text
RAG unclear
  ↓
check embeddings + retrieval + ranking metrics
  ↓
repair
  ↓
verify
  ↓
resume RAG
```

# 6. Fast-pass rule

A topic may be fast-passed only with evidence:
- explanation in own words;
- one correct application;
- one edge case/trade-off or transfer check.

Critical prerequisites should normally be Level 3+ before dependent advanced topics.

# 7. Gap-filling protocol

1. identify the missing prerequisite;
2. explain why it blocks the current topic;
3. save the interrupted topic;
4. teach the minimum complete foundation;
5. practice it;
6. transfer-check it;
7. update `PROGRESS.md`;
8. resume the interrupted topic.

# 8. Retention checks

Use lightweight recall:
- after 2–4 related topics;
- before a dependent case study;
- during mocks;
- after a long break.

If recall materially fails, mark the topic `revisit` and repair it before relying on it.

# 9. Reassessment triggers

Reassess when:
- a mastery gate is reached;
- repeated hints are required;
- a case study reveals a hidden gap;
- the learner returns after a long break;
- target role/company changes;
- the learner reports that a supposedly known topic is unclear.

Assessment is diagnostic, not punitive.
