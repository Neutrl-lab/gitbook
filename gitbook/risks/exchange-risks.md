# Exchange Risks

The protocol relies on centralized and decentralized exchanges (CEX and DEX) to execute its **funding arbitrage** and **hedging activities**. Centralized exchanges are critical for trading perpetual futures, while decentralized exchanges provide additional liquidity and arbitrage opportunities.

**Exchange Risk** arises when these venues experience operational disruptions, financial insolvency, regulatory crackdowns, or other failures that prevent the protocol from executing trades, settling positions, or accessing funds. Such events can lead to:

* Losses due to the inability to settle positions.
* Exposure to unrealized profits or collateral trapped on an exchange.
* Disruptions in hedging activities, potentially leaving the protocol unhedged against market volatility.

***

#### **Sources of Exchange Risk**

1. **Insolvency or Bankruptcy**:
   * Centralized exchanges may become insolvent due to poor financial management, hack-related losses, or external market events.
   * Examples include the collapse of FTX and Mt. Gox, which led to significant losses for users whose funds were trapped.
2. **Operational Failures**:
   * Exchanges may experience outages, degraded performance, or data inaccuracies during periods of high market volatility, preventing trades or liquidations from being executed in a timely manner.
3. **Regulatory Risks**:
   * Exchanges are subject to regulatory actions, including license revocations, trading restrictions, or asset freezes, which can impact users' ability to access funds.
   * For example, regional bans on certain exchanges or assets may prevent the protocol from maintaining positions or withdrawing collateral.
4. **Custodial Risks**:
   * Funds deposited directly on exchanges remain under custodial control of the exchange, leaving them vulnerable to mismanagement, fraud, or loss in the event of exchange failure.
5. **Liquidity Risks**:
   * Thin order books or a sudden drop in exchange liquidity can create slippage and impact trade execution, especially for large positions.
6. **Smart Contract Risks (DEX-Specific)**:
   * Decentralized exchanges rely on smart contracts, which may be exploited, malfunction, or experience downtime, leading to losses or the inability to execute trades.

***

#### **Risk Mitigation Measures**

**1. Off-Exchange Settlement**

* Protocol assets are not fully deposited on centralized exchanges. Instead, **off-exchange settlement providers** (e.g., Copper's Clearloop, CEFFU's MirrorX) are used to custody assets and minimize direct exposure to exchange custodial risks.
* These providers facilitate non-custodial trading workflows, allowing the protocol to execute trades without transferring full ownership of the collateral to the exchange.

**2. Diversification Across Exchanges**

* The protocol spreads trading activity across multiple exchanges to reduce reliance on any single venue.
* Strict concentration limits are enforced to ensure that no single exchange exceeds a predefined percentage of the protocol’s trading activity or collateral exposure.
* Exchanges are evaluated based on their financial health, liquidity, regulatory compliance, and operational reliability.

**3. Real-Time Monitoring**

* The protocol continuously monitors exchange solvency, operational performance, and market conditions.
* Factors monitored include:
  * Exchange reserve transparency and proof-of-reserves data (where available).
  * Trade execution performance and latency.
  * Regulatory developments affecting specific exchanges or jurisdictions.
* If an exchange shows signs of trouble (e.g., withdrawal delays, regulatory scrutiny, or significant reserve outflows), the protocol reduces or closes positions on that exchange.

**4. Frequent Settlement of PnL**

* Unrealized profits and losses (PnL) are settled frequently to prevent large balances from accumulating on any one exchange.
* Settlement cycles are determined based on the operational characteristics of each exchange (e.g., daily settlement on Binance and Deribit, hourly settlements on Bybit).

**5. Failover Mechanisms**

* In the event of an exchange failure, the protocol employs failover mechanisms to reallocate positions and maintain hedging activities.
* Failover actions include:
  * Transitioning open positions to alternative exchanges with sufficient liquidity.
  * Using alternative instruments, such as deliverable futures or decentralized derivatives, to maintain hedges.
  * Adjusting portfolio allocations to reduce reliance on derivatives temporarily.

**6. Stress Testing and Contingency Planning**

* The protocol conducts regular stress tests to simulate exchange failure scenarios, such as:
  * Abrupt insolvency of a major exchange.
  * Withdrawal freezes or delays.
  * Market-wide liquidity crises.
* Contingency plans are developed based on the results of these tests to ensure the protocol remains operational under adverse conditions.
