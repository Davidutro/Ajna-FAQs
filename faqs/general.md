# General

[What is the Ajna Protocol?](general.md#what-is-the-ajna-protocol)\
[What assets can be lent and borrowed?](general.md#what-assets-can-be-lent-and-borrowed-on-ajna)\
[How does Ajna work?](general.md#how-does-ajna-work)\
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
[What is governance in the context of a protocol?](general.md#what-is-governance-in-the-context-of-a-protocol)



### What is the Ajna Protocol?

The Ajna protocol is a noncustodial, peer-to-peer, permissionless lending, borrowing and trading system that requires no governance or external price feeds to function. The current version is built for Ethereum Virtual Machine compatible networks.&#x20;

### What assets can be lent and borrowed on Ajna?

The protocol consists of pools: pairings of quote tokens provided by lenders and collateral tokens provided by borrowers. Ajna is capable of accepting fungible tokens (ERC-20) as quote tokens and fungible (ERC-20) as well as non-fungible (ERC-721) tokens as collateral tokens. There is no governance process or gating mechanism that controls which assets can be used in a pairing.

### How does Ajna work?

Once a pairing of assets has been created, any user can come to the pool to lend or borrow quote token by pledging collateral. Lenders input a price that they’re willing to lend at (and conversely willing to purchase the collateral at) and borrowers are informed as to the best available liquidity for the amount of collateral they have. The smart contracts, using market mechanisms, manage liquidity, interest rates, and liquidations. Loans on Ajna are perpetual in nature and do not expire. More information on these mechanisms will be provided in the whitepaper on it’s release.

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

Ajna has been audited by: Trail of Bits, Prototech labs, Quantstamp, and Sherlock.

### Does Ajna have a bug bounty?

Ajna will have a bug bounty once deployed in Q2 2023.

### Does Ajna labs have admin control over the protocol?

No, Ajna Labs has no ability to change or manipulate the smart contracts once they are deployed.

### Where can I get information about Ajna?

The best way to get involved is to [learn](https://www.ajna.finance/eli5) about the system, [join](https://discord.gg/2YPNkzSH) the discord server, and [look out](https://twitter.com/ajnafi) for the upcoming launch.

### Where can I test the application?

When released there will be testnet and mainnet versions. Links will be posted on [https://ajna.finance](https://ajna.finance/).

### What are price racles?

Oracles provide external data to blockchain applications.

### Why is it a big deal that Ajna’s design excludes price oracles?

Relying on oracles for pricing data in a DeFi application creates an external point of failure as they can be manipulated or compromised. Ajna uses an internal order book empowering lenders to set asset values. This reduces the attack surface of the protocol and makes lending and borrowing more secure.

### What is governance in the context of a protocol?

Governance is when a protocol uses voting or another mechanism such as a centralized entity to implement changes to the protocol without user consent. It is often used to manipulate parameters or add functionality.

