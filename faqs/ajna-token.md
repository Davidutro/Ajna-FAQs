# 👁️ AJNA Token

[What are AJNA tokens and what are they used for?](ajna-token.md#what-are-ajna-tokens-and-what-are-they-used-for)\
[What is the total supply of AJNA tokens?](ajna-token.md#what-is-the-total-supply-of-ajna-tokens)\
[Can new tokens be minted?](ajna-token.md#can-new-tokens-be-minted)\
[Where can I learn about the token distribution?](ajna-token.md#where-can-i-learn-about-the-token-distribution)\
[How can I get AJNA tokens?](ajna-token.md#how-can-i-get-ajna-tokens)\
[What is burn wrapped AJNA, bwAJNA?](ajna-token.md#what-is-burn-wrapped-ajna-bwajna)\
[How do I burn wrap AJNA to get bwAJNA?](ajna-token.md#how-do-i-burn-wrap-ajna-to-get-bwajna)\
[Which bridge do I use to send my bwAJNA to another network?](ajna-token.md#which-bridge-do-i-use-to-send-my-bwajna-to-another-network)\
[Can I transfer bwAJNA tokens from one network to another?](ajna-token.md#can-i-transfer-bwajna-tokens-from-one-network-to-another)\
[Can I use a different bridge to bring bwAJNA to a network?](ajna-token.md#can-i-use-a-different-bridge-to-bring-bwajna-to-a-network)\
[Does each network have its own bwAJNA?](ajna-token.md#does-each-network-have-its-own-bwajna)

### What are AJNA tokens and what are they used for?

AJNA tokens are the Ajna Protocol's native token. They are used for voting in the grants program, enabling voters to delegate to themselves and earn additional AJNA. Additionally, they are bought and burned by the protocol with excess profits.

### What is the total supply of AJNA tokens?

1,000,000,000 tokens at protocol launch.

### Can new tokens be minted?

No.

### Where can I learn about the token distribution?

[https://mirror.xyz/0xc1112dbbcA87aAE49CAfe4F3aE065E1B0dDd5bbB/J5M0GWA581YTzUdf7vHntf-N1IvLOTrKwgVi5e0DYys](https://mirror.xyz/0xc1112dbbcA87aAE49CAfe4F3aE065E1B0dDd5bbB/J5M0GWA581YTzUdf7vHntf-N1IvLOTrKwgVi5e0DYys)

### How can I get AJNA tokens?

1. Buy them on the open market (once token is launched and distributed).
2. Earn them by participating as a delegate.
3. Earn them through usage-rewards offered by third parties.
4. If you have something you could do that would contribute to protocol success, [propose a grant](https://forum.ajna.finance/).

### What is burn wrapped AJNA, bwAJNA?

Burn-wrapped tokens are created when tokens from one chain are pre-burned, wrapped, and then transferred to another chain. They are a key component of the Ajna Protocol's multichain deployment design. Their purpose is to enable users to participate in =reserve pool auctions on other networks, to tie the value of Ajna deployments together, to defend against bridge hacks, and to ensure a high integrity for the token supply.\
\
In practice, the tokens act as a one-way path for AJNA tokens since they cannot be unburned or unwrapped. bwAJNA cannot be "unwrapped" to AJNA tokens on Ethereum. Ajna's original 1,000,000,000 token supply is located on Ethereum's mainnet network. All bwAJNA tokens come from this source. The only difference between the immutable AJNA protocol contract deployed on Ethereum vs the deployment on Polygon or any other network is the “address” of the AJNA token that can be used in reserve pool auctions.\
\
Here's how it works; Imagine a Polygon deployment of the Ajna protocol and there is a MATIC/DAI pool where the reserves of the pool have accumulated DAI tokens. To activate the reserve pool auction, one would need bwAJNA tokens to be able to buy the DAI.

To bridge the tokens one would first need to:\
\
\- obtain AJNA on Ethereum\
\- [mint bwAJNA on Ethereum](ajna-token.md#how-do-i-burn-wrap-ajna-to-get-bwajna)\
\- [bridge bwAJNA](ajna-token.md#which-bridge-do-i-use-to-send-my-bwajna-to-another-network) using polygon bridge\
\- use bwAJNA on the polygon side to start reserve pool auctions\
\
The bwAJNA tokens that are exchanged will be burned by the AJNA protocol on Polygon.

### How do I burn wrap AJNA to get bwAJNA?

Do so by going to [ajnafi.com](https://www.ajnafi.com), make sure you're on Ethereum mainnet, then navigate to any pool's "manage pool" section, then go to the "reserves" tab, then interact with the "Wrap AJNA for L2s" widget on the bottom left.

<figure><img src="https://lh7-us.googleusercontent.com/kFlR7WtT1lC6xgYFYO7LlNFjqhI8tQ9VS7m4hc3VTyCLA_crNz-G1RixA9meMoPKCse1TLmGJfU2ajKYXigLUNUZlgR3BtUsYBMvzgM-tNLw_mm5FXo-itINmZ4BhThlPQoHu0DUoTHOsKx0oKY1L3Q" alt=""><figcaption></figcaption></figure>

### Which bridge do I use to send my bwAJNA to another network?

If bridging bwAJNA to a network that already has bwAJNA on it, one must use the same bridge that was originally used. To find a list of canonical bridges for various Ajna deployments, look in our deployment addresses & bridges section.\
\
If bridging bwAJNA for the first time, as part of the process for deploying an Ajna Protocol instance, then be careful to [choose a bridge](https://l2beat.com/bridges/summary) that has the greatest probability of lasting for the long term.

### Can I transfer bwAJNA tokens from one network to another?

No. In doing so, the user would create an unofficial wrapped-bwAJNA token on the destination chain. All bwAJNA must originate from Ethereum L1 and then go through the original bridge it was transferred through from Ethereum to the specified network.

### Can I use a different bridge to bring bwAJNA to a network?

No you must use the original bridge that initially brought the bwAJNA to the network otherwise it will be a new token and not fungible with the first version of bwAJNA on the network.

### Does each network have its own bwAJNA?

Yes. There's only a single version of bwAjna on mainnet, but when bridged for the first time to a new chain, a new variant of bwAjna will be created.

\
