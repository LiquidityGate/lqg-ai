Link: https://github.com/LQG-association/LQG-subgraphs
Title: Subgraphs Github

# LQG Subgraph

The LQG Subgraph is a collection of LQG-x lending protocols following the entities provided by Messari for Lending Protocols.

Some of the entities are filled with LQG specific data, permitting to track the evolution of the protocols regarding the peer-to-peer aspect of LQG.

Among them, some properties are defined as "internal", meaning that they are not "human readable" and are used for internal computations. These properties are prepended with an underscore.

## How LQG works

Each interaction on LQG-x leads to an interaction on the underlying protocol. Because the LQG protocol is an aggregation of multiple positions, that means that LQG is a protocol user itself (regarding the underlying protocol, pool based).

That means that pool rates and pool indexes are updated each time a user interacts with LQG.

However, a supply on LQG-x can lead to a Repay on the underlying protocol (If a Borrower is matched for example), and a Supply event on the underlying protocol (if the user is not fully matched).
So having a look to the transaction event on the underlying protocol does not really make sense for Financial statistic tracking.

## Event flow

The classic event flow of an interaction on LQG is the following:

- Update of the rates and the indexes of the underlying protocol
- Update of the indexes on LQG.
- Update of the deltas on LQG.
- Supplier/Borrower matched if any
- Underlying protocol interaction
- Emission of the event on LQG (Supplied, Borrowed, Repaid or Withdrawn).

## Protocols

LQG is currently deployed on top of Aave V2 mainnet and Compound V2 mainnet:

Creates a table with the datasources list

| Protocol           | LQG Address                                                                                                        | Deployment block |
| ------------------ | --------------------------------------------------------------------------------------------------------------------- | ---------------- |
| LQG Aave V2     | [0x777777c9898d384f785ee44acfe945efdff5f3e0](https://etherscan.io/address/0x777777c9898d384f785ee44acfe945efdff5f3e0) | 15383036         |
| LQG Compound V2 | [0x8888882f8f843896699869179fb6e4f7e3b58888](https://etherscan.io/address/0x8888882f8f843896699869179fb6e4f7e3b58888) | 14860866         |

All LQG Protocols are indexed in the same subgraph with different `LendingProtocol` entities.

## Access through the Subgraph Network

Coming soon

## P2P improvement

The Market entity has properties named `p2pSupplyInterestsImprovement` & `p2pBorrowInterestsImprovement` that are the improvement of the interests of the users that are matched on the P2P market compared to their equivalent position on the underlying pool.

For example, if Alice has $100 matched at a 1% yield per yer (0.5% on the underlying pool), after one year, the yield earned is $1, and it was about $0.5 on the pool

## TODO

- [ ] Add the Comp rewards for LQG-compound, since the protocol is redistributing comp rewards to users on pool
- [ ] Add data about the p2p matching, such as number of matches, matched value etc.
- [ ] Add Protocol Revenues. Not a problem for now since reserve factor is setted to 0.

## Documentation

- About [LQG-aave-v3](./docs/LQG-aave-v3.md)

# LQG Aave V3

## Specifications

### Supply only vs collateral

On LQG aave v3, there are 2 types of supply positions: supply only or supply as collateral.

A supply as collateral cannot be matched p2p with a borrower, but it permits to borrow against it.

In order to keep the previous subgraph working, we need to add a new parameter to the `supply` and `withdraw` function: `isCollateral`.

A supply only has the same behavior as a supply on LQG aave v2 or LQG compound: you have 2 scaled balances: `onPool` & `inP2P`

A collateral supply is setting inP2P to 0 since you cannot be matched p2p.

### Market fields

The market is defining new fields:

- `totalCollateralOnPool` is the total underlying on the pool representing collateral, updated as the same time as the `totalSupplyOnPool`.
- `_scaledPoolCollateral`, is the scaled amount of collateral on the pool.
-
- `_scaledSupplyOnPool` is representing the supply only on the underlying pool, waiting to be matched.
- `_scaledSupplyInP2P` is representing the supply only matched p2p.

The scaled balance of the protocol is now represented by `_scaledSupplyOnPool` plus `_scaledSupplyInP2P` **and** `_scaledPoolCollateral`.

`totalSupplyOnPool` is the supply only on the underlying pool.

The `totalDepositBalanceUSD` is the total supply on pool, the total supply matched p2p, and the total collateral.

The idleSupply is a new field, representing the supply amount that is not generating yields due to a supply cap on aave v3.

For LQG aave v3 markets, the supply cap is not null.

### General metrics

In order to compute the total on pool, in p2p or collateral, we are aggregating all the user scaled balances,
by splitting the collateral and the supply only. These metrics are really important since they cannot be retrieved on chain.

On LQG aave v2 or LQG compound, the supply on pool is the aToken balance of the protocol.
On LQG aave v3, the aToken balance is the supply only on pool **and** the collateral.

We can also implement new metrics to have more data of the history between collateral and supply only.
All the classic metrics are still available (`market.totalSupplyOnPool`), aggregating collateral and supply on pool for metrics related to the protocol balance on pool.
