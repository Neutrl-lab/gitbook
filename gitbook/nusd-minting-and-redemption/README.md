# NUSD Minting & Redemption&#x20;

Neutrl's NUSD is not the same as a fiat stablecoin like USDC or USDT. NUSD is a synthetic dollar, backed with crypto assets, liquid synthetic dollars and corresponding short futures positions. This means that the risks implicated by interacting with NUSD are inherently different. Please refer to our extensive “Risks Section” (Insert hyperlink - https://docs.neutrl.fi/risks) for more information.

### Minting & Redemption Overview

The NUSD minting and redemption system employs a modular architecture centered on `Router` as the primary interface. Users deposit collateral to mint NUSD or burn NUSD to redeem collateral, with all assets secured in `AssetReserve`. From `AssetReserve`, designated custodians wallet (Fireblocks, Copper) can settle assets off-chain to execute trading strategies.

&#x20;Specialized `Minter` and `Redeemer` contracts handle asset-specific logic while maintaining standardized flows. The system features dual redemption paths—instant and queued—ensuring continuous liquidity access regardless of reserve conditions. This design enables flexible multi-collateral support with consistent security and operational efficiency.
