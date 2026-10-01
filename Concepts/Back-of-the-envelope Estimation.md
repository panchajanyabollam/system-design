---
type: concept
tags: [concept, estimation]
created: 2026-10-01
---

# Back-of-the-envelope Estimation

Quick, rough calculations done **before** designing, to know the scale you're designing for. The numbers decide things like: one database or many? Is a cache needed? How much storage over 5 years?

## What usually gets estimated
- **Traffic:** writes/sec and reads/sec (QPS), plus peak QPS (≈ 2× average)
- **Storage:** records/day × size per record × retention period
- **Bandwidth:** QPS × response size
- **Cache size:** often the 80/20 rule — cache the hottest 20% of daily reads

## Handy numbers
| Quantity | Value |
|----------|-------|
| Seconds in a day | ~86,400 ≈ 10⁵ |
| Seconds in a month | ~2.5 × 10⁶ |
| 1 million requests/day | ≈ 12 requests/sec |

## Used in
- [[TinyURL]] — `Estimations.md` (coming up)

> Reference: [[System Design Interview - An Insider's Guide]], chapter on back-of-the-envelope estimation.
