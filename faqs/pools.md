# 🌊 Pools

[How do I create a pool?](pools.md#how-do-i-create-a-pool)\
[What are the technical pool limitations?](pools.md#what-are-the-technical-pool-limitations)\
[What assets can be lent and borrowed?](pools.md#what-assets-can-be-lent-and-borrowed)\
[What assets are incompatible?](pools.md#what-assets-are-incompatible)\
[Does Ajna support rebase tokens?](pools.md#does-ajna-support-rebase-tokens)\
[Does Ajna support NFTs which charge a fee on transfer?](pools.md#does-ajna-support-nfts-which-charge-a-fee-on-transfer)\
[Why is a subset hash needed to separate between ERC-20 and ERC-721 pools?](pools.md#why-is-a-subset-hash-needed-to-separate-between-erc-20-pool-and-erc-721-pool)

### How do I create a pool?

1. Determine the assets you'd like to borrow or lend against.
2. See if the asset pairing you want to engage with already exists in the Ajna Protocol
3. If it doesn't exist, you can create the pool.
4. Enter the token addresses of the two assets.
5.  Next, pick which one will be collateral and which one will be the “quote token,” which is the asset that will be lent and borrowed .

    _note: Remember that while Ajna can support NFTs as collateral, quote tokens need to be ERC20._
6. Finally, select an interest rate between 1-10% that you think will be a good starting point for the pool – don’t worry about getting this wrong, the pool will self-adjust over time to find the correct parameters.
7. Once these steps are complete, you can begin lending or borrowing in this Ajna Pool.

### What are the technical pool limitations?

* Borrowers cannot draw debt from a pool in the same block as when the pool was created.
* With the exception of quantized prices, pool inputs and most accumulators are not explicitly limited. The pool will stop functioning when the bounds of a `uint256` need to be exceeded to process a request.

### What assets can be lent and borrowed?

Ajna enables lending for all ERC-20 tokens and borrowing for ERC-20, ERC-721, and ERC-721 collections or subsets through its pools. Pools are pairs of quote and collateral tokens provided by lenders and borrowers.

### What assets are incompatible?

The following types of tokens are incompatible with Ajna, and no countermeasures exist to explicitly prevent creating a pool with such tokens, actors should use them at their own risk:

* NFT and fungible tokens which charge a fee on transfer.
* Fungible tokens whose balance rebases.

The following types of tokens are incompatible with Ajna, and countermeasures exist to explicitly prevent creating a pool with such tokens:

* Fungible tokens with more than 18 decimals or 0 decimals, whose `decimals()` function does not return a constant value, or which do not implement the optional [decimals()](https://eips.ethereum.org/EIPS/eip-20#decimals) function.

### Does Ajna support rebase tokens?

Not natively, but if users wrap their rebase tokens they should work.

### Does Ajna support NFTs which charge a fee on transfer?

Not natively, but if users wrap their rebase tokens they should work.

### Why is a subset hash needed to separate between ERC-20 and ERC-721 pools?

Because Ajna contracts enable NFT collection pools in which any `tokenId` can be used as collateral, as well as nft subset pools in which only the tokenIds specified by the pool creator can be used as collateral. We use the subset hash to track the various pools created and prevent duplicates, while enabling subset and collection types pools to be enabled for the same NFT token address.
