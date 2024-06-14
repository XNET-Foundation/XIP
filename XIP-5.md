## XIP 5: Implementation of Price Oracle Algorithm 
Draft by bigXhaan, Dharma
_(Dated Emissions Tab): _[https://docs.google.com/spreadsheets/d/1QnhjSzbC_d4xOC7K7oRFP27Tqjc062vKElTSBGyQTcQ/edit#gid=160862862](https://docs.google.com/spreadsheets/d/1QnhjSzbC_d4xOC7K7oRFP27Tqjc062vKElTSBGyQTcQ/edit#gid=160862862)

### Implementation of Price Oracle Algorithms
In an effort to effectively manage token emissions in real time, this proposal is incorporating a price oracle algorithm. This tool aims to dynamically adjust token distribution based on the current market value of $XNET, ensuring that emissions are proportional to token worth. This strategy prevents excessive issuance during price spikes and maintains economic stability by linking the reward system directly to market conditions. The oracle algorithm allows XNET to provide a balanced incentive for network participation while safeguarding the ecosystem against inflation and ensuring a resilient supply mechanism.

A baseline price of $0.10 was chosen for the sake of this model, for simplicity of calculations and recent price stabilization. Changes to this baseline price can be explored in further proposals. Please note that this specific algorithm will only be applicable for CBRS radios- comparable to XNET

#### Formula Breakdown for Reward Adjustment
The reward adjustment formula is designed to dynamically scale the token rewards distributed to node operators based on the current market price of $XNET and the percentage growth of the network. This method ensures that rewards remain fair, sustainable, and aligned with the overall health and expansion of the network.

#### Adjustment Factor Calculation

![alt_text](images/image1.png "image_tooltip")

𝑘 = Sensitivity constant, determining how sharply the rewards decrease as the price increases. 

From testing, we have found a value of 𝑘=2 works well to reduce emissions at a reasonable rate. Please refer to Appendix A for more detail on the role of k.

#### Calculation of Adjustment Factors for Various Prices:
* At $0.05: ≈ 2.512
* At $0.10: ≈ 1
* At $0.50: ≈ 0.590
* At $1.00: ≈ 0.333
* At $5.00: ≈ 0.091

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
