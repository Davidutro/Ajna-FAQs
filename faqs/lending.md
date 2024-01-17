# 💸 Lending

[How do I lend?](lending.md#how-do-i-lend)\
[Where do I lend?](lending.md#where-do-i-lend)\
[What can I lend?](lending.md#what-can-i-lend)\
[What can I lend against?](lending.md#what-can-i-lend-against)\
[What are the fees?](lending.md#what-are-the-fees)\
[How do I decide on what price bucket to deposit into?](lending.md#how-do-i-decide-what-price-bucket-to-deposit-into)\
[How do I calculate the price buckets for short pools?](lending.md#how-do-i-calculate-the-price-buckets-for-short-pools)\
[What do I need to do after depositing quote tokens?](lending.md#what-do-i-need-to-do-after-depositing-quote-tokens)\
[Can I update my lending price if my assets are being utilized?](lending.md#can-i-update-my-lending-price-if-my-assets-are-being-utilized)\
[What can go wrong?](lending.md#what-can-go-wrong)\
[In what scenario(s) can a lender lose their deposit?](lending.md#in-what-scenario-s-can-a-lender-lose-their-deposit)\
[In what scenario(s) are lender deposits frozen?](lending.md#in-what-scenario-s-are-lender-deposits-frozen)\
[How does a lender get paid if a borrower defaults on their loan?](lending.md#how-does-a-lender-get-paid-if-a-borrower-defaults-on-their-loan)\
[Are there any notifications?](lending.md#are-there-any-notifications)\
[How much do I earn?](lending.md#how-much-do-i-earn)\
[When is my deposit eligible to earn interest?](lending.md#when-is-my-deposit-eligible-to-earn-interest)

### How do I lend?

Users can lend on Ajna through any applications that plug into the protocol.

Users choose what valuation they are willing to lend against by depositing tokens into specific price buckets.

### Where do I lend?

* Easy
  * [The Summer.Fi app](https://summer.fi/ajna)
  * [The BuiltbyMom app](https://www.ajnafi.com)
  * Other apps (soon)
* Advanced
  * Use [the SDK](https://www.npmjs.com/package/@ajna-finance/sdk) to build an interface or bots

### What can I lend?

Users can lend any ERC-20 token. \
Users cannot lend ERC-721 NFTs or NFT Collections, or any other NFT types.

The following types of tokens are incompatible with Ajna, and no countermeasures exist to explicitly prevent creating a pool with such tokens, actors should use them at their own risk:

* NFT and fungible tokens which charge a fee on transfer.
* Fungible tokens whose balance rebases.

The following types of tokens are incompatible with Ajna, and countermeasures exist to explicitly prevent creating a pool with such tokens:

* Fungible tokens with more than 18 decimals or 0 decimals, whose `decimals()` function does not return a constant value, or which do not implement the optional [decimals()](https://eips.ethereum.org/EIPS/eip-20#decimals) function.

### What can I lend against?

Users can lend their ERC-20 tokens against any ERC-20, ERC-721, or 721-subsets.\


The following types of tokens are incompatible with Ajna, and no countermeasures exist to explicitly prevent creating a pool with such tokens, actors should use them at their own risk:

* NFT and fungible tokens which charge a fee on transfer.
* Fungible tokens whose balance rebases.

The following types of tokens are incompatible with Ajna, and countermeasures exist to explicitly prevent creating a pool with such tokens:

* Fungible tokens with more than 18 decimals or 0 decimals, whose `decimals()` function does not return a constant value, or which do not implement the optional [decimals()](https://eips.ethereum.org/EIPS/eip-20#decimals) function.

### What are the fees?

1. Deposit Fee\
   All deposits incur a small fee equivalent to 8 hours of interest. The fee accrues on any new deposit, and any action which moves quote token down in price. The fee is not applied to actions which move quote token up in price.
2. Transaction Fees\
   These are fees that are charged on blockchain transactions generally, the more complex the transaction, the larger the fee.

### How do I decide what price bucket to deposit into?

Deciding on a price depends on the lender's risk tolerance. Both depositing too high and too low have risks.\
\
Depositing too high:

* Creates a need to more closely micromanage the position. Meaning the lender will need to move their deposit lower as the market price approaches their deposit's price bucket.
* Risks getting traded against at an unfavorable price if the market price crosses below the deposit's price bucket. Deposits are always swappable for collateral at the price of their buckets.
* Risks deposit being temporarily frozen, since the highest valued deposits are frozen first during a liquidation. The lender may have their deposit swapped for collateral when this occurs.

Depositing too low:

* May result in the deposit not earning interest if it is below the Pool's Highest Threshold Price (HTP).\
  \


<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption><p>Thank you Summer.fi team for this image!</p></figcaption></figure>

To learn more check out [Summer.fi's dive into this question.](https://docs.summer.fi/protocols/ajna/tutorials-and-guides/how-to-pick-the-right-level-for-lending)

### How do I calculate the price buckets for short pools?

The price buckets should be somewhere below _1 / market-price_. An example would be the USDC/AAVE pool where USDC is collateral in AAVE is the quote token.&#x20;

### What do I need to do after depositing quote tokens?

Occasionally users may want to move their deposits to different price buckets. Monitoring the market price of the collateral token is key to making such decisions.&#x20;

As the collateral price drops, users may want to consider moving their deposit down.&#x20;

As collateral price increases, users may want to consider moving their deposit up.

### Can I update my lending price if my assets are being utilized?

Yes, unless the assets are frozen due to an active liquidation or if moving them results in the LUP moving below the HTP.

### What can go wrong?

* The protocol gets hacked or exploited.
* Your quote tokens are traded against for collateral at an unfavorable price.
* If no one posts a bond and the position sits undercollateralized...
  * As a result of interest, bad debt accrues.
* If no one bids on a liquidation and the collateral is sold for close to 0, bad debt can result.
  * To cover the bad debt, reserves are depleted first and then the lenders from the highest price buckets down.

### In what scenario(s) can a lender lose their deposit?

There are three scenarios when a lender can lose their deposit:&#x20;

1. If the protocol gets hacked or exploited.
2. If a lender allows the market price to cross below their deposit's price bucket someone can trade collateral for their deposit, leaving the lender with collateral instead of quote tokens.
3. If there is bad debt and reserves are insufficient, lenders risk losing part or all of their deposits.

### In what scenario(s) are lender deposits frozen?

1. A lender cannot withdraw deposit if doing so would move the LUP below the HTP, as this would result in liquidation eligibility for one or more loans.
   * A borrower's position can be liquidated if the pool's LUP is below their TP.
   * If a lender wishes to remove deposit from a bucket that will cause the LUP to move below the HTP, they will need to liquidate the loan(s) that sit between the two points.
2. if there are active liquidations in the pool, deposits that are within _liquidation\_debt (amount)_ of the top of the book cannot withdraw until the liquidations are complete.

### How does a lender get paid if a borrower defaults on their loan?

If a borrower defaults, their loan will go through the liquidation process where the collateral is sold to cover the debt. The sale occurs through a Dutch Auction and can utilize lender deposits at the top valued price buckets.\
\
Lender deposits at the highest priced buckets are at risk to be traded against, leaving depositors with the options of claiming the collateral and selling it to retrieve their deposit, or to wait for someone to trade quote tokens for the collateral at that price.

### Are there any notifications?

Notifications are not a native feature of the Ajna Protocol. Please check with the application you are using or other 3rd parties for notification services.

### How much do I earn?

How much a lender earns depends on the pool and the [eligibility of the deposit.](https://faqs.ajna.finance/faqs/lending#when-is-my-deposit-eligible-to-earn-interest) \
To look at pools and their lender rates, check out [https://info.ajna.finance/](https://info.ajna.finance/)\
\
Rates are subject to change every 12 hours, in x1.1 or x0.9 increments.

A portion of the interest goes to the pool's reserves and is used to provide a liquidity cushion to lenders, and absorb bad debt if some should occur. This [Net Interest Margin](https://faqs.ajna.finance/faqs/reserve-auctions#what-is-net-interest-margin) (NIM) is approximately  10% of the interest rate revenue. &#x20;

### When is my deposit eligible to earn interest?

All deposits above a pool's HTP earn interest at the same rate. In the event that the HTP is above the LUP, usually during active liquidations, all deposits above LUP earn interest at the same rate.\
\
For more details see section 8 of [the whitepaper](https://www.ajna.finance/whitepaper).

