![Flowcarbon](https://user-images.githubusercontent.com/81234139/170294307-32cfffd3-fbdd-4341-adfb-4b107b6b3bb5.jpg)

**Flowcarbon** operates at the intersection of carbon and crypto, leveraging Web3 to protect the Earth’s natural carbon sinks. It was founded by a team steeped in environmental philanthropy, who saw firsthand the limitations of relying on philanthropy capital to preserve the Earth’s natural carbon sinks.

Realizing that key benefits of blockchain technology could be applied to the carbon markets, they set out to **bring carbon on chain** to create **democratized access to offsets** and **incentivize high impact climate change mitigation projects**.

Flowcarbon's flagship product, the **Goddess Nature Token (GNT)**, allows individuals and corporations to **buy and retire carbon credits** in an accessible and transparent market. While their scope is not limited to nature-based projects, the initial focus is on improving capital access for **nature-based projects** that optimize for climate change mitigation and adaptation, community-led land management, and critical ecosystem and biodiversity protection.

## Introduction

**Voluntary carbon credits** are transferable instruments issued to projects that remove or reduce carbon from the atmosphere. The steps to generating an offset are the following:
1. Project undertaken by proponent, often in nature (i.e., conservation, reforestation)
2. Carbon protected or removed by project is quantified by a third party
3. Project submitted to non-profit credit-granting registry (e.g., Verra)
4. Registry issues "voluntary credits": digital certificates certifying that a project has avoided or removed carbon
5. Voluntary credits don't expire until bought and "retired" by a company to offset its greenhouse gas emissions

Purchasing voluntary credits is a **key solution to climate change**, financing critical climate-mitigation projects that are otherwise financially non-viable. Rising demand and price create a **flywheel effect**:
1. Value rises as retail customers gain access
2. **Breakthrough:** Projects reach financial viability
3. Companies/individuals purchase and retire carbon credits, further driving up value as supply shrinks
4. More projects become economically viable

Corporate **demand for voluntary credits has surged**.
- Demand for voluntary carbon credits is set to **grow 15x by 2030**
- Corporate market to grow from $300M in 2018 to >$20B in 2030
  - Over 2000 companies announce net-zero ambitions to achieve Paris climate goals
- Nature-based projects saw **demand more than double in 2021** from 2020's already-record-high levels

Defining voluntary credits rests on four levers:
- **Age:** recent vintage years are more valuable
- **Certification:** by a market-recognized body like Verra or three equivalent registries
- **Project types:** nature-based projects fetch premium prices
- **More impact:** projects also protect wildlife or employ vulnerable people

Nonetheless, major **inefficiencies make the voluntary market slow**, difficult to scale, and keep value from project proponents:
- **Illiquid markets:** Most transactions are OTC, fragmented across numerous selling agents
- **Non-transparent, tedious price discovery:** No benchmark pricing
- **Value diverted by middlepersons:** Numerous brokers and marketing agents between projects and end buyers
- **Difficult sales cycle for corporates:** Voluntary offsets not treated as commodities with clear pricing and quality ratings; instead, need for diligence, reliance on third parties, and widely variable pricing
- **Closed to retail buyers:** Structurally almost impossible for retail and many institutions to hold voluntary credits
- **Low digitization in space:** Fragmented and opaque market means little incentive for wholescale innovation

Tokenizing voluntary carbon credits is the key solution, **creating a liquid, transparent market** that anyone can access.

**In just one month,** on-chain carbon credits have **doubled the YTD volume** of traditional carbon markets.
- **Off-chain market grew 100% YTD from 2020 highs**, reaching a record high of $1B+ this year
- **On-chain market has doubled the off-chain volume** since launching in October 2021 (KlimaDAO), raising the floor price of carbon credits by 10x

But demand scenarios are still very limit because the carbon on-chain so far is:
- **Low quality** voluntary credits with limited demand
- **Retired**, non-live voluntary credits with no off-chain value
- **Lacks functional features** enabling token holders to utilize the carbon effectively

# The Goddess Nature Token

**Goddess Nature Token** is the first multi-functional crypto primitive bringing institutional-grade carbon assets on chain. It maximizes the value of real-world voluntary carbon credits on-chain.

## Introduction to the GNT

### Key mechanics

- **Backed one-to-one** by voluntary carbon credits
- Voluntary credits are **live, "unretired",** and therefore retain full off-chain value with offsetters such as corporations
- Credits are deposited into a **bankruptcy-proof SPV** managed by a professional third-party, with regular audits, ensuring the one-to-one ratio

### Underlying voluntary credit criteria

- **Recent vintages:** Flowcarbon's five year vintage period will roll every year. Newest vintage will be the current year vintage. (e.g., in 2022, vintages eligible are V17-V22).
- **Backed by carbon credits from one of the four market-recognized registries:** Verra, Gold Standard, Climate Action Reserve, and American Carbon Registry.
- **Additional co-benefits for wildlife and humans:** i.e., protecting endangered habitats, employing people in the developing world, protecting indigenous rights and lands, etc.
- **Only nature-based methodologies accepted:** i.e., conservation, reforestation, nature restoration, etc.

GNT's unique attributes and real-world value make it the **first liquid carbon instrument designed for corporate, retail, institutional, and crypto buyers**.

**GNT represents a claim on pooled credits:** Each **off-chain carbon credit** will be tokenized into **GCO2 tokens** that are unique to each project and vintage year from which credits are sourced. GCO2s are **then added to a pool** with other GCO2s and **"wrapped" as a fungible, tradable, liquid pool token ("GNT")** representing a claim on the pool. This mitigates traditional project-level risk, offering safer exposure to the voluntary carbon market.

GNT's **two-way bridge** enables tokens to be **retired, unwrapped, or redeemed** as they move on and off the chain.
1. **Retire:** Token can be retired by token holder on demand and claimed as a carbon offset
2. **Unwrap:** Token can be unwrapped back from the fungible GNT token into the underlying GCO2 represneting an actual carbon credit from a specific project
3. **Redeem:** Token can be unwrapped and traded in for the underlying off-chain unretired carbon credit at any time, giving the token holder the right of delivery of the underlying carbon credit

![Flowcarbon's Bridging and Bundling Process](https://user-images.githubusercontent.com/81234139/170317714-854b1df4-c492-434b-8fa2-4d82e2f0d05a.png)

According to Flowcarbon, **GNT is the only viable interoperable crypto primitive for carbon,** and it's already being integrated with the world's leading protocols.

## Technical Overview

### Token Life Cycle

- **Minting:** Verifiable with a public registry such as Verra, using universally unique identifiers to prove that the tokens are backed by verified carbon credits
- **Purchasing and trading:**
  - Full feature list of the ERC20 Token interface
  - Can be transferred and fractionalized
  - Can be used in liquidity pools, lending protocols and every other protocol to utilize fungible tokens on EVM-supported chains
- **Retiring:**
  - Once the underlying carbon credit is used, it is "retired" and taken out of circulation
  - All retired tokens accumulate transparently within the contract until they exceed a complete batch. Flow then retires the credits in the underlying registry and is again committing a tamper-proof checksum as proof-of-existence

### Project Bundles & Deconstruction

- **The Bundle Contract:**
  - Projects with equal parameters can be pooled into a bundle token to allow high quality baskets of carbon credits
  - Each bundle features the ERC20 token standards and enjoys full integration into existing DeFi protocols
  - Bundles will be prominently placed in liqudiity pools and staking protocols
- **Depositing and withdrawing:**
  - Each project token can be freely deposited and withdrawn from a bundle if they fit the bundle requirements
  - Guaranteed 1:1 backing of each bundle token with a project token
- **Audited by [Quantstamp](https://quantstamp.com/)**

## Blockchain Advantage

Democratizing access for all via blockchain unlocks the speed and scale of crypto markets in financing planet-saving projects.

- **Democratized access:** DeFi ecosystem takes power away from middlemen and gatekeepers such as traditional brokers, marketing agents, and retailers and enable anyone to buy carbon credits. It provides permissionless borrowing and leverage, which doesn't exist in the off-chain market.
- **Price transparency:** Quick scaling of liquidity and trading enables rapid price discovery and the establishment of benchmark carbon prices through the power of markets.
- **Decentralized innovation:** Offering a crypto primitive with full functionality to other protocols expands the possibilities for innovation and growth.
- **Impact accountability:** Smart contracts governing carbon accounting provides buyers full transparency into what projects they are supporting, leading to safe and credible transactions.
