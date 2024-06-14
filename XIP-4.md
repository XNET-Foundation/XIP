## XIP 4: End of Phase X (Registration & Staking)

by bigXhaan, Dharma


### Background 

Phase X was an initiative introduced early in XNET’s launch to properly incentivize early network operators and entrants. Under current conditions, the incentives from Phase X seem heavily misaligned as the network begins to scale.  

The current circulating supply of $XNET is approximately [24,829,890](https://dune.com/queries/3535629/5954004). Through Q4 2024 the circulating supply is projected to grow to approximately 80,000,000 assuming fairly conservative radio growth. With XNET’s recent exponential growth, the circulating supply through Q4 2024 may be higher. 

_(Dated Emissions Tab): _[https://docs.google.com/spreadsheets/d/1QnhjSzbC_d4xOC7K7oRFP27Tqjc062vKElTSBGyQTcQ/edit#gid=160862862](https://docs.google.com/spreadsheets/d/1QnhjSzbC_d4xOC7K7oRFP27Tqjc062vKElTSBGyQTcQ/edit#gid=160862862)

In an effort to manage dilution and supply inflation in the near term and more importantly to incentivize balanced network growth we can aim to target a reduction in emission to CBRS radios. 

Currently CBRS radios account for most of the emissions from the operator pool (roughly 80% per epoch.) CBRS radios currently earn $XNET rewards via coverage, validation, and staking. In addition they also receive a bonus for being within a XNET designated cluster (gold/silver hex). An example for a Roofus (BLINQ FW-300) earnings during an epoch (2 weeks) is tabulated below. 


<table>
  <tr>
   <td><strong>Coverage</strong>
   </td>
   <td><strong>Validation </strong>
   </td>
   <td><strong>Staking</strong>
   </td>
   <td><strong>Gold Hex Bonus</strong>
   </td>
   <td><strong>Data (not live)</strong>
   </td>
   <td><strong>Total (per Epoch)</strong>
   </td>
  </tr>
  <tr>
   <td>1250 
   </td>
   <td>1250
   </td>
   <td>5000
   </td>
   <td>5000
   </td>
   <td>0
   </td>
   <td>12,500
   </td>
  </tr>
</table>


  


### Removal of Staking Bonus

Staking bonus was implemented in an effort to incentivize good network behaviors and provide additional incentives to early network adopters, especially those participants deploying larger units. Removal of the staking bonus will effectively cut ~40% of baseline CBRS emissions across all radios (assuming placement in gold/silver hex) 

With the passing of [XIP-1](https://docs.google.com/document/u/0/d/1-xnLwtmFrQw8TCEU2TkQ1roTdeJqfQXfR_4Y0YtpZnU/edit)- which rewards network operators for achieving sub-par radio uptime, the staking bonus serves as a disincentive to the network- especially in cases where up-front locked tokens have already been dispersed. This is now proposed to be removed, until slashing contracts are created and implemented on-chain to make the whole process more formalized-ideally allowing operators to choose their stake based on network contribution. It is suggested that a formal staking mechanism be explored to further reward long term deployments and good network performance. This change also drastically aids in balancing short term emissions in an effort to reduce short-term inflationary effects. 

An example of $XNET rewards for a Roofus (BLINQ-FW300) radio is shown below with the removal of staking.


<table>
  <tr>
   <td><strong>Coverage</strong>
   </td>
   <td><strong>Validation </strong>
   </td>
   <td><strong>Gold Hex Bonus</strong>
   </td>
   <td><strong>Data (not live)</strong>
   </td>
   <td><strong>Total (per Epoch)</strong>
   </td>
  </tr>
  <tr>
   <td>1250 
   </td>
   <td>1250
   </td>
   <td>5000
   </td>
   <td>0
   </td>
   <td>7,500
   </td>
  </tr>
</table>


The staking bonus given out every epoch will be immediately removed (Epoch 39) for those radios that have already received locked registration and Phase X bonus tokens. Operators that still have locked tokens from Phase X will continue to receive their staking bonus until their Phase X bonuses become unlocked at which no radios will receive the staking bonus. 

note: edge cases may need to be individually explored- however incentives for CBRS deployments are driven to XNET Gold/Silver hexes, where we may consider additional bounties.  


### Removal of Phase X Bonus 

[https://docs.google.com/spreadsheets/d/1sxYBrSoU9SzKRIIwvQzAWmRJOqY8qQOQMlxjd-o1Grc/edit#gid=0](https://docs.google.com/spreadsheets/d/1sxYBrSoU9SzKRIIwvQzAWmRJOqY8qQOQMlxjd-o1Grc/edit#gid=0)

Please refer Current Registration & CVS Rewards (Apr 2024) 

Alongside sunsetting the staking initiative it is also proposed that Phase X is moved away from as well. Phase X up-front bonus will be effectively removed for all new operators, registration tokens will still be present and subject to the 1-year lockup period. 

Refer to the spreadsheet linked above to visualize these changes, essentially up-front locked tokens when purchasing new equipment from XNET will be effectively halved.  

It is proposed that both of these changes will take effect from Epoch 40 (5/27). This is a fundamentally important step to manage near term inflation. 
