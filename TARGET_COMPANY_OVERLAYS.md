# Target-Company & Interview Archetype Overlays

This file changes **priority**, not prerequisite correctness.

Do not memorize candidate-reported questions as guaranteed current interview questions. Historical reports are directional signals only. Recruiter instructions and the current job level/role take precedence.

---

## Overlay A — Big Tech / large product companies

Prioritize:
- structured requirements;
- estimation;
- clean APIs/data models;
- distributed-systems fundamentals;
- consistency/failure reasoning;
- 2–3 deep dives;
- trade-off communication;
- production operability;
- unfamiliar transfer.

For senior roles, increase pressure on:
- ambiguity;
- architecture evolution;
- cost;
- reliability;
- migration;
- organizational/service boundaries;
- "why not X?" defense.

---

## Overlay B — Indian product companies

Common preparation emphasis:
- practical LLD/machine coding;
- runnable code;
- extensibility;
- concurrency;
- HLD fundamentals;
- production reasoning;
- fintech/marketplace/logistics patterns depending on company.

Useful LLD variants:
- booking/inventory;
- payment/ledger;
- notification;
- food ordering;
- scheduling;
- rate limiting;
- matching engines.

---

## Overlay C — Fintech / payments

Increase priority on:
- idempotency;
- money representation;
- double-entry ledger concepts;
- transaction boundaries;
- reconciliation;
- exactly-once business effect vs at-least-once delivery;
- auditability;
- retries/duplicates;
- consistency;
- fraud/risk signals;
- security/permissions;
- failure recovery.

Recommended practice:
- Wallet / BNPL
- ATM
- Payment System
- Digital Wallet
- Splitwise
- Double-entry ledger variant
- Order Matching Engine
- Stock Exchange
- Rate Limiter
- Notification System

---

## Overlay D — Marketplace / food / ride / travel

Increase priority on:
- inventory/availability;
- matching/assignment;
- location/proximity;
- booking consistency;
- state machines;
- cancellation/refund;
- async workflows;
- search/ranking;
- surge/dynamic pricing when ML is involved.

Recommended practice:
- Food Ordering
- Food Delivery Platform
- Ride Sharing
- Hotel Reservation
- Ticket Booking
- Proximity Service
- Search/Recommendation

---

## Overlay E — AI/ML product roles

Prioritize:
- product-to-ML framing;
- metrics;
- data quality;
- experimentation;
- recommendation/ranking/search;
- ML serving;
- monitoring/drift;
- cross-domain HLD + ML.

Avoid over-indexing on model architecture unless the role is explicitly modeling/research-heavy.

---

## Overlay F — GenAI / AI platform roles

Prioritize:
- approach selection;
- RAG;
- evaluation;
- inference serving;
- safety;
- multi-tenancy;
- permissions;
- agents/tools;
- observability;
- cost;
- model routing/fallback;
- cross-domain software + ML/GenAI reasoning.

---

# Historical India-specific directional signals

These are retained from earlier preparation material because they are useful for variation practice.

They are **not official company question banks** and may be stale.

| Company/archetype | Historically reported / useful practice flavor |
|---|---|
| Razorpay-style | Rate Limiter; payment/ledger; ATM; notification; expense/ledger variants |
| Flipkart-style | Event Calendar; food-ordering/machine-coding; judge/platform-style design |
| Navi-style | Stock exchange/order matching; ledger/bookkeeping |
| Cleartrip-style | property/listing/search-domain LLD |
| Udaan-style | dashboard/assignment-style machine coding |
| Swiggy/Zomato-style | food-order lifecycle, partner assignment strategies, state transitions, observer/status updates |

Use them as prompts to test transfer:
- same underlying concept;
- different domain vocabulary;
- different curveball.

---

## How to use an overlay

At profile calibration:

```text
Target:
Role level:
Primary round families:
Priority overlay:
Interview date:
Implementation language:
```

Then adjust:
- case-study order;
- depth;
- mock frequency;
- domain weighting.

Do **not** skip critical prerequisites simply because a company is rumored not to ask them.
