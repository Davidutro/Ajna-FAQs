---
description: Lender Guide
---

# 🪣 Choosing a Price Bucket

Read below and check out this short video tutorial:\
[https://youtu.be/Pu3mnV4NBJc?si=LigZJsf8z1G048Uy](https://youtu.be/Pu3mnV4NBJc?si=LigZJsf8z1G048Uy)\
\
When lending, a price bucket for the deposit of Quote Token must be selected. \
\
&#xNAN;_&#x54;ip: Pools are always described as **Collateral Token / Quote Token**_

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption><p>LFIX / USDC Lender Interface Example</p></figcaption></figure>

Price buckets are priced at X = 1 unit of collateral, X is denominated in the quote token. \
\
Eg: in the WETH (Collateral) / USDC (Quote) pool, prices should be $Discount to Market USDC = 1 unit of WETH

As a general rule, select a discount to market price or the price at which you are willing to buy if the value of the collateral were to decline. This is especially true for NFTs or long tail assets that have a thin or non-existent secondary market. However, be careful when selecting for short pools, as the prices are inverse, [see this page](https://faqs.ajna.finance/concepts/inverse-pricing) for more info and examples for short pool bucket pricing.&#x20;

Below are detailed examples of different pools, the market price of their collateral(MP), and their buckets:



**Long Pools**

`ETH/USDC, MP = $3300, Bucket = $3000`\
\
Long pools are typical. The price of the bucket is a discount to the collateral’s market price. Lenders select a bucket price of 1 Collateral Token(ETH) denominated in Quote Token(USDC) that represents a discount to the collateral market price. In this example the market price is $5000, the price bucket chosen is $3000, a 40% discount to the market.

_Tip: Lenders should account for the volatility of the collateral when determining the discount._\
\


**Short Pools**

`USDC/ETH, MP = 0.0003 ETH, Bucket = 0.0002 ETH`

Short markets are tricky, be careful. Please read the [inverse pricing section](inverse-pricing.md) to better understand the pricing conventions of this pool type. I’ll summarize below:\
\
Lenders select a bucket price of 1 Collateral Token(USDC) denominated in Quote Token(ETH) that represents a discount to the collateral market price. In this example the market price is 0.003, implying an ETH price of 1/0.003, or $3,333,33. The bucket selected is 0.0002 ETH, implying a price of $5000. \
As a lender you are saying that you are willing to exchange the ETH you lent for USDC as a price of $5000 if the price appreciates.\
\
In this case a borrower would get liquidated when the value of their collateral (USDC) drops in relation to their debt. \
\
`USDC is worth less in ETH terms when the price of ETH goes up.`\
`USDC is worth more in ETH terms when the price of ETH goes down.`

_Tip: In short pools, lenders should choose a price above market._



**Unstable Pool**\
\
`RBN/ETH, MP = 0.000236 ETH, Bucket = 0.00012 ETH`

An unstable pool contains assets on both sides that don’t hold stable values. An example of this is the RBN/ETH pool.\
\
Lenders select a bucket price of 1 Collateral Token(RBN) denominated in Quote Token(ETH) that represents a discount to the collateral market price. In this example the market price is 0.00236 ETH = 1 RBN. Price buckets under 0.00236 make sense for this pool, not accounting for the possible volatility of the RBN/ETH price.



**Stable Pool**

`sUSDe / DAI, MP = 1.05 DAI, Bucket = 0.995 DAI`

A stable pool contains assets on both sides that have relatively stable values. An example of this is the sUSDe/DAI pool.

Lenders select a bucket price of 1 Collateral Token(sUSDe) denominated in Quote Token(DAI) that represents a discount to the collateral market price. In this example the market price is 1.05 DAI = 1 sUSDe. Price buckets under 1.05 make sense, not accounting for the possible volatility of the sUSDe/DAI price.\


**Adjusting deposits**

As the market price of the collateral moves, lenders risk getting traded against at the price bucket of their deposit. To avoid this, lenders need to monitor their positions and adjust deposits as needed. Doing so requires withdrawal and redeposit of the lent tokens. In some cases the lender's deposit may be frozen, in which case adjusting will not be possible. This is a risk you take as a lender, especially as a deposit is closer to the market price.

\


\


\
\
