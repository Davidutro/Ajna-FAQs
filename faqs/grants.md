# Grants

[What is the Ajna grants program?](grants.md#what-is-the-ajna-grants-program)\
[What is a grant proposal?](grants.md#what-is-a-grant-proposal)\
[Where can I view grant proposals?](grants.md#where-can-i-view-grant-proposals)\
[How are grants selected?](grants.md#how-are-grant-proposals-selected)\
[How do I vote on a proposal?](grants.md#how-do-i-vote-on-a-proposal)\
[Why should I vote?](grants.md#why-should-i-vote)\
[What is a delegate?](grants.md#what-is-a-delegate)\
[Can I delegate to myself?](grants.md#can-i-delegate-to-myself)\
[Why should I delegate?](grants.md#why-should-i-delegate)\
[Can I earn rewards for delegating?](grants.md#can-i-earn-rewards-for-delegating)\
[Can I earn rewards for voting?](grants.md#can-i-earn-rewards-for-voting)\
[How much do delegates earn?](grants.md#how-much-do-delegates-earn)\
[Can I delegate partially to multiple parties?](grants.md#can-i-delegate-partially-to-multiple-parties)\
[How much AJNA is granted every cycle?](grants.md#how-much-ajna-is-granted-every-cycle)\
[How many grants can be funded per cycle?](grants.md#how-many-grants-can-be-funded-per-cycle)\
[Can less than 10 proposals be selected?](grants.md#can-less-than-10-proposals-be-selected)\
[Can a grantee return AJNA tokens to the protocol?](grants.md#can-a-grantee-return-ajna-tokens-to-the-protocol)\
[My proposal was approved, how do I claim the grant?](grants.md#my-proposal-was-approved-how-do-i-claim-the-grant)

### What is the Ajna grants program?

The grant program for the Ajna Protocol provides funding for growth and development opportunities proposed by independent contractors and teams. Funding may be provided for an array of software development and growth related proposals. Applications are reviewed and voted on by AJNA tokenholders and professional delegates. Funds are granted programmatically based on the results of on-chain votes.

### What is a grant proposal?

A Grant Proposal is submitted to an organization as an explicit request to fund an individual or team to execute on a body of work. Proposals get published, refined, and are then submitted for voting.

### Where can I view grant proposals?

https://forum.ajna.finance

### **How are grant selected?**

When assessing applications, the criteria below should be considered to guide decision making;\
\
Relevance \
All funded projects should be applicable to Ajna.

Benefit \
The goal of this program is to increase the protocol's probability for success.

* Does this project benefit Ajna and its users?
* Will there be a real positive impact?&#x20;

Feasibility \
Ideas and discussions are great, but only realistic projects with tangible results should be funded.

* Can the project really be accomplished? ‍
* Are the objectives and success case realistic?&#x20;

Execution \
Applicants should provide a clear execution plan for completing the project and reaching the goals.

* Is there a clear plan?
* Will grantees report progress?&#x20;

Qualification \
Applicants should provide background or credentials to prove their capabilities.

* Is the individual or team qualified to complete the project? &#x20;

Cost \
There is a sweet spot to attract high quality contributors with competitive funding without overspending.&#x20;

* Is the funding amount within reasonable means?
* Does it align with industry standards?

### How do I vote on a proposal?

To vote on proposals visit [https://app.ajna.finance/grants](https://app.ajna.finance/grants), delegate votes to an address you control, then use the grants section to vote. Another option is to delegate your votes to an address that will participate on your behalf.

### What is a delegate?

A delegate is an individual or group, identified by an Ethereum address, who represents themselves and other AJNA holders in grants voting.

### Can I delegate to myself?

Yes, you can self-delegate. This is expected to be done in order to earn delegate rewards.

### Why should I vote?

The two reasons an AJNA holder votes are to influence grant funding decisions and to earn rewards.

### Why should I delegate?

Voting directly does not earn rewards. Even if you vote yourself, delegating to your own address is recommended since the user can collect delegation rewards. Additionally, If you don’t want to vote, but want to earn rewards and support the growth of the protocol delegation is an easy way of doing that.

### Can I earn rewards for delegating?

No.

### How much do delegates earn?

In the normal grants process, also known as the Primary Funding Mechanism(PFM) 10% of the quarterly distribution is awarded to delegates. However, during an Extraordinary Funding Mechanism(EFM) vote, rewards do not apply.

### Can I earn rewards for voting?

Only if you self-delegate.

### Can I delegate partially to multiple parties?

No, you can only delegate to one at any given time.

### Can I cancel or modify my vote?

No, votes cannot be cancelled or modified. They are final once submitted.

### How much AJNA is granted every cycle?

2% of the treasury is the maximum AJNA granted per cycle. The treasury began with 30% of the total AJNA supply, a total of 300,000,000 AJNA tokens. The first grants distribution will be capped at 6,000,000 AJNA across 10 proposals.

### How many grants can be funded per cycle?

A maximum of 10 grants can be funded every cycle.

### Can less than 10 proposals be selected?

Yes

### Can a grantee return AJNA tokens to the protocol?

Yes, they can send back tokens directly to the treasury by calling `fundTreasury()` in a transaction to the contract address, `0x...`\
\
_**BEWARE**_ tokens cannot be sent to the contract address with a standard `transferFrom()` call.

### My proposal was approved, how do I claim the grant?

Grants can be claimed here, or by doing a manual transaction calling `something` on the treasury contract

\
