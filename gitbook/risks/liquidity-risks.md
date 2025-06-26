# Liquidity Risks

Liquidity risk refers to the protocol's ability to meet redemption requests without negatively impacting the value of the portfolio. This risk is exacerbated by the mix of illiquid (OTC/Secondary deals) and liquid (funding arbitrage) assets in the portfolio.

The illiquid nature of OTC/Secondary deals means that these positions ideally should be held to maturity. In order to meet redemption requests, the protocol must align its asset allocation with the duration of liabilities.

#### **Risk Mitigation Measures**

1. **Liability-Driven Allocation**:
   * The protocol matches the liquidity profile of assets with the duration of liabilities.
   * Short-term deposits are allocated to funding arbitrage, while longer-term deposits are allocated to OTC/Secondary deals.
2. **Liquidity Buffers**:
   * A majority of the TVL is held in liquid assets (e.g., stablecoins or funding arbitrage positions) as a buffer to handle unexpected redemption requests.
3. **Stress Testing**:
   * The protocol conducts regular stress tests to simulate extreme market conditions and assess the liquidity of the portfolio.
   * Stress tests account for scenarios such as sudden mass redemptions or temporary market disruptions.
4. **Redemption Limits**:
   * To protect the protocol from liquidity shortfalls, redemption requests may be queued or capped during periods of extreme market stress.
   * Redemption limits are designed to ensure the solvency of the protocol while minimizing disruption to users.
5. **Portfolio Rebalancing**:
   * Positions are rebalanced periodically to ensure the portfolio remains aligned with liability maturities.
   * This includes reallocating capital from funding arbitrage to OTC/Secondary deals (or vice versa) based on liquidity needs.
6. **Secondary Market Liquidity**:
   * The protocol has access at all times to the secondaries market to unwind illiquid positions through partnerships with leading secondaries brokerages and exchanges

