---
description: Architecture overview
---

# Smart Contract Architecture

Neutrl implements a modular architecture centered on NUSD, its native synthetic dollar. The protocol's smart contract infrastructure enables transparent minting and redemption of NUSD against multiple collateral types while providing yield generation through an integrated staking mechanism.

The architecture prioritizes modularity, segregating core functionalities into specialized systems and contracts. This design philosophy enhances security, simplifies maintenance, and ensures transparent on-chain operations.



### Core Systems

Neutrl  operates through two primary interconnected systems that govern the complete lifecycle and utility of NUSD.

**1. NUSD Minting & Redemption System**

Manages the minting and redemption of NUSD tokens through collateral deposits and withdrawals, maintaining collateralization and the synthetic dollar peg.

**2. NUSD Staking & Value Accrual System**

Facilitates yield distribution to protocol participants through the sNUSD staking mechanism, enabling passive yield distribution for NUSD holders.

