# Interview Formats & Round Adaptation

Interview fundamentals are stable; round formats are not.

Always adapt to the instructions for the actual interview instead of assuming one universal format.

---

## 1. LLD / OOD formats

### A. Design discussion / whiteboard
Expected output:
- requirements/use cases;
- entities/responsibilities;
- relationships;
- interfaces/contracts;
- key flows;
- extensibility/trade-offs.

Do not spend the entire round coding unless asked.

### B. Greenfield machine coding
Expected output:
- scope clarification;
- runnable core implementation;
- clean structure;
- tests;
- handling of at least one extension/curveball.

Prioritize a working vertical slice over a huge unfinished class diagram.

### C. Existing-codebase extension/refactor
Expected output:
- read unfamiliar code efficiently;
- identify contracts/invariants;
- make a minimal safe change;
- preserve existing behavior;
- add/update tests;
- explain refactoring trade-offs.

Do not rewrite the whole codebase just because the design is imperfect.

---

## 2. HLD formats

### A. Classic 45–60 minute system design
A practical time budget:

| Phase | Typical focus |
|---|---|
| first 5–10 min | scope + NFRs + rough scale |
| next 10 min | APIs/data model + simple architecture |
| middle 20–30 min | 2–3 deep dives forced by requirements |
| final 5–10 min | failures, observability, security/cost, summary |

The exact timing varies. Use it as pacing guidance, not a script.

### B. Architecture review / critique
You may receive an existing design and be asked:
- what breaks?
- what is missing?
- where is the bottleneck?
- how would you migrate it?
- what would you monitor?

### C. Production deep dive
The interviewer asks about a real system you worked on.

Be ready with:
- actual constraints;
- your contribution;
- alternatives rejected;
- incidents/failures;
- metrics;
- what you would change now.

---

## 3. ML System Design formats

Common variations:

### Product-to-ML design
Start from a product objective and derive:
- baseline;
- task;
- labels/data;
- metrics;
- model/representation;
- training;
- serving;
- experimentation;
- monitoring/retraining.

### Ranking/recommendation deep dive
Expect:
- candidate generation;
- features/embeddings;
- ranking;
- offline/online metrics;
- cold start;
- feedback loops;
- latency.

### ML platform / infrastructure
Expect:
- data/versioning;
- feature store;
- training orchestration;
- registry;
- deployment;
- experimentation;
- monitoring.

Do not answer a product-ML prompt as if it were only an infrastructure prompt.

---

## 4. GenAI / LLM System Design formats

### Product application
Choose among:
- deterministic logic;
- classical ML;
- prompt-only;
- RAG;
- fine-tuning;
- agents.

### RAG deep dive
Expect:
- ingestion/chunking;
- retrieval;
- reranking;
- freshness;
- permissions;
- evaluation;
- hallucination/grounding;
- latency/cost.

### Agent/tool-use design
Expect:
- tool contracts;
- permissions;
- state;
- retries/idempotency;
- verification;
- human escalation;
- runaway-loop/cost controls.

### LLM infrastructure
Expect:
- inference serving;
- routing;
- batching;
- caching;
- observability;
- evaluation platform;
- safety;
- multi-tenancy;
- cost controls.

---

## 5. AI-assisted interview variants

Some interview processes may permit, provide or explicitly test AI-assisted development.

The rule is simple:

**Follow the interviewer's/recruiter's policy exactly.**

If AI is allowed:
- state your plan before asking the tool;
- inspect generated output;
- test it;
- explain every important design/code decision;
- catch hallucinations or unsafe changes;
- retain ownership of the solution.

If AI is prohibited:
- do not use it.

A useful AI-assisted workflow is:

```text
PLAN → BUILD → VERIFY → REVIEW
```

The candidate is still responsible for correctness, architecture, tests and trade-offs.

---

## 6. Interviewer curveballs

Expect requirement changes such as:

### LLD
- add a new payment type;
- support concurrency;
- introduce persistence;
- support a new policy/strategy;
- make an operation undoable;
- expose an API.

### HLD
- 10× traffic;
- multi-region;
- strict ordering;
- stronger consistency;
- degraded dependency;
- regulatory/data-residency requirement;
- cost reduction.

### ML
- label delay;
- class imbalance;
- cold start;
- latency target;
- distribution shift;
- fairness/abuse issue.

### GenAI
- private documents;
- stale knowledge;
- prompt injection;
- tool failure;
- hallucination;
- cost spike;
- low retrieval recall;
- multi-tenant permissions.

Curveballs test structure and adaptability, not whether you guessed them upfront.

---

## 7. Before every real interview

Confirm:
- exact round type;
- duration;
- coding language;
- IDE/environment;
- whether code must run;
- whether internet/docs are allowed;
- whether AI assistance is allowed;
- expected seniority/bar;
- whether the round is product design, infra design or resume deep dive.

Do not rely on stale candidate reports when recruiter instructions are available.
