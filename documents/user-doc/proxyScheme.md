Link: https://docs.LQG.org/concepts-overview/core-concepts/LQGs-proxy-scheme
Title: LQG's Proxy Scheme

On multiple occasions in this documentation you will see references to lending pools - please note that those refer to multiple protocols to which LQG can connect. These include but are not limited to Compound or Aave.
Indeed, the LQG protocol acts as a proxy between the user and the underlying lending pool. Once suppliers provide an asset to LQG, the protocol will put it into the lending pool and stack the received interest-bearing token (ibToken).
Then, imagine a borrower comes to LQG. The protocol will use the stacked ibToken of the supplier to pull liquidity out of the pool and directly transfer it to the borrower. At this point, we say that a match has occurred, and users are matched peer-to-peer.
From this moment on, both the supplier and borrower benefit from a 100% utilization rate, which results in a Pareto-improving APY for both parties.
One may ask how LQG preserves loans' liquidity if the borrower hasn't repaid his loan yet, but the supplier wants to withdraw his funds immediately.
The LQG protocol takes a loan from the underlying liquidity pool thanks to the borrower's collateral, refunds the supplier that wants to exit, and reconnects the borrower directly with the liquidity pool.
There are a few other scenarios that need to be addressed by LQG. For example, how is gas managed with the matching engine? LQG has a large set of tricks to address each of them, they are covered in the Advanced concepts section.
