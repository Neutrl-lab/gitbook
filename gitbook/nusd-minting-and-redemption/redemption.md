# Redemption

The redemption system provides two execution paths based on AssetReserve liquidity availability, ensuring users maintain continuous access to their collateral.



<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

#### Instant Redemption

The primary redemption path, executed when AssetReserve holds sufficient collateral to immediately fulfill requests.

**Process Flow**

**1. Initiation**

* User calls `redeem()` on Router.sol with parameters:
  * NUSD amount to redeem
  * Desired collateral asset
  * Beneficiary address

**2. Liquidity Verification**

* Router queries AssetReserve liquidity status
* Executes `quoteRedemption()` to validate collateral availability
* Routes to appropriate Redeemer contract upon confirmation

**3. Valuation & Calculation** The Redeemer contract  performs:

* Fair market value determination for NUSD-to-collateral conversion
* Output calculation considering:
  * **Slippage protection**: `order.collateralAmount` as minimum output
  * **Rate limiting**: Enforces `maxRedeemPerBlock` constraints

**4. NUSD Burning**

* Redeemer executes `burn()` on NUSD.sol contract
* User's NUSD removed from total supply
* Transaction atomically reduces circulating NUSD

**5. Collateral Release**

* Router calls `processRedemption()` on AssetReserve
* Collateral transfers to beneficiary address



#### Queued Redemption

Alternative path activated when requested collateral temporarily exceeds available AssetReserve liquidity.

**Process Flow**

**1. Initiation & Liquidity Assessment**

* User initiates standard redemption via Router.sol
* Router detects insufficient collateral for immediate execution

**2. Request Queuing**

* User's NUSD transferred to Router contract for custody
* Router generates redemption Order with:
  * Unique request ID (auto-incremented)
  * Status: `PENDING`
  * Storage in `redemptionRequests` mapping

**3. Keeper Monitoring** Authorized keepers (REDEMPTION\_KEEPER\_ROLE) monitor and execute:

* Track AssetReserve liquidity replenishment
* Identify serviceable pending requests
* Call `serveRedemptionRequest()` with request ID

**4. Deferred Execution** Upon keeper activation:

* Router retrieves queued Order details
* Executes standard redemption flow using custodied NUSD
* Redeemer performs oracle valuation and burning
* AssetReserve releases collateral to original beneficiary
* Updates request status to `COMPLETED`



#### System Guarantees

This dual-path architecture ensures:

* **Liquidity Efficiency**: Instant redemptions when possible
* **Redemption Certainty**: Queued system guarantees eventual execution
* **Transparency**: All pending requests tracked on-chain
* **Protocol Stability**: Rate limits prevent liquidity runs

The system prioritizes user experience while maintaining protocol solvency, creating a robust redemption infrastructure that adapts to varying liquidity conditions.

