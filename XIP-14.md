# XIP-14: Fractals Receivables Financing for XNET

**Authors:** Fractals  
**Status:** In Development  
**Type:** Ecosystem / Operator Financing  
**Created:** 2026-07-02  
**Updated:** 2026-07-23

## Abstract

This program applies only to XNET enterprise payments (carrier offload revenue). It does not apply to token emissions or other non-enterprise payouts.

Fractals is developing a receivables financing program to help accelerate cash flow for XNET deployers. The program gives deployers the option to opt in to accelerated payments against earned carrier receivables, rather than waiting for the normal carrier reconciliation and settlement cycle.

Participation is entirely optional. Deployers who do not opt in continue receiving distributions on the existing settlement schedule.

## Motivation

XNET earns carrier offload revenue as traffic is generated across the network, but those payments are typically received after the carrier reconciliation and settlement cycle. Traffic generated throughout a given month is reconciled at month-end and generally paid by the carrier approximately 60 days later. Depending on when traffic was generated, deployers may wait between 60 and 90 days before receiving cash for revenue earned today.

XNET deployers deploy and maintain real-world telecom infrastructure. That requires upfront capital, ongoing maintenance, and the ability to reinvest as the network grows. Waiting months for earned revenue can slow down expansion.

Fractals aims to solve this timing gap by offering deployers the option to receive accelerated payments against earned receivables. Through this receivables financing program, Fractals can help deployers access cash sooner, improve working capital, and reinvest faster into their XNET deployments.

The goal is not to change XNET's core economics or carrier relationships. The goal is simply to give deployers more flexibility around when they receive their earned revenue.

## Opt-In Participation

Deployers may elect to receive accelerated payments in exchange for a financing fee.

- **Opt-in:** Deployers who choose to participate receive accelerated distributions against their allocated portion of eligible receivables.
- **Opt-out / default:** Deployers who do not participate continue receiving distributions according to the existing carrier settlement schedule.

No deployer is required to participate. The financing program does not alter tokenomics, emissions, or non-participating payouts.

## Pricing & Fees

The financing program charges a **9.5% financing fee** for deployers who elect to receive accelerated payment.

The fee is designed around the existing carrier settlement cycle:

- Revenue is reconciled at month-end
- Carrier payment typically follows approximately **net-60** timing
- An additional **15-day** payment buffer applies
- By advancing funds at the end of each month, Fractals is effectively financing receivables for approximately **75 days**

Because carrier revenue is earned continuously throughout the month, the effective financing period varies slightly by when traffic was generated. The 9.5% fee reflects the economics of advancing a deployer's entire monthly receivable as a single monthly payment, rather than pricing individual traffic events independently.

### Example

A deployer earns **$1,000** in offload during the month of June and has two choices:

| Option | Amount | Timing |
|--------|-------:|--------|
| **Standard settlement** | $1,000 | Claim between approximately August 30 and mid-September (up to ~75 days after month-end) |
| **Accelerated settlement** | $905 | Claim by June 30 (9.5% financing fee) |

### Participant Economics

| Participant | Economics |
|-------------|-----------|
| **Deployers** | Exchange a portion of future revenue for accelerated access to cash |
| **Fractals** | Earns financing fees for originating, administering, reconciling, and servicing financed receivables |
| **XNET** | Improves deployer liquidity without requiring direct subsidy or changes to network economics |

## How It Works

The initial implementation is expected to support **monthly advances**. Future updates could support weekly or daily advances.

At a high level:

1. Carrier offload traffic is generated across the XNET network.
2. Carrier revenue is reported and reconciled through existing systems.
3. Operator / deployer allocations are calculated using XNET's existing distribution methodology.
4. Participating (opted-in) deployers are identified.
5. Fractals advances capital against eligible receivables.
6. Accelerated payments are distributed to participating deployers (via Fractals Sync for distributions).
7. Carrier payment is received on the normal settlement cycle.
8. Fractals reconciles financed receivables and settles financing positions.

### Funding

The initial deployment is expected to be funded directly from Fractals' treasury. As financing demand grows, Fractals may expand capacity through institutional and, where appropriate, third-party capital, while maintaining the same deployer experience and settlement workflow.

## Summary

Fractals receivables financing gives XNET deployers a simple choice: wait for the normal carrier settlement cycle, or opt in to receive accelerated payment on eligible earned revenue for a 9.5% financing fee.

The purpose is straightforward: improve deployer liquidity, reduce the friction created by delayed settlement cycles, and help XNET infrastructure grow faster.
