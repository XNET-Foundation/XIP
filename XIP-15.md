# XIP-15: Data-Only Tokenomics

**Authors:** BigManBlastoise  
**Status:** Draft  
**Type:** Tokenomics  
**Revised:** 2026-09-09

## Summary

XNET retires Proof-of-Coverage (PoC) and Enhanced PoC (PoC+). One hundred percent of every epoch emission goes to hotspots that offload verified carrier data. Emissions step down every two years on a Fibonacci divisor schedule.

## Motivation

PoC pays for presence. This pays for utility.

- **Demand-aligned.** Rewards follow real traffic instead of empty coverage.
- **Forecastable.** One formula replaces layered PoC tiers. Operators can model earnings from a single input.
- **Un-gameable.** Location spoofing stops paying, because only moved bytes pay.
- **Scarce.** Fibonacci decay caps long-run supply while preserving an early-operator advantage.

## Reward Rule

Each epoch, every hotspot that offloads at least 1 GB of verified data receives:

```
Reward = (Hotspot GB ÷ Total Network GB) × Epoch Emission
```

Nothing else earns. Hotspots below 1 GB earn zero. Uptime, heartbeats, and coverage earn zero. Hardware without data-offload firmware is ineligible until that firmware ships — this applies equally to cellular and WiFi devices.

### Worked Example

Period 2 epoch emission of 1,250,000 XNET, 10,000 GB total network data:

| Hotspot | Data | Reward |
|---------|-----:|-------:|
| A | 0.8 GB | 0 XNET (below threshold) |
| B | 100 GB | 12,500 XNET |
| C | 1,000 GB | 125,000 XNET |

## Emission Schedule

Epoch emission = `2,500,000 ÷ Fib(n)`, where `n` advances one step every two years. Each period contains 48 epochs.

| Period | Start | Fib(n) | Epoch Emission | Period Total |
|-------:|------:|-------:|---------------:|-------------:|
| 1 | 2025 | 1 | 2,500,000 | 120,000,000 |
| 2 | 2027 | 2 | 1,250,000 | 60,000,000 |
| 3 | 2029 | 3 | 833,334 | 40,000,000 |
| 4 | 2031 | 5 | 500,000 | 24,000,000 |
| 5 | 2033 | 8 | 312,500 | 15,000,000 |
| 6 | 2035 | 13 | 192,308 | 9,230,769 |

**Total:** ~268,230,769 XNET

Successive periods retain 50%, 66.7%, 60%, 62.5%, and 61.5% of the prior emission, converging toward the golden ratio (~0.618) as the sequence advances.

## Implementation and Governance

- **Verification:** cryptographically signed data usage reports.
- **Auditability:** all data transfer rewards visible on the XNET explorer.
- **DAO oversight:** the DAO may vote to adjust the 1 GB threshold or the decay schedule.
