# Mock Interview Playbook

Mocks train **performance under ambiguity and pressure**, not recall of memorized diagrams.

Use with `INTERVIEW_READINESS_RUBRIC.md`.

---

## Progression

1. Guided
2. Semi-independent
3. Realistic untimed
4. Timed

Do not treat a guided solution as mock evidence.

---

## Interviewer rules

In realistic mock mode:

1. Give a short, vague prompt.
2. Stop talking.
3. Let the learner ask questions and drive.
4. Do not volunteer the hidden rubric.
5. Answer only what the interviewer reasonably knows.
6. Introduce at least one meaningful curveball.
7. Push back on one design choice.
8. Ask one failure/operability question.
9. Do not rescue the learner immediately after silence.
10. End with evidence-based feedback.

---

## LLD mock checklist

Observe:
- scope/use-case clarification;
- responsibility modeling;
- relationships/ownership;
- data structures;
- interface quality;
- invalid states;
- code readability;
- runnable core path;
- tests;
- complexity;
- concurrency if relevant;
- extensibility under change.

Possible curveballs:
- new subtype/strategy;
- concurrency;
- persistence;
- cancellation/refund;
- audit/history;
- external service failure;
- new API/consumer.

---

## HLD mock checklist

Observe:
- functional/NFR scope;
- scale assumptions;
- APIs/data model;
- simplest architecture first;
- component justification;
- bottleneck discovery;
- consistency;
- retries/duplicates/order;
- failure/degradation;
- observability;
- security;
- cost;
- 10× evolution.

Possible curveballs:
- regional outage;
- hotspot;
- duplicate event;
- stale read;
- queue backlog;
- database failover;
- cross-region requirement;
- sudden cost constraint.

---

## ML mock checklist

Observe:
- whether ML is needed;
- baseline;
- task framing;
- success metrics;
- labels/data;
- leakage;
- sampling/imbalance;
- representation/model choice;
- training/evaluation;
- serving;
- experimentation;
- drift/feedback loops;
- retraining;
- fairness/privacy/cost.

Possible curveballs:
- labels arrive 30 days late;
- new users/items;
- strong class imbalance;
- metric improves offline but hurts product KPI;
- distribution shifts;
- inference latency doubles.

---

## GenAI mock checklist

Observe:
- approach selection;
- quality criteria;
- knowledge/data;
- retrieval/fine-tune/agent choice;
- evaluation;
- permissions/freshness;
- hallucination/grounding;
- inference architecture;
- safety;
- tool failure;
- observability;
- latency/cost.

Possible curveballs:
- private documents;
- malicious document prompt injection;
- retrieval misses the answer;
- model API outage;
- tool executes twice;
- tenant data leakage risk;
- token cost doubles;
- answer must include verifiable citations.

---

## Resume / production deep-dive mock

Ask:
- What problem did the system solve?
- What was the real scale?
- What did you personally own?
- Why did you choose X?
- Why not Y?
- What failed in production?
- How did you detect it?
- What metric improved?
- What was the cost?
- What would you redesign today?

Do not reward vague "we scaled to millions" claims without defensible numbers.

---

## Feedback format

After a mock:

```text
Mock:
Mode:
Domain:

Strong evidence:
- <rubric dimension>: <specific behavior>

Weak evidence:
- <rubric dimension>: <specific behavior>

Critical gaps:
- <concept ID / skill>

Curveball response:
- ...

Communication:
- ...

Evidence awarded:
- Level 3 / Level 4 / no verification

Highest-impact next action:
- ...

Retry condition:
- ...
```

Feedback should identify 1–2 priorities, not 15 low-value comments.
