---
description: This page tracks Ajna contract deployments on various networks.
---

# ⛓ Deployment Addresses & Bridges

## Ethereum Mainnet

### Addresses

<table><thead><tr><th>Contract</th><th>Address</th><th>Date</th><th data-hidden></th></tr></thead><tbody><tr><td>AJNA token</td><td>0x9a96ec9B57Fb64FbC60B423d1f4da7691Bd35079</td><td>2022.09.05</td><td>AjnaToken.s.sol</td></tr><tr><td>ERC20 factory</td><td>0x6146DD43C5622bB6D12A5240ab9CF4de14eDC625</td><td>2024.01.04</td><td>deploy.s.sol</td></tr><tr><td>ERC721 factory</td><td>0x27461199d3b7381De66a85D685828E967E35AF4c</td><td>2024.01.04</td><td>deploy.s.sol</td></tr><tr><td>PoolInfoUtils</td><td>0x30c5eF2997d6a882DE52c4ec01B6D0a5e5B4fAAE</td><td>2024.01.04</td><td>deploy.s.sol</td></tr><tr><td>PoolInfoUtilsMulticall</td><td>0xe4e553243264f2bF7C135F1eC3a8c09078731227</td><td>2024.01.04</td><td>deploy.s.sol</td></tr><tr><td>PositionManager</td><td>0x87B0F458d8F1ACD28A83A748bFFbE24bD6B701B1</td><td>2024.01.04</td><td>deploy.s.sol</td></tr><tr><td>BurnWrapper</td><td>0x936Ab482d6bd111910a42849D3A51Ff80BB0A711</td><td>2023.08.14</td><td>BurnWrapper.s.sol</td></tr><tr><td>GrantFund</td><td>0x74d5b005ca64a5C9EE3611Bdc6F6C02D93C84b2f</td><td>2024.01.08</td><td></td></tr></tbody></table>

## Arbitrum One

Canonical bridge from Ethereum mainnet: [https://bridge.arbitrum.io/](https://bridge.arbitrum.io/)

Block explorer: [https://arbiscan.io/](https://arbiscan.io/)

### Addresses

<table><thead><tr><th>Contract</th><th>Address</th><th>Date</th><th data-hidden>Deployed via</th></tr></thead><tbody><tr><td>AJNA token</td><td>0xA98c94d67D9dF259Bee2E7b519dF75aB00E3E2A8</td><td>2024.01.04</td><td>Sent across <a href="https://bridge.arbitrum.io/">https://bridge.arbitrum.io/</a></td></tr><tr><td>ERC20 factory</td><td>0xA3A1e968Bd6C578205E11256c8e6929f21742aAF</td><td>2024.01.17</td><td>deploy.s.sol</td></tr><tr><td>ERC721 factory</td><td>0x6ae3324612bEfD4AE460244c369f30Ab9CB8cAE2</td><td>2024.01.17</td><td>deploy.s.sol</td></tr><tr><td>PoolInfoUtils</td><td>0x8a7F5aFb7E3c3fD1f3Cc9D874b454b6De11EBbC9</td><td>2024.01.17</td><td>deploy.s.sol</td></tr><tr><td>PoolInfoUtilsMulticall</td><td>0xCcaf0542c78A3A5e55f99630a2B126A5BAA44FC3</td><td>2024.01.17</td><td>deploy.s.sol</td></tr><tr><td>PositionManager</td><td>0x9A0BE971530Ed2B53597AC9155AC050ca1Bab7A3</td><td>2024.01.17</td><td>deploy.s.sol</td></tr></tbody></table>

## Base

Blockchain explorer: [https://basescan.org/](https://basescan.org/)

Network info: [https://docs.base.org/network-information](https://docs.base.org/network-information)

Chain id: 8453

Canonical bridge from Ethereum Mainnet: [https://bridge.base.org/deposit](https://bridge.base.org/deposit) Since bwAJNA won’t be in their UX, can manually bridge by following steps below:

1. You need to make the bwAJNA token address on the Ethereum side approve the BASE bridge contract to be able to grab your bwAJNA. For this, navigate to [bwAJNA token address](https://etherscan.io/token/0x936ab482d6bd111910a42849d3a51ff80bb0a711#writeContract) and enter `0x3154Cf16ccdb4C6d922629664174b904d80F2C35` for spender (address).
2. Navigate to [token bridge contract](https://etherscan.io/address/0x3154Cf16ccdb4C6d922629664174b904d80F2C35#writeProxyContract#F5) on etherscan and connect wallet.
3. Choose _Write as Proxy_ and expand 5. `depositERC20`
4. Populate fields:
   1. set `_l1Token` to `0x936Ab482d6bd111910a42849D3A51Ff80BB0A711`
   2. set `_l2Token` to `0xf0f326af3b1Ed943ab95C29470730CC8Cf66ae47`
   3. set `_amount` to however much you want to send across the bridge, in wei
   4. set `_minGasLimit` to `100000`
   5. set `_extraData` to 0x0 (at least this worked one time)
5. Click _Write_ button. After TX included in L1, may take 10-30 minutes for L2 to show updated balance.

### Addresses

<table><thead><tr><th>Contract</th><th>Address</th><th>Date</th><th data-hidden>Deployed via</th></tr></thead><tbody><tr><td>AJNA token</td><td>0xf0f326af3b1Ed943ab95C29470730CC8Cf66ae47</td><td>2023.08.24</td><td><a href="https://basescan.org/address/0xf23d369d7471bd9f6487e198723eea023389f1d4#writeContract">https://basescan.org/address/0xf23d369d7471bd9f6487e198723eea023389f1d4#writeContract</a></td></tr><tr><td>ERC20 factory</td><td>0x214f62B5836D83f3D6c4f71F174209097B1A779C</td><td>2024.01.17</td><td>deploy.s.sol</td></tr><tr><td>ERC721 factory</td><td>0xeefEC5d1Cc4bde97279d01D88eFf9e0fEe981769</td><td>2024.01.17</td><td>deploy.s.sol</td></tr><tr><td>PoolInfoUtils</td><td>0x97fa9b0909C238D170C1ab3B5c728A3a45BBEcBa</td><td>2024.01.17</td><td>deploy.s.sol</td></tr><tr><td>PoolInfoUtilsMulticall</td><td>0x249BCE105719Ae4183204371697c2743800C225d</td><td>2024.01.17</td><td>deploy.s.sol</td></tr><tr><td>PositionManager</td><td>0x59710a4149A27585f1841b5783ac704a08274e64</td><td>2024.01.17</td><td>deploy.s.sol</td></tr></tbody></table>

## Optimism

Canonical bridge from Ethereum Mainnet: [https://app.optimism.io/bridge/deposit](https://app.optimism.io/bridge/deposit)

Blockchain explorer: [https://optimistic.etherscan.io/](https://optimistic.etherscan.io/)

#### Addresses

<table><thead><tr><th>Contract</th><th>Address</th><th>Date</th><th data-hidden>Deployed via</th></tr></thead><tbody><tr><td>AJNA token</td><td>0x6c518f9D1a163379235816c543E62922a79863Fa</td><td>2023.08.27</td><td><a href="https://optimistic.etherscan.io/address/0x4200000000000000000000000000000000000012#writeProxyContract">https://optimistic.etherscan.io/address/0x4200000000000000000000000000000000000012#writeProxyContract</a></td></tr><tr><td>ERC20 factory</td><td>0x609C4e8804fafC07c96bE81A8a98d0AdCf2b7Dfa</td><td>2024.01.17</td><td>deploy.s.sol</td></tr><tr><td>ERC721 factory</td><td>0xAAa20ba75A7ed4Fa895E4659861448a828fa6E48</td><td>2024.01.17</td><td>deploy.s.sol</td></tr><tr><td>PoolInfoUtils</td><td>0xdE6C8171b5b971F71C405631f4e0568ed8491aaC</td><td>2024.01.17</td><td>deploy.s.sol</td></tr><tr><td>PoolInfoUtilsMulticall</td><td>0x33e5c2b41e915acFC268a4eaACC567f612f96601</td><td>2024.01.17</td><td>deploy.s.sol</td></tr><tr><td>PositionManager</td><td>0x72bF565f2BdA43294C6cC2BfE17C7FaE5258F819</td><td>2024.01.17</td><td>deploy.s.sol</td></tr></tbody></table>

## Polygon POS

Canonical Bridge from Ethereum Mainnet: [https://wallet.polygon.technology/polygon/bridge/deposit](https://wallet.polygon.technology/polygon/bridge/deposit)

Blockchain explorer: [https://polygonscan.com/](https://polygonscan.com/)

#### RC9 addresses

<table><thead><tr><th>Contract</th><th>Address</th><th>Date</th><th data-hidden>Deployed via</th></tr></thead><tbody><tr><td>AJNA token</td><td>0xA63b19647787Da652D0826424460D1BBf43Bf9c6</td><td>2023.08.14</td><td><a href="https://mapper.polygon.technology/map">https://mapper.polygon.technology/map</a></td></tr><tr><td>ERC20 factory</td><td>0x1f172F881eBa06Aa7a991651780527C173783Cf6</td><td>2024.01.17</td><td>deploy.s.sol</td></tr><tr><td>ERC721 factory</td><td>0x8B7f874D15c25BeCC4F7c1906b3677533fe60A6e</td><td>2024.01.17</td><td>deploy.s.sol</td></tr><tr><td>PoolInfoUtils</td><td>0x519021054846cd3D9883359B593B5ED3058Fbe9f</td><td>2024.01.17</td><td>deploy.s.sol</td></tr><tr><td>PoolInfoUtilsMulticall</td><td>0xe6F4d9711121e5304b30aC2Aae57E3b085ad3c4d</td><td>2024.01.17</td><td>deploy.s.sol</td></tr><tr><td>PositionManager</td><td>0xb8DA113516bfb986B7b8738a76C136D1c16c5609</td><td>2024.01.17</td><td>deploy.s.sol</td></tr></tbody></table>

## Görli / Goerli

#### rc9-2024.01.04 addresses

<table><thead><tr><th>Contract</th><th>Address</th><th>Date</th><th data-hidden>Deployed via</th><th data-hidden></th></tr></thead><tbody><tr><td>AJNA token</td><td>0xaadebCF61AA7Da0573b524DE57c67aDa797D46c5</td><td>2022.12.06</td><td>forge create</td><td></td></tr><tr><td>ERC20PoolFactory</td><td>0xDB61f8aD0B3ed0c5522b8FE71b80023fe9188e9e</td><td>2024.01.04</td><td>deploy.s.sol</td><td></td></tr><tr><td>ERC721PoolFactory</td><td>0x8FA83D458CDbB2FCeA66d9bc31FDa80511e0AA56</td><td>2024.01.04</td><td>deploy.s.sol</td><td></td></tr><tr><td>PoolInfoUtils</td><td>0xdE8D83e069F552fbf3EE5bF04E8C4fa53a097ee5</td><td>2024.01.04</td><td>deploy.s.sol</td><td></td></tr><tr><td>PoolInfoUtilsMulticall</td><td>0x63feF8659ECdC4F909ddFB55a8B701957115B906</td><td>2024.01.04</td><td>deploy.s.sol</td><td></td></tr><tr><td>PositionManager</td><td>0x7b6C6917ACA28BA790837d41e5aA4A49c9Ad4570</td><td>2024.01.04</td><td>deploy.s.sol</td><td></td></tr><tr><td>GrantFund</td><td>0x17C7eb98aD29c8C07C2842C4B64342142C405aF4</td><td>2023.10.25</td><td>deployer using multisig</td><td></td></tr><tr><td>BurnWrapper</td><td>0xE38DFd7aB36806B882bD7332a8aE454f2273D015</td><td>2023.08.01</td><td>BurnWrapper.s.sol</td><td></td></tr></tbody></table>

