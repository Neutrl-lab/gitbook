# Portfolio Allocation

The protocol’s portfolio is strategically allocated to balance liquidity, yield generation, and risk management. This allocation ensures the stability of NUSD while maximizing returns for sNUSD stakers. The portfolio can be divided into three main categories:

**1. Liquid Reserves (Stablecoins and Yield-Bearing Instruments)**

* **Allocation**:\
  A portion of the portfolio is held in highly liquid stablecoins (e.g., USDC, USDT, USDe) and yield-bearing stablecoins.
* **Purpose**:
  * Provides immediate liquidity to ensure NUSD holders can redeem at any time.
  * Funds the **base yield** distributed to sNUSD.
* **Risk Profile**:\
  These assets are lower-risk and highly liquid, ensuring the protocol can meet redemption demands and maintain stability during periods of market stress.

***

**2. Hedged OTC Positions (Discounted Assets)**

* **Allocation**:\
  The protocol allocates a portion of its portfolio to acquire crypto assets at a discount through OTC deals.
* Locked tokens are hedged to eliminate price risk, and the protocol may strategically sell or stake these assets to capture additional yield.
* **Risk Profile**:\
  While OTC positions carry slightly higher risk due to market and liquidity factors, the protocol mitigates this through diversification, hedging, and careful risk management.

***

**3. Delta-Neutral Yield Strategies**

* **Allocation**:\
  A portion of the portfolio is deployed in delta-neutral strategies, such as:
  * Perpetual futures funding arbitrage.
  * Basis trading (e.g., capturing spreads between spot and futures markets).
* **Purpose**:
  * Generates consistent, low-risk yield by exploiting inefficiencies in derivatives markets.
  * Ensures a steady stream of revenue without exposing the portfolio to directional price risk.
* **Risk Profile**:\
  These strategies are market-neutral and designed to minimize exposure to volatile price movements, making them a reliable source of yield, while still being liquid enough to meet redemptions.

***

#### Duration Matching Approach

<div align="center" data-full-width="true"><figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption><p> Illiquid OTC assets may be selected with matched durations based on known maturities of liabilities, increasing profitability and reducing liquidity crunch risk </p></figcaption></figure></div>

A fundamental principle of the protocol is ensuring that liabilities are duration-matched with the assets it holds. This “duration match” works alongside over-collateralization and capital buffers as a key safety mechanism for the protocol. The benefits are clear:

* **Reduces Forced Selling:** By aligning the maturity of liabilities with assets, the protocol avoids the need to sell positions at a discount during redemptions. This eliminates fire-sale risks, ensuring stability even during high withdrawal periods.
* **Regulatory Compliance:** Supervisors, auditors, and potential partners view a lower weighted-average maturity gap as a safer structure. This enhances the protocol’s credibility, paving the way for partnerships, regulatory approvals, and increased TVL growth.
* **Optimizes Capital Efficiency:** With redemptions funded by maturing assets, Neutrl can maintain a leaner cash buffer and deploy more capital into productive trades—boosting net yields for sNUSD holders.

As users roll their positions from one lock to the next, the protocol re-ladders its assets - closing matured positions and reallocating capital into new positions further along the curve. In cases where inflows and outflows are not perfectly synchronized, the protocol may allocate a portion of shorter-term assets (e.g., a 6-month position) into the next tenor (e.g., a 9-month trade). This ensures continuity in the ladder while avoiding idle capital drag.

While this approach may lead to some bunching of redemptions further down the line, the protocol has mechanisms in place to mitigate this risk. Immediate liquidity from secondary markets and third-party credit lines can alleviate potential redemption queues (see Redemption section for details).

The result: **higher, more sustainable yields for sNUSD holders and faster, more reliable redemptions for NUSD users.**

***

**Dynamic Allocation Strategy**

The protocol employs a **dynamic allocation strategy** to adapt to changing market conditions and optimize risk-adjusted returns. Key principles include:

1. **Liquidity Prioritization**:
   * A percentage of the portfolio is always allocated to liquid reserves to ensure the protocol can meet redemption demands.
   * The overall portfolio is duration matched to the protocol's underlying liabilities
2. **Yield Optimization**:
   * The protocol balances short-term, liquid investments (e.g., yield-bearing stablecoins) with higher-yield, longer-term investments (e.g., OTC positions and delta-neutral strategies).
3. **Risk Management**:
   * Assets are diversified across multiple strategies to reduce concentration risk.
   * Hedging is employed to manage risks associated with locked tokens and market positions.
4. **Treasury Growth**:
   * Some portion of yields are retained in the reserve fund, allowing the protocol to strengthen its financial stability for times of market stress

**Putting the Philosophy into Practice**

Crypto markets swing from fear to euphoria faster than any traditional markets. This volatility demands a nimble and adaptive allocator. Neutrl's strategy is designed to respond dynamically to changing market conditions:

* **OTC Sleeve:** Deal flow is highly opportunistic. In some weeks, attractive 6- or 9-month deals may surface; in others, suitable opportunities may be scarce. The protocol only deploys into positions when returns exceed our risk-adjusted hurdle rate and aligns with the duration ladder. If no suitable deals are available, we simply wait.
* **Liquid strategy:** Capital is deployed only when the expected return beats both the cash-equivalent yield-bearing rate benchmark and the internal excess-return target. This ensures protocol safety by preserving over-collateralization, liquidity buffers, and minimal weighted-average maturity gaps.

Because the liability curve is constantly evolving - users can roll, extend, or redeem - the allocation engine continuously rebalances. Buckets that shrink are allowed to roll off, while buckets that grow are funded by closing surplus trades. If the market offers favourable spreads, new positions may be opened further out on the curve.

The result is an allocation strategy that adapts to the protocol’s liabilities in real time—remaining liquid and defensive during bearish conditions, while maximizing opportunities during bullish markets.

<figure><img src="../.gitbook/assets/telegram-cloud-photo-size-4-5951673806160512769-y.jpg" alt=""><figcaption><p>Assets backing NUSD/sNUSD adapt dynamically based on prevailing market conditions and yield opportunities </p></figcaption></figure>



***

#### **Example Portfolio Allocation Breakdown**

Below is an example of how the protocol might allocate its portfolio under normal market conditions:

| **Asset Category**                      | **Allocation (% of Portfolio)** | **Purpose**                                  |
| --------------------------------------- | ------------------------------- | -------------------------------------------- |
| Liquid Reserves (Yield-bearing Dollars) | 20%                             | Ensures liquidity and base yield.            |
| Hedged OTC Positions                    | 20%                             | Generates revenue via discounts and staking. |
| Delta-Neutral Strategies                | 60%                             | Provides consistent, low-risk yield.         |

_Note: The exact allocation will vary depending on market conditions, protocol growth, and liquidity needs._

