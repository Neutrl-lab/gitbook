# NUSD Minting & Redemption&#x20;

### Minting & Redemption Overview

The NUSD minting and redemption system employs a modular architecture centered on `Router` as the primary interface. Users deposit collateral to mint NUSD or burn NUSD to redeem collateral, with all assets secured in `AssetReserve`. From `AssetReserve`, designated custodians wallet (Fireblocks, Copper) can settle assets off-chain to execute trading strategies.

&#x20;Specialized `Minter` and `Redeemer` contracts handle asset-specific logic while maintaining standardized flows. The system features dual redemption paths—instant and queued—ensuring continuous liquidity access regardless of reserve conditions. This design enables flexible multi-collateral support with consistent security and operational efficiency.
