# Funding Risks

Neutrl uses perpetual futures contracts to hedge the delta in both OTC and funding arbitrage components. Perpetual futures contracts are subject to **Funding Rate**, where payments are exchanged between long and short position holders to maintain price alignment between the perpetual contract and the spot market.

**Funding Risk** arises when the funding rates become persistently negative (i.e., the protocol must pay funding rather than receive it). This can impact the profitability of the strategy and potentially reduce the protocol's overall revenue.

While this is a risk to strategy profitability, historical data shows that periods of negative funding rarely persist, and show mean-reverting characteristics.

#### **Risk Mitigation Measures**

1. **Dynamic Allocation of TVL**:
   * The protocol dynamically shifts capital between OTC/Secondary deals and funding arbitrage.
   * During periods of negative funding, the protocol will shift allocation to arbitrage pairs exhibiting positive funding, or in the case of market stresses, shift to yield-bearing stablecoins to minimize impact on protocol yield.
   * Conversely, during periods of favorable funding, TVL is allocated to arbitrage pairs exhibiting high positive funding to maximize yield.
2. **Reserve Fund**:
   * A reserve fund is maintained to absorb losses during occasional periods of negative funding.
   * The reserve fund is capitalized using a portion of protocol revenue generated during periods of strong positive funding.
3. **Historical Behavior of Funding Rates**:
   * Funding rates for major assets (e.g., BTC, ETH) have historically shown a **mean-reverting, positively biased trend**.
   * Analysis of data over the past three years indicates that negative funding periods are typically short-lived, and the annualized average funding rate remains positive (\~7.8% for BTC and \~9.15% for ETH).
4. **Hedging Funding Exposure**:
   * The protocol can hedge funding rate exposure by taking positions in alternative derivative instruments, such as calendar futures with fixed funding.
5. **Real-Time Monitoring and Adjustment**:
   * Funding rates across exchanges are monitored in real-time.
   * Positions are adjusted dynamically to take advantage of exchanges offering the most favorable funding.
