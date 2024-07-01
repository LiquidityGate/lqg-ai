Link: https://docs.LQG.org/concepts-overview/core-concepts/liquidations-and-price-oracles
Title: Liquidations & Price Oracles

To reproduce the same liquidation conditions as the lending pool for its users, LQG will copy on-chain all the different risk parameters.
Price Oracles
LQG's prices are the same as those used by the lending pools that LQG plugs into. If the price changes for the lending pool, the exact change happens simultaneously for LQG.
Liquidations
LQG has its own independent liquidators that directly scan the book of users. LQG mirrors on-chain all the collateral ratios and close factors of the lending pools. This way, assuming LQG has liquidators operating, the liquidation guarantees for users are the same as for lending pool users.
Please refer to the developers' documentation to become a liquidator or for more technical details concerning liquidation: calculation of balances, health factors, and liquidation parameters.
