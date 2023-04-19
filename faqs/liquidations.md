# Liquidations

What is a liquidation?\
When does a liquidation occur?\
Who triggers liquidations?\
What is required to trigger a liquidation?\
What is a liquidation bond?\
When is it profitable to post a liquidation bond?\
How is a loan's liquidation price set?\
How do I participate in liquidation auctions?\
What if a liquidation auction clears below a loan's Threshold Price?\


### What is a liquidation?

A liquidation is a process of selling off assets to pay off debts. In the context of loans, a liquidation occurs when collateral that was used to secure a loan is sold. The proceeds from the sale of the collateral are used to repay the outstanding balance of the loan. Liquidations are a last resort for when a borrower is unable to repay a loan. The process of liquidating collateral can be complex, and it is important for borrowers to understand the potential consequences of defaulting on a loan before they take out the loan.

### When does a liquidation happen?

To determine whether a loan can be appropriately liquidated there are three important variables used by the system; the loan’s Threshold Price (TP), the loan’s Neutral Price(NP) and the pool’s Lowest Utilized Price (LUP). TP is set by the borrower and is a loan’s debt divided by the collateral. A pool’s LUP is defined as the lowest collateral price bucket against which someone is actively borrowing. If the borrower’s TP crosses above the LUP, then their position is eligible for liquidation. The NP of a loan is set at origination and acts as the liquidation price of the loan. It is usually some number above the TP. A loan is profitable to liquidate when the market price of the collateral crosses below the loan's NP.

### Who triggers liquidations?

Anyone can trigger a liquidation by posting a liquidation bond for the loan in question.

### What is required to trigger a liquidation?

The purchase of a liquidation bond is required to trigger liquidations.

### What is a liquidation bond?

A liquidation bond is effectively a bet on the outcome of a pay-as-bid dutch auction for the collateral.

### Why is a liquidation bond needed?

This requirement creates a disincentive to liquidate loans that are well collateralized with respect to the collateral's market price and creates an incentive to liquidate loans that become under-collateralized with respect to their Neutral Prices.

### When should a liquidation bond be posted?

It is profitable to post a liquidation bond when the sale of collateral is expected to clear below the neutral price of the liquidated loan.\
\
Consider the examples:\
Bob sees Dave's loan is eligible for liquidation. The price of ETH is $1800, while the NP of the loan is $1830. Bob expects the collateral to be sold under $1830 and decides to put up the bond and initiate the liquidation of the loan to earn a reward.\
\
Bob sees Dave's loan is eligible for liquidation. The price of ETH is $1850, while the NP of the loan is $1830. Bob expects the collateral to be sold above $1830 and decides not to start the liquidation despite its eligibility.

### How is a loan's liquidation price set?

In Ajna each loan's Neutral Price (NP) acts as the liquidation price. The NP is set at the origination of debt and is the current Most Optimistic Matching Price (MOMP) times the ratio of the loan’s Threshold Price (TP) to the LUP, plus one year’s interest. In simpler terms, it's set some amount above a loan's Threshold Price (1:1 LTV collateral price.)\
\
Consider these examples:\
Bob has ETH, and would like to borrow some DAI. The APR to borrow is 1%.  He places 10 ETH into the ETH/DAI pool and withdraws a loan of 5000 DAI. An origination fee is applied and his debt becomes 5002.5 his collateral pledged is 10, and his TP is 5002.5/10 = 500.25. When he created the loan, the pool's MOMP was 1600 while the LUP was 1500. As a result the NP =1600 \* 500.25/1500 +  50.025 = 533.6. **(Safe)**

Bob has ETH, and would like to borrow some DAI. The APR to borrow is 1%.  He places 10 ETH into the ETH/DAI pool and withdraws a loan of 10000 DAI. An origination fee is applied and his debt becomes 10005 his collateral pledged is 10, and his TP is 10005/10 = 1000.5. When he created the loan, the pool's MOMP was 1600 while the LUP was 1500. As a result the NP =1600 \* 1000.5/1500 + 100.05 = 1163.2. **(Moderate)**\
\
Bob has ETH, and would like to borrow some DAI. The APR to borrow is 1%. He places 10 ETH into the ETH/DAI pool and withdraws a loan of 14800 DAI. An origination fee is applied and his debt becomes 14,807.4 his collateral pledged is 10, and his TP is 14,807.4/10 = 1,480.74. When he created the loan, the pool's MOMP was 1600 while the LUP was 1500. As a result the NP =1600 \* 1,480.74/1500 + 148.074 = 1707.344. **(almost at the limit)**\
\
Bob has ETH, and would like to borrow some DAI. The APR to borrow is 1%.  He places 10 ETH into the ETH/DAI pool and withdraws a loan of 15000 DAI. An origination fee is applied and his debt becomes 15007.5 his collateral pledged is 10, and his TP is 15007.5/10 = 1500.75. When he created the loan, the pool's MOMP was 1600 while the LUP was 1500. As a result the NP =1600 \* 1500.75/1500 + 150.075 = 1600.8. **(INVALID: TP > LUP)**

### How do I participate in liquidation auctions?

cc

### What if a liquidation auction clears below a loan's Threshold Price?

xx
