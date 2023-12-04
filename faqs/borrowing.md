# 💰 Borrowing

[How do I borrow?](borrowing.md#how-do-i-borrow)\
[Where do I borrow?](borrowing.md#where-do-i-borrow)\
[What can I borrow?](borrowing.md#what-can-i-borrow)\
[What can I borrow against?](borrowing.md#what-can-i-borrow-against)\
[Can I borrow NFTs?](borrowing.md#can-i-borrow-nfts)\
[What are the fees?](borrowing.md#what-are-the-fees)\
[Is there a minimum or maximum I can borrow?](borrowing.md#is-there-a-minimum-or-maximum-i-can-borrow)\
[How much would I pay in interest?](borrowing.md#how-much-would-i-pay-in-interest)\
[How are interest rates determined?](borrowing.md#how-are-interest-rates-determined)\
[Is there a minimum and maximum interest rate?](borrowing.md#is-there-a-minimum-and-maximum-interest-rate)\
[How long does it take the interest rate to halve or double?](borrowing.md#how-long-does-it-take-the-interest-rate-to-halve-or-double)\
[Can I borrow at a fixed rate?](borrowing.md#can-i-borrow-at-a-fixed-rate)\
[When do I need to pay back the loan?](borrowing.md#when-do-i-need-to-pay-back-the-loan)\
[Why am I being blocked from paying back a partial amount of my loan?](borrowing.md#why-am-i-being-blocked-from-paying-back-a-partial-amount-of-my-loan)\
[Can I repay my loan early, and if so, are there any penalties?](borrowing.md#can-i-repay-my-loan-early-and-if-so-are-there-any-penalties)\
[What can go wrong?](borrowing.md#what-can-go-wrong)\
[What happens if the collateral value drops below the debt amount?](borrowing.md#what-happens-if-the-collateral-value-drops-below-the-debt-amount)\
[What happens if my loan gets liquidated?](borrowing.md#what-happens-if-my-loan-gets-liquidated)\
[What is the penalty for getting liquidated?](borrowing.md#what-is-the-penalty-for-getting-liquidated)\
[How do I know my loan's liquidation price?](borrowing.md#how-do-i-know-my-loans-liquidation-price)\
[How is the liquidation price set?](borrowing.md#how-is-the-liquidation-price-set)\
[How does Ajna determine if my loan is insufficiently collateralized?](borrowing.md#how-does-ajna-determine-if-my-loan-is-insufficiently-collateralized)

### How do I borrow?

Borrowers deposit collateral tokens into pools and may borrow quote tokens. A liquidation price will be set depending on how much is borrowed relative to the value of the collateral.

### Where do I borrow?

* Easy
  * The Summer.Fi app (soon)
  * Static Open Source Frontend (soon)
  * Other apps with Ajna integrated (soon)
* Advanced
  * Use the SDK to build an interface or bots (soon)
  * Ether.js or Web3.py (interacts with Ethereum) & connect to your own node (soon)

### What can I borrow?

Users can borrow any ERC-20 token.

### What can I borrow against?

Users can use any ERC-20 token, ERC-721 NFTs, or 721-subset as collateral. If a pool doesn't exist for a token, one can be created. The only other limitation is finding someone to lend Quote Tokens.

The following types of tokens are incompatible with Ajna, and no countermeasures exist to explicitly prevent creating a pool with such tokens, actors should use them at their own risk:

* NFT and fungible tokens which charge a fee on transfer.
* Fungible tokens whose balance rebases.

The following types of tokens are incompatible with Ajna, and countermeasures exist to explicitly prevent creating a pool with such tokens:

* Fungible tokens with more than 18 decimals or 0 decimals, whose `decimals()` function does not return a constant value, or which do not implement the optional [decimals()](https://eips.ethereum.org/EIPS/eip-20#decimals) function.

### Can I borrow NFTs?

No.

### What are the fees?

1. Origination Fee\
   This fee is charged to all debt and is the greater of one week of interest or 0.05%.
2. Variable Interest Rate \
   This is the APR being paid on the borrower’s debt, which is subject to change every 12 hours.
3. Liquidation Take Penalty (Also known as the Borrower Take Penalty)\
   This fee is maximum 4.5%, and is applied once the first sale of collateral occurs and is variable depending on the collateral price settled at the auction as well as the liquidator's Bond Factor.
4. Transaction Fees\
   These are fees that are charged on blockchain transactions generally, the more complex the transaction, the larger the fee.\
   \
   For specifics, see the [whitepaper](https://www.ajna.finance/whitepaper).

### Is there a minimum or maximum I can borrow?

Yes. The minimum borrow size is 10% of the pool’s average loan’s debt. A minimum is set only after 10 borrow positions are created in a given pool.\
\
The maximum borrow size depends the pool's available lender liquidity.

### How much would I pay in interest?

Each pool has its own interest rate that should be displayed in the pool information. The interest rate is subject to change every 12 hours.

### How are interest rates determined?

Interest rates are determined by pool utilization. If there is a surplus of lender liquidity, rates are lowered, and if there is a shortage of lender liquidity, rates are increased. Rates can change once every 12 hours and occur in +- 10% increments. If the rate is rising, the previous rate is multiplied by 1.1; if the rate is decreasing, the previous rate is multiplied by 0.9\
\
For a specific overview of the interest rate algorithm, see section 8 of the [whitepaper](https://www.ajna.finance/whitepaper).

### Is there a minimum and maximum interest rate?

Yes, so cannot go below 0.001% or above 400%.

### How long does it take the interest rate to halve or double?

\~3.5 days assuming consistent interest rate updates every 12 hours.

### Can I borrow at a fixed rate?

Yes, but the rate is only fixed for 12 hours at a time. Rates may change once every 12 hours if conditions are met.

### When do I need to pay back the loan?

Ajna loans can be paid back at any time.

### Why am I being blocked from paying back a partial amount of my loan?

Ajna has a minimum borrow amount for loans, this means users might be unable to pay back a partial amount of their debt if it would push their balance below this minimum. \
\
If this happens, pay back less or pay back the entire amount.

### Can I repay my loan early, and if so, are there any penalties?

Loans can be repaid at any time, there is no early repayment penalty.

### What can go wrong?

* The protocol gets hacked or exploited.
* Your loan gets liquidated.
* Your loan gets liquidated unfairly, leaving you with no debt and some leftover claimable collateral. If this happens the liquidator loses money on the bond they had to post in order to send your loan to liquidation.

### What happens if the collateral value drops below the debt amount?

If the value of the collateral, as measured by the external market price, drops below the loan's Threshold Price (debt/collateral), then before that point the system would have liquidated the loan. Once the market price crosses below a loan's Neutral Price it becomes profitable to liquidate the position. The Neutral Price is always set above the Threshold Price of a given loan.

### What happens if my loan gets liquidated?

When a loan is liquidated it will proceed to an auction where a liquidation penalty is applied to each sale of collateral. When the liquidation is complete the borrower is no longer responsible for paying back their debt balance since the system sold their collateral and to cover the balance. In some cases there may be collateral left over that the user can claim.

### What is the penalty for getting liquidated?

The Borrower Take Penalty is applied to debt when collateral is taken during a liquidation auction.

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

### How do I know my loan's liquidation price?

The liquidation price is something that should be displayed by the interface you use to manage the loan. A borrower has full control of their liquidation price. A liquidation price is set when a loan is created and can move with changes in debt or collateral amounts. Under normal circumstance the liquidation price moves slightly over time as interest accrues to a borrower's debt.

### How is the liquidation price set?

In Ajna the Neutral Price (NP) acts as the liquidation price.

When a loan is initiated or modified (the first debt, additional debt drawn, or collateral is removed from the loan), the neutral price is set to

&#x20;                                                        <img src="../.gitbook/assets/image (10).png" alt="" data-size="original">\
\
where r is the current borrower rate of the pool..

### How does Ajna determine if my loan is insufficiently collateralized?

To determine whether a loan is insufficiently collateralized there are three important variables being used; the loan’s Threshold Price (TP), the loan’s Neutral Price(NP) and the pool’s Lowest Utilized Price (LUP). TP is set by the borrower and is a loan’s debt divided by the collateral. A pool’s LUP is defined as the lowest collateral price bucket against which someone is actively borrowing. If the borrower’s TP crosses above the LUP, then their position is eligible for liquidation. The NP of a loan is set at origination and acts as the liquidation price of the loan. Meaning that a loan must be both eligible and out of position with respect to the NP for it to be profitably liquidated. A loan is liquidatable when the market price of the collateral crosses below the NP.
