# 🌐 General

[What is the Ajna Protocol?](general.md#what-is-the-ajna-protocol)\
[What are the key features of the Ajna Protocol?](general.md#what-are-the-key-features-of-the-ajna-protocol)\
[What are some of the use cases?](general.md#what-are-some-of-the-use-cases)\
[Where can I use the Ajna Protocol?](general.md#where-can-i-use-the-ajna-protocol)\
[Who are the Stakeholders of the protocol?](general.md#who-are-the-stakeholders-of-the-protocol)\
[What are the Fees?](general.md#what-are-the-fees)\
[Does Ajna use token governance to make changes to its smart contracts?](general.md#does-ajna-use-token-governance-to-make-changes-to-its-smart-contracts)\
[What other networks will Ajna be deployed on?](general.md#what-other-networks-will-ajna-be-deployed-on)\
[Has Ajna been audited?](general.md#has-ajna-been-audited)\
[Does Ajna have a bug bounty?](general.md#does-ajna-have-a-bug-bounty)\
[What happens if the code becomes outdated?](general.md#what-happens-if-the-code-becomes-outdated)\
[Does Ajna labs have admin control over the protocol?](general.md#does-ajna-labs-have-admin-control-over-the-protocol)\
[What are price Oracles?](general.md#what-are-price-oracles)\
[Why is it a big deal that Ajna’s design excludes price oracles?](general.md#why-is-it-a-big-deal-that-ajnas-design-excludes-price-oracles)\
[What is the Ajna Foundation?](general.md#what-is-the-ajna-foundation)\
[Where can I get information about Ajna?](general.md#where-can-i-get-information-about-ajna)\
[How can I get involved?](general.md#how-can-i-get-involved)

### What is the Ajna Protocol?

The Ajna protocol is a noncustodial, peer-to-pool, permissionless lending and borrowing system that requires no governance or external price feeds to function. The current version is built for Ethereum Virtual Machine(EVM) compatible networks.&#x20;

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
[Summer.fi](https://summer.fi/ajna) ([Rewards active](https://blog.summer.fi/ajna-rewards-update/)) | https://summer.fi/ajna/earn&#x20;

_**Current UIs for liquidations**_\
[Liquidations UI](https://app.ajna.finance/markets) | https://app.ajna.finance/markets\
_To be a kicker or participate in auctions, click on pool details and click "manage pool"_&#x20;

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

<table><thead><tr><th width="135.33333333333331">Who</th><th width="225">Fee</th><th>Detail</th></tr></thead><tbody><tr><td>Lender</td><td>Unutilized Deposit Fee</td><td>Charged when depositing below the LUP, <br>equivalent to <em>24 hours of interest.</em></td></tr><tr><td>Borrower</td><td>Origination Fee</td><td>Charged to all debt and is <br><em>the greater of one week of interest or 0.05%.</em></td></tr><tr><td>Borrower</td><td>Variable Interest Rate </td><td>APR charged on debt, <em>may change</em> <br><em>once every 12 hours in +- 10% steps.</em></td></tr><tr><td>Borrower</td><td>Liquidation Penalty 1</td><td>Charged when position liquidation is triggered, equivalent to <em>90 days of interest</em>.</td></tr><tr><td>Borrower</td><td>Liquidation Penalty 2</td><td>Charged at the first sale of collateral,<br>equivalent to <em>7% applied to the debt amount.</em></td></tr><tr><td>Everyone</td><td>Network transaction fees</td><td>Charged on all transactions, <br><em>varies by network and other factors.</em></td></tr></tbody></table>

### Does Ajna use token governance to make changes to its smart contracts?

No, Ajna is an immutable set of smart contracts that cannot be changed. If a new version of Ajna is deployed, existing liquidity will need to migrate to these new contracts.

### What other networks will Ajna be deployed on?

The protocol is written to work on any EVM (Ethereum Virtual Machine) compatible chain. The first launch will be on the Ethereum Mainnet chain with secondary launches on various L2s and compatible L1s.

### Has Ajna been audited?

Ajna has been audited by\
\
[Trail of Bits](https://www.trailofbits.com/) - [https://github.com/ajna-finance/audits/tree/main/tob](https://github.com/ajna-finance/audits/tree/main/tob)\
[Quantstamp](https://quantstamp.com/) - [https://github.com/ajna-finance/audits/tree/main/quantstamp](https://github.com/ajna-finance/audits/tree/main/quantstamp)\
[Sherlock](https://www.sherlock.xyz/) - [https://github.com/ajna-finance/audits/tree/main/sherlock](https://github.com/ajna-finance/audits/tree/main/sherlock)\
[Code4arena](https://code4rena.com/) - [https://github.com/ajna-finance/audits/tree/main/code4rena](https://github.com/ajna-finance/audits/tree/main/code4rena)\
Prototech labs - [https://github.com/ajna-finance/audits/tree/main/prototech](https://github.com/ajna-finance/audits/tree/main/prototech)

### Does Ajna have a bug bounty?

Ajna will have a bug bounty once deployed in Q2 2023.

### What happens if the code becomes outdated?

The Ajna smart contracts are non-upgradable, so if something causes them to break or work sub-optimally the only remedy is to launch a newer version of Ajna in parallel that contains any needed fixes.&#x20;

### Does Ajna labs have admin control over the protocol?

No, Ajna Labs has no ability to change or manipulate the smart contracts once they are deployed.

### What are price Oracles?

Oracles provide external data to blockchain applications.

### Why is it a big deal that Ajna’s design excludes price oracles?

Relying on oracles for pricing data in a DeFi application creates an external point of failure as they can be manipulated or compromised. Ajna uses an internal order book empowering lenders to set asset values. This reduces the attack surface of the protocol and makes lending and borrowing more secure.

### What is the Ajna Foundation?

The Ajna Foundation, formed in mid-2023, is an entity responsible for the stewardship of the Ajna Protocol's brand assets and to pay for designated maintenance and support services.

### Where can I get information about Ajna?

[ELI5](https://www.ajna.finance/eli5) | https://www.ajna.finance/eli5 \
[FAQs](https://faqs.ajna.finance/) | https://faqs.ajna.finance/ \
[Whitepaper](https://www.ajna.finance/whitepaper) | https://www.ajna.finance/whitepaper \
[GitHub](https://github.com/ajna-finance) | https://github.com/ajna-finance \
[Twitter](https://twitter.com/ajnafi) | https://twitter.com/ajnafi \
[Website](https://www.ajna.finance) | https://www.ajna.finance \
[Analytics](https://info.ajna.finance/ethereum) | https://Info.ajna.finance/ethereum \
[Audits](https://github.com/ajna-finance/audits) | https://github.com/ajna-finance/audits\
[Deployment Addresses](https://faqs.ajna.finance/info/deployment-addresses) | https://faqs.ajna.finance/info/deployment-addresses

### How can I get involved?

Join our [discord server](https://discord.gg/T9WSMKfMYJ).\
Participate in the [grants program](https://faqs.ajna.finance/faqs/grants).\
Give integrators like [summer.fi](https://summer.fi/) your feedback.

