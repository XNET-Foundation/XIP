# XIP 8: Token Realignment on move to Solana
By: Dharma (23 Aug 2024)
 
## Background
On Friday Aug 16, 2024, the $XNET token migrated from the Polygon chain to Solana. This was quickly followed, on Monday Aug 19, 2024, by an epoch distribution day for Epoch 45. This distribution was done exclusively in the new Solana token. All further transactions and distributions in the Polygon token had ceased by this time.
The intent, in moving from the Polygon to Solana chain, was to facilitate a reduction in the Total Supply from 24 Billion to 2.4 Billion tokens, a 90% reduction (refer to XIP 3 above). In doing so, it was assumed that the reduction in the various rewards should also be reduced by 90%. This was expected to be reflected in a change in actual market value of the tokens, to ensure a similar value dispersed to the Operators.
However, it is clear that, while there has been some considerable increase in value of the tokens, this has not compensated for a 90% reduction in emissions to Operators.
The ideal solution for this would be to introduce the Oracle pricing adjustments based on an agreed dollar-value reward assigned for a collection of parameters (based on GBs of data  served, type of radio, type of rewards and type of hex). Please refer to XIPs 5 and 6 for more detail on these historic proposals.
Given the urgency of resolving this before the next epoch dispersal on Monday Sep 02, 2024 (dispersal for epoch 46), we should introduce some adjustment to the  rewards before then.
The proposal below is to change the number of token rewards for Coverage & Validation and for Data Per GB. The former is needed for the Cellular radios that gain these rewards based on their Hex Type; the latter is for the various WiFi AP units that are expected to move back to getting rewards based on measured GB Traffic from this epoch.

## WiFi Data Rewards
In the currently published rewards on the XNET website, there are various rewards put forward by radio type, ranging from 5 to 10 tokens per GB of measured data traffic. It is proposed to simplify this and revert back to the previous reward (under Polygon) of 50 tokens per GB of measured traffic.
This would ensure that those units get fair recompense for their measured traffic in this early stage of network growth. Later we should apply the proposed changes, subject to our usual debate, listed above in XIP 6. This would peg the token rewards per GB to a combination of a fixed number + a conversion of a fiat dollar value (using an Oracle pricing mechanism).
This more elaborate determination of Per GB rewards will presumably require more debate. Given the time constraints, it is proposed that we go with the 50 tokens power GB for now and move to the more elaborate mechanism after such debate.
Coverage & Validation Rewards
In the currently published rewards on the XNET website, there is a table of Coverage + Validation rewards per Radio Type and Hex Type.
The Hex Types are Blue, Silver and Gold. However, there are only 16 units that currently reside in Silver hexes. In an effort to rationalize this, it is proposed that all Silver hexes are promoted to be Gold hexes. This is entirely reasonable as they are hexes adjacent to Gold hexes in city centers.

<!--Radio Type
Current Rewards
Proposed Rewards


Blue
Silver
Gold
Blue
Gold
Felix / Lucius (430 / 430i)
50
200
350
200
500
Roofus (FW-300i)
500
1000
1500
1500
4000
Magnus (846N)
750
1500
2250
2000
5000
Linus (436Q)
400
800
1200
750
2000-->

These rewards are subject to having at least a 75% uptime in a particular epoch. There is a reduction of rewards to 50% of these values where the uptime is between 50% and 75%. There is an increase of rewards to 110% of these values where the uptime is greater than or equal to 99.9%. Please refer to previously passed XIP 1. 
These rewards would ensure a reasonable return for Operators running these radios. It would also ensure that they cover their monthly operational costs, vital to ensure a healthy running network.
It is proposed that these rewards adjustments are introduced from the emissions for epoch 46, and can even be back-dated to the reward calculations for Epoch 45. To be discussed.

## Token Emissions and Dilution
Given the increase in numbers above, it might be worth discussing the impact of these on the expected emissions and the potential for dilution of the existing token holders.
Given the move to Data Rewards based on measured data in GB, and not Universal Basic Income (as in recent epochs), this will exclude a large number of dormant WiFi AP units from rewards. While it should increase the rewards for those AP units delivering excellent data traffic, the overall token reward emissions for Data is expected to be roughly comparable, at least in the short term. This may increase as there are more radios online with eligible traffic.
As an example, the Data Rewards for Epoch 45, using the old UBI mechanism, was approximately 296,000 tokens. If we assume a guesstimate of around 5 TB of eligible traffic per epoch (at least initially), this would mean an emission of (50 x 5,000 GB) = 250,000 tokens per epoch. Hopefully, we can increase this amount of traffic, and the corresponding rewards, in time. This would have much larger benefits on our network health than just the possible dilution for these rewards.
For the Coverage & Validation rewards, the emissions in epoch 44 (using the old Polygon token) were around 715,000 tokens. Using the published rates on the XNET website, the emissions for Coverage & Validation for Epoch 45 were approximately 85,000 tokens (Solana). Under the proposed changes, the emissions for epoch 45 for C+V would have been approximately 220,000 tokens (Solana). 
Given this, we think this proposal is a good balance of adjusting rewards to balance required operational coverage of ongoing expenses, with limiting the current and ongoing emission rate on the new Solana token.

## Future Adjustments
These proposed rewards are to allow an immediate response to the situation we find ourselves in for the emissions for Epoch 46 and beyond. While we expect these proposals to remain the case for the next few epochs, it is also expected that we reopen the discussions on XIPs 5 and 6: the pegging of part or all of these rewards to a fiat currency value and an Oracle pricing mechanism.
We hope we can start these discussions as soon as possible after we pass the above XIP. This should be part of the new governance mechanisms undertaken by the XNET Foundation.
