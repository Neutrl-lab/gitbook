# Peg Mechanism

Maintaining Stability: The Foundation of NUSD

Ensuring a stable peg is critical to the reliability and utility of NUSD. The protocol employs arbitrage-driven mechanisms to maintain NUSD’s $1 peg, even during periods of market volatility. This system works alongside a direct 1:1 redemption feature for major stablecoins, providing a robust and reliable foundation for price stability.

**Arbitrage as a Stabilizing Force**

Arbitrage serves as a cornerstone of NUSD’s price stability. When the price of NUSD deviates from $1 in external markets, arbitrageurs step in to profit from these discrepancies by minting or redeeming NUSD directly through the protocol. This process naturally realigns NUSD’s market price with its $1 target by adjusting supply and demand dynamics.

In addition to arbitrage, the protocol ensures NUSDs stability through its **1:1 USD redeemability for stablecoins**, which provides consistent liquidity and price confidence. Users can redeem NUSD at any time, ensuring that its inherent value is always backed by the stability of stablecoin reserves.

***

**Arbitrage Scenarios**

There are two primary scenarios where arbitrage and the 1:1 redeemability mechanism work together to maintain the peg:

1. **NUSD Trades Below $1 in External Markets**:
   * If NUSD is priced below $1 on an external market, an arbitrageur can:
     1. Purchase NUSD at the discounted price ($0.95) on the external market.
     2. Redeem the purchased NUSD directly through the protocol at its full value of $1, receiving USDC.
     3. Realize a profit from the price difference.
   * This activity reduces the supply of NUSD in circulation, helping restore its price to the $1 peg.
2. **NUSD Trades Above $1 in External Markets**:
   * If NUSD is priced above $1 on an external market, an arbitrageur can:
     1. Mint NUSD directly from the protocol using USDC at the fixed 1:1 USD ratio.
     2. Sell the newly minted NUSD on the external market at the higher price ($1.05).
     3. Profit from the price difference.
   * This activity increases the supply of NUSD in circulation, driving its price back toward $1.

***

**Backing and Liquidity Management**

* NUSD is fully backed by a diversified portfolio of assets, with a portion held in major stablecoins to facilitate **1:1 redemptions**.
* A fraction of the reserves (e.g., 0.50%) is held directly in the mint-and-redeem contract to enable immediate redemptions, while the protocol systematically replenishes this balance from the broader reserve pool.
* This ensures that NUSD holders can always redeem their tokens for stablecoin, providing liquidity and stability even during periods of heightened redemption activity.

***

**Market Resilience**

The 1:1 redeemability of NUSD for USD equivalent in stablecoins ensures that the NUSD's value remains unaffected by temporary liquidity shocks or price dislocations in external markets. This feature, combined with arbitrage incentives, creates a self-correcting system that maintains NUSD's peg during periods of high demand or volatility.

***

**Key Benefits of the Peg Mechanism**

1. **Guaranteed Redeemability**:
   * NUSD holders can always redeem their tokens 1:1 (in USD value) for stablecoin, ensuring confidence in the token’s intrinsic value.
2. **Self-Stabilizing System**:
   * Arbitrage opportunities incentivize users to restore NUSD's price to its peg, without requiring active intervention by the protocol.
3. **Liquidity Assurance**:
   * Systematic management of stablecoin reserves ensures that redemptions occur seamlessly, even during periods of high activity.
4. **Market Efficiency**:
   * The protocol supports minting and redeeming on demand, encouraging arbitrage activity across centralized and decentralized markets to maintain price parity.
5. **Resilience in Volatility**:
   * The combination of reserve backing, liquidity management, and arbitrage mechanisms ensures stability even in volatile market conditions.
