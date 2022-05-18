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

# Bridge

The Carbon Bridge allows anybody to bring their carbon credits on-chain in a tokenized form. Even though the Carbon Bridge currently connects legacy carbon registries exclusively with the Toucan Registry (an on-chain registry on the Polygon network), the plan is to turn carbon into a **multi-chain** asset, so more public blockchains will be supported in the future.

<p align="center">
  <img src="https://user-images.githubusercontent.com/81234139/169004621-374a1d0f-e74e-4ee5-89ae-cd8533520b37.png" />
</p>

In order to prevent double-counting, the Toucan Carbon Bridge is **one-way**: carbon credits can be brought on-chain but can't go the other way. Users of the Carbon Bridge need to retire the credits on the source registry before bringing them on-chain.

## Requirements

In order to bring carbon credits over the Carbon Bridge onto the Toucan Registry, you'll need to have access to a few things:
- **Carbon credits in the Verra registry (Verified Carbon Units, VCUs)**, along with a retirement account or a partner who can retire the credits for you, specifying that they are destined for the Toucan Bridge.
- **An Ethereum account** controlled by your Metamask wallet **with some MATIC**.

To be **eligible for bridging**, carbon credits must fulfill the following criteria:
- The methodology applied in the project issuing the VCUs must **not** be **included** in the **blocklist of methodologies**\*.
- The difference between the **date of verification** (aka. the "vintage") and the **date of issuance** of the credits must be **less than 10 years**.

* Blocklisted methodologies include, for instance, projects related to HFC-23, a byproduct of the refrigerant manufacturing process, which stopped being issued by the Verified Carbon Standard in 2014 based on Verra's acknowledgement of the misincentives created by these methodologies. Recently, Toucan updated the gating criteria of the Base Carbon Pool to prevent the phased out credits which had already been tokenized from being deposited into the pool in return for BCT tokens.

## Bridging Process

### 1. Initiate

The bridging process starts on Toucan's dApp with the **minting of a non-fungible token**: a **BatchNFT**. The BatchNFT is in an initialized state and doesn't have any offset-specific metadata yet except for a **Reference-ID**, a unique identifier which is used as input for step 2 of the process and includes a transaction hash, a reference to Toucan Protocol and its version, and a Chain ID as a reference to the blockchain in question.

**User POV:** Click on "Initialize bridging", select the registry from which you are bridging the credits from (only Verra supported at launch) and indicate whether you have access to the registry or have a partner who can retire these credits for you. Click "Initialize Batch" and confirm the transaction on Metamask.

<img src="https://user-images.githubusercontent.com/81234139/169019062-91d24a69-c3ad-49b1-a208-2233c138b3e8.png" width="500px" />

### 2. Retire

Next, the carbon credits to be tokenized are **retired in the off-chain carbon registry** and the **Reference-ID of the BatchNFT is included in the retirement note** in order to establish a backlink to Toucan.

**User POV:** Retire the batch of carbon credits you want to bridge on the off-chain registry. Include all the information provided by Toucan when submitting the retirement. Receive a retirement serial number, and click "I have my serial".

<img src="https://user-images.githubusercontent.com/81234139/169012365-18231ca7-e26c-453f-8d10-cec4ff7abaa0.png" width="500px" />

### 3. Bridge

Offsets are retired in batches and each retired batch of credits has a unique **retirement serial number** provided by the registry after retirement. This serial number carries a lot of relevant information, including the number of offsets, certifying standard body, project identifier, country, monitoring period (vintage), and more.

The **BatchNFT is updated with this serial number**, completing the link between the legacy and on-chain registries: the BatchNFT is linked to the retirement entry in the legacy registry through the serial number and the retirement entry has the NFT's unique identifier in its metadata. Furthermore, the serial number is used to update the BatchNFT with **project-specific attributes**, some of which are stored on-chain while others are stored as metadata on IPFS.

**User POV:** Add one or more serial numbers to create a batch offset, keeping in mind that retirements from the same project with a different vintage (or same vintage but different projects) must be retired separately as different batch offsets. Optionally, enter an email to receive status updates on your retirement. Click "Confirm serials".

<img src="https://user-images.githubusercontent.com/81234139/169013552-090646a8-752c-4c4d-b12c-4ccc473933c9.png" width="500px" />

### 4. Submit

Submitting the serial number to the BatchNFT contract changes the state of the NFT to *awaits approval*.

**User POV:** Check that the information is correct and click "Submit for approval", then confirm the transaction in Metamask.

<img src="https://user-images.githubusercontent.com/81234139/169013726-e0bada1c-6490-45dc-a0ed-b7b2ad2a9e0c.png" width="500px" />

### 5. Await

Once the BatchNFT is updated with a serial number, it needs to be approved by a **Toucan Verifier**, a trusted member of the Toucan community. This step is required to protect against fraudulent inputs and, although for now it remains dependent on human action and trust, Toucan is exploring ways to automate this process in the future, e.g. with a decentralized arbitration service like Kleros managing disputes.

Once the correctness of the serial number input is confirmed by a Toucan Verifier, the state of the BatchNFT changes to *approved* and it becomes a fully **tokenized batch of carbon credits (in the form of an ERC721)** that can be sold on NFT marketplaces or used as collateral in DeFi lending markets.

### 6. Fractionalize

Since NFTs can be a bit unpractical for many other use cases (such as sending a fraction of a credit or creating carbon reference tokens), the user can **fractionalize the BatchNFT** to mint an equivalent number of fully fungible ERC20 tokens (TCO2s). A BatchNFT representing a batch of 100 credits can be fractionalized into 100 TCO2 tokens.

**User POV:** Sign in, and once the batch is verified, click "Finalize". Approve the transaction and receive your TCO2 tokens.

When you fractionalize a BatchNFT, the ERC20 token will have TCO2- as a prefix, followed by an information-rich name that includes the registry of origin, the project, the vintage, and so on (e.g., TCO2-GS-0001-2019).

There's one downside to this: because they are specific to a single project and vintage, TCO2 tokens are not very liquid. What if we want to create a liquid market for soil carbon where all soil carbon credits are treated equally? This would allow deep liquidity to be aggregated, key for fair and efficient price discovery for a specific type of carbon asset—something we are struggling to find in the "real world". The solution to this problem are **Carbon Pools**.
