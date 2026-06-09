# XIP-13: XNET Token Design Proposal

**Author:** Brent Beane  
**Status:** In Development  
**Type:** Tokenomics  
**Date:** 2026-06-05

## Abstract

The aim of this proposal is to allow the Foundation to decide when to buy tokens off the open market, or alternatively, accrue that fiat value in a Foundation Treasury Book. This treasury book would directly support both the operation of the Foundation and the value of the token itself.

## Benefits

There are a number of benefits expected from this mechanism:

- Allow the Foundation to build a fiat & digital asset treasury book to support the value of the token.
- Reduce the incentivisation of short-term investors and accrue value for long-term holders of the token. This will align token holders with long-term objectives of XNET, to create a sustainable ecosystem and retain flexibility as the treasury grows.
- Allow certain Operators to be paid directly in fiat currency at the determined Clearing Price (minus a fee/discount) for the token at that epoch. This would effectively allow them to participate in a Shared Revenue model, while we still support the tokenomics of the project.
- Improve the governance of the token by encouraging holders to stake their tokens to facilitate voting control over the treasury pool. Align governance with long-term objectives of XNET to hold $XNET tokens, participate in governance operations/improvements and to grow the overall XNET ecosystem.

## Mechanism

The key metric to determine this facility is the **Clearing Price** of the token (sometimes referred to as the Base Price in other documents). This Clearing Price is determined each month by the simple formula:

```
Clearing Price = Total BuyBack Value in that month / Total Emitted Operator Tokens in that month
```

These figures have to be calculated monthly, and not by epoch, as payments are actually received on a monthly cadence. The monthly tokens can be relatively easily calculated using the scheduled epoch emission charts and a simple aggregation by month (see [Addendum B: Monthly Emitted Tokens](#addendum-b-monthly-emitted-tokens)).

The proposal is to use this Clearing Price to calculate potential fiat payments for certain Operators, in lieu of $XNET distributions. Crucially, the token distributions still take place, supporting the entire tokenomics, but these Operators can onboard and treat the monthly fiat flow as an effective revenue-sharing mechanism (see detail below).

## Current Scenario — Worked Example

Assuming that $100,000 is received for data offload in a particular month from clients (MNOs/MVNOs). This means that:

- **$20,000 (20%)** is kept by XNET to cover operational costs
- **$20,000 (20%)** is used by the Foundation for Market Liquidity support
- **$60,000 (60%)** is used by the Foundation for BuyBack & Burn

The $60k is gone forever as it cashes out either 1) a Deployer (a good thing), or 2) a Seller/Speculator.

The $20k used by the Foundation for Liquidity support at least builds some book value in USDC/XNET or SOL/XNET. This stays with the treasury and builds over time to back the token book value.

## Proposed Scenario — Worked Example

Assuming that $100,000 is received for data offload in a particular month from clients (MNOs/MVNOs). It is proposed that:

- **$20,000 (20%)** is kept by XNET to cover operational costs (as before)
- **$20,000 (20%)** is used by the Foundation for Market Liquidity support (as before)
- **$60,000 (60%)** is used by the Foundation for token acquisition or fiat pooling

Crucially, the tokens acquired by the Foundation are either at:

- the Clearing Price from larger operators, minus a facilitation fee
- the Market Price from exchanges, up to the Clearing Price of the token

However, in neither case are the tokens sent to a Burn mechanism. Instead, they are accrued in the Foundation Treasury Book, supporting the value of the token.

If the Market Token Price is greater than the Clearing Price then the Foundation could accrue those fiat values in USDC in the Treasury Book, thus supporting the overall token valuation.

Any accrued $XNET tokens could be used at a later date for various purposes, e.g.:

- Opportunistic trading on exchanges for values in USDC/SOL
- Swap equity with a synergistic business or protocol
- Issue a convertible note paid in $XNET tokens
- Incentivise a large deployer with a future piece of equity

In this scenario $80,000 is staying with the XNET protocol to raise the floor value of the token, while keeping in place the buying pressure from buybacks. The difference is we aren't burning an asset.

## Clearing Price — Worked Example

So by example, if the total offload revenue in a month is $100,000, then the BuyBack Value for that month would be ($100,000 × 80%) = **$80,000** (using current parameters).

The monthly emitted tokens can be calculated using the appropriate epoch emitted tokens, corrected for that particular month. For instance, for May 2026, the monthly emitted tokens can be calculated as `(2,500,000 × 2 × 31/28) = 5,535,714 $XNET`.

In this example the Clearing Price for that month would be:

```
Clearing Price = $80,000 / 5,535,714 = $0.015
```

This Clearing Price could only be calculated in any month once the paid offload numbers are available for that month. That said, these numbers should be predicted a couple of months ahead based on expected revenues, i.e. from data offload already done.

For certain designated Operators, they may choose to be paid only in fiat currency. The value to be paid to these Operators would be their assigned tokens in that period multiplied by the Clearing Price, minus a small fee. It is assumed that these large Operators would be comfortable being paid monthly in arrears.

## Foundation Treasury Book

### Token BuyBack Executed up to the Clearing Price for Each Month

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

## Fiat Payments to Large Operators

For certain large Operators, particularly larger corporations such as ISPs and MSPs, there is a strong desire by them to be paid in fiat currency, not tokens. They have great difficulty accruing tokens of any sort on their balance sheet. They would need monthly fiat payments instead.

To date, there has been work to create a mechanism to translate the tokens provided to an operator in any epoch into an equivalent fiat currency value. This would seem to require an open market sale of the tokens, or the sale via a liquidity provider such as a large market maker. Such discussions are ongoing. Once the $XNET token is listed on a CEX, such mechanisms should be able to be supported.

However, there is a much simpler mechanism available by using the Clearing Price associated with the month. The Foundation could choose to divert some of the funds from the BuyBack route to direct fiat payments to such Operators. These payments would be at the Clearing Price, less a facilitation fee.

The calculation of the payment due to an operator under such a mechanism would be:

```
Operator Payment = (Operator tokens assigned for that month × Clearing Price) − Facilitation Fee
```

The tokens assigned to an Operator in any month is made up of Data Offload tokens + Proof of Coverage tokens. Most of the tokens are assigned for data offload (70%), with the remainder (30%) for PoC.

The total data offload for an operator is usually correlated with their total number of AP units, particularly those serving enough data to earn the Enhanced PoC reward (> 3GB). This means that a fair assumption is that the total number of tokens received by an Operator is proportional to their data offload. Based on this assumption, we can approximate the number of tokens received in an epoch as:

```
Operator tokens assigned for that month = (Operator GB Offload in that month / Total GB Offload in that month) × Total Emitted Operator Tokens in that month
```

Given that the Clearing Price is defined by:

```
Clearing Price = Total Buy & Burn Value in that month / Total Emitted Operator Tokens in that month
```

This means that the Operator Payment simplifies to:

```
Operator Payment = (Operator GB Offload in that month / Total GB Offload in that month) × Total BuyBack Value in that month − Facilitation Fee
```

### Facilitation Fee

In this mechanism, the Foundation would receive the equivalent tokens for this Operator's payment. These tokens would be transferred to the Foundation Treasury for later use (e.g. they could be sold at favourable market conditions). The real value of this mechanism is the ability to avoid any purchase or sale of tokens to facilitate the fiat payment, while still supporting the distribution of tokens for the operator, albeit to the Foundation.

For these Operators, this simplified formula means that they effectively participate in a Shared Revenue mechanism with XNET. By simple manipulation of terms, their calculation of their offload value becomes:

```
XNET Blended GB Offload Price in any month = Total BuyBack Value in that month / Total GB Offload in that month
```

Therefore for any particular month, the Operator can calculate:

```
Operator Payment = (Operator GB Offload × XNET Blended GB Offload Price) − Facilitation Fee
```

A key point for this mechanism is the ability to accrue value to the XNET token via fee/discount by providing the fiat bypass service for large operators. Our deployers not using this mechanism are transacting in thin markets with large slippage depending on size, so a facilitation fee of 5% is not unreasonable. If business continues to grow, it's possible XNET trades above the Clearing Price, paying deployers a premium for not using the fiat bypass.

## Receivables Financing & Accelerated Settlement

Certain Operators, particularly ISPs, MSPs, enterprise deployments, and venue owners, may require more frequent and predictable cash flows than underlying carrier or enterprise payment cycles provide.

To support network growth, the Foundation may permit approved third-party financing providers to offer optional receivables financing, factoring, or accelerated settlement facilities to Operators.

Such providers may underwrite future Operator receivables using factors including historical offload performance, assigned token emissions, Clearing Price calculations, expected Offload Revenue, and other network metrics.

Participation in any financing arrangement shall be voluntary and independent of the Operator reward mechanism. The Foundation shall not be required to guarantee any financing facility provided by a third party.

Examples of potential financing providers may include infrastructure finance platforms, credit funds, or ecosystem participants such as Fractals.

## Token Governance

Once the Foundation holds a sizable Treasury Book value, there will be more interest in token holders to participate in decisions on the control of such funds.

By principal, we wish that long-term, impactful decisions should be made by long-term stakeholders and deployers. It is expected that the voting will be aligned to long-term staking of the $XNET token.

A principled formula must be agreed upon that aligns governance power to **Stake × Duration**, ensuring active deployers are represented.

## Addendum A: Historical Data

| Month | Epoch Tokens | Adjusted Monthly Tokens | Projected Offload Payment | GB Offloaded | Blended Offload Rate | Clearing Price |
|-------|-------------:|------------------------:|--------------------------:|-------------:|---------------------:|---------------:|
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

## Addendum B: Monthly Emitted Tokens

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
