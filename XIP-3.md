## XIP 3: reduce $XNET total supply by 99%

By: Connor Lovely

### Background
XNET has hit an inflection point in growth recently across important network metrics such as online nodes, paid data transferred, and number of token holders (see [here](https://dune.com/steve314600/xnet)).

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

### Implementation
This XIP will be simple to implement since the token burns can come purely from _future_ emissions (unissued tokens). In the “Burn in Place” scenario, the XNET team would systematically burn 99% of the unissued tokens from each pool, including the operator pool, the foundation pool, and the insiders/investor pool.  
