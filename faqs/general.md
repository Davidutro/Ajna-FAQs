# General

[What is the Ajna Protocol?](general.md#what-is-the-ajna-protocol)\
[Where can I use the Ajna Protocol?](general.md#where-can-i-use-the-ajna-protocol)\
[What assets can be lent and borrowed?](general.md#what-assets-can-be-lent-and-borrowed-on-ajna)\
[How does Ajna work?](general.md#how-does-ajna-work)\
[How do I create a pool?](general.md#how-do-i-create-a-pool)\
[Does Ajna use token governance to make changes to its smart contracts?](general.md#does-ajna-use-token-governance-to-make-changes-to-its-smart-contracts)\
[What networks are you going to deploy on and do you have any plans for deployment on an Ethereum L2?\
](general.md#what-chains-are-you-going-to-deploy-on-and-do-you-have-any-plans-for-deployment-on-an-ethereum-l2)[When will the Ajna Protocol launch?](general.md#when-will-the-ajna-protocol-launch)\
[How can I get involved?](general.md#how-can-i-get-involved)\
[Is Ajna custodial?](general.md#is-ajna-custodial)\
[Has Ajna been audited?](general.md#has-ajna-been-audited)\
[Does Ajna have a bug bounty?](general.md#does-ajna-have-a-bug-bounty)\
[Does Ajna labs have admin control over the protocol?](general.md#does-ajna-labs-have-admin-control-over-the-protocol)\
[Where can I get information about Ajna?](general.md#where-can-i-get-information-about-ajna)\
[Where can I test the application? ](general.md#where-can-i-test-the-application)\
[What are price Oracles?](general.md#what-are-price-oracles)\
[Why is it a big deal that Ajna’s design excludes price oracles?](general.md#why-is-it-a-big-deal-that-ajnas-design-excludes-price-oracles)\
[What is governance in the context of a protocol?](general.md#what-is-governance-in-the-context-of-a-protocol)\
[What is the Ajna Foundation?](general.md#what-is-the-ajna-foundation)

### What is the Ajna Protocol?

The Ajna protocol is a noncustodial, peer-to-pool, permissionless lending and borrowing system that requires no governance or external price feeds to function. The current version is built for Ethereum Virtual Machine(EVM) compatible networks.&#x20;

### Where can I use the Ajna Protocol?

1. [Summer.fi](https://summer.fi/ajna)
2. Static Open Source Frontend _(coming end of summer)_
3. _Others coming soon._

### What assets can be lent and borrowed on Ajna?

Ajna enables lending for all ERC-20 tokens and borrowing for ERC-20, ERC-721, and ERC-721 collections or subsets through its pools. Pools are pairs of quote and collateral tokens provided by lenders and borrowers.

### How does Ajna work?

Once a pool has been created, any user can lend or borrow. \
Lenders deposit quote tokens at a price they’re willing to lend at while borrowers deposit collateral to borrow against. Loans on Ajna are perpetual in nature and do not expire. The system automatically manages interest rates and liquidations.\
\
This is all possible because Ajna is open source software&#x20;

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

### When will the Ajna Protocol launch?

Q2 2023.

### How can I get involved?

At this time, the best way to get involved is to learn about the system and see how you can contribute. Please join our discord server to get more involved.

### Is Ajna custodial?

No Ajna is entirely non-custodial, user’s are in charge of their private keys at all times.

### Has Ajna been audited?

Ajna has been audited by: Trail of Bits, Prototech labs, Quantstamp, Sherlock, and Code4arena.

### Does Ajna have a bug bounty?

Ajna will have a bug bounty once deployed in Q2 2023.

### Does Ajna labs have admin control over the protocol?

No, Ajna Labs has no ability to change or manipulate the smart contracts once they are deployed.

### Where can I get information about Ajna?

The best way to get involved is to learn about the system through the [Whitepaper](https://www.ajna.finance/whitepaper), [FAQs](https://faqs.ajna.finance/getting-started/ajna-101), or [ELI5](https://www.ajna.finance/eli5). Join the [discord server](https://discord.com/invite/PJzKTDXdgA), and [look out](https://twitter.com/ajnafi) for the upcoming launch.

### Where can I test the application?

When released there will be testnet and mainnet versions. Links will be posted on [https://ajna.finance](https://ajna.finance/).

### What are price Oracles?

Oracles provide external data to blockchain applications.

### Why is it a big deal that Ajna’s design excludes price oracles?

Relying on oracles for pricing data in a DeFi application creates an external point of failure as they can be manipulated or compromised. Ajna uses an internal order book empowering lenders to set asset values. This reduces the attack surface of the protocol and makes lending and borrowing more secure.

### What is governance in the context of a protocol?

Governance is when a protocol uses voting or another mechanism such as a centralized entity to implement changes to the protocol without user consent. It is often used to manipulate parameters or add functionality.

### What is the Ajna Foundation?

The Ajna Foundation, formed in mid-2023, is an entity responsible for the stewardship of the Ajna Protocol's brand assets and to pay for designated maintenance and support services.

