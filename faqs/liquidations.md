# Liquidations

[What is a liquidation?](liquidations.md#what-is-a-liquidation)\
[Where can I access a UI for liquidations?](liquidations.md#where-can-i-access-a-ui-for-liquidations)\
[When does a liquidation happen?](liquidations.md#when-does-a-liquidation-happen)\
[What is the liquidation trigger price?](liquidations.md#what-is-the-liquidation-trigger-price)\
[Who triggers liquidations?](liquidations.md#who-triggers-liquidations)\
[What is required to trigger a liquidation?](liquidations.md#what-is-required-to-trigger-a-liquidation)\
[Where can I trigger liquidations?](liquidations.md#where-can-i-trigger-liquidations)\
[What is a liquidation bond?](liquidations.md#what-is-a-liquidation-bond)\
[Why is a liquidation bond needed?](liquidations.md#why-is-a-liquidation-bond-needed)\
[How much does the liquidation bond cost?](liquidations.md#how-much-does-the-liquidation-bond-cost)\
[How is a loan's liquidation price set?](liquidations.md#how-is-a-loans-liquidation-price-set)\
[How do I participate in liquidation auctions?](liquidations.md#how-do-i-participate-in-liquidation-auctions)\
[What if a liquidation auction clears below a loan's Threshold Price?](liquidations.md#what-if-a-liquidation-auction-clears-below-a-loans-threshold-price)\
[In NFT-collection pools, can a borrower use multiple NFTs in a single position?](liquidations.md#in-nft-collection-pools-how-do-group-liquidations-work)\
[In NFT-collection pools, do liquidation auctions happen per single NFT?](liquidations.md#in-nft-collection-pools-do-liquidation-auctions-happen-per-single-nft)\
[In NFT-collection pools, how do group liquidations work?](liquidations.md#in-nft-collection-pools-how-do-group-liquidations-work)\


### What is a liquidation?

Liquidation is a process of selling off assets to pay off debts.\
\
In the context of loans, a liquidation occurs when collateral that was used to secure a loan is sold; proceeds from the sale of the collateral are used to repay the debt. \
\
Liquidation is a last resort for when a borrower is unable to repay a loan. Liquidations often include penalties. It is important for borrowers to understand the potential consequences of defaulting on a loan before they take out the loan.

### Where can I access a UI for liquidations?

1. Go to [https://app.ajna.finance/](https://app.ajna.finance/)
2. Click `Pool Details`\
   ![](../.gitbook/assets/chrome\_2023-08-07\_14-18-35.png)
3. Click `Manage Pool`

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

4.  Navigate and interact withh loans available to be liquidated.\


    <figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

### When does a liquidation happen?

A liquidation happens when the borrower fails to keep their loan in good standing.\
\
To determine whether a loan can be appropriately liquidated there are three important variables used by the system; the loan’s _Threshold Price (TP)_, the loan’s _Neutral Price(NP)_ and the pool’s _Lowest Utilized Price (LUP)_. \
\
TP is set by the borrower and is a loan’s debt divided by the collateral. \
NP is set at origination, is usually some number above the TP, and acts as the liquidation trigger price of the loan.\
LUP moves freely and is defined as the lowest collateral price bucket against which someone is actively borrowing.\
\
If a loan's TP crosses above the pool's LUP, then their position is eligible for liquidation. This is referred to as the _liquidation trigger price_. A loan may be profitable to liquidate, with regard to the [liquidation bond](https://faqs.ajna.finance/faqs/liquidations#what-is-a-liquidation-bond), when the price of the collateral crosses below the NP of a given loan.

### What is the liquidation trigger price?

The liquidation trigger price is the price at which a loan can be triggered for liquidation, though it may not necessarily be profitable to do so. When a loan's _Threshold Price (TP)_ crosses above the pool's Lowest Utilized Price (LUP), their position is eligible for liquidation.

### Who triggers liquidations?

Anyone can trigger a liquidation by posting a [liquidation bond](https://faqs.ajna.finance/faqs/liquidations#what-is-a-liquidation-bond) for the loan in question.

### What is required to trigger a liquidation?

The purchase of a [liquidation bond](https://faqs.ajna.finance/faqs/liquidations#what-is-a-liquidation-bond) is required to trigger liquidations.

### Where can I trigger liquidations?

1. Go to [https://app.ajna.finance/](https://app.ajna.finance/)
2. Click `Pool Details`\
   ![](<../.gitbook/assets/chrome\_2023-08-07\_14-18-35 (1).png>)
3.  Click `Manage Pool`\


    <figure><img src="../.gitbook/assets/chrome_2023-08-07_14-19-04 (1).png" alt=""><figcaption></figcaption></figure>
4.  Navigate and interact with loans available to be liquidated.\


    <figure><img src="../.gitbook/assets/chrome_2023-08-07_14-23-08.png" alt=""><figcaption></figcaption></figure>

### What is a liquidation bond?

A liquidation bond is effectively a bet on the outcome of a collateral sale. In the Ajna protocol, the purchase of a liquidation bond is required to liquidate a loan.

### Why is a liquidation bond needed?

This requirement creates a disincentive to liquidate loans that are sufficiently collateralized with respect to the collateral's market price and creates an incentive to liquidate loans that become under-collateralized with respect to their Neutral Prices.

### How much does the liquidation bond cost?

A bond is priced as a percentage of the debt that is being liquidated. It can range from 1% to 30%.\
\
See section _7.3.2 Sizing the Bond_ in the [whitepaper](https://www.ajna.finance/whitepaper) for full detail.

### When should a liquidation bond be posted?

It is profitable to post a liquidation bond when the sale of collateral is expected to clear below the neutral price of the liquidated loan.\
\
Consider the examples:\
Bob sees Dave's loan is eligible for liquidation. The price of ETH is $1800, while the NP of the loan is $1830. Bob expects the collateral to be sold under $1830, accounting for the time the auction takes, and decides to post the bond and trigger the liquidation of the loan to earn a reward.\
\
Bob sees Dave's loan is eligible for liquidation. The price of ETH is $1850, while the NP of the loan is $1830. Bob expects the collateral to be sold above $1830 and decides not to start the liquidation despite its eligibility.

### How is a loan's liquidation price set?

In Ajna each loan's Neutral Price (NP) acts as the liquidation price. The NP is set at the origination of debt and is the Most Optimistic Matching Price (MOMP) times the ratio of the loan’s Threshold Price (TP) to the LUP, plus one year’s interest, all at the time of origination. In rougher terms, it's set some amount above a loan's Threshold Price, which can be thought of as a loan's collateral price when it hits 1:1 LTV.\
\
Consider these examples:\
\
Safe\
Bob has ETH, and would like to borrow some DAI. The APR to borrow is 1%.  He places 10 ETH into the ETH/DAI pool and withdraws a loan of 5000 DAI. An origination fee is applied and his debt becomes 5002.5 his collateral pledged is 10, and his TP is 5002.5/10 = 500.25. When he created the loan, the pool's MOMP was 1600 while the LUP was 1500. As a result the NP =1600 \* 500.25/1500 +  50.025 = 533.6. \
\
Moderate\
Bob has ETH, and would like to borrow some DAI. The APR to borrow is 1%.  He places 10 ETH into the ETH/DAI pool and withdraws a loan of 10000 DAI. An origination fee is applied and his debt becomes 10005 his collateral pledged is 10, and his TP is 10005/10 = 1000.5. When he created the loan, the pool's MOMP was 1600 while the LUP was 1500. As a result the NP =1600 \* 1000.5/1500 + 100.05 = 1163.2.\
\
Almost at the limit\
Bob has ETH, and would like to borrow some DAI. The APR to borrow is 1%. He places 10 ETH into the ETH/DAI pool and withdraws a loan of 14800 DAI. An origination fee is applied and his debt becomes 14,807.4 his collateral pledged is 10, and his TP is 14,807.4/10 = 1,480.74. When he created the loan, the pool's MOMP was 1600 while the LUP was 1500. As a result the NP =1600 \* 1,480.74/1500 + 148.074 = 1707.344.\
\
INVALID: TP > LUP\
Bob has ETH, and would like to borrow some DAI. The APR to borrow is 1%.  He places 10 ETH into the ETH/DAI pool and withdraws a loan of 15000 DAI. An origination fee is applied and his debt becomes 15007.5 his collateral pledged is 10, and his TP is 15007.5/10 = 1500.75. When he created the loan, the pool's MOMP was 1600 while the LUP was 1500. As a result the NP =1600 \* 1500.75/1500 + 150.075 = 1600.8.

### How do I participate in liquidation auctions?

There are two ways to participate. \
\
The first, as a loan "kicker". This actor posts liquidation bonds and kicks loans into liquidation. \
The second, as an auction bidder. This actor bids on collateral during liquidation auctions.\
\
Beginners could use the Ajna application to access this functionality while advanced actors can develop their own UIs or automations.

### What if a liquidation auction clears below a loan's Threshold Price?

If a liquidation fails to sell collateral at or above the threshold price, then the loan's left over debt gets deducted from the pool's [reserves](https://faqs.ajna.finance/faqs/reserve-auctions#what-are-reserves). If that is insufficient, then the debt is deducted from the quote token liquidity in the highest price buckets, diluting LPB holders in those buckets.

### In NFT-collection pools, can a borrower use multiple NFTs in a single position?

Yes.

### In NFT-collection pools, do liquidation auctions happen per single NFT?

If a borrower’s position is backed by multiple NFTs, they will all go to auction simultaneously. If the position is backed by a single NFT, then only that NFT will go to auction.

### In NFT-collection pools, how do group liquidations work?

In a case where a borrower position backed by multiple NFTs is getting liquidated, Is it all or nothing? Can the NFTs get broken up? Is there a default order if they do? Can bidders specify which NFT they are bidding on?\
\
Similar to regular liquidations, once an auction is initiated the entire lot of collateral is available for purchase. Bidder have the option to place a bid on the entire lot or on a specific NFT during a group liquidation. If a bidder does not specify an NFT for their partial bid, a random one is selected (We haven't documented order in which they are taken.)

For `take`, taker provides an integer number of NFTs in `maxAmount_` argument. `bucketTake` can result in fragmenting NFTs in buckets.\
\


