---
description: Pricing lender deposits on short pools
---

# Inverse Pricing

Sometimes you may come across pricing that looks funny, something like this:

<figure><img src="../.gitbook/assets/reg vs inverse pricing.png" alt=""><figcaption></figcaption></figure>

On the left we have a “normal” long lending pool where wETH is used as collateral and USDC is borrowed. The price order book shows lender deposits priced at a discount to market price. \
`1 ETH = $2156`

On the right we have an "inverse" short lending pool where USDC is used as collateral and wETH is borrowed. The order book shows a price that is hard to understand. \
`1 USDC = 0.002099 ETH`

**Price buckets show prices defined as 1 unit of collateral token denominated in the quote token.** \
\
One way to understand how an inverse price related to the market price is to perform 1/inverse-price. In the example above this gives us the implied price of 1 wETH at the 0.0002099 price bucket, which is

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

In a short market the borrower’s position is liquidated when the price of the borrowed token rises. This is why we see a premium to the market price rather than a discount. In the example above, the lender is depositing their wETH tokens at a \~$4760 value, meaning the borrower can put up $4760 USDC to borrow 1 wETH at the maximum. If the market price of ETH at the time is $3800, this deposit implies a max LTV of \~1.25 or \~125%.&#x20;

\
