---
title: "XIP-13-A: XNET Token Design Proposal"
sidebar_position: 15
---

# XIP-13-A: XNET Token Design Proposal

The aim of this proposal is to allow the Foundation to decide when to buy tokens off the open market, or alternatively, accrue that fiat value in a Foundation Treasury Book. This treasury book would directly support both the operation of the Foundation and the value of the token itself.

There are a number of benefits expected from this mechanism:

- Allow the Foundation to build a fiat & digital asset treasury book to support the value of the token.
- Reduce the incentivisation of short-term investors and accrue value for long-term holders of the token. This will align token holders with long-term objectives of XNET, to create a sustainable ecosystem and retain flexibility as the treasury grows.
- Allow certain Operators to be paid directly in fiat currency at the determined Clearing Price (minus a fee/discount) for the token at that epoch. This would effectively allow them to participate in a Shared Revenue model, while we still support the tokenomics of the project.
- Initially, these larger operators are expected to be defined as having > 1TB data offload per day, on average.
- Improve the governance of the token by encouraging holders to stake their tokens to facilitate voting control over the treasury pool. Align governance with long-term objectives of XNET to hold $XNET tokens, participate in governance operations/improvements and to grow the overall XNET ecosystem.

## Mechanism

The key metric to determine this facility is the Clearing Price of the token (sometimes referred to as the Base Price in other documents). This Clearing Price is determined each month by the simple formula:

```
Clearing Price = Total BuyBack Value in that month / Total Emitted Tokens in that month
```

These figures have to be calculated monthly, and not by epoch, as payments are actually received on a monthly cadence. The monthly tokens can be relatively easily calculated using the scheduled epoch emission charts and a simple aggregation by month (see Appendix B: Monthly Emitted Tokens).

The proposal is to use this Clearing Price to calculate potential fiat payments for certain Operators, in lieu of $XNET distributions. Crucially, the token distributions still take place, supporting the entire tokenomics, but these Operators can onboard and treat the monthly fiat flow as an effective revenue-sharing mechanism (see detail below).

## Current Scenario - Worked Example

Assuming that $100,000 is received for data offload in a particular month from clients (MNOs/MVNOs). This means that:

- $20,000 (20%) is kept by XNET to cover operational costs
- $20,000 (20%) is used by the Foundation for Market Liquidity support
- $60,000 (60%) is used by the Foundation for BuyBack & Burn

The $60k is gone forever as it cashes out either 1) a Deployer (a good thing), or 2) a Seller/Speculator.

The $20k used by the Foundation for Liquidity support at least builds some book value in USDC/XNET or SOL/XNET.  This stays with the treasury and builds over time to back the token book value.

## Proposed Scenario - Worked Example

Assuming that $100,000 is received for data offload in a particular month from clients (MNOs/MVNOs). It is proposed that:

- $20,000 (20%) is kept by XNET to cover operational costs (as before)
- $20,000 (20%) is used by the Foundation for Market Liquidity support (as before)
- $60,000 (60%) is used by the Foundation for token acquisition or fiat pooling

Crucially, the tokens acquired by the Foundation are either at:

- the Clearing Price from larger operators, minus a facilitation fee
- the Market Price from exchanges, up to the Clearing Price of the token

However, in neither case are the tokens sent to a Burn mechanism. Instead, they are accrued in the Foundation Treasury Book, supporting the value of the token.

If the Market Token Price is greater than the Clearing Price then the Foundation could accrue those fiat values in USDC in the Treasury Book, thus supporting the overall token valuation.

Any accrued $XNET tokens could be used at a later date for various purposes,e.g.

- Opportunistic trading on exchanges for values in USDC/SOL
- Swap equity with a synergistic business or protocol
- Issue a convertible note paid in $XNET tokens
- Incentivise a large deployer with a future piece of equity

In this scenario $80,000 is staying with the XNET protocol to raise the floor value of the token, while keeping in place the buying pressure from buybacks. The difference is we aren't burning an asset.

## Clearing Price - Worked Example

So by example, if the total offload revenue in a month is $100,000, then the BuyBack Value for that month would be ($100,000 * 80%) = $80,000 (using current parameters).

The monthly emitted tokens can be calculated using the appropriate epoch emitted tokens, corrected for that particular month. For instance, for May 2026, the monthly emitted tokens can be calculated as (2,500,000 * 2 * 31/28) = 5,535,714 $XNET.

In this example the Clearing Price for that month would be:

```
Clearing Price = $80,000 / 5,535,714 = $0.015
```

This Clearing Price could only be calculated in any month once the paid offload numbers are available for that month. That said, these numbers should be predicted a couple of months ahead based on expected revenues, i.e. from data offload already done.

For certain designated Operators, they may choose to be paid only in fiat currency. The value to be paid to these Operators would be their assigned tokens in that period multiplied by the Clearing Price, minus a small fee. It is assumed that these large Operators would be comfortable being paid monthly in arrears.

## Foundation Treasury Book

### Token BuyBack executed up to the Clearing Price for each Month

The proposal is that if the current $XNET market price is greater than the Clearing Price then the BuyBack value for that month is not used to buy tokens off the open market. Instead, that value would be transferred to a Foundation Treasury Book.

A portion of the BuyBack value in any month may be used for open market token purchases, and a portion diverted to the Foundation Treasury Book. This would be determined by the fluctuating open market value of the token during the BuyBack process.

In the example Clearing Price from above of $0.015, the Foundation would buy tokens up to this price off the open market but once that price is exceeded, it would divert the funds to the treasury book.

The Foundation Treasury Book would be used primarily to support the value of the $XNET token. This could be done either as an assigned value per token (Treasury Book value / Total Emitted tokens in circulation), or by later tactical trading support on the open market.

The usage of the Treasury Book funds would be determined by staked voting of token holders.

### Foundation Operational Expenses

The Foundation would use some portion of the treasury pool funds to cover ongoing operational costs. These costs should be a small percentage of the overall value of the pool. Some Foundation expenses may be payable in $XNET tokens from the Foundation accrued values.

### Treasury Book Value

By accruing value into a Foundation Treasury Book, this should directly support the book value of the total emitted tokens in circulation.

The remaining cash, after BuyBack and operating expenses, is kept in the treasury book. The $XNET token value drivers are the ongoing BuyBack (Cost of Goods Sold) values + Treasury Assets (Book Value). The Book Value raises the token price floor permanently and can consist of USDC, SOL, BTC, TAO, etc., as decided by Governance.

Treasury assets are an important driver of long-term value as they provide a floor for the $XNET token, and protect the business and stakeholders in the long term.

## Fiat Payments to large Operators

For certain large Operators, particularly larger corporations such as ISPs and MSPs, there is a strong desire by them to be paid in fiat currency, not tokens. They have great difficulty accruing tokens of any sort on their balance sheet. They would need monthly fiat payments instead.

To date, there has been work to create a mechanism to translate the tokens provided to an operator in any epoch into an equivalent fiat currency value. This would seem to require an open market sale of the tokens, or the sale via a liquidity provider such as a large market maker. Such discussions are ongoing. Once the $XNET token is listed on a CEX, such mechanisms should be able to be supported.

However, there is a much simpler mechanism available by using the Clearing Price associated with the month. The Foundation could choose to divert some of the funds from the BuyBack route to direct fiat payments to such Operators. These payments would be at the Clearing Price, less a facilitation fee.

The calculation of the payment due to an operator in any month under such a mechanism would be:

```
Operator Payment = ( Operator Tokens * Clearing Price )
- Facilitation Fee
```

The tokens assigned to an Operator in any month is made up of Data Offload tokens + Proof of Coverage tokens. Most of the tokens are assigned for data offload (70%), with the remainder (30%) for PoC.

The total data offload for an operator is usually correlated with their total number of AP units, particularly those serving enough data to earn the Enhanced PoC reward (> 3GB). This means that a fair assumption is that the total number of tokens received by an Operator is proportional to their data offload. Based on this assumption, we can approximate the number of tokens received by an operator in any month as:

```
Operator Tokens = ( Operator GB Offload / Total GB Offload )
* Total Emitted Tokens
```

Given that the Clearing Price for any month is defined by:

```
Clearing Price = Total BuyBack Value / Total Emitted Tokens
```

This means that the Operator Payment in any month simplifies to:

```
Operator Payment = ( Operator GB Offload / Total GB Offload )
* Total Offload Value
* ( BuyBack Revenue Percentage - Facilitation Fee)
```

In this mechanism, the Foundation would receive the equivalent tokens for this Operator's payment. These tokens would be transferred to the Foundation Treasury for later use (e.g. they could be sold at favourable market conditions). The real value of this mechanism is the ability to avoid any purchase or sale of tokens to facilitate the fiat payment, while still supporting the distribution of tokens for the operator, albeit to the Foundation.

For these Operators, this simplified formula means that they effectively participate in a Shared Revenue mechanism with XNET.

We can define an important parameter that we can share with operators every month:

```
XNET Offload Blended Price = Total Offload Value / Total GB Offload
```

Therefore for any particular month, the Operator can calculate:

```
Operator Payment =  ( Operator GB Offload * XNET Offload Blended Price )
* ( BuyBack Revenue Percentage - Facilitation Fee)
```

A key point for this mechanism is the ability to accrue value to the XNET token via fee/discount by providing the fiat bypass service for large operators. Our deployers not using this mechanism are transacting in thin markets with large slippage depending on size, so a facilitation fee of 5% is not unreasonable. If business continues to grow, it's possible XNET trades above the Clearing Price, paying deployers a premium for not using the fiat bypass.

The BuyBack Revenue Percentage is currently 80%. This means that 80% of any received offload revenue is passed to the Foundation. Using the Facilitation Fee value of 5% above, this would mean the Operator Payment would be:

```
Operator Payment = (Operator GB Offload * XNET Offload Blended Price) * 75%
```

The assumption in this version of the XIP is that all tokens assigned to the fiat operator, both Data and PoC, are transferred to the Treasury Book.

Please refer to Appendix C: Operator Payment Calculations to see this represented in short-hand mathematically.

## Receivables Financing & Accelerated Settlement

Certain Operators, particularly ISPs, MSPs, enterprise deployments, and venue owners, may require more frequent and predictable cash flows than underlying carrier or enterprise payment cycles provide.

To support network growth, the Foundation may permit approved third-party financing providers to offer optional receivables financing, factoring, or accelerated settlement facilities to Operators.

Such providers may underwrite future Operator receivables using factors including historical offload performance, assigned token emissions, Clearing Price calculations, expected Offload Revenue, and other network metrics.

Participation in any financing arrangement shall be voluntary and independent of the Operator reward mechanism. The Foundation shall not be required to guarantee any financing facility provided by a third party.

Examples of potential financing providers may include infrastructure finance platforms, credit funds, or ecosystem participants such as Fractals.

## Token Governance

Once the Foundation holds a sizable Treasury Book value, there will be more interest in token holders to participate in decisions on the control of such funds.

By principal, we wish that long-term, impactful decisions should be made by long-term stakeholders and deployers. It is expected that the voting will be aligned to long-term staking of the $XNET token.

A principled formula must be agreed upon that aligns governance power to Stake × Duration, ensuring active deployers are represented.

## Appendix A: Historical Data

| Month | Epoch Tokens | Adjusted Monthly Tokens | Projected Offload Payment | GB Offloaded | Blended Offload Price (per GB) | Clearing Price (per token) |
|-------|-------------:|------------------------:|--------------------------:|-------------:|-------------------------------:|---------------------------:|
| Jan 2025 | 2,500,000 | 5,535,714 | $1,396.92 | 13,969 | $0.1000 | $0.0002 |
| Feb 2025 | 2,500,000 | 5,000,000 | $1,704.18 | 17,042 | $0.1000 | $0.0003 |
| Mar 2025 | 2,500,000 | 5,535,714 | $2,118.10 | 21,180 | $0.1000 | $0.0003 |
| Apr 2025 | 2,500,000 | 5,357,143 | $2,539.17 | 25,393 | $0.1000 | $0.0004 |
| May 2025 | 2,500,000 | 5,535,714 | $2,333.24 | 23,335 | $0.1000 | $0.0003 |
| Jun 2025 | 2,500,000 | 5,357,143 | $2,466.38 | 24,668 | $0.1000 | $0.0004 |
| Jul 2025 | 2,500,000 | 5,535,714 | $4,337.78 | 43,381 | $0.1000 | $0.0006 |
| Aug 2025 | 2,500,000 | 5,535,714 | $3,747.07 | 37,475 | $0.1000 | $0.0005 |
| Sep 2025 | 2,500,000 | 5,357,143 | $5,370.97 | 53,716 | $0.1000 | $0.0008 |
| Oct 2025 | 2,500,000 | 5,535,714 | $7,472.60 | 74,733 | $0.1000 | $0.0011 |
| Nov 2025 | 2,500,000 | 5,357,143 | $5,028.81 | 50,291 | $0.1000 | $0.0008 |
| Dec 2025 | 2,500,000 | 5,535,714 | $7,865.43 | 78,654 | $0.1000 | $0.0011 |
| Jan 2026 | 2,500,000 | 5,535,714 | $9,707.31 | 71,773 | $0.1353 | $0.0014 |
| Feb 2026 | 2,500,000 | 5,000,000 | $11,915.76 | 89,560 | $0.1330 | $0.0019 |
| Mar 2026 | 2,500,000 | 5,535,714 | $14,957.00 | 121,921 | $0.1227 | $0.0022 |
| Apr 2026 | 2,500,000 | 5,357,143 | $24,248.53 | 154,963 | $0.1565 | $0.0036 |
| May 2026 | 2,500,000 | 5,535,714 | $32,758.38 | 197,495 | $0.1659 | $0.0047 |

## Appendix B: Monthly Emitted Tokens

| Month | Epoch Tokens | Adjusted Monthly Tokens |
|-------|-------------:|------------------------:|
| Jul 2026 | 2,500,000 | 5,535,714 |
| Aug 2026 | 2,500,000 | 5,535,714 |
| Sep 2026 | 2,500,000 | 5,357,143 |
| Oct 2026 | 2,500,000 | 5,535,714 |
| Nov 2026 | 2,500,000 | 5,357,143 |
| Dec 2026 | 2,500,000 | 5,535,714 |
| Jan 2027 | 1,250,000 | 2,767,857 |
| Feb 2027 | 1,250,000 | 2,500,000 |
| Mar 2027 | 1,250,000 | 2,767,857 |
| Apr 2027 | 1,250,000 | 2,678,571 |
| May 2027 | 1,250,000 | 2,767,857 |
| Jun 2027 | 1,250,000 | 2,678,571 |
| Jul 2027 | 1,250,000 | 2,767,857 |
| Aug 2027 | 1,250,000 | 2,767,857 |
| Sep 2027 | 1,250,000 | 2,678,571 |
| Oct 2027 | 1,250,000 | 2,767,857 |
| Nov 2027 | 1,250,000 | 2,678,571 |
| Dec 2027 | 1,250,000 | 2,767,857 |
| Jan 2028 | 1,250,000 | 2,767,857 |
| Feb 2028 | 1,250,000 | 2,500,000 |
| Mar 2028 | 1,250,000 | 2,767,857 |
| Apr 2028 | 1,250,000 | 2,678,571 |
| May 2028 | 1,250,000 | 2,767,857 |
| Jun 2028 | 1,250,000 | 2,678,571 |
| Jul 2028 | 1,250,000 | 2,767,857 |
| Aug 2028 | 1,250,000 | 2,767,857 |
| Sep 2028 | 1,250,000 | 2,678,571 |
| Oct 2028 | 1,250,000 | 2,767,857 |
| Nov 2028 | 1,250,000 | 2,678,571 |
| Dec 2028 | 1,250,000 | 2,767,857 |
| Jan 2029 | 833,334 | 1,845,240 |
| Feb 2029 | 833,334 | 1,666,668 |
| Mar 2029 | 833,334 | 1,845,240 |
| Apr 2029 | 833,334 | 1,785,716 |
| May 2029 | 833,334 | 1,845,240 |
| Jun 2029 | 833,334 | 1,785,716 |
| Jul 2029 | 833,334 | 1,845,240 |
| Aug 2029 | 833,334 | 1,845,240 |
| Sep 2029 | 833,334 | 1,785,716 |
| Oct 2029 | 833,334 | 1,845,240 |
| Nov 2029 | 833,334 | 1,785,716 |
| Dec 2029 | 833,334 | 1,845,240 |
| Jan 2030 | 833,334 | 1,845,240 |
| Feb 2030 | 833,334 | 1,666,668 |
| Mar 2030 | 833,334 | 1,845,240 |
| Apr 2030 | 833,334 | 1,785,716 |
| May 2030 | 833,334 | 1,845,240 |
| Jun 2030 | 833,334 | 1,785,716 |
| Jul 2030 | 833,334 | 1,845,240 |
| Aug 2030 | 833,334 | 1,845,240 |
| Sep 2030 | 833,334 | 1,785,716 |
| Oct 2030 | 833,334 | 1,845,240 |
| Nov 2030 | 833,334 | 1,785,716 |
| Dec 2030 | 833,334 | 1,845,240 |

## Appendix C: Operator Payment Calculations

The calculations below are a reformulation of the calculations in the text above, but using short-hand mathematical representation. All values below refer to Monthly totals rather than per epoch.

### Definitions

- A = Total BuyBack Value
- B = Total Emitted Tokens
- C = Total Offload Value
- D = Total Offload measured in GB
- E = Operator Offload measured in GB
- F = Operator Assigned Tokens
- G = Facilitation Fee
- CP = Clearing Price (per token)
- BP = XNET Offload Blended Price (per GB)
- BRP = BuyBack Revenue Percentage (currently 80%)
- OP = Operator Payment

### Calculations

```
OP = ( F * CP ) - G
```

However, by definition:

```
CP = A / B
∴ OP = (F * A) / B - G
```

Given the strong correlation of the total tokens given to an operator to their total offload GB (see main-body text) we have:

```
F ≈ ( E / D ) * B
∴ OP = ( ( E / D ) * B * A / B ) - G = ( E * A ) / D - G
```

However, by definition:

```
BP = C / D
∴ D = C / BP
∴ OP = ( E * A ) / (C / BP) - G = ( E * A * BP) / C - G
```

However, by definition:

```
A = C * BRP
∴ OP = ( E * C * BRP * BP) / C - G = (E * BRP * BP) - G
```

Importantly, this equation is independent of any token-related parameters.

If we assume that the Facilitation Fee (G) can be represented as a percentage, then we have:

```
OP = (E * BP) * (BRP - G)
```

Assuming a BuyBack Revenue Percentage (BRP) of 80% and a Facilitation Fee (G) of 5%, the would give us the simplified:

```
OP = (E * BP) * (80% - 5%) = (E * BP) * 75%
```

```
Operator Payment = (Operator Offload * XNET Offload Blended Price) * 75%
```

## Appendix D: Projected Example Clearing Prices

The table below represents possible scenarios for projected offload and associated revenues. Based on these projections, we can calculate the fiat price per GB that could be offered to operators that opt for fiat payments instead of tokens. This assumes the 75% share of the Blended Offload price per GB (refer to main-body text).

We can also calculate the Clearing Price based on these projections. This is effectively the support price used by the Foundation to buy tokens off the open market up to that value, or accrue fiat values in the Foundation Treasury Book where the market price is above that value.

The month of May 2026 are actuals, all other months are projections. These projections are indicative only.

| Month | Adjusted Monthly Tokens | Total Offload GB (Projected) | Total Offload Value (Projected) | Offload Blended Price (per GB) | Offload Fiat Price (per GB) | Clearing Price (per Token) |
|-------|------------------------:|-----------------------------:|--------------------------------:|-------------------------------:|----------------------------:|---------------------------:|
| May 2026 | 5,535,714 | 197,495 | $32,758 | $0.1600 | $0.1200 | $0.0047 |
| Jun 2026 | 5,357,143 | 230,000 | $36,800 | $0.1600 | $0.1200 | $0.0055 |
| Sep 2026 | 5,357,143 | 300,000 | $48,000 | $0.1600 | $0.1200 | $0.0072 |
| Dec 2026 | 5,535,714 | 400,000 | $64,000 | $0.1600 | $0.1200 | $0.0092 |
| Mar 2027 | 2,767,857 | 500,000 | $80,000 | $0.1600 | $0.1200 | $0.0231 |
| Jun 2027 | 2,678,571 | 800,000 | $128,000 | $0.1600 | $0.1200 | $0.0382 |
| Sep 2027 | 2,678,571 | 1,500,000 | $240,000 | $0.1600 | $0.1200 | $0.0717 |
| Dec 2027 | 2,767,857 | 3,000,000 | $480,000 | $0.1600 | $0.1200 | $0.1387 |
| Dec 2028 | 2,767,857 | 12,000,000 | $1,920,000 | $0.1600 | $0.1200 | $0.5549 |
| Dec 2029 | 1,845,240 | 24,000,000 | $3,840,000 | $0.1600 | $0.1200 | $1.6648 |
| Dec 2030 | 1,845,240 | 36,000,000 | $5,760,000 | $0.1600 | $0.1200 | $2.4972 |

If we assume that 75% of the monthly traffic is for the larger operators who opt for fiat payments only, then, using the same assumptions as above, we can project numbers of $XNET tokens and USDC accumulated in various pools.

| Month | Total Offload GB (Projected) | Total Offload Value (Projected) | Tokens Paid to non-Fiat Operators | Tokens Accrued in Treasury Book | Assumed Fiat Operators Payment | Opco Retained Value (20%) | BuyBack / Accrual Value |
|-------|-----------------------------:|--------------------------------:|----------------------------------:|--------------------------------:|-------------------------------:|--------------------------:|------------------------:|
| May 2026 | 197,495 | $31,599 | 1,383,929 | 4,151,786 | $17,775 | $6,320 | $7,505 |
| Jun 2026 | 230,000 | $36,800 | 1,339,286 | 4,017,857 | $20,700 | $7,360 | $8,740 |
| Sep 2026 | 300,000 | $48,000 | 1,339,286 | 4,017,857 | $27,000 | $9,600 | $11,400 |
| Dec 2026 | 400,000 | $64,000 | 1,383,929 | 4,151,786 | $36,000 | $12,800 | $15,200 |
| Mar 2027 | 500,000 | $80,000 | 691,964 | 2,075,893 | $45,000 | $16,000 | $19,000 |
| Jun 2027 | 800,000 | $128,000 | 669,643 | 2,008,929 | $72,000 | $25,600 | $30,400 |
| Sep 2027 | 1,500,000 | $240,000 | 669,643 | 2,008,929 | $135,000 | $48,000 | $57,000 |
| Dec 2027 | 3,000,000 | $480,000 | 691,964 | 2,075,893 | $270,000 | $96,000 | $114,000 |
| Dec 2028 | 12,000,000 | $1,920,000 | 28,526,786 | 2,075,893 | $1,080,000 | $384,000 | $456,000 |
| Dec 2029 | 24,000,000 | $3,840,000 | 110,089,286 | 1,383,930 | $2,160,000 | $768,000 | $912,000 |
| Dec 2030 | 36,000,000 | $5,760,000 | 436,250,000 | 1,383,930 | $3,240,000 | $1,152,000 | $1,368,000 |

## Appendix E: BuyBack & Burn Projections

Under the current BuyBack & Burn rules, the monthly offload revenue received is split as follows:

- 20% is kept by XNET to cover operational costs
- 20% is used by the Foundation for Market Liquidity support
- 60% is used by the Foundation for BuyBack & Burn

However, once we introduce fiat payments for certain operators, then the value that would be available for BuyBack would be greatly reduced (see tables in Appendix D).

If we assume that we use the projections in the tables of Appendix D, and retain the existing BuyBack & Burn rules, we can make some projections for the amount of tokens that might be acquired and Burnt over time. For this we will retain the previous assumption data traffic is for operators who opt for fiat payments rather than $XNET tokens. These calculations would work well with other assumed splits.

To facilitate these calculations, we have to use the projected emission tables for the Operator Pool over several months and years. These are well described in XIP-11.

We also have to project some estimates for other emissions, particularly the unlocking of Insider and Investor tokens. These tokens are mostly on a five-year non-linear monthly unlocking schedule, starting in Jan 2025 and continuing for five years till 2030. The monthly unlocks are weighted heavily towards the end of this period.

As of the date of this writing, the key metrics of the $XNET token are:

- Total Supply: 1,304,367,625
- Circulating Supply: 137,461,986 (10.54%)

| Year | Circulating Supply | Operator Tokens | Unlocking Tokens | % of Total |
|------|-------------------:|----------------:|-----------------:|-----------:|
| 2026 H2 | 200,447,115 | 32,500,000 | 30,485,129 | 15% |
| 2027 | 295,902,500 | 32,500,000 | 62,955,386 | 23% |
| 2028 | 454,313,272 | 32,500,000 | 125,910,771 | 35% |
| 2029 | 643,860,984 | 21,666,684 | 167,881,028 | 49% |
| 2030 | 673,921,719 | 21,666,684 | 8,394,051 | 52% |
| | | 140,833,368 | 395,626,365 | |

From the table above we can work out the possible impact of a BuyBack & Burn mechanism on the total circulating supply. For this we will need to interpolate the data values forecast in Appendix D, in order to get annual figures for 2026-2030.

| Year | Total Offload GB (Projected) | Clearing Price (per Token) | Total Offload Value (Projected) | BuyBack / Accrual Value | Annual BuyBack Tokens | Accumulated BuyBack Tokens | Circulating Supply | % of Circulating Supply |
|------|-----------------------------:|---------------------------:|--------------------------------:|------------------------:|----------------------:|---------------------------:|-------------------:|------------------------:|
| 2026 | 2,775,712 | $0.007 | $435,987 | $103,547 | 15,479,911 | 15,479,911 | 200,447,115 | 7.72% |
| 2027 | 14,710,000 | $0.072 | $2,353,600 | $558,980 | 7,739,955 | 23,219,866 | 295,902,500 | 7.85% |
| 2028 | 86,400,000 | $0.423 | $13,824,000 | $3,283,200 | 7,739,955 | 30,959,821 | 454,313,272 | 6.81% |
| 2029 | 222,000,000 | $1.634 | $35,520,000 | $8,436,000 | 5,159,974 | 36,119,796 | 643,860,984 | 5.61% |
| 2030 | 366,000,000 | $2.695 | $58,560,000 | $13,908,000 | 5,159,974 | 41,279,770 | 673,921,719 | 6.13% |
| Totals | | | $110,693,587 | $26,289,727 | | 41,279,770 | | |

It is fair to assume that not many token holders would want to sell their tokens at much of a discount to the Clearing Price for that month. As can be seen from the table, this means that the cumulative impact of burning these acquired tokens would be not significant.

A more significant support of the token value would be to accumulate these fiat balances within the Treasury Book, adding another contributor to the overall price of the token. This contribution would be the diluted book value.

```
Diluted Book Value = Total Treasury Book Value / Circulating Supply

Fair Token Price = Clearing Price + Diluted Book Value
```
