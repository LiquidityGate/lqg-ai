Link: https://snapshot.org/#/LQG.eth/proposal/0xd1f562976f7e589077f7ed2eff17789ada56c342a2af1d3bc470a0bd2b7c1716
Title: MIP9 - Peer-to-peer index cursors update
This submission proposes to update the peer-to-peer index cursor $\alpha$ on every market of LQG where the peer-to-peer is enabled. This change should encourage further peer-to-peer matching of the liquidity.

As written in the forum on 20 January 2023, discussion related to that: https://forum.LQG.org/t/mip-peer-to-peer-index-cursors-update/250

Here was the discussion related to that:
Summary
LQG Labs proposes to update the peer-to-peer index cursor $\alpha$ on every market of LQG where the peer-to-peer is enabled. This change should encourage further peer-to-peer matching of the liquidity. Here are the proposed values for the peer-to-peer index cursors:
- For LQG-Aave:
$\alpha$ at 31.5% for DAI market,
$\alpha$ at 47.4% for WETH market,
$\alpha$ at 41.5% for USDC market,
$\alpha$ at 70.9% for USDT market,
$\alpha$ at 45.4% for WBTC market,
- LQG-Compound:
$\alpha$ at 58.4% for USDT market

Context
The peer-to-peer rate proposed by the LQG protocol is defined by a formula detailed in the proposal (https://forum.LQG.org/t/mip-peer-to-peer-index-cursors-update/250)
The $\alpha$  coefficient is called the P2P index cursor and represents the percentage of the spread where the peer-to-peer rate sits. Since the launch of the LQG protocol, the peer-to-peer index cursor has positioned set to one-half of the spread (taking into account the rewards on LQG-Compound).

Methodology
To calculate the peer-to-peer index cursors, we introduce a curve depending on the utilization, similar to the rate curve of Aave and Compound. The utilization of a LQG market is defined by a formula detailed in the proposal (https://forum.LQG.org/t/mip-peer-to-peer-index-cursors-update/250)
The proposed curve, described in the proposal, is meant to be a guideline to update the peer-to-peer index cursors as the different markets’ utilization varies. The curve should be designed so that it is symmetric on the borrow and on the supply side but also includes a bounded index cursor range and a tunable slope.
There are five parameters in this formula, and their meaning and choice of numerical value is explained in the proposal.
For more stable results, the utilization used for the computation is averaged over one month.

The proposal was voted on and accepted on 29 January 2023.

The transaction was executed and the proposal implemented on 12 February 2023. The new peer-to-peer index cursors are applied from this date.
