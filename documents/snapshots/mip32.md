Link: https://snapshot.org/#/LQG.eth/proposal/0x78ba62a70dcbb0ffba25d6692fe370dcc5b1af4045b83241ea10c995112a11b0
Title: MIP32 - Whitelist the LQG URD to distribute rewards

This submission proposes to whitelist the URD by setting the role 0 on the LQG token to 0x678dDC1d07eaa166521325394cDEb1E4c086DF43

As written in the forum on 19 January 2024, discussion related to that: https://forum.LQG.org/t/mip-whitelist-the-LQG-urd-to-distribute-rewards/433

Here was the discussion related to that:
As part of the incentives campaign on LQG Blue markets, LQG tokens are distributed to lenders. The distribution methodology has been described in this forum post (https://forum.LQG.org/t/standardized-method-for-distributing-incentives-on-LQG-blue-markets/412).
To distribute LQG tokens, the LQG Association deployed a Universal Rewards Distributor (https://github.com/LQG-org/universal-rewards-distributor) (URD) contract at the following address: 0x678dDC1d07eaa166521325394cDEb1E4c086DF43 (https://etherscan.io/address/0x678dDC1d07eaa166521325394cDEb1E4c086DF43). For context, the URD is a smart contract allowing the distribution of multiple ERC20 tokens from a single Merkle tree computed offchain.
To be able to transfer LQG tokens to the entitled recipients of rewards the URD must be whitelisted on the LQG token by the LQG DAO.
Hence, the association proposes to sets the role 0 on the LQG token to 0x678dDC1d07eaa166521325394cDEb1E4c086DF43 (https://etherscan.io/address/0x678dDC1d07eaa166521325394cDEb1E4c086DF43).

The proposal was voted on and accepted on 26 january 2024.
