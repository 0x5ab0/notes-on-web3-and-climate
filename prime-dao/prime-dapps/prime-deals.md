[\[←\]](../README.md)

# Prime Deals

**Prime Deals** is an interface that facilitates DAO to DAO (D2D) interactions, such as:
- **Token swaps:** swap tokens from different DAOs with each other, with customizable vesting options in a trustless way
- **Co-liquidity provision:** co-seed funds into a custom smart contract that turns into a liquidity pool
- **Join venture formation:** co-fund a meta-wallet representing a joint venture between the funding DAOs

DAOs can utilize Prime Deals to start, ratify, and archive negotiations and execute on-chain deals. Just as DAO interfaces currently show current and past proposals, the interface will become a public archive of previous proposals facilitated by the D2D mechanism.

Using the negotiation interface and the initial base contracts of Prime Deals, DAOs are able to:
1. **Define the terms of ther proposed DAO agreement** by filling out a proposal template, which is then uploaded to IPFS
2. **Create the on-chain conditions** for the partnered DAOs to execute a **token exchange**

Prime Deals emerged as an outcome of the research led by Curve Labs and BlockScience.

## Principles

Prime Deals is built on four core principles. It is:

- **Agnostic:** Any DAO that can issue external transaction calls can use Prime’s D2D mechanism. It doesn’t matter if you’re running on [Gnosis Safe](https://gnosis-safe.io/), [Daohaus](https://daohaus.club/), or [DAOstack](https://daostack.io/) — any governance framework can work
- **Trustless:** All parties can recover any funding issued for a D2D collaboration when all conditions are not satisfied
- **Flexible:** The D2D prototype goes beyond traditional escrow mechanisms to allow for flexible negotiations that operate closer to existing, real-world negotiations
- **Granular:** Conditions can be as simple or as complex as the parties involved wish them to be. The complexity of collaborations is decided by the parties creating the conditions, and they may choose anything between a single shallow condition or deeply nested, granular conditions.
