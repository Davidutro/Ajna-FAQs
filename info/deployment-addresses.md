---
description: This page tracks Ajna contract deployments on various networks.
---

# ⛓ Deployment Addresses

## Ethereum Mainnet

| Contract       | Address                                    | TX hash                                                            | Date       | Deployed via    |
| -------------- | ------------------------------------------ | ------------------------------------------------------------------ | ---------- | --------------- |
| AJNA token     | 0x9a96ec9B57Fb64FbC60B423d1f4da7691Bd35079 | 0xccfff0a57555a21edcf6ce805f47bb3ccc7ec48d4183f8a70ae7829b780b3ab5 | 2022.09.05 | AjnaToken.s.sol |
| ERC20 factory  | 0xe6F4d9711121e5304b30aC2Aae57E3b085ad3c4d | 0xa4e102f700608b3b75f7121ccf14de30417e03a4cdc1585a1dc16ba5c34bb73e | 2023.07.04 | deploy.s.sol    |
| ERC721 factory | 0xb8DA113516bfb986B7b8738a76C136D1c16c5609 | 0x4e612f5736e8818e488402a6a095f14c550b4a89087a90fe90e74350539e6233 | 2023.07.04 | deploy.s.sol    |
| PoolInfoUtils  | 0x154FFf344f426F99E328bacf70f4Eb632210ecdc | 0x5aebb637bfed7ec211253ff1da3a149aadf03333282346703a1838065dc05127 | 2023.07.04 | deploy.s.sol    |

Deployment of `factory contracts` and `PoolInfoUtils` was done with a modified `deploy.s.sol` which excludes `PositionManager` and `RewardsManager`. Those are intended to be deployed by the end of the summer of 2023 along with the `GrantFund` deployment.

## Görli / Goerli

### Deployment Notes

Before following instructions in repositories, move your `.env` file out-of-the-way, and remove `block_timestamp`, `block_number`, and `fork_block_number` from your `foundry.toml`.

### RC6 addresses

| Contract        | Address                                    | Date       | Deployed via              |
| --------------- | ------------------------------------------ | ---------- | ------------------------- |
| AJNA token      | 0xaadebCF61AA7Da0573b524DE57c67aDa797D46c5 | 2022.12.06 | `forge create`            |
| ERC20 factory   | 0x01Da8a85A5B525D476cA2b51e44fe7087fFafaFF | 2023.07.04 | deploy.s.sol              |
| ERC721 factory  | 0x37048D43A65748409B04f4051eEd9480BEf68c82 | 2023.07.04 | deploy.s.sol              |
| PoolInfoUtils   | 0xBB61407715cDf92b2784E9d2F1675c4B8505cBd8 | 2023.07.04 | deploy.s.sol              |
| PositionManager | 0x23E2EFF19bd50BfCF0364B7dCA01004D5cce41f9 | 2023.07.04 | deploy.s.sol              |
| RewardsManager  | 0x994dE190dd763Af3126FcC8EdC139275937d800b | 2023.07.04 | deploy.s.sol              |
| GrantFund       | 0x881b4dFF6C72babA6f5eA60f34A61410c1EA1ec2 | 2023.07.05 | GrantFund.s.sol           |
| TokensFactory   | 0x459A2644102d206663Db4Af5B45A38831d373Db9 | 2023.02.23 | DeployTokensFactory.s.sol |

