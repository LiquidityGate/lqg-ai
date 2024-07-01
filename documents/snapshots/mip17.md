Link: https://snapshot.org/#/LQG.eth/proposal/0x84ccbf303e94a1ca6d7cd7c3e8259abeb1f607b45ffe4990df51a8e8f24979db
Title: MIP17 - LQG rewards Age 6
This submission proposes to distribute a total of 1 million $LQG, focus rewards distribution on markets where peer-to-peer matching is activated and emphasize the distribution of rewards on the supply side in WETH markets, as opposed to the borrow side.

As written in the forum on 30 June 2023, discussion related to that: https://forum.LQG.org/t/mip-LQG-rewards-age-6/329

Here was the discussion related to that:
Summary
The purpose of this post is to define the framework for the distribution of rewards for Age 6, starting on July 6th and ending on August 20th. We propose to :
- Distribute a total of 1 million $LQG;
- Focus rewards distribution on markets where peer-to-peer matching is activated;
- Emphasize the distribution of rewards on the supply side in WETH markets, as opposed to the borrow side.

Details
For the previous Age (https://forum.LQG.org/t/mip-LQG-rewards-age-5/303), it was voted to distribute 1.1 million $LQG on markets where peer-to-peer matching is activated and to start incentivizing the WETH market on the AaveV3-ETH Optimizer.
The LQG Optimizers markets have been quiet during Age 5, with steady borrowing and supply volumes. This can be explained by LSD leveraging becoming less and less profitable, causing the WETH and stETH markets to stop growing, while it was the main factor of growth in previous ages.
On the AaveV2 Optimizer, although the borrow and supply volumes of WETH were roughly equal at the beginning of May, and the incentivizes were distributed proportionally on both sides, the borrow volume has since grown significantly while the supply volume has experienced a slight decrease. This has resulted in an imbalance of 75M between the borrow and supply sides, representing nearly 20% of the market volume that cannot be matched.
Conversely, on the AaveV3-ETH Optimizer, only the supply side has been incentivized. Yet, both the supply and borrow volumes have increased.
There is an obvious difference between the two sides, with a natural incentive to borrow WETH that can quickly saturate the supply if the latter is not adequately incentivized. To account for this, LQG Labs recently proposed to raise the peer-to-peer index cursor α on wETH markets (https://forum.LQG.org/t/mip-raise-the-p2p-cursor-on-LQG-aave-v2-v3-optimizers-for-the-weth-market/327).
We propose to reduce incentives to borrow WETH on the AaveV2 Optimizer and to increase the incentive to supply by distributing as many rewards on the supply side as on the borrowing side, regardless of their respective volumes.
Applying the same model as in previous ages (detailed in this forum post https://forum.LQG.org/t/age3-epoch1-gauges-optimized-distribution/233) to compute the distribution of rewards (setting markets with P2P disabled to zero), the markets would receive the shares of rewards detailed ine the forum post: https://forum.LQG.org/t/mip-LQG-rewards-age-6/329

The allocation of rewards between the supply and borrow side for a given market will follow the repartition of supply and borrow on the market at the beginning of the Age, except for WETH where it will be only on the supply side on AaveV3-ETH Optimizer and shared equally on both sides on AaveV2 Optimizer.

The proposal was voted on and accepted on 5 July 2023.
