---
description: Earn rewards by staking NUSD for sNUSD
---

# sNUSD

### Earning Yield <a href="#earning-yield" id="earning-yield"></a>

Neutrl distributes generated yield exclusively to sNUSD holders. Users stake NUSD tokens through the staking contract to receive sNUSD, which represents their proportional share of the yield-bearing vault. The sNUSD token automatically appreciates in value as yield accrues, enabling passive yield earning without requiring any manual actions from users.

### Unstaking process

Upon unstaking, sNUSD tokens are burned and users receive their proportional share of NUSD based on the current exchange rate. The protocol enforces a 30-day cooldown period before withdrawals can be executed.

{% hint style="info" %}
The cooldown period ensures that the protocol can withdraw enough collateral, which may require time.
{% endhint %}

### Yield Accrual Mechanism

**1. Staking NUSD**

* Users deposit NUSD into the staking contract
* The contract mints sNUSD based on the current sNUSD:NUSD exchange rate
* Initial exchange rate: 1 sNUSD = 1 NUSD
* The exchange rate increases over time as yield accumulates

**2. Yield Distribution**

* Protocol generates yield through market-neutral strategies and revenue-generating activities
* Yield continuously flows into the staking contract, increasing total NUSD reserves
* Each sNUSD token appreciates proportionally as the vault grows

**3. Passive Growth**

* Yield accrual requires no user intervention
* Returns are automatically reflected in the increasing sNUSD redemption value



### Calculation & Example

$$
\text{sNUSD:NUSD ratio} = \frac{\text{total sNUSD supply}}{\text{total NUSD staked} + \text{total protocol revenue deposited in NUSD terms}}
$$

<table><thead><tr><th width="87.7890625">Time period</th><th width="111.5234375">sNUSD supply</th><th width="154.78125">Protocol revenue (NUSD)</th><th>sNUSD : NUSD ratio</th><th align="center">sNUSD Received for 1 NUSD Staked</th><th>NUSD Received for 1 sNUSD Burned</th></tr></thead><tbody><tr><td>Day 0</td><td>5 000 000</td><td>0</td><td>1 </td><td align="center">1</td><td>1</td></tr><tr><td>Day 90</td><td>5 000 000</td><td>250 000</td><td>1,05</td><td align="center">0.95</td><td>1.05</td></tr><tr><td>Day 180</td><td>5 000 000</td><td>500 000</td><td>1,1</td><td align="center">0.9</td><td>1.1</td></tr><tr><td>Day 270</td><td>5 000 000</td><td>750 000</td><td>1,15</td><td align="center">0.87</td><td>1.15</td></tr><tr><td>Day 365</td><td>5 000 000</td><td>1 000 000</td><td>1,2</td><td align="center">0.833</td><td>1.2 </td></tr></tbody></table>

### &#x20;<a href="#about-erc-4626" id="about-erc-4626"></a>

