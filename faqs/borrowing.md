# Borrowing

[How do I borrow?](borrowing.md#how-do-i-borrow)\
[Where do I borrow?](borrowing.md#where-do-i-borrow)\
[What can I borrow?](borrowing.md#what-can-i-borrow)\
[Can I borrow NFTs?](borrowing.md#can-i-borrow-nfts)\
[What are the fees?](borrowing.md#what-are-the-fees)\
[Is there a minimum or maximum I can borrow?](borrowing.md#is-there-a-minimum-or-maximum-i-can-borrow)\
[How much would I pay in interest?](borrowing.md#how-much-would-i-pay-in-interest)\
[How are interest rates determined?](borrowing.md#how-are-interest-rates-determined)\
[Can I borrow at a fixed rate?](borrowing.md#can-i-borrow-at-a-fixed-rate)\
[When do I need to pay back the loan?](borrowing.md#when-do-i-need-to-pay-back-the-loan)\
[Can I repay my loan early, and if so, are there any penalties?](borrowing.md#can-i-repay-my-loan-early-and-if-so-are-there-any-penalties)\
[What can go wrong?](borrowing.md#what-can-go-wrong)\
[What happens if the collateral value drops below the debt amount?](borrowing.md#what-happens-if-the-collateral-value-drops-below-the-debt-amount)\
[What happens if my loan gets liquidated?](borrowing.md#what-happens-if-my-loan-gets-liquidated)\
[What is the penalty for getting liquidated?](borrowing.md#what-is-the-penalty-for-getting-liquidated)\
[How do I know my loan's liquidation price?](borrowing.md#how-do-i-know-my-loans-liquidation-price)\
[How is the liquidation price set?](borrowing.md#how-is-the-liquidation-price-set)\
[How does Ajna determine if my loan is insufficiently collateralized?](borrowing.md#how-does-ajna-determine-if-my-loan-is-insufficiently-collateralized)\


### How do I borrow?

Borrowers deposit collateral tokens into a pool and may borrow quote tokens. A liquidation price will be set depending on how much is borrowed relative to the value of the collateral.

### Where do I borrow?

Users can borrow on Ajna by using any applications that plug into the protocol.\
\
Existing applications include Ajna's own app and Oasis.&#x20;

### What can I borrow?

Users can borrow any ERC-20 token.

### Can I borrow NFTs?

No.

### What are the fees?

1. Origination Fee\
   This fee is charged to all debt and is the greater of one week of interest or 0.05%.
2. Variable Interest Rate \
   This is the APR being paid on the borrower’s debt, which is subject to change every 12 hours.
3. Liquidation Penalty 1\
   This fee is applied when a loan is triggered for liquidation and is equivalent to 90 days of interest.
4. Liquidation Penalty 2\
   This fee is applied once the first sale of collateral occurs and is 7%.
5. Transaction Fees\
   These are fees that are charged on blockchain transactions generally, the more complex the transaction, the larger the fee.

### Is there a minimum or maximum I can borrow?

Yes. The minimum borrow size is 10% of the pool’s average loan’s debt. The maximum borrow size depends the pool's available liquidity.

### How much would I pay in interest?

Each pool has its own interest rate that should be displayed in the pool information. The interest rate is subject to change every 12 hours.

### How are interest rates determined?

Interest rates are determined by pool utilization. If there is a surplus of lender liquidity, rates are lowered, and if there is a shortage of lender liquidity, rates are increased. Rates can change once every 12 hours, at 10% increments of the existing rate in either direction.\
\
For a specific overview of the interest rate algorithm, see section 8 of the whitepaper.

### Can I borrow at a fixed rate?

Yes, but only for a maximum of 12 hours. Rates are subject to change every 12 hours.

### When do I need to pay back the loan?

Ajna loans can be paid back at any time.

### Can I repay my loan early, and if so, are there any penalties?

Loans can be repaid at any time, there is no early repayment penalty.

### What can go wrong?

* The protocol gets hacked or exploited.
* Your loan gets liquidated.
* Your loan gets liquidated unfairly, leaving you with no debt and some leftover claimable collateral.
* xxx??

### What happens if the collateral value drops below the debt amount?

If the value of the collateral, as measured by the external market price, drops below the loan's Threshold Price (debt/collateral), then before that point the system would have liquidated the loan. Once the market price crosses below a loan's Neutral Price it becomes profitable to liquidate the position. The Neutral Price is always set above the Threshold Price of a given loan.

### What happens if my loan gets liquidated?

When a loan is liquidated the first liquidation penalty of 90 days of interest is applied to the debt and a one hour grace period begins when the borrower can save their loan by paying back debt or adding collateral. If the borrower doesn't save the loan then it will proceed to an auction where the second liquidation penalty of 7% is applied once the first sale of collateral occurs. When the liquidation is complete the borrower is no longer responsible for paying back their debt balance since the system sold their collateral and to cover the balance. In some cases there may be collateral left over that the user can claim.

### What is the penalty for getting liquidated?

1. Liquidation Penalty 1\
   This fee is applied when a loan is triggered for liquidation and is equivalent to 90 days of interest.
2. Liquidation Penalty 2\
   This fee is applied once the first sale of collateral occurs and is 7%.

### How do I know my loan's liquidation price?

The liquidation price is something that should be displayed by the interface you use to manage the loan. A borrower has full control of their liquidation price. A liquidation price is set when a loan is created and can move with changes in debt or collateral amounts. Under normal circumstance the liquidation price moves slightly over time as interest accrues to a borrower's debt.

### How is the liquidation price set?

In Ajna the Neutral Price (NP) acts as the liquidation price. The NP is the current Most Optimistic Matching Price (MOMP) times the ratio of the loan’s Threshold Price (TP) to the LUP, plus one year’s interest. \
\
Consider these examples:\
Bob has ETH, and would like to borrow some DAI. The APR to borrow is 1%.  He places 10 ETH into the ETH/DAI pool and withdraws a loan of 5000 DAI. An origination fee is applied and his debt becomes 5002.5 his collateral pledged is 10, and his TP is 5002.5/10 = 500.25. When he created the loan, the pool's MOMP was 1600 while the LUP was 1500. As a result the NP =1600 \* 500.25/1500 +  50.025 = 533.6. **(Safe)**

Bob has ETH, and would like to borrow some DAI. The APR to borrow is 1%.  He places 10 ETH into the ETH/DAI pool and withdraws a loan of 10000 DAI. An origination fee is applied and his debt becomes 10005 his collateral pledged is 10, and his TP is 10005/10 = 1000.5. When he created the loan, the pool's MOMP was 1600 while the LUP was 1500. As a result the NP =1600 \* 1000.5/1500 + 100.05 = 1163.2. **(Moderate)**\
\
Bob has ETH, and would like to borrow some DAI. The APR to borrow is 1%. He places 10 ETH into the ETH/DAI pool and withdraws a loan of 14800 DAI. An origination fee is applied and his debt becomes 14,807.4 his collateral pledged is 10, and his TP is 14,807.4/10 = 1,480.74. When he created the loan, the pool's MOMP was 1600 while the LUP was 1500. As a result the NP =1600 \* 1,480.74/1500 + 148.074 = 1707.344. **(almost at the limit)**\
\
Bob has ETH, and would like to borrow some DAI. The APR to borrow is 1%.  He places 10 ETH into the ETH/DAI pool and withdraws a loan of 15000 DAI. An origination fee is applied and his debt becomes 15007.5 his collateral pledged is 10, and his TP is 15007.5/10 = 1500.75. When he created the loan, the pool's MOMP was 1600 while the LUP was 1500. As a result the NP =1600 \* 1500.75/1500 + 150.075 = 1600.8. **(INVALID: TP > LUP)**\


### How does Ajna determine if my loan is insufficiently collateralized?

To determine whether a loan is insufficiently collateralized there are three important variables being used; the loan’s Threshold Price (TP), the loan’s Neutral Price(NP) and the pool’s Lowest Utilized Price (LUP). TP is set by the borrower and is a loan’s debt divided by the collateral. A pool’s LUP is defined as the lowest collateral price bucket against which someone is actively borrowing. If the borrower’s TP crosses above the LUP, then their position is eligible for liquidation. The NP of a loan is set at origination and acts as the liquidation price of the loan. Meaning that a loan must be both eligible and out of position with respect to the NP for it to be profitably liquidated. A loan is liquidatable when the market price of the collateral crosses below the NP.
