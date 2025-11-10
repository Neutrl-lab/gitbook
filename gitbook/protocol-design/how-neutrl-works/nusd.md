# NUSD

NUSD is a synthetic dollar backed by a diversified portfolio of yield bearing crypto-native assets as well as optimised liquid basis positions.

## Minting NUSD

Currently NUSD minting is via a permissionless process.  NUSD is minted by depositing liquid assets, such as USDC, USDT or USDe, on 1:1 dollar value basis.&#x20;

NUSD can also be bought on the secondary market via different liquidity venues.&#x20;

## Redeeming NUSD&#x20;

Approved KYB/KYC counterparties may redeem NUSD for backing assets (USDC, USDT, or USDe) at a 1:1 USD value basis. Upon redemption, the protocol burns the corresponding NUSD tokens and transfers the equivalent value in the selected backing asset to the user. Currently NUSD redemptions are only open to users who have passed relevant KYC procedures with the protocol.

#### Liquidity Management

The protocol employs a dynamic liquidity management system through the `AssetReserve` contract, optimizing between capital efficiency and redemption availability.

**Instant Redemptions**

The AssetReserve maintains a dynamically calibrated liquid buffer designed to serve immediate redemption requests. When the requested redemption amount falls within the available buffer capacity, transactions are processed instantly with no delays.

**Queued Redemptions**

For redemption requests exceeding the current liquid buffer:

* The protocol generates a redemption request and adds it to the processing queue
* All queued requests aim to be fulfilled within a 48-hour processing window but is not guaranteed
* Users retain full visibility of their redemption status throughout the process





