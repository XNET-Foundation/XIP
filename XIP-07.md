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
