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




## XIP 2 : Cellular Paid Data Buy and Burn Rate 


### Background

XNET distributes earned revenues to the community using the XNET token Buy and Burn mechanism. This means that a percentage of the revenue received by XNET is used to Buy XNET tokens from the community (using various marketplaces) and then ‘Burning’ them, i.e. sending them irrevocably to a Burn wallet.

The current Paid Data rate for Cellular data is 40% as there are high costs associated with running the central Telco Core for Cellular traffic. However, it has become clear that 40% is too low and this can be moved to 50%


### Proposal

The current Buy and Burn rate for Paid Data on Cellular radios is 40%. This means that 40% of the revenue received by XNET from MNOs and MVNOs is used to buy and irrevocably burn $XNET tokens. This rate is proposed to be changed to 50%. This means that 50% of the revenue received by XNET from MNOs and MVNOs will be used to buy and irrevocably burn $XNET tokens.

This change does not affect the Buy and Burn Rate for WiFi Paid Data which is still currently at 80%, i.e. 80% of the WiFi-related revenue received by XNET is used to Buy tokens and Burn them.


## XIP 3: reduce $XNET total supply by 99%

Proposed by Connor Lovely


### Background

XNET has hit an inflection point in growth recently across important network metrics such as online nodes, paid data transferred, and number of token holders (see [here](https://dune.com/steve314600/xnet)).  \
 \
With the creation of a large liquidity pool on Ethereum, the token is much more accessible and liquid, which has resulted in significant recent price appreciation. This is good for all stakeholders and will speed the network growth flywheel (higher token price = higher $ incentives for deployment = more deployment = bigger network = more data transfer = more token burn for data transfer = higher token price). 

In spite of all of this recent progress, the primary complaint of would be investors and industry peers (that is fair IMO) is XNET’s massive and irregular token supply overhang. The market doesn’t like tiny floats because the large difference between circulating supply and total supply (of tokens) means current and future tokenholders are greatly concerned about being diluted when future tokens come online. 

I don’t believe we need nearly as many tokens as were initially laid out in the $XNET tokenomics and propose a 99% reduction in the total supply. This can come purely from _future_ emissions and will be relatively simple to implement given that a 99% cut will leave us with 240M tokens total, which is >10x the circulating supply of tokens, meaning no one will need to burn/send their current tokens anywhere. 

The below chart shows the current state of DeWi tokenomics. Note XNET’s tiny float compared to much larger industry peers.


<table>
  <tr>
   <td>
   </td>
   <td><strong>XNET</strong>
   </td>
   <td><strong>Helium</strong>
   </td>
   <td><strong>World Mobile</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Circ. tokens</strong>
   </td>
   <td>22M
   </td>
   <td>165M
   </td>
   <td>576M
   </td>
  </tr>
  <tr>
   <td><strong>Token price</strong>
   </td>
   <td>$0.15
   </td>
   <td>$5
   </td>
   <td>$0.31
   </td>
  </tr>
  <tr>
   <td><strong>Circ. MC</strong>
   </td>
   <td>$3.3M
   </td>
   <td>$825M
   </td>
   <td>$179M
   </td>
  </tr>
  <tr>
   <td><strong>Total tokens</strong>
   </td>
   <td>24B
   </td>
   <td>223M
   </td>
   <td>2B
   </td>
  </tr>
  <tr>
   <td><strong>FDV</strong>
   </td>
   <td>$3.6B
   </td>
   <td>$1.1B
   </td>
   <td>$630.5M
   </td>
  </tr>
  <tr>
   <td><strong>Float</strong>
   </td>
   <td><span style="text-decoration:underline;">0.08%</span>
   </td>
   <td><span style="text-decoration:underline;">73%</span>
   </td>
   <td><span style="text-decoration:underline;">28.5%</span>
   </td>
  </tr>
</table>



### Proposal

I’m proposing a 99% cut to $XNET total token supply, which is detailed below. Even a 90% cut is not enough in my opinion given that it will still leave XNET with a tiny float compared to peers.

**It’s important to note that this burn comes purely from unissued tokens, which if executed will be extremely beneficial to current tokenholders as their tokens won’t be touched while future tokens/dilution will be greatly reduced.**

The column highlighted in green is my proposal and would put us more closely in line with industry peers. 


<table>
  <tr>
   <td>
   </td>
   <td><strong>XNET</strong>
   </td>
   <td><strong>XNET w 90% cut</strong>
   </td>
   <td><strong>XNET w 99% cut</strong>
   </td>
   <td><strong>Helium</strong>
   </td>
   <td><strong>World Mobile</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Circ. tokens</strong>
   </td>
   <td>22M
   </td>
   <td>22M
   </td>
   <td>22M
   </td>
   <td>165M
   </td>
   <td>576M
   </td>
  </tr>
  <tr>
   <td><strong>Token price</strong>
   </td>
   <td>$0.15
   </td>
   <td>$0.15
   </td>
   <td>$0.15
   </td>
   <td>$5
   </td>
   <td>$0.31
   </td>
  </tr>
  <tr>
   <td><strong>Circ. MC</strong>
   </td>
   <td>$3.3M
   </td>
   <td>$3.3M
   </td>
   <td>$3.3M
   </td>
   <td>$825M
   </td>
   <td>$179M
   </td>
  </tr>
  <tr>
   <td><strong>Total tokens</strong>
   </td>
   <td>24B
   </td>
   <td>2.4B
   </td>
   <td>240M
   </td>
   <td>223M
   </td>
   <td>2B
   </td>
  </tr>
  <tr>
   <td><strong>FDV</strong>
   </td>
   <td>$3.6B
   </td>
   <td>$360M
   </td>
   <td>$36M
   </td>
   <td>$1.1B
   </td>
   <td>$630.5M
   </td>
  </tr>
  <tr>
   <td><strong>Float</strong>
   </td>
   <td><span style="text-decoration:underline;">0.08%</span>
   </td>
   <td><span style="text-decoration:underline;">0.8%</span>
   </td>
   <td><span style="text-decoration:underline;">8%</span>
   </td>
   <td><span style="text-decoration:underline;">73%</span>
   </td>
   <td><span style="text-decoration:underline;">28.5%</span>
   </td>
  </tr>
</table>


 \



### Implementation

This XIP will be simple to implement since the token burns can come purely from _future_ emissions (unissued tokens). In the “Burn in Place” scenario, the XNET team would systematically burn 99% of the unissued tokens from each pool, including the operator pool, the foundation pool, and the insiders/investor pool.  


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


## XIP 5: Implementation of Price Oracle Algorithm 

Draft by bigXhaan, Dharma

_(Dated Emissions Tab): _[https://docs.google.com/spreadsheets/d/1QnhjSzbC_d4xOC7K7oRFP27Tqjc062vKElTSBGyQTcQ/edit#gid=160862862](https://docs.google.com/spreadsheets/d/1QnhjSzbC_d4xOC7K7oRFP27Tqjc062vKElTSBGyQTcQ/edit#gid=160862862)


### Implementation of Price Oracle Algorithms

In an effort to effectively manage token emissions in real time, this proposal is incorporating a price oracle algorithm. This tool aims to dynamically adjust token distribution based on the current market value of $XNET, ensuring that emissions are proportional to token worth. This strategy prevents excessive issuance during price spikes and maintains economic stability by linking the reward system directly to market conditions. The oracle algorithm allows XNET to provide a balanced incentive for network participation while safeguarding the ecosystem against inflation and ensuring a resilient supply mechanism.

A baseline price of $0.10 was chosen for the sake of this model, for simplicity of calculations and recent price stabilization. Changes to this baseline price can be explored in further proposals. Please note that this specific algorithm will only be applicable for CBRS radios- comparable to XNET


#### Formula Breakdown for Reward Adjustment

The reward adjustment formula is designed to dynamically scale the token rewards distributed to node operators based on the current market price of $XNET and the percentage growth of the network. This method ensures that rewards remain fair, sustainable, and aligned with the overall health and expansion of the network.


#### Adjustment Factor Calculation



<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image1.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image1.png "image_tooltip")




<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>



<p id="gdcalert3" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert4">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

 



<p id="gdcalert4" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert5">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>





<p id="gdcalert5" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert6">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>



<p id="gdcalert6" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert7">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>





<p id="gdcalert7" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert8">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>



𝑘 = Sensitivity constant, determining how sharply the rewards decrease as the price increases. 

From testing, we have found a value of 𝑘=2 works well to reduce emissions at a reasonable rate. Please refer to Appendix A for more detail on the role of k.


#### Calculation of Adjustment Factors for Various Prices:



* At $0.05:



<p id="gdcalert8" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert9">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>



<p id="gdcalert9" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert10">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

 ≈ 2.512



* At $0.10:



<p id="gdcalert10" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert11">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>



<p id="gdcalert11" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert12">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

 ≈ 1



* At $0.50:



<p id="gdcalert12" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert13">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>



<p id="gdcalert13" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert14">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

 ≈ 0.590



* At $1.00:



<p id="gdcalert14" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert15">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>



<p id="gdcalert15" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert16">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

 ≈ 0.333



* At $5.00:



<p id="gdcalert16" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert17">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>



<p id="gdcalert17" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert18">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

 ≈ 0.143



* At $10.00:



<p id="gdcalert18" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert19">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>



<p id="gdcalert19" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: equation: use MathJax/LaTeX if your publishing platform supports it. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert20">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>

 ≈ 0.091


<table>
  <tr>
   <td><strong>Price of $XNET</strong>
   </td>
   <td><strong>Adjustment Factor</strong>
   </td>
  </tr>
  <tr>
   <td>$0.05
   </td>
   <td>2.512
   </td>
  </tr>
  <tr>
   <td>$0.10
   </td>
   <td>1.000
   </td>
  </tr>
  <tr>
   <td>$0.50
   </td>
   <td>0.590
   </td>
  </tr>
  <tr>
   <td>$1.00
   </td>
   <td>0.333
   </td>
  </tr>
  <tr>
   <td>$5.00
   </td>
   <td>0.143
   </td>
  </tr>
  <tr>
   <td>$10.00
   </td>
   <td>0.091
   </td>
  </tr>
</table>


Worked example for associated $XNET rewards for a Roofus (BLINQ-FW300) radio during an Epoch at the respective adjustment factors:  


<table>
  <tr>
   <td><strong>Adjustment Factor</strong>
   </td>
   <td><strong>Adjusted Coverage</strong>
   </td>
   <td><strong>Adjusted Validation</strong>
   </td>
   <td><strong>Adjusted Gold</strong>
   </td>
   <td><strong>Total Epoch Rewards</strong>
   </td>
  </tr>
  <tr>
   <td>2.512
   </td>
   <td>3140
   </td>
   <td>3140
   </td>
   <td>12560
   </td>
   <td>18840.0
   </td>
  </tr>
  <tr>
   <td>1.000
   </td>
   <td>1250
   </td>
   <td>1250
   </td>
   <td>5000
   </td>
   <td>7500.0
   </td>
  </tr>
  <tr>
   <td>0.590
   </td>
   <td>737.50
   </td>
   <td>737.50
   </td>
   <td>2950
   </td>
   <td>4425.0
   </td>
  </tr>
  <tr>
   <td>0.333
   </td>
   <td>416.25
   </td>
   <td>416.25
   </td>
   <td>1665
   </td>
   <td>2497.5
   </td>
  </tr>
  <tr>
   <td>0.143
   </td>
   <td>178.75
   </td>
   <td>178.75
   </td>
   <td>715
   </td>
   <td>1072.5
   </td>
  </tr>
  <tr>
   <td>0.091
   </td>
   <td>113.75
   </td>
   <td>113.75
   </td>
   <td>455
   </td>
   <td>682.5
   </td>
  </tr>
</table>



### Managing XNET Price Selection and Mitigating Oracle Attacks

Given the relatively lower liquidity of XNET, the model is indeed susceptible to potential oracle attacks, where investors might attempt to manipulate the market price to influence the reward system. To combat this risk, XNET implements a robust mechanism for selecting the token price:

**Bi-weekly Price Bands**: The price of XNET is updated every two weeks based on predefined price bands. These bands are designed to smooth out volatility and provide a more stable and predictable basis for reward calculations.

**Discretionary Selection**: The selection of the specific price within these bands is at the discretion of the XNET team. This approach allows for expert judgment to play a role in assessing market conditions, ensuring that the chosen price reflects a fair and reasonable value that is resistant to manipulation.

**Mitigation Strategies**:

Monitoring and Analysis: Continuous monitoring of trading patterns and price movements to identify and respond to potential manipulation attempts.

**Adjustment of Price Bands**: The bands themselves can be adjusted based on long-term market trends and changes in market dynamics to ensure they remain relevant and effective.


### Oracle Implementation

We propose an oracle that is the volume-weighted average price, averaged over 30 days, based on data from CoinGecko. CoinGecko provides historical and real-time data for a wide variety of tokens and is plugged into many DEXs.  CoinGecko provides historical information free of charge for up to one year in the past, and has a very functional API. 

We created an example 30-day volume weighted average spreadsheet to illustrate the process, using both static (scraped) data from CoinGecko, as well as calculations based on a live API feed.  You can find that spreadsheet here: [https://docs.google.com/spreadsheets/d/1VBsZFStevZtbjeKP0lSBznMt9oCaffHgXvjKlyjmmKw/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1VBsZFStevZtbjeKP0lSBznMt9oCaffHgXvjKlyjmmKw/edit?usp=sharing)




### Sensitivity Factor _k_


#### Role of 𝑘 in the Adjustment Factor Formula

Definition: 𝑘 is a numeric constant used to modulate the impact of the logarithmic component within the formula.

Function: It scales the output of the logarithm of the ratio _P/P<sub>0 </sub>_where _P_ is the current market price and _P<sub>0</sub>_ is the baseline price. The logarithm provides a smooth, controlled adjustment to the rewards as the price changes.

High 𝑘 Value: A higher value of 𝑘 means the formula is more sensitive to changes in price. Small changes in the price ratio will result in larger adjustments to the rewards, making the rewards decrease more sharply as the price increases.

Low 𝑘 Value: Conversely, a lower value of 𝑘 makes the formula less sensitive to price changes. This results in a gentler slope of reward adjustment, where rewards decrease more gradually as the price increases.


#### Example Usage

If the current price 𝑃 is significantly higher than the baseline price 𝑃<sub>0,</sub>, the logarithmic term log⁡<sub>𝑏</sub>(_P/P<sub>0</sub>_)_ _will yield a positive value. The impact of this positive value on the adjustment factor depends on 𝑘:

If 𝑘 is large, the term 𝑘× log⁡<sub>𝑏</sub>(_P/P<sub>0</sub>_)_ _significantly increases, leading to a smaller adjustment factor, thus reducing the rewards more substantially.

If 𝑘 is small, the increase in 𝑘× log⁡<sub>𝑏</sub>(_P/P<sub>0</sub>_) is more modest, leading to a less dramatic reduction in the adjustment factor, and thus a less severe cut in rewards.


#### Practical Consideration

Choosing the right value for 𝑘 is critical because it directly influences how the reward system reacts to market dynamics, ensuring that the mechanism is neither too volatile (which could destabilize node operator incentives) nor too stagnant (which could fail to adequately respond to significant price increases). The choice of 𝑘 should reflect strategic objectives regarding the stability and economic behavior of the network.


##  XIP 6 : Wi-Fi Data Payout Modification 

Draft by: Heated Lime


### Background

Currently, deployers are paid a fixed 50 XNET per GB for Wi-Fi offload, regardless of the price of XNET. Therefore, it’s hard for deployers to negotiate a fixed amount per GB split with hosts, as those payouts may vary per epoch. Further, a deployer could offload 100 GB per month in different months, and receive a varying fiat amount converted from XNET due to market fluctuations. 

In an effort to make data rewards more predictable for deployers, this XIP proposes implementing a variable amount of XNET corresponding to the average price per epoch, along with a fixed XNET token reward per GB (i.e. $X.XX worth of XNET plus X amount of XNET)


### Proposal

This XIP proposes the following payout schedule per GB for Wi-Fi offload:


<table>
  <tr>
   <td>Period
   </td>
   <td>Fixed Fiat Amount Worth of XNET per GB
   </td>
   <td>Fixed Token Amount per GB
   </td>
  </tr>
  <tr>
   <td>Q2 2024
   </td>
   <td>$3.50 
   </td>
   <td>10 XNET
   </td>
  </tr>
  <tr>
   <td>Q3 2024
   </td>
   <td>$3.50
   </td>
   <td>8 XNET
   </td>
  </tr>
  <tr>
   <td>Q4 2024
   </td>
   <td>$3.50
   </td>
   <td>6 XNET
   </td>
  </tr>
  <tr>
   <td>Q1 2025
   </td>
   <td>$3.00
   </td>
   <td>5 XNET
   </td>
  </tr>
  <tr>
   <td>Q2 2025
   </td>
   <td>$3.00
   </td>
   <td>5 XNET
   </td>
  </tr>
  <tr>
   <td>Q3 2025
   </td>
   <td>$2.50
   </td>
   <td>5 XNET
   </td>
  </tr>
  <tr>
   <td>Q4 2025
   </td>
   <td>$2.50
   </td>
   <td>5 XNET
   </td>
  </tr>
  <tr>
   <td>Q1 2026
   </td>
   <td>$2.00
   </td>
   <td>5 XNET
   </td>
  </tr>
  <tr>
   <td>Q2 2026
   </td>
   <td>$2.00
   </td>
   <td>5 XNET
   </td>
  </tr>
  <tr>
   <td>Q3 2026
   </td>
   <td>$1.50
   </td>
   <td>5 XNET
   </td>
  </tr>
  <tr>
   <td>Q4 2026+
   </td>
   <td>$1.50
   </td>
   <td>5 XNET
   </td>
  </tr>
</table>


The average XNET price from all days in the epoch in which the data occurred will be used to calculate the price in which the fiat amount is calculated. For example, this example will assume 30 GB of Wi-Fi data was offloaded from the past epoch in Q2 2024, and will assume the following price of XNET from that epoch:


<table>
  <tr>
   <td>Epoch Day
   </td>
   <td>Average Daily Price
   </td>
  </tr>
  <tr>
   <td>Day 1
   </td>
   <td>$.045
   </td>
  </tr>
  <tr>
   <td>Day 2
   </td>
   <td>$.056
   </td>
  </tr>
  <tr>
   <td>Day 3
   </td>
   <td>$.082
   </td>
  </tr>
  <tr>
   <td>Day 4
   </td>
   <td>$.090
   </td>
  </tr>
  <tr>
   <td>Day 5
   </td>
   <td>$.055
   </td>
  </tr>
  <tr>
   <td>Day 6
   </td>
   <td>$.05
   </td>
  </tr>
  <tr>
   <td>Day 7
   </td>
   <td>$.049
   </td>
  </tr>
  <tr>
   <td>Day 8
   </td>
   <td>$.0420
   </td>
  </tr>
  <tr>
   <td>Day 9
   </td>
   <td>$.069
   </td>
  </tr>
  <tr>
   <td>Day 10
   </td>
   <td>$.056
   </td>
  </tr>
  <tr>
   <td>Day 11
   </td>
   <td>$.065
   </td>
  </tr>
  <tr>
   <td>Day 12
   </td>
   <td>$.053
   </td>
  </tr>
  <tr>
   <td>Day 13
   </td>
   <td>$.052
   </td>
  </tr>
  <tr>
   <td>Day 14
   </td>
   <td>$.050
   </td>
  </tr>
  <tr>
   <td><strong>Average Price for Epoch</strong>
   </td>
   <td><strong>$0.0581</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Variable XNET Reward</strong>
   </td>
   <td><strong>(3.50/.0581) = 60.24</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Fixed XNET Reward</strong>
   </td>
   <td><strong>10</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Total XNET Reward for Epoch</strong>
   </td>
   <td><strong>70.24</strong>
   </td>
  </tr>
</table>



## XIP 7: Chain Migration/XNET Foundation 

By: bigXhaan, Dharma, connexa 


### Background 

The $XNET token launched on the Polygon blockchain on November 16, 2022. While Polygon was a good place for XNET to start, it has become clear that Polygon - for all of its virtues - may not be the best place for the next phase of XNET development. With the upcoming launch of the XNET Foundation we thought it was appropriate to consider whether there might be a better home for XNET going forward. Having spent several months looking into it, we believe that there is.


#### Why did XNET Start on Polygon?

Two years ago when $XNET launched, the landscape of L1s looked very different. The only mature blockchain technology (other than Bitcoin and its forks) was the Ethereum Virtual Machine. Even then, the Ethereum L1 was expensive and slow. Polygon promised a higher-throughput, lower-cost alternative that was based on the same fundamental technology. Alternatives existed, but were highly experimental. 


#### Why Move Now?

Polygon was the right place for XNET to start, and has been a good home for XNET in many ways. However, Polygon itself has become more and more congested and expensive since XNET’s launch. While this isn’t a barrier to XNET’s operations now, it puts a practical limit on how much of XNET’s operations could ever be moved on-chain. Furthermore, as XNET has developed, other technologies have matured, and certain Layer 1 (L1) blockchains and Layer 2 (L2) solutions now surpass Polygon in several key metrics, as highlighted in this [analysis.](https://dune.com/decrypto_space/state-of-ethereum-scaling)

Beyond technical evolution, XNET’s sector of crypto has also been maturing. When XNET started, the term Decentralized Physical Infrastructure Networks (DePIN) didn’t exist, and Decentralized Wireless (DeWi) was not in wide use.  Now, DePIN is an emerging sector with significant market interest and a growing community. However, the center of that community isn’t on Polygon. Newer chains, like IoTeX, SUI, and Solana, have distinguished themselves as premier platforms for DePIN, and Base has emerged as the better, faster alternative to Polygon for EVM-centric development. 

The opportunity to move XNET to a platform with higher performance and lower fees, closer to the center of activity in the emerging DePIN sector, can’t be ignored. And if we are to make such a move, now is the time — we will be launching the XNET Foundation soon, and once the foundation is launched a new DAO governance structure will be rolled out relying on a formal on-chain voting system. It will never be easier to make this transition in the future than it is right now. 

Furthermore, XIP 3 and community discussions have identified a significant issue with $XNET's supply overhang. The mechanism to address this identified in XIP 3 isn’t workable for regulatory and operational reasons.  However, this can be addressed as part of a chain migration and token relaunch.

This proposal will detail the implementation of the chain migration. 


### Token Supply and Conversion Overview

A new token will be minted on a different blockchain with a new maximum supply, proposed to be 2.4 billion tokens. For differentiation purposes, this new token will have a new ticker — in this document we will use $X, though the choice of ticker is not final.

To allow and encourage current holders of $XNET to exchange $XNET for $X, we propose the following :  



1. We will create a token exchange contract on the new chain that will swap bridged $XNET for $X in a pre-defined ratio. See “Token Exchange”, below.
2. We will unlock all $XNET that are held in our standard lock-with-escrow contract.  See “Locked Radio Tokens,” below.
3. We will accelerate the issuance of all $XNET that would have been distributed as the result of staking bonuses, or other incentive mechanisms. See “Staking Rewards Payout,” below. The goal is to make all $XNET that would be issued for operational purposes in the near future available now for exchange.  
4. The token exchange mechanism will temporarily support a 1:1 conversion ratio, thus offering current $XNET holders an effective 10x multiplier on their holdings.  This will incentivize the migration of $XNET to $X.  After the expiration of this incentive period, tokens will be exchangeable at a 10:1 ratio reflective of the new, lower supply cap. See “Token Exchange”, below.
5. After the TGE and migration, all new operational rewards will be issued in the new token, $X.
6. Once the Foundation DAO is active, all governance voting will be conducted through the new $X token, and the soon-to-be-issued, non-transferable $XGOV governance token. 


### Token Exchange

To exchange $XNET for $X, current $XNET holders will first bridge their tokens to the new chain via the Wormhole bridge, resulting in wrapped $XNET, or $WXNET.  Then, holders of $WXNET will use the $X token exchange contract (XTEC) to exchange $WXNET for $X, in a pre-defined ratio.

That exchange ratio will initially be 1:1 - with the reduced maximum supply of $X vs $XNET, this is an effective 10x multiplier in the fraction of total supply. This will have the effect of reducing the supply overhang to the benefit of our early adopters, as well as incentivizing the exchange of $XNET for $X, as this exchange ratio will be temporary. 

After the expiration of the incentive exchange period (which will be long enough to accommodate an orderly exchange - a period of weeks, but not months) the exchange ratio will be reset to 10:1, and stay that way indefinitely.  This will allow for any stragglers to convert their $XNET into $X, but at a much less favorable ratio. 


### Locked Radio Tokens

There are a number of tokens that have already been issued but are locked, i.e. held in a closed account and not available for circulation. By far the majority of these are the Registration Bonus tokens issued to newly registered radios, primarily Cellular. To date there are approximately 5.6 million tokens that are locked for this reason. We would like to provide a reasonable opportunity to convert these locked tokens during the incentive conversion period when a 1:1 ratio is available, hence the necessity to unlock and issue these tokens.

Staking Rewards Payout

There are also a significant number of $XNET staking payout tokens that would be issued after the incentive conversion period is past.  In the most recent epoch disbursement (Epoch 40), the Staking Rewards were modified to take into account the Registration Bonus tokens that had become unlocked, and thus no longer eligible for staking rewards.

So that those operators eligible for the staking payouts don’t miss their opportunity to convert at the most favorable exchange ratio, we will be accelerating the payout of the staking rewards  due for each eligible locked balance. These pay-outs would be unlocked and in lump sum, allowing the conversion of such balances to the new token at the 1:1 ratio.
