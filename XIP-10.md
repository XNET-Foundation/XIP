# XIP-10 : Reduce $XNET total supply
## Summary
This XIP proposes a significant reduction in the total supply of XNET tokens to address concerns about future dilution and incentivize network development. This reduction will be achieved through a burn mechanism that will burn a portion of future emissions proportionally among the existing token pools.
The burn rate will start high and gradually decrease over time, ensuring a significant reduction in total supply while maintaining a sustainable emission schedule. This proposal aims to optimize XNET's tokenomics for long-term growth and stability.

## Rationale
Before the move to Solana, XIP 3 was introduced and passed to address XNET’s irregular token supply overhang. The XNET community implemented a 90% supply reduction, which has helped, but did not completely solve the problem. It still has left XNET with a smaller float compared to industry peers.

|              | XNET   | Helium | World Mobile | 
|-------------:|:----------------|:-------------|
| Circ. Tokens | 64.12M | 170.5M | 576M         |
| Total Tokens | 2.4B   | 223M   | 2B           |
| Float        | 2.67%  | 76.4%  | 28.8%        |

The original tokenomics envisioned a need for larger long-tail token distributions to incentivize development 10+ years in the future. This gave the appeal of flexible future emission concepts, but at the expense of long term dilution of the circulating supply. However, the fundamental DePIN flywheel is designed to drive rapid growth to reach network scale within a 5-10 year period, after which the fundamental emissions/burn model should stabilize. Therefore, a large unemitted supply is unnecessary, and in fact serves to undermine the initial bootstrapping phase of network development due to future dilution uncertainty.

The project does not need nearly as many tokens as were kept during the migration, so this XIP proposes a reduction in the total supply based on a multiple of emissions over the next 26 epochs. This burn will come purely from future emissions and can be split on a pro rata share across the emission pools.

## Related XIPs
XIP-3: Reduce $XNET total supply
XIP-7: Chain Migration/XNET Foundation

## Proposal Details
### Unemitted XNET Burn
The burn will be based on a multiple of the total emissions per epoch, starting in Epoch 50. At the end of each epoch, the total emissions towards coverage & validation, data, and bonuses will be multiplied by the future supply reduction factor. This factor will be very large (1000x) to start in order to address the total supply immediately, and then will reduce substantially once total supply drops below 1.5B (500x), 1B (2x), and 900M (1x). The factor will remain at 1x until the end of Epoch 75, at which point the burn mechanism will be eliminated entirely.

Total Burn per Epoch, TB = (RCV+RD+RB)  kFSR
RCV = Coverage & Validation Rewards 
RD =Data Rewards 
RB =Bonus Rewards 
kFSR =Future Supply Reduction Factor 

### Burn Per Pool
The burn will be done a pro rata share across the existing token pools.
- Operator Pool Burn = 0.39 TB
- Foundation Pool Burn = 0.18 TB
- Investor Pool Burn = 0.15 TB
- Insider Pool Burn = 0.15 TB
- Ecosystem Pool Burn = 0.13 TB

### Projected Total Supply Reduction
Based on the current emissions projections model, these are the expected cuts to total supply over the next 26 epochs:

<!--Epoch End Date
Epoch Number
Tokens Emitted
Future Supply Reduction Factor
Future Supply Reduced
Fully Diluted Supply
Notes
10/14/2024
Epoch 49
462,105
0.0x
0
2,400,000,000


10/28/2024
Epoch 50
462,105
1000.0x
(462,105,000)
1,937,895,000
1000x until below 1.5B
11/11/2024
Epoch 51
503,323
1000.0x
(503,323,000)
1,434,572,000
11/25/2024
Epoch 52
503,323
500.0x
(251,661,500)
1,182,910,500
500x until below 1.0B
12/9/2024
Epoch 53
549,319
500.0x
(274,659,250)
908,251,250
12/23/2024
Epoch 54
549,319
2.0x
(1,098,637)
907,152,613
2x until below 900M
1/6/2025
Epoch 55
545,645
2.0x
(1,091,289)
906,061,324
1/20/2025
Epoch 56
545,645
2.0x
(1,091,289)
904,970,035
2/3/2025
Epoch 57
594,964
2.0x
(1,189,928)
903,780,107
2/17/2025
Epoch 58
594,964
2.0x
(1,189,928)
902,590,179
3/3/2025
Epoch 59
650,055
1.0x
(650,055)
901,940,124
1x until Epoch 75
3/17/2025
Epoch 60
650,055
1.0x
(650,055)
901,290,069
3/31/2025
Epoch 61
650,055
1.0x
(650,055)
900,640,014
4/14/2025
Epoch 62
711,703
1.0x
(711,703)
899,928,312
4/28/2025
Epoch 63
711,703
1.0x
(711,703)
899,216,609
5/12/2025
Epoch 64
780,804
1.0x
(780,804)
898,435,805
5/26/2025
Epoch 65
780,804
1.0x
(780,804)
897,655,001
6/9/2025
Epoch 66
858,388
1.0x
(858,388)
896,796,613
6/23/2025
Epoch 67
858,388
1.0x
(858,388)
895,938,225
7/7/2025
Epoch 68
881,915
1.0x
(881,915)
895,056,311
7/21/2025
Epoch 69
881,915
1.0x
(881,915)
894,174,396
8/4/2025
Epoch 70
970,613
1.0x
(970,613)
893,203,783
8/18/2025
Epoch 71
970,613
1.0x
(970,613)
892,233,170
9/1/2025
Epoch 72
1,070,436
1.0x
(1,070,436)
891,162,734
9/15/2025
Epoch 73
1,070,436
1.0x
(1,070,436)
890,092,298
9/29/2025
Epoch 74
1,070,436
1.0x
(1,070,436)
889,021,862
10/13/2025
Epoch 75
1,182,945
1.0x
(1,182,945)
887,838,918-->


### Maximum Burn Cap
The total burn will be capped to not reduce the supply below 850M XNET. This burn is independent of the data buy/burn, so the total supply can continue to reduce based on the future buy/burn mechanism.
For example, if the actual emissions exceed the projected emissions, and the total burn amount from this proposal would drop the total supply below 850M XNET, the supply reduction factor would be changed so that the total supply drops to exactly 850M XNET. Also, the supply reduction factor would be set to 0 for all Epochs following this occurrence.

### Impact Assessment
The XIP was modeled based on the XNET Foundation’s emissions projections.
The impact to total supply is projected to be a reduction from 2.4B XNET to 888M XNET over a 1 year period.
The impact to the community will be a lower impact of long term dilution of the token supply.

### Voting Options
Community members can choose the following options: `For, Against, Abstain`
