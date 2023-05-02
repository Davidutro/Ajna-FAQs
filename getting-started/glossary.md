---
description: Definitions are simplified and may not be comprehensive.
---

# Glossary

**Borrower Inflator (BI)**:  The borrower inflator is used in the calculation of the neutral price, which can be used as a liquidation price. The BI at a given time is the debt that a borrower would have incurred if they had borrowed a single quote token at the initiation of the contract and had never repaid or taken out any additional debt.

**Challenge Period**: At the end of each PFM cycle there is a seven day challenge period to contest the payout configuration.

**Claimable Collateral**: Each price bucket may have claimable collateral which is exchangeable with quote tokens.

**Claimable Reserve Auction (CRA)**: Claimable reserves are set aside and can be auctioned off in a Dutch auction known as a CRA. Once the CRA is initiated, AJNA tokens may be used to bid in exchange for the claimable reserves, which are always denominated in a pool's quote token.

**Collateral Token (CT)**: Can be a regular fungible token (ERC20) or an NFT (ERC721). Borrowers deposit this into the protocol to ensure debts are paid.

**Deposit**: When a lender provides quote token liquidity to a specified price bucket it is called a deposit.

**Dutch Auction**: A type of auction where the price starts high and gradually decreases until a buyer agrees to make a purchase.

**Extraordinary Funding Mechanism (EFM)**: This is an alternative funding mechanism that is meant to be used in special cases. An EFM vote uses one token one vote, lasts for one month, and requires a quorum to pass depending on the amount being requested.

**Fenwick Tree**: A Fenwick tree or binary indexed tree is a data structure that can efficiently update elements and calculate prefix sums in a table of numbers. The Ajna Protocol uses a modified Fenwick Tree to hard code price buckets in Ajna pools.

**Funding Stage**: This is the second stage in the PFM which uses a quadratic voting schema, lasts for 10 days, and involves up to 10 proposals.

**Highest Price Bucket (HPB)**: The highest-priced bucket which contains a deposit, not counting claimable collateral.

**Highest Threshold Price (HTP)**: The threshold price of the least collateralized loan. Lender Deposits above the HTP earn interest.

**Kick**: A technical term synonymous with "initiate". When a loan is under-collateralized it needs to be “kicked”, which initiates the sale of its collateral through a liquidation auction.

**Liquidation Auction**: A dutch auction which enables anyone to purchase portions of the collateral at a price that starts at 32 times the MOMP and exponentially decays with a half life of one hour.

**Liquidation Bond**: A bond paid in quote token, purchased by the initiator of a liquidation auction, that is awarded or penalized depending on the settling auction price relative to the loan's Neutral Price. The bond exists to prevent unfair liquidations.

**Liquidation Debt**: The total amount of debt being liquidated.

**Liquidity Provider Balance (LPB)**: A claimable token that represents a user's transferable share of  a price bucket of a given pool.

**Lowest Utilized Price (LUP)**: The LUP is the lowest price bucket where there is a utilized deposit. It could also be seen as the price of the marginal (lowest priced and therefore least aggressive) lender matched with a borrower.

**Meaningful Actual Utilization (MAU)**: The ratio of the 12 hour moving average of debt to the 12 hour moving average of meaningful deposit, where meaningful deposit is the amount of deposit priced at or above the average threshold price of all loans, weighted by their debt.

**Meaningful Deposit (MD)**: Deposit above the debt-weighted average threshold price of loans.

**Minimum Borrow Size**: The minimum borrow size is 10% of the average loan size in a given pool. This is designed to deter small loans. Small loans are bad for the system because they risk abandonment due to transaction costs and may be unprofitable to liquidate for the same reason.

**Most Optimistic Matching Price (MOMP)**: MOMP is the price at which the amount of deposit above it is equal to the average loan size of the pool. MOMP is short for “Most Optimistic Matching Price”, as it’s the price at which a loan of average size would match with the most favorable lenders on the book.

**Net Interest Margin (NIM)**: NIM accrues in reserves and is used to provide a liquidity cushion to lenders, and absorb the first bit of bad debts if some should occur. It is also used to buy and burn AJNA tokens.

**Neutral Price (NP)**: If a liquidation auction yields a value that is over the NP of the loan, the kicker forfeits a portion or all of their bond. The NP at any point in time is the MOMP at the time the loan was stamped times the ratio of the loan’s TP to the pool LUP, plus one year’s worth of interest times the ratio of the current borrower inflator to that borrower inflator at the time the loan was last stamped. This is recomputed every time the borrower draws more debt, or removes collateral.

**Origination Fee**: Calculated as the greater of the current annualized borrower interest rate divided by 52 (one week of interest) or 5 bps multiplied by the loan’s debt.

**Pool**: A pool aggregates all lending and borrowing activity of a specific quote token as secured by a specific collateral token type.

**Pool Collateralization**: A percentage that represents a pool's debt to collateral ratio. In Ajna this is calculated by the following formula: Total Available Collateral / Total Encumbered Collateral = (Total Collateral)\*LUP/Debt.

**Price bucket**: Price buckets are hard coded prices at which lenders are willing to lend against collateral. A price bucket can be freely traded against. In the worst case scenario, lenders would end up buying collateral at their chosen prices.

**Primary Funding Mechanism (PFM)**: On a quarterly basis, a portion of the treasury is distributed to projects to facilitate the growth of Ajna. Teams and/or individuals submit proposals that are voted on by Ajna token holders and delegates.

**Quote Token (QT)**: Must be an ERC20 token and is what lenders deposit into Price Buckets.

**Reserves**: Origination fees, deposit penalties, and net interest margin on loans are accumulated in a pool’s reserves. Reserves are used to provide a liquidity cushion to lenders by absorbing bad debt if some should occur. Reserves are also used to buy and burn AJNA tokens.

**Screening Stage**: This is the first stage in the PFM which uses a one-token-one-vote schema, lasts for 80 days, and involves an unlimited number of proposals.

**Target Utilization (TU)**: The ratio of the 3.5 day EMA of system debt to 3.5 day EMA of LUP\*totalCollateral. This may be sampled every half day to determine whether an interest rate update is available.

**Threshold Price (TP)**: The price at which the value of the collateral equals the value of the debt. By taking a loan’s debt and dividing it by the amount of collateral pledged, the loan’s threshold price, TP, can be calculated.

**Total Encumbered Collateral**: Total Debt when described in Quote Token terms or Total Debt/LUP if described in collateral unit terms.

**Treasury**: A balance of AJNA tokens held by a hard-coded address associated with the protocol.

\




