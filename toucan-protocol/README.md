Toucan is building the public infrastructure needed to create programmable carbon.

To bring carbon on-chain, they've built the **Carbon Bridge**, which allows anybody to tokenize their carbon credits. **Carbon Pools** then turn tokenized carbon credits into more liquid carbon reference tokens, enabling price discovery for different classes of carbon assets and providing a new money lego to DeFi.

# Introduction

## Overarching Design of the Toucan Protocol



<p align="center">
  <img src="https://user-images.githubusercontent.com/81234139/168833780-2bcaf94c-ea07-4acd-b10e-e2e8e8808feb.png" />
</p>

**From bottom to top:**
- **Off-chain registries** maintained by standards bodies like Verra issue carbon credits when **projects** can show they've engaged in activity that meets their standard.
- The **Carbon Bridge** provides an on-ramp for carbon credits from these source registries onto the **Toucan Registry**, a set of smart contracts built on Polygon.
- Once bridged, tokenized carbon credits (called **TCO2 tokens**) can be deposited in a **Carbon Pool**.
- These carbon reference pools only accept carbon tokens that contain a set of attributes, meaning every TCO2 token in the pool shares a set of gating attributes. By depositing TCO2 tokens into a pool, users receive **carbon reference tokens**, a fungible pool token that is backed by one carbon token held in the pool's smart contract.
  - Toucan's first Carbon Pool, designed with KlimaDAO, is the **Base Carbon Tonne**, or **BCT**.
- By aggregating carbon credits in the Carbon Pool smart contracts, the Toucan Protocol enables the creation of liquid carbon tokens like BCT. As fungible ERC20 tokens with deep liquidity, these carbon reference tokens serve as the **carbon building block across Web3**.

## Carbon Markets

The main goal of the **voluntary carbon market** is to drive finance to climate-positive projects that reduce greenhouse gas (GHG) emissions. Carbon credits are the vehicle that connects carbon projects with consumers that purchase and retire credits to achieve their climate targets. A carbon credit represents a measurable and verifiable removal, reduction, or avoidance of GHG emissions and is denominated in tCO2e (which means "**tonne of CO2 equivalent**").

In the voluntary carbon market, **carbon standards** set the rules and requirements carbon projects need to follow in order to demonstrate they meet minimum quality criteria. **Verra** and **Gold Standard** are the two major players.

The "rules" carbon projects need to follow are a combination of high-level requirements and processes set by the standard and specific **accounting methodologies**. A methodology dictates things like monitoring requirements and is different for each carbon credit-generating activity. Independent 3rd parties—a list of **auditors** authorized by each standard—will assess projects against these rules and requirements. Only after a successful verification will the project be issued carbon credits by the standard body.

Each standard maintains a **centralized registry** with a list of all its projects, and the issued and retired credits associated with each project.

After projects have proven that they've removed or reduced GHG emissions they are issued **carbon credits** that are in an **active** state. Because projects generally don't have direct contact with companies who will buy their credits to satisfy sustainability claims, they often sell them to intermediaries—brokers, resellers, and retailers. Active carbon credits can pass from one hand to another without changing their status. But when an end-buyer wants to use the credits to compensate their GHG emissions for carbon accounting purposes, the credits need to be **retired**. Now the carbon credit has fulfilled its "duty" and nobody else will be able to claim the carbon removal or reduction for their books. A registry account is needed to trade carbon credits in an active state. These accounts can cost $1000 a year in the case of Gold Standard.
