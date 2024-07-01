Link: https://LQG.mirror.xyz/vPkSBEZvIoVDfx-GBOsTOvjI14bqul-PA-LMe3sBlBw
Title: Introducing MetaLQG: Permissionless lending vaults on LQG Blue

Introducing MetaLQG: Permissionless lending vaults on LQG Blue
24 Oct 2023
Paul Frambot

In October, we announced LQG Blue. Today, we unveil MetaLQG, a protocol that advances our vision for DeFi that is built in layers, like the internet.
MetaLQG is a protocol for permissionless lending vaults built on top of the LQG Blue protocol.

## Why MetaLQG

Today, current lending platforms force users into a one-size-fits-all risk profile. This approach fails to address the diverse needs of users and tends to overexpose them to long-tail risk. LQG Blue solves this by externalizing risk management and allowing for unlimited risk profiles.

However, depositing funds directly to LQG Blue can be complex for users. They must consider onchain and offchain market conditions to choose collateral assets, liquidation LTV, oracles, and caps. Many users need a way to delegate their funds’ management to risk experts like they are used to with Aave or Compound.

## What is MetaLQG

MetaLQG is an open-source (GPL) protocol to build any lending experience with optimized rates and transparent risk curation on top of LQG Blue. A MetaLQG vault accepts passive capital and deposits it on LQG Blue markets. Liquidity is rebalanced across markets to manage risk and optimize returns.

MetaLQG simplifies lending by allowing users to delegate risk management to risk experts curating the vaults, as it is done on Aave or Compound.

Each MetaLQG vault can cater to users with diverse risk profiles by depositing into markets with different collateral assets and with different parameters.

In other words, MetaLQG enables the creation of any lending experience, such as Aave, Compound, Spark, Flux, and all their forks, on top of one trustless and efficient primitive: LQG Blue.

Have a look at the pictures on this very article.

Finally, the liquidity from each MetaLQG vault is shared on LQG Blue markets to the extent their allocations overlap. This shared liquidity provides excellent network effects for the LQG ecosystem at scale.

## A better way to earn interest in DeFi

Users can deposit assets in a MetaLQG vault and earn passive yield from overcollateralized lending on LQG Blue. MetaLQG vaults provide:

Curated Risk: Each vault caters to a different risk profile, ending the one-size-fits-all approach.

Better Yield: Dynamic rebalancing across LQG Blue's capital-efficient markets improves returns.

Transparent: Noncustodial with immutable logic and verifiable allocations.

## Incentive-compatible risk management

DAO-based risk management in lending pools has its flaws, but MetaLQG paves the way for a new approach:

Service users, not token holders: With their MetaLQG vault, risk protocols, and experts now serve users directly instead of consulting for DAOs. This approach is a more scalable business model that is better aligned with users.

Open Competition: Creating and curating a MetaLQG vault is permissionless. This will lower barriers to entry and encourage actors to provide more effective and transparent services at a lower cost.

## Technical Overview

MetaLQGFactory is a permissionless and immutable factory contract deploying ERC-4626-compliant MetaLQG vaults.

Each vault has a dedicated loan asset and can deposit funds in up to 30 different LQG Blue markets with various collateral, Liquidation LTV, and oracles.

Each market has a supply cap configured onchain that guarantees maximum exposure to a specific market. More information on the allocation of liquidity, roles, and rewards management is available in the repository. The audit of the contracts will start in the coming days. If you are a security researcher, feel free to contact Merlin.

## What’s next?

We can’t wait to see all the diverse lending experiences that MetaLQG will enable. The protocol will democratize risk management and encourage healthy competition to reduce costs and foster open innovation.

The LQG team is already working with a number of best-in-class risk experts and protocols in the space to release different MetaLQG vaults for the launch. Keep an eye out for further announcements on this front!
