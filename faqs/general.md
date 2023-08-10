# General

[What is the Ajna Protocol?](general.md#what-is-the-ajna-protocol)\
[What are the key features of the Ajna Protocol?](general.md#what-are-the-key-features-of-the-ajna-protocol)\
[Where can I use the Ajna Protocol?](general.md#where-can-i-use-the-ajna-protocol)\
[Who are the Stakeholders of the protocol?](general.md#who-are-the-stakeholders-of-the-protocol)\
[What assets can be lent and borrowed?](general.md#what-assets-can-be-lent-and-borrowed-on-ajna)\
[What assets are not compatible with Ajna?](general.md#what-assets-are-not-compatible-with-ajna)\
[What are the Fees?](general.md#what-are-the-fees)\
[How do I create a pool?](general.md#how-do-i-create-a-pool)\
[Does Ajna support rebase tokens?](general.md#does-ajna-support-rebase-tokens)\
[Does Ajna use token governance to make changes to its smart contracts?](general.md#does-ajna-use-token-governance-to-make-changes-to-its-smart-contracts)\
[What networks are you going to deploy on and do you have any plans for deployment on an Ethereum L2?](general.md#what-chains-are-you-going-to-deploy-on-and-do-you-have-any-plans-for-deployment-on-an-ethereum-l2)\
[How can I get involved?](general.md#how-can-i-get-involved)\
[Has Ajna been audited?](general.md#has-ajna-been-audited)\
[Does Ajna have a bug bounty?](general.md#does-ajna-have-a-bug-bounty)\
[Does Ajna labs have admin control over the protocol?](general.md#does-ajna-labs-have-admin-control-over-the-protocol)\
[Where can I get information about Ajna?](general.md#where-can-i-get-information-about-ajna)\
[What are price Oracles?](general.md#what-are-price-oracles)\
[Why is it a big deal that Ajna’s design excludes price oracles?](general.md#why-is-it-a-big-deal-that-ajnas-design-excludes-price-oracles)\
[What is protocol governance?](general.md#what-is-protocol-governance)\
[What is the Ajna Foundation?](general.md#what-is-the-ajna-foundation)

### What is the Ajna Protocol?

The Ajna protocol is a noncustodial, peer-to-pool, permissionless lending and borrowing system that requires no governance or external price feeds to function. The current version is built for Ethereum Virtual Machine(EVM) compatible networks.&#x20;

### What are the key features of the Ajna Protocol?

* Immutable protocol
* Permissionless pool creation
* Borrow or lend with ERC-20 tokens
* Borrow against ERC-721 NFTs and NFT subsets
* Perpetual loans
* Price-specified lending
* Utilization based interest rates
* Liquidation bonds
* Non-rehypothecated collateral

### Where can I use the Ajna Protocol?

1. [Summer.fi](https://summer.fi/ajna) (Rewards active)
2. Static Open Source Frontend _(coming end of summer)_
3. _Others coming soon._

### Who are the Stakeholders of the protocol?

* **Lender**: Lenders choose what valuation they are willing to lend against by depositing tokens into specific price buckets.
* **Borrower**: Borrowers deposit collateral tokens into pools and borrow quote tokens.
* **AJNA Tokenholder**: Delegate their tokens or self-delegate and vote on grant funding decisions.
* **Delegate**: Receives delegated votes and votes on grant proposals.
* **Liquidator**: Triggers liquidation of bad loans by putting up 1-30% of the positions debt in a liquidation bond that pays out depending on the outcome of the collateral sale.
* **Liquidation Auction Bidder**: Bids for and purchases collateral on sale during liquidation auctions.
* **Reserve Auction Bidder**: Bids for and purchases AJNA on sale during reserve auctions.
* **Integrator**: 3rd party that decides to integrate Ajna into their own application, product, or platform.

### What assets can be lent and borrowed on Ajna?

Ajna enables lending for all ERC-20 tokens and borrowing for ERC-20, ERC-721, and ERC-721 collections or subsets through its pools. Pools are pairs of quote and collateral tokens provided by lenders and borrowers.

### What assets are not compatible with Ajna?

The following types of tokens are incompatible with Ajna, and no countermeasures exist to explicitly prevent creating a pool with such tokens, actors should use them at their own risk:

* NFT and fungible tokens which charge a fee on transfer.
* Fungible tokens whose balance rebases.

The following types of tokens are incompatible with Ajna, and countermeasures exist to explicitly prevent creating a pool with such tokens:

* Fungible tokens with more than 18 decimals or 0 decimals, whose `decimals()` function does not return a constant value, or which do not implement the optional [decimals()](https://eips.ethereum.org/EIPS/eip-20#decimals) function.

### What are the fees?

<table><thead><tr><th width="135.33333333333331">Who</th><th width="226">Fee</th><th>Detail</th></tr></thead><tbody><tr><td>Lender</td><td>Unutilized Deposit Fee</td><td>Charged when depositing below the LUP, <br>equivalent to <em>24 hours of interest.</em></td></tr><tr><td>Borrower</td><td>Origination Fee</td><td>Charged to all debt and is <br><em>the greater of one week of interest or 0.05%.</em></td></tr><tr><td>Borrower</td><td>Variable Interest Rate </td><td>APR charged on debt, <em>may change</em> <br><em>once every 12 hours in +- 10% steps.</em></td></tr><tr><td>Borrower</td><td>Liquidation Penalty 1</td><td>Charged when position liquidation is triggered, equivalent to <em>90 days of interest</em>.</td></tr><tr><td>Borrower</td><td>Liquidation Penalty 2</td><td>Charged at the first sale of collateral,<br>equivalent to <em>7% applied to the debt amount.</em></td></tr><tr><td>Everyone</td><td>Network transaction fees</td><td>Charged on all transactions, <br><em>varies by network and other factors.</em></td></tr></tbody></table>

### How do I create a pool?

1. Determine the assets you'd like to borrow or lend against.
2. See if the asset pairing you want to engage with already exists in the Ajna Protocol
3. If it doesn't exist, you can create this pool.
4. First, enter the token addresses of the two assets you would like to comprise the Ajna Pool.
5.  Next, pick which one will be collateral and which one will be the “quote token,” which is the asset that will be lent and borrowed .

    _note: Remember that while Ajna can support NFTs as collateral, quote tokens need to be ERC20._
6. Finally, select an interest rate between 1-10% that you think will be a good starting point for the pool – don’t worry about getting this wrong, the pool will self-adjust over time to find the correct parameters.
7. Once these steps are complete, you can begin lending or borrowing in this Ajna Pool.

### Does Ajna support rebase tokens?

Not natively, but if users wrap their rebase tokens they should work.

### Does Ajna use token governance to make changes to its smart contracts?

No, Ajna is an immutable set of smart contracts that cannot be changed. If a new version of Ajna is deployed, existing liquidity will need to migrate to these new contracts.

### What networks are you going to deploy on and do you have any plans for deployment on an Ethereum L2?

The protocol is written to work on any EVM (Ethereum Virtual Machine) compatible chain. The first launch will be on the Ethereum Mainnet chain with secondary launches on various L2s and compatible L1s.

### How can I get involved?

Join our [discord server](https://discord.gg/T9WSMKfMYJ).\
Participate in the [grants program](https://faqs.ajna.finance/faqs/grants).\
Give integrators like [summer.fi](https://summer.fi/) your feedback.

### Has Ajna been audited?

Ajna has been audited by\
\
[Trail of Bits](https://www.trailofbits.com/) - [https://github.com/ajna-finance/audits/tree/main/tob](https://github.com/ajna-finance/audits/tree/main/tob)\
\
[Quantstamp](https://quantstamp.com/) - [https://github.com/ajna-finance/audits/tree/main/quantstamp](https://github.com/ajna-finance/audits/tree/main/quantstamp)\
\
[Sherlock](https://www.sherlock.xyz/) - [https://github.com/ajna-finance/audits/tree/main/sherlock](https://github.com/ajna-finance/audits/tree/main/sherlock)\
\
[Code4arena](https://code4rena.com/) - [https://github.com/ajna-finance/audits/tree/main/code4rena](https://github.com/ajna-finance/audits/tree/main/code4rena)\
\
Prototech labs - [https://github.com/ajna-finance/audits/tree/main/prototech](https://github.com/ajna-finance/audits/tree/main/prototech)

### Does Ajna have a bug bounty?

Ajna will have a bug bounty once deployed in Q2 2023.

### Does Ajna labs have admin control over the protocol?

No, Ajna Labs has no ability to change or manipulate the smart contracts once they are deployed.

### Where can I get information about Ajna?

[ELI5](https://www.ajna.finance/eli5) | https://www.ajna.finance/eli5 \
[FAQs](https://faqs.ajna.finance/) | https://faqs.ajna.finance/ \
[Whitepaper](https://www.ajna.finance/whitepaper) | https://www.ajna.finance/whitepaper \
[GitHub](https://github.com/ajna-finance) | https://github.com/ajna-finance \
[Twitter](https://twitter.com/ajnafi) | https://twitter.com/ajnafi \
[Website](https://www.ajna.finance) | https://www.ajna.finance \
[Analytics](https://info.ajna.finance/ethereum) | https://Info.ajna.finance/ethereum \
[Deployment Addresses](https://faqs.ajna.finance/info/deployment-addresses) | https://faqs.ajna.finance/info/deployment-addresses

### What are price Oracles?

Oracles provide external data to blockchain applications.

### Why is it a big deal that Ajna’s design excludes price oracles?

Relying on oracles for pricing data in a DeFi application creates an external point of failure as they can be manipulated or compromised. Ajna uses an internal order book empowering lenders to set asset values. This reduces the attack surface of the protocol and makes lending and borrowing more secure.

### What is protocol governance?

Protocol Governance is when a protocol uses token voting to implement changes to the protocol without user consent. It is often used to adjust parameters or add functionality.\
\
AJNA tokens have voting rights in the Grants program, but cannot adjust parameters or add functionality to the protocol itself.

### What is the Ajna Foundation?

The Ajna Foundation, formed in mid-2023, is an entity responsible for the stewardship of the Ajna Protocol's brand assets and to pay for designated maintenance and support services.

