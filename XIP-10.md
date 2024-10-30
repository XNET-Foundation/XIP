# XIP-10 : Unemitted Supply Burn Mechanism
## Summary
This XIP proposes a significant reduction in the total supply of XNET tokens to address concerns about future dilution and incentivize network development. This reduction will be achieved through a burn mechanism that will burn a portion of future emissions proportionally among the existing token pools.

The burn rate will start high and gradually decrease over time, ensuring a significant reduction in total supply while maintaining a sustainable emission schedule. This proposal aims to optimize XNET's tokenomics for long-term growth and stability.

## Rationale
Before the move to Solana, XIP 3 was introduced and passed to address XNET’s irregular token supply overhang. The XNET community implemented a 90% supply reduction, which has helped, but did not completely solve the problem. It still has left XNET with a smaller circulating supply to total supply percentage compared to industry peers.

| Value        | XNET   | Helium | World Mobile | 
|-------------:|:-------|--------|:-------------|
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

The burn will be based on a multiple of the total emissions per epoch, starting in Epoch 50. At the end of each epoch, the total emissions towards coverage & validation, data, and bonuses will be multiplied by the future supply reduction factor. This factor will be very large (450x) to start in order to address the total supply within a short time, and then will reduce substantially once total supply drops below 1.0B (20x). The factor will remain at 20x until the end of Epoch 75 or at a floor supply of 850M, at which point the burn mechanism will be eliminated entirely.

Total Burn per Epoch, TB = (RCV+RD+RB)  kFSR
RCV = Coverage & Validation Rewards 
RD =Data Rewards 
RB =Bonus Rewards 
kFSR =Future Supply Reduction Factor 

### Burn Per Pool
The burn will be done as a pro rata share across the existing token pools of unallocated tokens.

Operator Pool Burn = 0.4969 TB
Foundation Pool Burn = 0.2089 TB
Investor Pool Burn = 0.0658 TB
Insider Pool Burn = 0.0746 TB
Ecosystem Pool Burn = 0.1539 TB

### Projected Total Supply Reduction
Based on the current emissions projections model, these are the expected cuts to total supply over the next 26 epochs
Epoch End Date
Epoch Number
Tokens Emitted
Future Supply Reduction Factor
Future Supply Reduced
Fully Diluted Supply

10/14/2024
Epoch 49
462,105
0.0x
0
2,400,000,000
10/28/2024
Epoch 50
462,105
450.0x
(207,947,250)
2,192,052,750
450x until below 1.0B
11/11/2024
Epoch 51
503,323
450.0x
(226,495,350)
1,965,557,400
11/25/2024
Epoch 52
503,323
450.0x
(226,495,350)
1,739,062,050
12/9/2024
Epoch 53
549,319
450.0x
(247,193,325)
1,491,868,725
12/23/2024
Epoch 54
549,319
450.0x
(247,193,325)
1,244,675,400
1/6/2025
Epoch 55
545,645
450.0x
(245,540,025)
999,135,375
1/20/2025
Epoch 56
545,645
20.0x
(10,912,890)
988,222,485
20x until Epoch 75 or floor of 850M
2/3/2025
Epoch 57
594,964
20.0x
(11,899,280)
976,323,205
2/17/2025
Epoch 58
594,964
20.0x
(11,899,280)
964,423,925
3/3/2025
Epoch 59
650,055
20.0x
(13,001,100)
951,422,825
3/17/2025
Epoch 60
650,055
20.0x
(13,001,100)
938,421,725
3/31/2025
Epoch 61
650,055
20.0x
(13,001,100)
925,420,625
4/14/2025
Epoch 62
711,703
20.0x
(14,234,050)
911,186,575
4/28/2025
Epoch 63
711,703
20.0x
(14,234,050)
896,952,525
5/12/2025
Epoch 64
780,804
20.0x
(15,616,080)
881,336,445
5/26/2025
Epoch 65
780,804
20.0x
(15,616,080)
865,720,365
6/9/2025
Epoch 66
858,388
18.3x
(15,720,365)
850,000,000
6/23/2025
Epoch 67
858,388
0.0x
0
850,000,000
7/7/2025
Epoch 68
881,915
0.0x
0
850,000,000
7/21/2025
Epoch 69
881,915
0.0x
0
850,000,000
8/4/2025
Epoch 70
970,613
0.0x
0
850,000,000
8/18/2025
Epoch 71
970,613
0.0x
0
850,000,000
9/1/2025
Epoch 72
1,070,436
0.0x
0
850,000,000
9/15/2025
Epoch 73
1,070,436
0.0x
0
850,000,000
9/29/2025
Epoch 74
1,070,436
0.0x
0
850,000,000
10/13/2025
Epoch 75
1,182,945
0.0x
0
850,000,000

### Projected Burn By Pool
Epoch Number
Total Supply Burn
Operator Pool Burn
Foundation Pool Burn
Investor Pool Burn
Insider Pool Burn
Ecosystem Pool Burn
Fully Diluted Supply

Epoch 50
(207,947,250)
(103,324,331)
(43,442,057)
(13,679,465)
(15,503,393)
(31,998,004)
2,192,052,750
Epoch 51
(226,495,350)
(112,540,467)
(47,316,923)
(14,899,620)
(16,886,237)
(34,852,103)
1,965,557,400
Epoch 52
(226,495,350)
(112,540,467)
(47,316,923)
(14,899,620)
(16,886,237)
(34,852,103)
1,739,062,050
Epoch 53
(247,193,325)
(122,824,827)
(51,640,917)
(16,261,202)
(18,429,363)
(38,037,016)
1,491,868,725
Epoch 54
(247,193,325)
(122,824,827)
(51,640,917)
(16,261,202)
(18,429,363)
(38,037,016)
1,244,675,400
Epoch 55
(245,540,025)
(122,003,339)
(51,295,527)
(16,152,443)
(18,306,102)
(37,782,614)
999,135,375
Epoch 56
(10,912,890)
(5,422,371)
(2,279,801)
(717,886)
(813,605)
(1,679,227)
988,222,485
Epoch 57
(11,899,280)
(5,912,486)
(2,485,867)
(782,774)
(887,144)
(1,831,009)
976,323,205
Epoch 58
(11,899,280)
(5,912,486)
(2,485,867)
(782,774)
(887,144)
(1,831,009)
964,423,925
Epoch 59
(13,001,100)
(6,459,955)
(2,716,047)
(855,256)
(969,290)
(2,000,552)
951,422,825
Epoch 60
(13,001,100)
(6,459,955)
(2,716,047)
(855,256)
(969,290)
(2,000,552)
938,421,725
Epoch 61
(13,001,100)
(6,459,955)
(2,716,047)
(855,256)
(969,290)
(2,000,552)
925,420,625
Epoch 62
(14,234,050)
(7,072,581)
(2,973,622)
(936,363)
(1,061,212)
(2,190,273)
911,186,575
Epoch 63
(14,234,050)
(7,072,581)
(2,973,622)
(936,363)
(1,061,212)
(2,190,273)
896,952,525
Epoch 64
(15,616,080)
(7,759,280)
(3,262,340)
(1,027,278)
(1,164,248)
(2,402,933)
881,336,445
Epoch 65
(15,616,080)
(7,759,280)
(3,262,340)
(1,027,278)
(1,164,248)
(2,402,933)
865,720,365
Epoch 66
(15,720,365)
(7,811,097)
(3,284,126)
(1,034,138)
(1,172,023)
(2,418,980)
850,000,000
Epoch 67
0
0
0
0
0
0
850,000,000
Epoch 68
0
0
0
0
0
0
850,000,000

Total
(1,550,000,000)
(770,160,287)
(323,808,989)
(101,964,176)
(115,559,400)
(238,507,149)
850,000,000
Unallocated Tokens Available
1,824,170,088
906,389,263
381,085,595
120,000,000
136,000,000
280,695,230

Percentage Available
49.69%
20.89%
6.58%
7.46%
15.39%

### Maximum Burn Cap
The total burn will be capped to not reduce the supply below 850M XNET. This burn is independent of the data buy/burn, so the total supply can continue to reduce based on the future buy/burn mechanism.
For example, if the actual emissions exceed the projected emissions, and the total burn amount from this proposal would drop the total supply below 850M XNET, the supply reduction factor would be changed so that the total supply drops to exactly 850M XNET. Also, the supply reduction factor would be set to 0 for all Epochs following this occurrence. 

### Impact Assessment
The XIP was modeled based on the XNET Foundation’s emissions projections.
The impact to total supply is projected to be a reduction from 2.4B XNET to 850M XNET over a 1 year period.
The impact to the community will be a lower impact of long term dilution of the token supply.
### Voting Options
Community members can choose the following options on Align: `Support 👍🏼 or Against 👎🏼`
