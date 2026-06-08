# XIP-12: Percentage Allocation from Buy and Burn to Liquidity Provisioning

**Authors:** Merstradamous, Big Man Blastoise, Chase  
**Status:** Proposed  
**Type:** Tokenomics  
**Created:** 2025-05-22  
**Updated:** 2025-07-01  
**Revision:** 2025-10-12

## Abstract

This proposal outlines a mechanism to reallocate a portion of "Buy and Burn" and redistribute to $XNET/$USDC liquidity pools. Specifically, it proposes that 20% of offload revenue would be instead directed to bolster market liquidity on decentralized exchanges (DEXs). This initiative aims to enhance market stability, reduce price volatility, and improve overall liquidity for token holders.

## Motivation

The current tokenomics include a mechanisms for token burning via carrier offload revenue, which reduces the total supply and can theoretically increase scarcity and value. While burning is beneficial for deflationary pressure, a significant challenge for nascent and growing decentralized networks is maintaining robust liquidity.

Low liquidity can lead to:

- **Increased Price Volatility:** Large buy or sell orders can cause significant price swings, deterring institutional and larger individual investors.
- **Poor Trading Experience:** Users may experience high slippage, making it costly to enter or exit positions.
- **Reduced Accessibility:** Limited liquidity can make it harder for new users to acquire $XNET tokens efficiently.
- **Limited Ecosystem Growth:** A less liquid token may hinder the development of applications and services that rely on a stable token market.

By redirecting 20% of burned tokens to the LP, we can address these issues without sacrificing the deflationary goals of the burning mechanism. This approach creates a dual benefit: reducing supply while simultaneously strengthening market depth and stability.

## Specification

The proposed mechanism shall operate as follows:

1. Resume monthly cadence of Buy and Burn Event with Carrier offload revenue payments.

### Allocation Split

- **60%** of $USDC will be used to market buy $XNET and be subsequently burned via the designated burn wallet (`B9SXSuPwpzmYUgk1GRfuW9R9QDMJ6P9SfTybSoawHiLj`) and permanently removed from the circulating supply.
- **20%** will be routed to $XNET/$USDC liquidity pools.
- **20%** will be used for XNET Inc. operating expenses.

### Liquidity Pool Integration

LP strategy will be managed by the XNET Foundation. Liquidity will be placed efficiently across markets lowering slippage and token price swings.

### Transparency

LP wallet fees and price arbitrage profits will be compounded back into the LPs ensuring long-term sustainability.

## Benefits

- **Significant Liquidity Boost:** A consistent influx of liquidity will gradually increase market depth, leading to reduced slippage and more stable pricing.
- **Stable Coin LP Stability:** $XNET/$USDC = one volatile base asset + one stable quote asset → predictable, much easier to manage.
- **Sustainable Growth:** Improved liquidity makes $XNET more attractive to new traders, investors, and external participants, fostering long-term growth and better future token distribution.
- **Reduced Volatility:** Deeper liquidity acts as a buffer against large price swings, creating a more predictable trading environment.
- **Community Confidence:** Demonstrates a proactive approach to market health and sustainability.

## Considerations

- **Impact on Burn Rate:** While 60% still burns, the overall rate of supply reduction will be 20% lower than if 80% were burned. This is a deliberate trade-off for more liquidity.
- **$XNET Supplied to LP:** Addressing the need to match the $USDC side of the LP with an equal value amount of $XNET from the Foundation pool.

If market dynamics lead to the holding more $USDC and less $XNET it means the market is buying $XNET from the pool, providing organic demand and reducing circulating sell pressure. Unlike OTC deals or token grants that immediately introduce supply into the market, this approach adds liquidity without adding selling pressure.

Additionally, the LP is actively managed by the Foundation and the $XNET side remains within Foundation control, it isn't being distributed, sold, or lost. It's being used to stabilize markets, deepen liquidity, and earn fees.
