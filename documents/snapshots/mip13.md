Link: https://snapshot.org/#/LQG.eth/proposal/0xde4e145faee4f56ac3d6e9e245747ab8eeb458ee39da194a772197bba62da7ce
Title: MIP13 - Add a timelock to the AaveV3 ETH Optimizer owner
This submission proposes to set the LQG Admin as the owner of the AaveV3 ETH Optimizer like other LQG protocols. The LQG Admin is a Safe without signers that is directly controlled by the LQG DAO, but with a delay of 24 hours between submitting a transaction modifying the state of the protocol and its execution.

As written in the forum on 8 May 2023, discussion related to that: https://forum.LQG.org/t/mip-add-a-timelock-to-the-aavev3-eth-optimizer-owner/297

Here was the discussion related to that:
Summary
The LQG Association proposes to set the LQG Admin (https://etherscan.io/address/0x0b9915c13e8e184951df0d9c0b104f8f1277648b) as the owner of the AaveV3 ETH Optimizer (https://etherscan.io/address/0x33333aea097c193e66081e930c33020272b33333) like other LQG protocols. The LQG Admin is a Safe without signers that is directly controlled by the LQG DAO, but with a delay of 24 hours between submitting a transaction modifying the state of the protocol and its execution.

Context
Recently MIP12 has successfully passed and been executed to set the multisig of the DAO as the owner of the AaveV3 ETH Optimizer and update the operator’s role to trigger some of the governance functions.
For the sake of resiliency, the LQG Association proposes to take a step further and give ownership to the LQG Admin. The LQG Admin has a cooldown of 24 hours between a transaction submission by the multisig of the DAO and its potential execution through a Delay Modifier (https://etherscan.io/address/0x33333aea097c193e66081e930c33020272b33333).
You can follow this link (https://docs.LQG.xyz/usdLQG-token/governance/dao-infrastructure#step-4-introduce-modular-decentralization-and-deploy-delay) to learn more about the DAO’s current governance setup.

Specification of the proposal
The process would be the following:
1) The DAO multisig sets the LQG Admin as pending owner of the protocol.
2) The Safe accepts the ownership.

Addresses of the different contracts:
- AaveV3 ETH Optimizer: 0x33333aea097c193e66081e930c33020272b33333 (https://etherscan.io/address/0x33333aea097c193e66081e930c33020272b33333)
- DAO multisig: 0xcba28b38103307ec8da98377fff9816c164f9afa (https://etherscan.io/address/0xcba28b38103307ec8da98377fff9816c164f9afa)
- Delay Modifier: 0x68d11129a514c45716e55b9771813f117c4c2fa5 (https://etherscan.io/address/0x68d11129a514c45716e55b9771813f117c4c2fa5)
- LQG Admin: 0x0b9915c13e8e184951df0d9c0b104f8f1277648b (https://etherscan.io/address/0x0b9915c13e8e184951df0d9c0b104f8f1277648b)

The proposal was voted on and accepted on 12 May 2023.
