##  XIP 1 : SLA (Cellular Radio Uptime) Based Token Bonus 
### Background
All Cellular radios are linked to a gateway—a compact hardware appliance located alongside the Cellular radios. This gateway facilitates radio management, operates a segment of the Evolved Packet Core (EPC), and establishes a connection to the XNET backend infrastructure. Every ten minutes, the XNET backend initiates contact with each gateway to assess its condition (determining if the gateway is accessible and functioning as anticipated) and the status of its radios. Gateways reporting normal operations are classified as "UP." Those indicating issues are tagged as faulty. Gateways failing to report are labeled as down. Similarly, the radios are also designated as up, faulty, or down based on their status.

Currently, Cellular radios are eligible for full $XNET CVS rewards for an epoch only if their radio maintains an uptime of 75% or more during that period. The present epoch duration of two weeks discourages radio operators from resolving issues if a significant portion of the epoch has already elapsed. This proposal aims to introduce extra incentives to improve uptime. Furthermore, XNET recognizes the request for shorter epoch durations and has identified this as a priority for future action as we progress towards moving more infrastructure onto the blockchain.

### Proposal
Cellular radios achieving 50-75% uptime during an Epoch will qualify for 50% of the maximum total $XNET CVS rewards for that period.

For example, if a radio has 58% Uptime in an Epoch, then this radio will get 50% of its CVS rewards. If the radio was a Lucius (Baicells Nova 430) in a Blue hex, then its normal epoch CVS rewards would be 1,250 tokens. In this scenario, it would receive 50% of those rewards, i.e. 625 tokens. Previously, in this scenario, such a radio would receive 0 token rewards for CVS.

To be clear, any Paid Data token rewards are not affected and are paid in full.

Radios that achieve 99.9% uptime during an Epoch will qualify for an additional bonus atop the maximum $XNET rewards they are eligible for in that Epoch. It is proposed that this bonus be an extra 10% on the maximum $XNET earnings for that radio.

For example, if a radio has 99.91% Uptime in an Epoch, then this radio will get 110% of its CVS rewards. Again, if the radio was a Lucius (Baicells Nova 430) in a Blue hex, then its normal epoch CVS rewards would be 1,250 tokens. In this scenario, it would receive 110% of those rewards, i.e. 1,375 tokens. Previously, in this scenario, such a radio would receive 1,250 token rewards for CVS.

Again, to be clear, any Paid Data token rewards are not affected and are paid in full at 100%.
