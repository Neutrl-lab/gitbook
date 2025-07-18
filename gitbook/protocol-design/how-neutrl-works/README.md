# How Neutrl Works



<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption><p>Typical Neutrl user flow: 1) Deposit → Mint nUSD 2) Stake → Earn sNUSD yield 3) Lock → Boost rewards.</p></figcaption></figure>

#### N**USD** Issuance & Redemption

1. **Deposit collateral**
   * Eligible assets: **USDC, USDT, USDe**
   * Any time you deposit one of these tokens to the **Router Contract,** the system settles your deposit on-chain.
2. **Receive the receipt token**
   * The router mints N**USD 1 : 1** against your collateral and returns it to your wallet in the same transaction.
3. **Institutional custody & deployment**
   * Collateral routes to segregated vaults at institutional custodians (Fireblocks, Copper, Ceffu etc.).
   * From there it is deployed into **delta-neutral, duration-matched strategies** that power the protocol’s yield engine.
4. **Unmatched liquidity**
   * NUSD is an ERC-20, with plug-and-play across CEX margin accounts, DeFi money-markets and on-chain primitives.
   * Fast redemptions plus full backing make it “blue-chip” collateral wherever dollars are needed.

#### Staking N**USD → sNUSD**

1. **Stake**
   * Stake your NUSD into the **Staking Contract** to convert it into **sNUSD**.
2. **Earn the Neutrl rate**
   * All protocol income - basis arbitrage, OTC carry, on-chain reference yield - flows to the yield pool.
   * Every epoch the pool **re-indexes sNUSD balances upward**

_(Unstake at any time and you receive NUSD + accrued yield, subject to the 30-day cool-down.)_

#### Locking N**USD / sNUSD**

1. **Choose a lock tenor**
   * Lock assets for **6 to 12 months** inside the **Locking Contract**.
2. **Boost your rewards**
   * Longer locks earn higher points → a larger slice of future emissions & incentive campaigns.
3. **Future-proof distribution**
   * The protocol may evolve to a **weighted-average maturity** model, seamlessly routing more yield toward longer-dated lockers to keep duration perfectly balanced.
