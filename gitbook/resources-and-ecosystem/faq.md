# FAQ

### General Questions

#### 1. How is this protocol different from other stablecoins, like Usual or Ethena?

* Yield is derived primarily from OTC Locked Tokens, where the delta is fully hedged
* The remainder of the portfolio is deployed to liquid strategies to maintain sufficient liquidity buffer in times of capital stress

#### 2. How can I trust that NUSD will maintain the Stablecoin peg?

* NUSD maintains its peg through **delta-neutral strategies**, **on-chain transparency**, and **overcollateralization**:
  * **Delta-Neutral Hedging**: Derivatives and perpetual futures offset directional risk, keeping NUSD stable during market volatility.
  * **OTC Discounts**: Discounted OTC asset purchases provide a safety margin, supporting the peg even in challenging conditions.
  * **Duration Matching**: The protocol aligns asset and liability durations to ensure sufficient liquidity for redemptions.
  * **Liquid Reserves**: Stablecoins (e.g., USDT, USDC, USDe) and liquid delta-neutral positions back NUSD, maintaining stability under stress.

#### 3. How is NUSD backed, and how do I know it's secure?

* NUSD is fully backed by a diversified portfolio of assets designed to provide security, transparency, and resilience
* **Portfolio Composition**:\
  NUSD is backed by a mix of:
  * **OTC-acquired crypto assets**: Purchased at significant discounts, providing a higher margin of safety.
  * **Stablecoins (e.g., USDT, USDC, USDe)**: Highly liquid and composable within DeFi and CeFi ecosystems.
  * **Delta-Neutral Positions**: Liquid positions that generate yield while mitigating directional risk.
* **Transparency**:
  * All assets are confirmed using a combination of ZK-proofs, custodian attestations, and third party audits
* **Risk Management Framework**:
  * The protocol employs a robust risk management framework that includes stress testing, margin monitoring, and proactive position adjustments to protect the backing assets and ensure their security.
  * For more information, see [Risks](../risks/)

#### 4. What happens if NUSD loses its peg?

* If NUSD temporarily loses its peg, the protocol has several mechanisms in place to restore stability:
  * **Market Incentives**:\
    Arbitrage opportunities naturally arise when NUSD deviates from its peg, incentivizing traders and market makers to buy or sell NUSD and redeem against USDC 1:1 to bring its price back in line with its intended value. See [Peg Mechanism](../how-it-works/peg-mechanism.md)
  * **Delta Hedging Adjustments**:\
    The protocol adjusts its derivatives and perpetual futures positions to rebalance the collateral portfolio and stabilize NUSD's value.
  * **Reserve Deployment**:\
    Liquid reserves, including stablecoins and delta-neutral positions, can be rapidly deployed to support the peg and meet redemption demands.
  * **Proactive Adjustments to Backing**:\
    If market conditions are extreme, the protocol may temporarily scale down exposure to volatile assets or rebalance its portfolio to prioritize stability over yield.
* The combination of these measures ensures that NUSD can recover its peg efficiently, even during periods of high market volatility.

#### 5. Isn't the Locked Token Funding Pool risky since the investments are illiquid?

* While the locked token strategy involves longer-term, illiquid investments, the protocol mitigates these risks through careful design, liquidity management, and diversification:
  * **OTC Discounts**: Locked tokens are purchased at discounts, providing a safety margin even in adverse markets.
  * **Delta-Neutral Hedging**: Market risk is reduced through hedging strategies, limiting exposure to price fluctuations.
  * **Diversified Portfolio**: Locked tokens are balanced with liquid assets like stablecoins and delta-neutral positions, ensuring operational liquidity.
  * **Secondary Market Access**: Partnerships with OTC brokers and secondary markets enable asset liquidation to generate additional liquidity.
* For more information, see [Liquidity Risks](../risks/liquidity-risks.md)

#### 6. What will happen if there's a flight to safety and users mass redeem NUSD?

* In the event of a mass redemption (e.g., during periods of extreme market stress), the protocol has mechanisms in place to manage liquidity and protect NUSD holders:
  * **Liquid Reserves**:\
    A portion of the protocol’s backing assets consists of liquid stablecoins (e.g., USDT, USDC, USDe) and delta-neutral positions. These reserves can be quickly deployed to meet redemption requests.
  * **OTC Discounts Provide Cushion**:\
    The discounted cost basis of OTC-acquired assets ensures that the protocol’s collateral has a higher margin of safety, even if some assets are sold under stressed conditions.
  * **Gradual Unwind of Positions**:\
    In the event of a liquidity crunch, the protocol can gradually unwind positions to avoid unnecessary slippage or losses.
  * **Dynamic Hedging Adjustments**:\
    The protocol’s delta-neutral strategies are designed to adapt to changing market conditions, helping to stabilize the collateral portfolio during periods of heightened redemption activity.
  * **Reserve Fund Support**:\
    The protocol’s reserve fund acts as a safety net, providing additional liquidity to meet redemption demands and maintain market confidence.
* While a mass redemption scenario represents an extreme stress test, the protocol’s focus on liquidity, diversification, and risk management ensures it can respond effectively without compromising USDn’s stability or long-term viability.

### Tokenomics and Incentives

#### 1. What is the purpose of the NTRL token?

The **NTRL token** is the core governance and value-accrual asset of the Neutrl protocol. It plays a multi-faceted role:

* **Governance:** NTRL holders govern key protocol parameters, including yield allocation, risk thresholds, collateral types, insurance pool management, and product expansion decisions.

### Security and Risk Management

#### 1. How do you ensure the protocol is secure from exploits or hacks?

*   **Audits by Top-Tier Firms**

    All smart contracts powering Neutrl — including minting, redemption, staking, and collateral management — are audited by **independent security firms** prior to deployment. Additional audits are conducted with each major upgrade.&#x20;
* **Modular, Minimally Permissive Architecture modular, battle-tested frameworks**                                                                                     Contracts are built using  with strict access controls and minimal privileges. Wherever possible, **immutable contracts** or time-locked upgrade paths are used to limit attack surfaces and governance abuse.
* **Off-Exchange Custody & Segregation**                                                                                                       Assets deployed to exchanges for hedging are managed through **segregated, monitored accounts** with **read-only API keys** and **withdrawal restrictions**, reducing centralised risk vectors.
* **Real-Time Monitoring & Risk Parameters**                                                                                                   The protocol continuously monitors margin ratios, funding rate shifts, and position health. **Automated risk guards** are built into the system to prevent overexposure or cascading liquidations during volatile market conditions.
* **Bug Bounties & White Hat Engagement**                                                                                                 Before public mainnet launch Neutrl will launch a **public bug bounty programme** to incentivise ethical hackers to discover and responsibly disclose vulnerabilities.&#x20;
* **Transparency and Response Planning**                                                                                                     In the unlikely event of a vulnerability, the Neutrl team is prepared with a **pre-coordinated incident response plan**, including governance pause functions, user communication protocols, and asset safeguarding procedures.

#### 2. What happens if the collateral value drops significantly?

*   If collateral value drops significantly, the protocol mitigates risk through:

    * **Overcollateralization**: Assets are secured with significant safety margins, with OTC-acquired discounts providing additional protection.
    * **Dynamic Hedging**: Derivatives are used to neutralize directional risk and stabilize the portfolio value.
    * **Reserve Deployment**: Liquid reserves, including stablecoins, are deployed to support NUSD’s peg and meet redemptions.
    * **Portfolio Rebalancing**: Allocations are adjusted to prioritize stability during downturns.
    * **Stress Testing**: Regular simulations ensure collateral buffers can withstand extreme market conditions.

    These measures ensure the protocol remains resilient even during severe market volatility.

#### 3. How do you manage counterparty risk for token purchases?

* The protocol minimizes counterparty risk in OTC purchases through:
  * **Due Diligence**: Counterparties are vetted for AML/KYC compliance, financial health, and reputation.
  * **Enforced Delivery**: Smart contracts, escrow mechanisms, or collateralized deals ensure token delivery.
  * **Diversification**: Transactions are spread across multiple counterparties to limit exposure.
  * **Legal Safeguards**: Binding agreements include enforcement measures in case of default.
* For more details, see [Counterparty Risks](../risks/counterparty-risks.md)

#### 4. How do you manage exchange counterparty risk?

* Exchange risk is mitigated by:
  * **Off-Exchange Settlement**: Providers like Copper’s Clearloop custody assets off exchanges, reducing custodial risk.
  * **Diversification**: Trading activity is spread across multiple exchanges with strict concentration limits.
  * **Real-Time Monitoring**: Exchange solvency and operational health are actively tracked, with positions adjusted if risks emerge.
  * **Frequent PnL Settlement**: Unrealized profits are regularly settled to minimize funds left on exchanges.
  * **Failover Mechanisms**: If an exchange fails, positions are reallocated to other venues or instruments.
* For more details, see [Exchange Risks](../risks/exchange-risks.md)

#### 5. How do you manage liquidation risk?

* Liquidation risk is managed through:
  * **Leverage Limits**: Conservative leverage limits (max 2x) reduces the likelihood of margin calls.
  * **Overcollateralization**: Margin buffers ensure positions remain secure during volatility.
  * **Dynamic Monitoring**: Real-time tracking of margin levels allows proactive collateral deployment.
  * **Position Diversification**: Positions are spread across exchanges to avoid concentration risks.
  * **Stress Testing**: Simulations prepare for extreme market scenarios.
  * **Reserve Fund Support**: Liquid reserves are available for margin top-ups during stress events.
  * **24/7 Oversight**: A global trading team ensures rapid intervention when needed.
* For more details, see [Margin Risks](../risks/margin-risks.md)

### Transparency and Governance

#### 1. How can users trust the team and the protocol?

Neutrl is built on the principles of **transparency, accountability, and verifiable performance**. Trust is earned through:

* **On-chain transparency:** All critical contract interactions — including minting, redemptions, staking, collateral management, and strategy performance — are visible and auditable on-chain.
* **Off-exchange custody controls:** The protocol uses verifiable custody arrangements for assets held on exchanges, with risk parameters enforced by smart contracts.
* **Credible backing:** The team is supported by respected investors and advisors from across DeFi, trading, and institutional markets.
* **Experienced team:** Neutrl is led by individuals with backgrounds in high-frequency trading, portfolio management, OTC structuring, and DeFi protocol architecture.

Over time, the protocol will progressively decentralise through **on-chain governance**, enabling the community to shape and secure Neutrl’s evolution.

#### 2. How are governance decisions made?

Governance is powered by the **NTRL token**, with holders able to propose and vote on protocol changes, including:

* Yield allocation and incentive design
* Risk parameters and treasury management
* New collateral types or strategy integrations
* Treasury spending and ecosystem grants
* Insurance fund deployments and backstop mechanisms

Proposals may initially go through a **community discussion phase**, followed by a formal **on-chain vote** via a governance interface (to be launched post-TGE).

In the early stages, a **core governance council** will ensure operational stability, with progressive transition toward full community governance as NTRL is distributed more widely.

#### 3. What transparency information do you provide? How do you ensure the accuracy of this information?

Neutrl provides real-time, public access to key protocol data:

* **Strategy dashboards**: Showing live performance of OTC arbitrage and hedged positions
* **Collateral composition**: Breakdown of NUSD backing assets and their risk profiles
* **Protocol revenues and fees**: Real-time and historical earnings from funding, arbitrage, and spreads
* **TVL and user activity**: Usage metrics, staking, mint/redeem flows, and PLP participation

All data is **on-chain where possible** and supplemented by **off-chain attestations** (e.g. exchange custody balances, OTC deal documentation).

Accuracy is ensured through:

* **Third-party audits** of smart contracts and risk models
* Use of **reputable oracles and indexers** for pricing and position tracking
* Eventual implementation of **proof-of-reserve frameworks** for off-chain holdings

Trust in DeFi must be earned — and at Neutrl, transparency is not an option, it’s foundational.
