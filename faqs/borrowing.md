# Borrowing

How do I borrow?\
Where do I borrow?\
What can I borrow?\
Can I borrow NFTs?\
What are the fees?\
Is there a minimum or maximum I can borrow?\
How much would I pay in interest?\
How are interest rates determined?\
Can I borrow at a fixed rate?\
When do I need to pay back the loan?\
Can I repay my loan early, and if so, are there any penalties?\
What can go wrong?\
What happens if the collateral value drops below the debt amount?\
What happens if I get liquidated?\
What is the penalty for getting liquidated?\
How do I know my loan's liquidation price?\
How is the liquidation price set?\
How does Ajna determine if my loan is insufficiently collateralized?\


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

Yes. The minimum borrow size is 10% of the pool’s average loan’s debt. The maximum borrow size depends the pool's available quote token liquidity.

### How much would I pay in interest?

Each pool has its own interest rate that should be displayed in the pool information. The interest rate is subject to change every 12 hours.

### How are interest rates determined?

Interest rates are determined by pool utilization. If there is a surplus of lender liquidity, rates are lowered, and if there is a shortage of lender liquidity, rates are increased. Rates can change once every 12 hours, at 10% of the existing rate in either direction.\
\
For a more specific definition of the interest rate algorithm, see section 8 of the whitepaper.

### Can I borrow at a fixed rate?

Yes, but only at a maximum of 12 hours. Rates are subject to change every 12 hours.

### When do I need to pay back the loan?

Ajna loans have no terms for repayment.

### Can I repay my loan early, and if so, are there any penalties?

Loans can be repaid at any time, there is no early repayment penalty.

### What can go wrong?

xxx

### What happens if the collateral value drops below the debt amount?

If this happens, then it may be profitable for someone to liquidate the loan. A liquidation may be triggered, causing a penalty of 90 days of interest to be added to the borrower's debt. The triggered liquidation will start to sell the loan's collateral unless the borrower saves their position within the 1 hour grace period.

### What happens if I get liquidated?

### &#x20;What is the penalty for getting liquidated?

1. Liquidation Penalty 1\
   This fee is applied when a loan is triggered for liquidation and is equivalent to 90 days of interest.
2. Liquidation Penalty 2\
   This fee is applied once the first sale of collateral occurs and is 7%.

### How do I know my loan's liquidation price?

The liquidation price is something that should be displayed by the interface you use to manage the loan. A borrower has full control of their liquidation price. A liquidation price is set when a loan is created and can move with changes in debt or collateral amounts. Under normal circumstance the liquidation price moves slightly over time as interest accrues to a borrower's debt.

### How is the liquidation price set?

xxx

### How does Ajna determine if my loan is insufficiently collateralized?

To determine whether a loan is insufficiently collateralized there are three important variables being used; the loan’s Threshold Price (TP), the loan’s Neutral Price(NP) and the pool’s Lowest Utilized Price (LUP). TP is set by the borrower and is a loan’s debt divided by the collateral. A pool’s LUP is defined as the lowest collateral price bucket against which someone is actively borrowing. If the borrower’s TP crosses above the LUP, then their position is eligible for liquidation. The NP of a loan is set at origination and acts as the liquidation price of the loan. Meaning that a loan must be both eligible and out of position with respect to the NP for it to be profitably liquidated. A loan is liquidatable when the market price of the collateral crosses below the NP.
