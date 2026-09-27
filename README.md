# Unified Design Interview Preparation

An **assessment-first, prerequisite-driven interview system** for engineers preparing for modern design interviews.

It covers four major technical interview tracks plus the production/resume round:

- **Software LLD / OOD / machine coding** — TypeScript / Node.js by default
- **Software HLD / distributed systems**
- **Machine Learning System Design**
- **Generative AI / LLM System Design**
- **Cross-domain systems** that combine software, ML and GenAI
- **Resume / production-system deep dives**
- **Realistic mock interviews** with evidence-based readiness gates

> Scope: this repository is for design-interview readiness. DSA/coding screens, behavioral interviews, SQL-only rounds and aptitude rounds are separate tracks unless explicitly added later.

---

## Design principles

This repository is not a fixed course to "finish." It is an interview-performance system.

```text
profile calibration
      ↓
lightweight baseline
      ↓
prerequisite repair only where needed
      ↓
concept teaching
      ↓
learner attempt
      ↓
transfer check
      ↓
retention recall
      ↓
case-study ladder
      ↓
realistic mocks
      ↓
evidence-based readiness
```

Core rules:

1. **Assume nothing; verify first.**
2. **Do not over-assess.** Test only enough to find the next useful learning step.
3. **Fast-pass demonstrated knowledge.**
4. **Repair missing prerequisites immediately, then resume the exact interrupted topic.**
5. **Start with the simplest valid design.** Add complexity only when a requirement forces it.
6. **Do not reward technology or model name-dropping.**
7. **Readiness requires transfer to unfamiliar problems**, not lesson completion.
8. **No fixed daily duration.** Stop and resume from the exact saved state.
9. **Every major design choice must be explainable as requirement → decision → trade-off.**
10. **Every revision must preserve prior concept and problem coverage.**

---

## Interview tracks

### 1. LLD / OOD / machine coding

You should be able to:

- clarify requirements before coding;
- identify responsibilities, entities and ownership;
- model relationships and invalid states;
- choose useful patterns without forcing them;
- write clean, runnable, testable TypeScript;
- reason about complexity and concurrency;
- extend a design when the interviewer changes a requirement;
- work in all three common modes:
  - design discussion;
  - greenfield design + runnable code/tests;
  - existing-codebase extension/refactor.

### 2. HLD / distributed systems

You should be able to:

- negotiate functional and non-functional requirements;
- estimate scale;
- derive APIs and data models from access patterns;
- produce the simplest viable architecture first;
- identify bottlenecks and failure modes;
- reason about caching, queues, replication, partitioning and consistency;
- handle retries, duplicates, ordering and partial failure;
- discuss deployment, observability, security and cost;
- deep-dive into storage engines, consensus, real-time communication and stream/batch processing when relevant.

### 3. ML System Design

You should be able to:

- decide whether ML is appropriate at all;
- define a non-ML baseline;
- frame the prediction/ranking/recommendation task;
- choose product, offline and guardrail metrics;
- design data and labeling pipelines;
- prevent leakage and train/serve skew;
- select a reasonable representation/model family;
- design training, serving and experimentation;
- detect drift and feedback loops;
- reason about retraining, fairness, abuse, privacy, latency and cost.

### 4. GenAI / LLM System Design

You should be able to:

- choose among deterministic software, classical ML, prompt-only LLM, RAG, fine-tuning and agents;
- reason about tokens, context, embeddings, retrieval and transformers at interview depth;
- design RAG with chunking, retrieval, reranking, permissions and freshness;
- define evaluation before claiming quality;
- design inference for latency, throughput and cost;
- handle prompt injection, PII, tool permissions and output validation;
- design agents with verification, retries/idempotency and human escalation;
- reason about long context, memory, multimodality and generative-media systems when relevant.

---

## Canonical runtime sources

Read these in this order when mentoring or resuming study:

1. `SESSION_STATE.md`
2. `PROGRESS.md`
3. `ASSESSMENT.md`
4. `PREREQUISITE_MAP.md`
5. `INTERVIEW_CURRICULUM.md`
6. `INTERVIEW_READINESS_RUBRIC.md`
7. `HLD_LLD_Prompt.md`

### Supporting references

Use these when relevant; they are not a replacement for the canonical curriculum:

- `INTERVIEW_FORMATS.md` — round variants, time-management templates and AI-assisted-round rules
- `MOCK_PLAYBOOK.md` — realistic mock structure and curveballs
- `REFERENCE_NUMBERS.md` — estimation formulas and order-of-magnitude references
- `TARGET_COMPANY_OVERLAYS.md` — target-company/archetype prioritization and historical directional signals
- `RESOURCES.md` — curated backup references
- `LEGACY_COVERAGE_MANIFEST.md` — concept-preservation audit for future revisions

---

## Evidence model

`PROGRESS.md` uses the same scale everywhere:

| Level | Meaning |
|---:|---|
| U | unassessed |
| 0 | unfamiliar |
| 1 | learning / recognizes after explanation |
| 2 | practices with guidance |
| 3 | independently applies to a familiar problem |
| 4 | independently transfers to an unfamiliar problem and defends trade-offs |
| R | revisit required |

A domain is **not interview-ready** merely because its lessons are complete.

Readiness requires:

- critical prerequisites at Level 3+;
- multiple Level 4 transfer checks;
- unfamiliar mocks;
- at least one timed mock;
- handling a meaningful interviewer curveball;
- no unresolved critical gap;
- communication that is understandable without the mentor reconstructing the learner's reasoning.

---

## Case-study policy

Problem banks provide **coverage**, not memorized solutions.

For each case:

1. start from a short, ambiguous interviewer-style prompt;
2. let the learner drive;
3. reveal constraints progressively;
4. require explicit trade-offs;
5. introduce at least one curveball in mock mode;
6. use references only after the learner has attempted the problem;
7. route weaknesses back to exact prerequisite IDs.

The curriculum retains a permanent legacy bank of **125 interview problem titles** across LLD, HLD, ML and GenAI.

---

## Superset guarantee

Future revisions must preserve **both**:

1. **concept/capability coverage**, tracked by `LEGACY_COVERAGE_MANIFEST.md`;
2. **problem-title coverage**, preserved in `INTERVIEW_CURRICULUM.md`.

A topic may be renamed, regrouped or moved, but it must remain discoverable through an explicit alias or mapping.

No revision is complete until the legacy manifest has been checked.

---

## Language policy

Default LLD / machine-coding language: **TypeScript / Node.js**.

The design principles are language-independent. If a target interview requires another language, keep the same modeling/testability bar and switch only the implementation syntax.

---

## Pacing

There is **no fixed 6–7 week requirement**.

Pacing is driven by:

- current evidence;
- available study time;
- interview date if one exists;
- target role/seniority;
- target-company overlay;
- retention quality;
- mock performance.

Short sessions are valid. The repository must preserve the exact next action so study can resume without reconstructing context.
