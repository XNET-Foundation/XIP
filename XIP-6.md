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
