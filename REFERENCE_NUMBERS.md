# Reference Numbers for System Design Interviews

Use this as a **sanity-check sheet**, not as a list of exact constants.

Interview estimation is about:
- stating assumptions;
- showing the formula;
- rounding aggressively;
- checking whether the result is plausible;
- using the result to justify architecture choices.

---

## Time conversions

| Quantity | Approximation |
|---|---:|
| 1 minute | 60 seconds |
| 1 hour | 3,600 seconds |
| 1 day | 86,400 seconds ≈ 100,000 for fast math |
| 1 month | ≈ 2.6 million seconds |
| 1 year | ≈ 31.5 million seconds |

Useful shortcut:

```text
1 million requests/day ≈ 11.6 requests/second average
```

Round to ≈ 12 QPS.

---

## Traffic estimation

```text
average QPS = requests per day / 86,400
peak QPS = average QPS × peak factor
```

When no better evidence exists, state a peak-factor assumption such as 2–3× average and explicitly call it an assumption.

Also estimate:
- read/write ratio;
- burstiness;
- geographic concentration;
- fan-out per request;
- retries;
- background/async traffic.

A "request" to one API can create many downstream operations.

---

## Storage estimation

```text
daily storage = writes/day × bytes/write
retention storage = daily storage × retention days
replicated storage = raw storage × replication factor
```

Quick scale intuition:

| Approximation | Result |
|---|---:|
| 1 KB × 1 million records | ≈ 1 GB |
| 1 KB × 1 billion records | ≈ 1 TB |
| 1 MB × 1 million objects | ≈ 1 TB |

Include:
- indexes;
- metadata;
- replication/erasure coding overhead;
- logs/events;
- backups;
- compression;
- growth margin.

---

## Bandwidth

```text
bandwidth ≈ QPS × payload size
```

Do inbound and outbound separately when they differ.

Example:

```text
10,000 requests/s × 100 KB response
≈ 1 GB/s egress
```

This is often a better architecture signal than raw request count.

---

## Latency order-of-magnitude intuition

These are deliberately rough and environment-dependent.

| Operation | Rough intuition |
|---|---|
| CPU cache access | nanoseconds |
| RAM access | ~100 ns order |
| local SSD random read | ~100 μs order |
| same-datacenter network round trip | sub-ms to low-ms |
| regional service call | low-ms to tens of ms |
| cross-region round trip | tens to 100+ ms |
| internet/mobile request | highly variable, often tens to hundreds of ms |

Do not argue over a tiny constant. Use the order of magnitude to reason about:
- cache vs database access;
- chatty service graphs;
- cross-region consistency;
- fan-out;
- tail latency.

---

## Availability intuition

Approximate annual downtime if availability were distributed evenly:

| Availability | Downtime/year |
|---|---:|
| 99% | ~3.65 days |
| 99.9% | ~8.8 hours |
| 99.99% | ~52.6 minutes |
| 99.999% | ~5.3 minutes |

Interview use:
- ask whether this applies to one component or the end-to-end user journey;
- distinguish availability from durability;
- connect targets to redundancy, failover and cost.

---

## Cache sizing

```text
cache memory ≈ hot objects × average object size
```

Also account for:
- metadata/overhead;
- eviction headroom;
- replicas;
- hot-key skew;
- TTL behavior.

A 95% hit rate does not automatically mean the remaining 5% load is safe for the database.

---

## Database sanity checks

Do not memorize one "QPS per database" number.

Instead state that capacity depends on:
- query complexity;
- indexes;
- read/write mix;
- row/document size;
- transaction isolation;
- connection count;
- hardware;
- caching;
- replication;
- hotspots.

Use estimates to determine whether a single primary is plausible, then discuss measurement/load testing.

---

## ML / GenAI sizing prompts

For ML:
- requests/s;
- feature-fetch latency;
- model inference latency;
- model size;
- batch size;
- training data volume;
- retraining frequency;
- online vs batch traffic.

For GenAI:
- requests/s;
- input tokens/request;
- output tokens/request;
- tokens/second;
- time-to-first-token;
- concurrency;
- model/context size;
- KV-cache memory;
- retrieval fan-out;
- tool calls;
- cost/request.

Useful cost formula:

```text
cost/request
≈ input_tokens × input_token_price
 + output_tokens × output_token_price
 + retrieval/tool/compute costs
```

Always treat prices as provider/model-specific and current-date dependent.

---

## Estimation answer template

```text
1. State the workload assumption.
2. Convert it to average QPS.
3. Apply a justified peak factor.
4. Estimate payload/storage.
5. Identify the likely bottleneck.
6. Sanity-check the result.
7. Explain what architecture decision the number changes.
```

Bad estimation:
> "We have 50K QPS, so we need Kafka."

Better:
> "At 50K peak writes/s, a single transactional primary may become the bottleneck. I would first validate batching/index cost and then consider partitioning or asynchronous ingestion depending on consistency requirements."
