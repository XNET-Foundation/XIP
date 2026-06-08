# XIP-9: Restore 1:1 Converter
By: awarshauer (9/10/2023)

## Background

The migration of the XNET project from the Polygon chain to Solana was a successful endeavor for the project, bringing new participants from the Solana DePIN community into XNET and addressing the token overhang issues described in XIP-3 and XIP-7
As part of the migration process, the project used a multistep process to move XNET on Polygon to XNET on Solana. This process has two main steps:

Bridging from Polygon XNET to wrapped Solana XNET using the Wormhole portal token bridge
Converted wrapped Solana XNET to Solana XNET using the XNET Foundation’s token conversion tool

In XIP-7 this converter tool was supposed to have an exchange ratio of 1:1 “for a period of weeks” to allow for token holders adequate time to be properly informed of the migration and to navigate the multistep migration process. It should be noted that this XIP did not go through rigorous community discussion or voting to align on the details of the proposal around this conversion process. 

Unfortunately, the 1:1 conversion process had several issues that led to a large percentage of “old” XNET stranded on various chains. There is an estimated 5.4M Polygon XNET, 0.4M IoTeX XNET, and 1.2M Ethereum XNET, representing roughly 10% of total supply. This has negatively impacted token holders, as evidenced by multiple comments in the discord from community members expressing discontent with the current 10:1 exchange.

### A few of the issues included:
Insufficient notification of the migration process, such as:
- Lack of email(s) to previous equipment purchasers to notify of migration
- Unclear timeline and triggers for closing the 1:1 exchange
- Outdated materials listed on the Coingecko “Old” token, with no mention of 1:1 exchange ending on a specific date
- Late announcement of 1:1 exchange ending (4 days prior), timed around a major US holiday weekend 
- Total of 17 days from 1:1 converter opening (8/16/24-9/3/24) until 1:1 closure
- No community input on shifting from 1:1 to 10:1

## Related XIPs
XIP-3: Reduce $XNET total supply
XIP-7: Chain Migration/XNET Foundation

## Proposal
On the 9-11-2024 governance call, the team acknowledged that there should be a process for legitimate token holders to bridge 1:1 in the short-to-intermediate term. They also expressed that restoring the original 1:1 token converter could cause issues with investors and market participants, so it would be difficult to roll back the change to 10:1 for the tool. As a compromise, the team proposed a renewed information campaign to encourage token holders of the original XNET token to bridge and convert to Solana, coupled with a mechanism to convert at 1:1 through contact with the XNET team. 

### This proposal has four actionable steps: 
Restore the 1:1 converter tool
Extend the 1:1 period by the following criteria:
A total of 6 weeks from the passage of XIP-9
2 weeks past a threshold of 95% migration
Update the Coingecko page for the “old” XNET token with the latest XNET migration documentation
Email all Polygon wallet holders in the XNET reward database to inform them of the migration. 
Create a method of inquiry for token holders to contact the XNET team and convert at a 1:1 exchange ratio after verification

### Rationale
While the XNET migration was a technical success, the 1:1 conversion process did not leave adequate time, and there was not a full good-faith effort to maximize the percentage of tokens migrated to Solana. This was clearly evidenced by 15-20% of the supply not being bridged over within the condensed time period. 

While this is held up by some community members as a positive for the project to reward “active” participants at the expense of diluting 15-20% of the original holders, it more likely creates animosity towards the project for an arbitrary decision without proper governance. There has been no stated rationale by the team for why the 1:1 conversion time period should not be extended to be more inclusive of “passive” token holders.
