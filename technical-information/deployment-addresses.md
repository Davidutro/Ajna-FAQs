---
description: This page tracks Ajna contract deployments on various networks.
---

# Deployment Addresses

## Ethereum Mainnet

| Contract       | Address                                    | TX hash                                                            | Date       | Deployed via              |
| -------------- | ------------------------------------------ | ------------------------------------------------------------------ | ---------- | ------------------------- |
| AJNA token     | 0x9a96ec9B57Fb64FbC60B423d1f4da7691Bd35079 | 0xccfff0a57555a21edcf6ce805f47bb3ccc7ec48d4183f8a70ae7829b780b3ab5 | 2022.09.05 | AjnaToken.s.sol           |
| ERC20 factory  | 0xe6F4d9711121e5304b30aC2Aae57E3b085ad3c4d | 0xa4e102f700608b3b75f7121ccf14de30417e03a4cdc1585a1dc16ba5c34bb73e | 2023.07.04 | deploy.s.sol              |
| ERC721 factory | 0xb8DA113516bfb986B7b8738a76C136D1c16c5609 | 0x4e612f5736e8818e488402a6a095f14c550b4a89087a90fe90e74350539e6233 | 2023.07.04 | deploy.s.sol              |
| PoolInfoUtils  | 0x154FFf344f426F99E328bacf70f4Eb632210ecdc | 0x5aebb637bfed7ec211253ff1da3a149aadf03333282346703a1838065dc05127 | 2023.07.04 | deploy.s.sol              |
| TokensFactory  | 0x80A21A780f1300aa37Df1CCA0F96981FBc2785BD | 0x256b52fbeb9cea0478582868d9295ae50a276fd68cbb53a480fe23c9645295a8 | 2023.06.16 | DeployTokensFactory.s.sol |

Deployment of factory contracts and `PoolInfoUtils` was done with a modified `deploy.s.sol` which excludes `PositionManager` and `RewardsManager`. Those should be deployed sometime July 2023 with `GrantFund` deployment planned for late August 2023.
