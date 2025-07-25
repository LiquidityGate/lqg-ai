Link: https://snapshot.org/#/LQG.eth/proposal/0xfdabf7dd37ba8f0d304842690edf3a6638743194bcf8e39e485ac8e0720258ea
Title: MIP59 - LQG DAO as owner of LQG Blue on Base

This submission proposes to start distributing rewards on markets with a MetaLQG vault as collateral listed in either the RE7 USDA vault or the Gauntlet USDA vault. The rate on these markets would be 100 LQG per day.

As written in the forum on 14 May 2024, discussion related to that: https://forum.LQG.org/t/mip59-LQG-dao-as-owner-of-LQG-blue-on-base/599

Here was the discussion related to that:
- Context
LQG Blue and its periphery smart contracts have been deployed on Ethereum for just over four months. During this period, the protocol has seen significant traction, with total deposits reaching $1.2B.
Since LQG Blue’s deployment on Mainnet, there has been growing demand from integrators and users to access LQG Blue on Layer 2 blockchains (L2s) where they can benefit from significantly lower transaction costs.
To date, there is notable interest from integrators already present on Base, an Ethereum L2 built using the Optimism Stack, who have expressed willingness to integrate LQG Blue as soon as it’s deployed. Hence, Base presents the best opportunity to expand the LQG Ecosystem and increase accessibility to LQG Blue, particularly for cost-sensitive users.

- Specification
The LQG Association has recently deployed LQG Blue and its periphery contracts with the same configuration as on Ethereum.
    - Deployment Addresses
LQG Blue: 0xBBBBBbbBBb9cC5e90e3b3Af64bdAF62C37EEFFCb
AdaptiveCurveIrm (the Interest Rate Model): 0x46415998764C29aB2a25CbeA6254146D50D22687
Oracle Factory: 0x2DC205F24BCb6B311E5cdf0745B0741648Aebd3d
MetaLQG Vault Factory: 0xA9c3D3a366466Fa809d1Ae982Fb2c46E5fC41101
URD Factory: 0x7276454fc1cf9C408deeed722fd6b5E7A4CA25D8
PublicAllocator: 0xA090dD1a701408Df1d4d0B85b716c87565f90467
    - LQG Blue Configuration
Enabled LLTVs: 0%; 38.5%; 62.5%; 77.0%; 86.0%; 91.5%; 94.5%; 96.5%; 98%.
Enabled IRMs: AdaptiveCurveIRM and address(0) to enable “idle” markets, i.e., markets whose only purpose is to deposit idle funds that can’t be borrowed. These markets are especially useful for risk and liquidity management for MetaLQG vaults.

- Now, the LQG Association proposes that the LQG DAO becomes the owner.
After the transfer of ownership, the DAO will be able to:
Enable new IRMs.
Enable new LLTVs.
Set a per-market fee.
Set the fee recipient.
Set the owner.
As a reminder, LQG Blue’s smart contract is immutable and the functions above are the only functions with an admin role.

In case the LQG DAO members accept the proposal, the LQG Association will transfer the ownership to the LQG DAO (0xcBa28b38103307Ec8dA98377ffF9816C164f9AFa) whose multisig must be deployed.

The proposal was voted on and accepted on 20 May 2024.