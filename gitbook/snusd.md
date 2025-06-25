# sNUSD

The staking system centers on `sNUSD`, an ERC4626-compliant vault where users deposit NUSD to receive sNUSD shares representing their proportional claim on vault holdings. These shares appreciate in value as the protocol accrues and distributes yield through a reward mechanism.



<figure><img src=".gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

#### Yield Generation Flow

`YieldDistributor` manages the complete yield lifecycle:

1. **Collection**: Aggregates yield tokens from external sources and protocol revenue streams
2. **Conversion**: Utilizes `Router` infrastructure to convert yield tokens to NUSD&#x20;
3. **Distribution**: Transfers newly minted NUSD to sNUSD&#x20;

#### Unstaking Process

The system enforces a structured withdrawal mechanism:

1. **Cooldown Initiation**
   * Users call `cooldownAssets()` or `cooldownShares()` on sNUSD
   * Underlying NUSD transfers to `Silo` contract for temporary custody
2. **Cooldown Period**
   * Funds remain locked in Silo for `cooldownDuration`
   * Prevents immediate withdrawal after unstaking request
3. **Final Withdrawal**
   * After cooldown expires, users call `unstake()` on sNUSD
   * sNUSD instructs Silo to release NUSD to user
   * Completes the unstaking cycle
