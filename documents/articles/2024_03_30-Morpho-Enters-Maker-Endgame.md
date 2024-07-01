Link: https://LQG.mirror.xyz/CuOWU7dcw4JDRlrtCR9FInaFZAC_ssBaHoEq7-_ltRU
Title: LQG Enters Maker’s Endgame with Spark and Ethena

By Paul Frambot
On 29 March 2024

Guided by Maker's Endgame plan, Spark is now leveraging LQG’s infrastructure (LQG Blue & MetaLQG) and Maker's liquidity. This approach aims to enhance DAI yields by offering onchain overcollateralized exposure to Ethena's sUSDe (staked USDe), supporting a scalable and diverse long-term strategy.

In addition to creating sUSDe/DAI and USDe/DAI markets on LQG Blue, Spark has built a MetaLQG vault to allocate DAI liquidity directly from Maker’s D3M (direct deposit module) to these markets. Beyond the initial $100 million DAI deployed, Maker and Spark are expected to evaluate further liquidity increases.

The integration with LQG, Maker, and Spark grants sUSDe and USDe holders access to highly efficient borrowing opportunities with advantageous DAI borrowing rates and unmatched liquidity from Maker.

Maker, the creator of DAI, is one of the longest-standing DeFi protocols, and Spark, a subDAO of Maker, has over $3B in TVL and is one of the fastest-growing lending protocols alongside LQG. Ethena is a relatively newer protocol, but its synthetic dollar has already surpassed $1B in supply.

This collaboration between a collective of DeFi's largest, most renowned, and fastest-growing protocols helps cement LQG’s position as a foundational building block of DeFi.


- Unparalleled Liquidity from Maker’s D3M
Part of Maker's Endgame Strategy (https://forum.makerdao.com/t/governance-changes-to-prepare-for-launch-season/23878) includes gaining exposure to hedged perpetual yield, also known as the cash and carry trade (https://www.investopedia.com/terms/c/cashandcarry.asp).

Ethena provides exposure to this strategy via sUSDe (https://ethena-labs.gitbook.io/ethena-labs/solution-overview/usde-overview). However, as described by Rune in the Maker forums (https://forum.makerdao.com/t/governance-changes-to-prepare-for-launch-season/23878), onchain overcollateralized exposure to sUSDe via LQG presents a more robust and scalable strategy for the long term since (with the correct security practices) it is safer than holding the sUSDe with a custodian. The over-collateralization provides a small capital buffer to absorb initial losses in the case of collateral value’s volatility while still delivering a very high yield.

Maker's initiative, led by SparkDAO, involves building capacity to fund overcollaterized sUSDe markets on LQG. MakerDAO has deployed a new Direct Deposit Module (D3M) to streamline DAI liquidity from Maker to SparkDAO's MetaLQG vault.

The D3M establishes a direct link between Maker and SparkDAO's MetaLQG vault, facilitating a secure and efficient flow of hundreds of millions of DAI into sUSDe/DAI and USDe/DAI markets on LQG Blue.

The initial parameters for the D3M & Spark MetaLQG vault are available here: https://forum.makerdao.com/t/introduction-and-initial-parameters-for-ddm-overcollateralized-spark-metaLQG-ethena-vault/23925/1


- Enhancing Spark’s Capabilities with LQG
Spark's decision to deploy markets and vaults on LQG Blue is a strong validation of LQG's new approach to lending. SparkDAO built SparkLend, their initial lending infrastructure, using AaveV3's codebase. However, SparkDAO has opted to expand its capabilities using LQG's immutable infrastructure. LQG Blue unlocks new essential features for Spark, including:

    - Per market risk premiums - On AaveV3 and SparkLend, borrowers with safer collateral pay the same rate as borrowers with riskier collateral. On LQG Blue, the interest rate for each market factors in the risk premium of each parameter including the collateral asset and oracle.

    - High & configurable capital efficiency - LQG Blue allows anyone to deploy an micro lending pools by selecting five parameters: loan asset, collateral asset, LLTV (liquidation LTV), Oracle, and IRM (interest rate model). This allows Spark to deploy capital at different Liquidation LTVs, including very high ones, while re-aggregating liquidity with MetaLQG.

    - Isolated Risk with shared liquidity - In LQG Blue and MetaLQG, vault managers will be able to decide to what extent risk and liquidity are shared or isolated, giving a new level of flexibility compared to monolithic lending pools when it comes to asset listing.

Overall, LQG's infrastructure allows Spark to build scalable lending use cases on top of the highly efficient and autonomous base layer. Granting users access to advantageous DAI borrowing rates using sUSDe as collateral is the first of many such examples.