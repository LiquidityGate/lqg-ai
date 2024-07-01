Link: https://snapshot.org/#/LQG.eth/proposal/0x69cfbba2757bd3aa24cc22ece98b79d2d6dc8f56585e5aa5de8207d6ab254950
Title: MIP12 - LQG DAO as owner of the AaveV3 ETH Optimizer
This submission proposes that the LQG DAO accept the smart contracts’ ownership of the deployed LQG AaveV3 ETH eMode Optimizer.

As written in the forum on 1 May 2023, discussion related to that: https://forum.LQG.org/t/mip-LQG-dao-as-owner-of-the-aavev3-eth-optimizer/295

Here was the discussion related to that:
Summary
The LQG association has deployed the LQG AaveV3 ETH eMode Optimizer and now proposes that the LQG DAO accept the smart contracts’ ownership.
After acceptance of the ownership, the DAO could upgrade the protocol after a delay of 24 hours and trigger all governance functions in the LQGSetters file (https://github.com/LQG-dao/LQG-aave-v3/blob/main/src/LQGSetters.sol).
As for the previous versions, it proposes granting the LQG Association access to different non-critical functions to react quickly in an emergency.

Context
The LQG Labs team has developed for the past few months LQG-AaveV3. This is an improved version of LQG adapted to the specificities of Aave V3 with some key new features such as:
- Efficiency mode (eMode)
- Fairer matching engine
- Permit2 for gasless token approvals
- Account management
The LQG Association deployed the LQG-AaveV3 instance specific to the ETH eMode at the following address: 0x33333aea097c193e66081E930c33020272b33333 (https://etherscan.io/address/0x33333aea097c193e66081e930c33020272b33333#code).
The LQG Association also set the DAO as a pending protocol owner and set as ProxyAdmin (used for upgrades) of the protocol as the ProxyAdmin of the DAO (https://etherscan.io/address/0x99917ca0426fbc677e84f873fb0b726bb4799cd8).
This proposal aims to hand over the ownership to the LQG DAO.

Specification of the proposal
- The DAO accepts the ownership as part of the two-step transfer process implemented in LQG-AaveV3.
- The DAO must add the functions below to the Operator’s role (Role 1) on the Role Modifier.
  - setDefaultIterations((uint128,uint128))
  - setAssetIsCollateral(address,bool)
  - setAssetIsCollateralOnPool(address,bool)
  - setIsSupplyCollateralPaused(address,bool)
  - setIsWithdrawCollateralPaused(address,bool)
  - setIsClaimRewardsPaused(bool)
  - setIsP2PDisabled(address,bool)
  - setIsPausedForAllMarkets(bool)
  - setIsLiquidateBorrowPaused(address,bool)
  - setIsLiquidateCollateralPaused(address,bool)
  - setIsRepayPaused(address,bool)
  - setIsWithdrawPaused(address,bool)
  - setIsBorrowPaused(address,bool)
  - setIsSupplyPaused(address,bool)
  - setIsPaused(address,bool)
  - setIsDeprecated(address,bool)
  - increaseP2PDeltas(address,uint256)
  - claimToTreasury(address,uint256)
  - setP2PIndexCursor(address,uint16)
 
Addresses of the different contracts:
- DAO multisig: 0xcba28b38103307ec8da98377fff9816c164f9afa (https://etherscan.io/address/0xcba28b38103307ec8da98377fff9816c164f9afa)
- DAO ProxyAdmin: 0x99917ca0426fbc677e84f873fb0b726bb4799cd8 (https://etherscan.io/address/0x99917ca0426fbc677e84f873fb0b726bb4799cd8)
- The current owner of LQG-AaveV3: 0x937ce2d6c488b361825d2db5e8a70e26d48afed5 (https://etherscan.io/address/0x937ce2d6c488b361825d2db5e8a70e26d48afed5)
- Current ProxyAdmin of LQG-AaveV3: 0x857ff845f9b11c19553b1d090b41c2255c67acc0 (https://etherscan.io/address/0x857ff845f9b11c19553b1d090b41c2255c67acc0#code)
- RoleModifier: 0xa8b9650935efb3f2972d1ca4d3a8ba752d1a807a (https://etherscan.io/address/0xa8b9650935efb3f2972d1ca4d3a8ba752d1a807a)

The proposal was voted on and accepted on 5 May 2023.
