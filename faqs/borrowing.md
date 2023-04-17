# Borrowing

How do I borrow?\
Where do I borrow?\
What can I borrow?\
Can I borrow NFTs?\
What are the fees?\
How much can I borrow? Is there a minimum or maximum?\
How much would I pay in interest?\
How are interest rates determined?\
Can I borrow at a fixed rate?\
When do I need to pay back the loan?\
Can I repay my loan early, and if so, are there any penalties?\
How do I payback the loan?\
What happens if the value of my collateral drops below the amount of my loan?\
What can go wrong? \*\*think about whether to remove\
How do I know my loan is safe/is there a liquidation price?\
What happens if I get liquidated?\
What is the penalty for getting liquidated?\


### How do I borrow?

Borrowers deposit collateral tokens into a pool and are given a maximum amount of quote tokens that they can borrow and a liquidation price depending on their decision.

### Where do I borrow?

Users can borrow on Ajna through any applications that plug into the protocol.\
\
Existing applications include Ajna's native app and Oasis.&#x20;

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

### How much can I borrow? Is there a minimum or maximum?

ccc

### How much would I pay in interest?

xxx

### How are interest rates determined?

ccc

### Can I borrow at a fixed rate?

xxx

When do I need to pay back the loan?

xxx

Can I repay my loan early, and if so, are there any penalties?

xxx\


How do I payback the loan?

\
What happens if the value of my collateral drops below the amount of my loan?

\
What can go wrong? \*\*think about whether to remove

\
How do I know my loan is safe/is there a liquidation price?

\
What happens if I get liquidated?

\
What is the penalty for getting liquidated?





### How does the system determine if my loan is insufficiently collateralized?

To determine whether a loan is insufficiently collateralized there are three important variables being used; the loan’s Threshold Price (TP), the loan’s Neutral Price(NP) and the pool’s Lowest Utilized Price (LUP). TP is set by the borrower and is a loan’s debt divided by the collateral. A pool’s LUP is defined as the lowest collateral price bucket against which someone is actively borrowing. If the borrower’s TP crosses above the LUP, then their position is eligible for liquidation. The NP of a loan is set at origination and acts as the liquidation price of the loan. Meaning that a loan must be both eligible and out of position with respect to the NP for it to be profitably liquidated. A loan is liquidatable when the market price of the collateral crosses below the NP.
