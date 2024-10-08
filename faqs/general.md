# 🌐 General

[What is the Ajna Protocol?](general.md#what-is-the-ajna-protocol)\
[What are the key features of the Ajna Protocol?](general.md#what-are-the-key-features-of-the-ajna-protocol)\
[What are some of the use cases?](general.md#what-are-some-of-the-use-cases)\
[Where can I use the Ajna Protocol?](general.md#where-can-i-use-the-ajna-protocol)\
[Who are the Stakeholders of the protocol?](general.md#who-are-the-stakeholders-of-the-protocol)\
[What are the Fees?](general.md#what-are-the-fees)\
[How much Net Interest Margin does the Ajna Protocol earn?](general.md#how-much-net-interest-margin-does-the-ajna-protocol-earn)\
[Can an asset be too expensive or too cheap to use in Ajna?](general.md#can-an-asset-be-too-expensive-or-too-cheap-to-use-in-ajna)\
[Does Ajna use token governance to make changes to its smart contracts?](general.md#does-ajna-use-token-governance-to-make-changes-to-its-smart-contracts)\
[What other networks will Ajna be deployed on?](general.md#what-other-networks-will-ajna-be-deployed-on)\
[Has Ajna been audited?](general.md#has-ajna-been-audited)\
[Does Ajna have a bug bounty?](general.md#does-ajna-have-a-bug-bounty)\
[What happens if the code becomes outdated?](general.md#what-happens-if-the-code-becomes-outdated)\
[What happens if the front end sites go down?](general.md#what-happens-if-the-front-end-sites-go-down)\
[Does Ajna labs have admin control over the protocol?](general.md#does-ajna-labs-have-admin-control-over-the-protocol)\
[Why is it a big deal that Ajna’s design excludes price oracles?](general.md#why-is-it-a-big-deal-that-ajnas-design-excludes-price-oracles)\
[What is the Ajna Foundation?](general.md#what-is-the-ajna-foundation)\
[Where can I get information about Ajna?](general.md#where-can-i-get-information-about-ajna)\
[How can I get involved?](general.md#how-can-i-get-involved)

### What is the Ajna Protocol?

The Ajna protocol is a noncustodial, peer-to-pool, permissionless lending and borrowing system that functions without governance or external price feeds. The current version is built for Ethereum Virtual Machine(EVM) compatible networks.&#x20;

### What are the key features of the Ajna Protocol?

* Permissionless pool creation
* Borrow or lend with ERC-20 tokens
* Borrow against ERC-721 NFTs and NFT subsets
* Perpetual loans
* Price-specified lending
* Utilization based interest rates
* Liquidation bonds
* Non-rehypothecated collateral
* Uncapped pools (no maximum lend or borrow amounts)
* Immutable protocol (no protocol governance)
* No whitelists
* No oracles

### What are some of the use cases?

Stablecoin/Stablecoin

Ajna enables the creation of like-asset money markets. For example, stablecoin collateral and stablecoin quote tokens can be used, such as USDC as collateral and USDT as quote token. The lowest collateralization ratio is only possible with Ajna because this parameter is set by users rather than by governance.

Leverage

Ajna offers borrowers the ability to access leverage, which involves using borrowed funds to increase their trading position beyond what would be possible with their cash balance alone. While existing DeFi protocols work well for large and liquid tokens, they often have high minimum collateralization ratios that limit the maximum amount of leverage available. Ajna's unique feature of allowing lenders to choose their own collateralization ratios enables borrowers to open positions that may not be feasible with current protocols. Where current protocols reject lower tier tokens, Ajna creates a possibility for these assets to be utilized for leverage.

NFT borrowing

Another use case is NFT borrowing. In the current market, only the top 20 collections are serviced, but Ajna has no such limitation. It can be used by current NFT owners to get loans instead of selling their assets. This is especially useful for newer projects that don’t want to deal with getting their NFTs whitelisted elsewhere.

Shorting Markets

Lastly, Ajna can facilitate shorting markets. By designating an “XYZ” token as the quote token and a stablecoin as the collateral token, a borrowing market is created where “XYZ” tokens can be borrowed and shorted, allowing for speculation on the “XYZ” token's declining price. Such facilities are essential for market makers to develop efficient sell-side liquidity. What makes Ajna distinct among current DeFi protocols is the variety of possible shorting markets it can offer.

### Where can I use the Ajna Protocol?

_**Current UIs for borrow/lending**_ \
[Summer.fi](https://summer.fi/ajna) | [https://summer.fi/ajna/earn ](https://summer.fi/ajna)\
[BuiltbyMom UI](https://ajnafi.com) | [https://Ajnafi.com](https://ajnafi.com)\
[Yearn Lender UI](https://twitter.com/yearnfi) | [https://juiced.app/pools](https://juiced.app/pools)

_**Current UIs for liquidations**_\
[Liquidations UI](https://app.ajna.finance/markets) | https://Ajnafi.com\
_To be a kicker or participate in auctions, click on pool details and click "manage pool"_ \
\
_**Access Old Pools from first deployment**_\
[_https://retired.ajnafi.com/_](https://retired.ajnafi.com/)

### Who are the Stakeholders of the protocol?

* **Lender**: Lenders choose what valuation they are willing to lend against by depositing tokens into specific price buckets.
* **Borrower**: Borrowers deposit collateral tokens into pools and borrow quote tokens.
* **AJNA Tokenholder**: Delegate their tokens or self-delegate and vote on grant funding decisions.
* **Delegate**: Receives delegated votes and votes on grant proposals.
* **Liquidator**: Triggers liquidation of bad loans by putting up 1-30% of the positions debt in a liquidation bond that pays out depending on the outcome of the collateral sale.
* **Liquidation Auction Bidder**: Bids for and purchases collateral on sale during liquidation auctions.
* **Reserve Auction Bidder**: Bids for and purchases AJNA on sale during reserve auctions.
* **Integrator**: 3rd party that decides to integrate Ajna into their own application, product, or platform.

### What are the fees?

<table><thead><tr><th width="135.33333333333331">Who</th><th width="225">Fee</th><th>Detail</th></tr></thead><tbody><tr><td>Lender</td><td>Deposit Fee</td><td>Charged when depositing quote tokens or moving them to lower price buckets, <br>equivalent to <em>8 hours of interest.</em></td></tr><tr><td>Borrower</td><td>Origination Fee</td><td>Charged to all debt and is <br><em>the greater of one week of interest or 0.05%.</em></td></tr><tr><td>Borrower</td><td>Variable Interest Rate </td><td>APR charged on debt, <em>may change</em> <br><em>once every 12 hours in +- 10% steps.</em></td></tr><tr><td>Borrower</td><td>Liquidation Penalty, <br>AKA the <a href="https://faqs.ajna.finance/getting-started/glossary#borrower-take-penalty">Borrower Take Penalty</a></td><td>Charged when collateral is taken from the auction at a variable rate depending on the collateral's sale price.</td></tr><tr><td>Everyone</td><td>Network transaction fees</td><td>Charged on all transactions, <br><em>varies by network and other factors.</em></td></tr></tbody></table>

### How much Net Interest Margin does the Ajna Protocol earn?

The protocol earns between 3.23 and 14.95% NIM. It depends on the pool's utilization, see the table below:

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### Can an asset be too expensive or too cheap to use in Ajna?

Yes. Think carefully when you get into the 9 digit range; 100m+\
Quote Tokens with very small unit sizes are dangerous as well.\
\
_Limits_\
max auction bid = 50b\
auction starting price is 256x reference price (capped at 50B)

max price bucket is slightly less than 1B (999969141.897...)\
min price bucket is 0.00000009983628289

_Guidelines_\
Be within a factor of 10 with the assets (assume 10x up or down)

### Does Ajna use token governance to make changes to its smart contracts?

No, Ajna is an immutable set of smart contracts that cannot be changed. If a new version of Ajna is deployed, existing liquidity will need to migrate to these new contracts.

### What other networks will Ajna be deployed on?

The protocol is written to work on any EVM (Ethereum Virtual Machine) compatible chain. The first launch will be on the Ethereum Mainnet chain with secondary launches on various L2s and compatible L1s.

### Has Ajna been audited?

The Ajna Protocol code went through 10 audits.\
\
A full breakdown of all the audits can be [found here, on the Ajna Github](https://github.com/ajna-finance/audits/blob/main/README.md).\
\
1\. Sherlock 1st contest (Jan 9, 2023 - Jan 30, 2023)\
2\. Trail Of Bits Audit (Feb 13, 2023 - April 3, 2023)\
3\. Quantstamp Audit (April 24, 2023 - May 3, 2023)\
4\. Prototech Audit (April 26, 2023 - June 5, 2023)\
5\. Code4rena Audit (May 3, 2023 - May 11, 2023)\
6\. Sherlock 2nd contest (June 5, 2023 - June 22, 2023)\
7\. Fixed Point Solutions & Servo Farms (August 7, 2023 - August 31, 2023)\
8\. Kirill (October 6, 2023 - December 21, 2023)\
9\. Certora (October 6, 2023 - December 21, 2023)\
10\. Sherlock 3rd contest (October 13, 2023 - October 27, 2023)

### Does Ajna have a bug bounty?

Ajna will have a bug bounty once redeployed.

### What happens if the code becomes outdated?

The Ajna smart contracts are non-upgradable, so if something causes them to break or work sub-optimally the only remedy is to launch a newer version of Ajna in parallel that contains any needed fixes.&#x20;

### What happens if the front end sites go down?

Even though ajnafi.com does utilize a helper contract, in result you get a regular position, with no gotchas. Meaning it'll work in Etherscan's contracts UI or in theoretical alternative frontend.

Summer.fi contracts are all executable through etherscan too, and their frontend is opensource too for anyone to be able to run it themselves (although it takes some technical understanding and you're own RPC keys etc)

### Does Ajna labs have admin control over the protocol?

No, Ajna Labs has no ability to change or manipulate the smart contracts once they are deployed.

### Why is it a big deal that Ajna’s design excludes price oracles?

Relying on [oracles](https://faqs.ajna.finance/getting-started/glossary#oracle) for pricing data in a DeFi application creates an external point of failure as they can be manipulated or compromised. Ajna uses an internal order book empowering lenders to set asset values. This reduces the attack surface of the protocol and makes lending and borrowing more secure.

### What is the Ajna Foundation?

The Ajna Foundation, formed in mid-2023, is an entity responsible for the stewardship of the Ajna Protocol's brand assets and to pay for designated maintenance and support services.

### Where can I get information about Ajna?

[Analytics](https://info.ajna.finance/ethereum) | https://Info.ajna.finance/ethereum \
[Audits](https://github.com/ajna-finance/audits) | https://github.com/ajna-finance/audits\
[Blog](https://forum.ajna.finance/c/blog) | https://forum.ajna.finance/c/blog\
[Deployment Addresses](https://faqs.ajna.finance/info/deployment-addresses) | https://faqs.ajna.finance/info/deployment-addresses\
[ELI5](https://www.ajna.finance/eli5) | https://www.ajna.finance/eli5 \
[FAQs](https://faqs.ajna.finance/) | https://faqs.ajna.finance/ \
[GitHub](https://github.com/ajna-finance) | https://github.com/ajna-finance \
[Twitter](https://twitter.com/ajnafi) | https://twitter.com/ajnafi \
[Website](https://www.ajna.finance) | https://www.ajna.finance \
[Whitepaper](https://www.ajna.finance/whitepaper) | https://www.ajna.finance/whitepaper&#x20;

### How can I get involved?

Join our [discord server](https://discord.gg/T9WSMKfMYJ).\
Participate in the [grants program](https://faqs.ajna.finance/faqs/grants).\
Give integrators like [summer.fi](https://summer.fi/) your feedback.

