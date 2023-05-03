# Lending

[How do I lend?](lending.md#how-do-i-lend)\
[Where do I lend?](lending.md#where-do-i-lend)\
[What can I lend?](lending.md#what-can-i-lend)\
[What are the fees?](lending.md#what-are-the-fees)\
[How do I decide on what price bucket to deposit into?](lending.md#how-do-i-decide-what-price-bucket-to-deposit-into)\
[What do I need to do after depositing quote tokens?](lending.md#what-do-i-need-to-do-after-depositing-quote-tokens)\
[What can go wrong?](lending.md#what-can-go-wrong)\
[In what scenario(s) can a lender lose their deposit?](lending.md#in-what-scenario-s-can-a-lender-lose-their-deposit)\
[Are there any notifications?](lending.md#are-there-any-notifications)\
[How much do I earn?](lending.md#how-much-do-i-earn)

## How do I lend?

Users can lend on Ajna through any applications that plug into the protocol.

Users choose what valuation they are willing to lend against by depositing tokens into specific price buckets.

## Where do I lend?

* Easy
  * The Ajna app (soon)
  * The Oasis app (soon)
  * Other apps with Ajna integrated (soon)
* Advanced
  * Use the SDK to build an interface or bots (soon)
  * Ether.js or Web3.py (interacts with Ethereum) & connect to your own node (soon)

## What can I lend?

Users can lend any ERC-20 token. \
Users cannot lend ERC-721 NFTs or NFT Collections, or any other NFT types.

## What are the fees?

1. Unutilized Deposit Fee\
   Deposit below the LUP incur a small fee equivalent to 24 hours of interest.
2. Transaction Fees\
   These are fees that are charged on blockchain transactions generally, the more complex the transaction, the larger the fee.

## How do I decide what price bucket to deposit into?

Deciding on a price depends on the lender's risk tolerance. Both depositing too high and too low have risks.\
\
Depositing too high:

* Creates a need to more closely micromanage the position. Meaning the lender will need to move their deposit lower as the market price approaches their deposit's price bucket.
* Risks getting traded against at an unfavorable price if the market price crosses below the deposit's price bucket. Deposits are always swappable for collateral at the price of their buckets.
* Risks deposit being temporarily frozen, since the highest valued deposits are frozen first during a liquidation. The lender may have their deposit swapped for collateral when this occurs.

Depositing too low:

* May result in the deposit not earning interest if it is below the Pool's Highest Threshold Price (HTP).
* Additionally, if a deposit is made below the Lowest Utilized Price (LUP), then an unutilized deposit fee is charged equivalent to 24 hours of interest.

## What do I need to do after depositing quote tokens?

Occasionally users may want to move their deposits to different price buckets. Monitoring the market price of the collateral token is key to making such decisions.&#x20;

As the collateral price drops, users may want to consider moving their deposit down.&#x20;

As collateral price increases, users may want to consider moving their deposit up.

## What can go wrong?

* The protocol gets hacked or exploited.
* Your quote tokens are traded against for collateral at an unfavorable price.
* If no one posts a bond and the position sits undercollateralized,...
  * As a result of interest, bad debt accrues.
* If no one bids on a liquidation and the collateral is sold for close to 0, bad debt can result.
  * To cover the bad debt, reserves are depleted first and then the lenders from the highest price buckets down.

## In what scenario(s) can a lender lose their deposit?

There are three scenarios when a lender can lose their deposit:&#x20;

1. If the protocol gets hacked or exploited.
2. If a lender allows the market price to cross below their deposit's price bucket someone can trade collateral for their deposit, leaving the lender with collateral instead of quote tokens.
3. If there is bad debt and reserves are insufficient, the lender risks losing part of their deposit.

## Are there any notifications?

Notifications are not a native feature of the Ajna Protocol. Please check with the application you are using or other 3rd parties for notification services.

## How much do I earn?

How much a lender earns depends on the pool and the eligibility of the deposit. All deposits above a pool's HTP earn interest at the same rate. Where the rate is displayed varies depending on what interface you are using. Rates are subject to change every 12 hours.

A portion of the interest goes to the pool's reserves and is used to provide a liquidity cushion to lenders, and absorb bad debt if some should occur. This Net Interest Margin (NIM) is approximately&#x20;

