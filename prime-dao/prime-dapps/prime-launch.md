[\[←\]](../README.md)

# Prime Launch

## Overview

**Prime Launch** is a platform for hosting decentralized token launches on Ethereum, powered by [Balancer V2](https://docs.balancer.fi/), that enables fair and user-friendly token launches. It uses fully decentralized infrastructure and it is run by a DAO.

- Project teams and DAOs can use Prime Launch to distribute tokens and attract resources.
- Users looking to acquire tokens can get access to a DAO-curated list of newly launching Web3 projects.

## The challenge: IDOs are a hostile frontier

An increasing number of crypto projects have shifted from listing tokens on centralized exchanges to listing on decentralized exchanges. With this transition, new mechanisms for market-making and token offerings have emerged, collectively called *Initial Decentralized Offerings* (IDOs).

These mechanisms have removed many frictions from the industry, as projects no longer need to wait (or pay) for centralized exchanges to list their assets. This has allowed a more diverse group of DeFi projects to emerge.

While IDOs remove some friction, they also create new challenges, namely:

- Time / money costs of researching available IDO tools and potentially developing a custom interface and UX
- Large initial capital requirements to host the IDO (depending on the protocol)
- Exploits like [frontrunning](https://www.bitcoinsuisse.com/research/decrypt/arbitrage-and-frontrunning-in-defi) and [sandwich attacks](https://hackernoon.com/no-sandwich-please-popular-defi-attack-strategy-analysis-jk1734rf)
- Lack of curation, or poor curation, on CEX interfaces, making it difficult for users to find reputable new projects

**The solution:** Prime Launch provides token-launchers with ready-to-go launch infrastructure: smooth UX, low initial capital requirements, well-curated project lists, and a relevant network of users.

## Launch options

There are two methods for hosting a Prime Launch:

### Seed Launch

A **Seed Launch** is a token offering by an early-stage project to a small group of contributors, in order to raise initial resources for the venture, carried out via a fixed swap function whereby contributors can swap the funding token for the seed token at a fixed, pre-determined price.

Seeds may specify:
- **Funding target:** if the funding target is not met, contributors can reclaim their tokens
- **Whitelist:** which addresses will be allowed to contribute to their Seed
- **Cliff:** an amount of time during which contributors who have received tokens cannot transfer them
- **Vest:** an amount of time, beginning after the cliff, during which a contributor's purchased tokens unlock linearly

### Liquid Launch

A **Liquid Launch** is a public token offering that works by attempting to bootstrap the liquidity of a new token. Liquid Launches use Balancer V2's Liquidity Bootstrapping Pools (LBPs) to facilitate fair and efficient environments for distributing tokens. The mechanism has been utilized dozens of times with promising results.

In the back end, a Liquid Launch is an adjustable Balancer V2 LBP designed for initial distribution and price discovery of a new asset. LBPs are liquidity pools that change weights over time. As the weights change, they create selling pressure on the project token, leading to the price of a project token dropping if there is no buying pressure.

The pool weights initially favor D2D (96%) and will gradually move to an equilibrium where D2D is 50% of the pool. The linear step-down creates constant downward pressure on the price, balancing the upward buy pressure, ideally keeping the price oscillating around perceived market value. This relatively stable price discourages arbitrage bot manipulation as they can't count on the steadily decreasing price.

The result is a fair and accessible token launch shown to effectively discover the market price of an asset and raise funds for the project team, without requiring prohibitive initial capital or enabling problematic frontrunning.

Balancer V2 and LBPs provide several benefits:
- **Capital-efficient:** distribute more tokens at efficient price points with less initial capital.
- **Fair:** constant downward price pressure disincentivizes front-running and large buys from whales, giving better opportunities to intended contributors
- **Multi-use:** Liquid Launch can be configured to segue directly into another use case (e.g., serve as a 50/50 AMM after the initial sale)
- **Multi-asset:** smart order routing lets users trade any token in exchange for the project token at the price of higher slippage
- **Balancer's reward protocol:** users of the protocol receive BAL tokens to make up for up to 90% of transaction costs when participating in Liquid Launches

## Contributing to a Launch

To contribute to a launch and receive tokens, users only need to have a compatible wallet set up (i.e., Metamask and all wallets compatible with WalletConnect) and fund it with the funding tokens that the project is accepting in its launch, as well as some ETH for paying transaction costs. Users can view all upcoming launches on the Launches page.

### Contributing to a Seed Launch

To contribute to a Seed Launch, users must hold some of the launch's funding token.

In the "Contribute" box, exchange the funding token for rights to claim a fixed amount of the project token when the launch ends. Contributors can reclaim the tokens they contributed anytime before the launch ends (but will lose rights to claim project tokens if they do).

Seed Launches end when the maximum funding is reached or the contribution time window is over (whether or not the funding target is reached). If the launch ends and the funding target has not been reached, no project tokens will be distributed and contributors can reclaim their funding tokens.

If the funding target or the maximum funding is reached, contributors can claim project tokens in the "Claim" box after the launch ends. Note, however, that many Seed Launches will have vesting periods with cliffs and/or vesting time.

### Contributing to a Liquid Launch

To contribute to a Liquid Launch, users must have any token with liquidity on the Balancer Protocol, for example, ETH, DAI, USDC, or D2D.

In the "Contribute" box on the right of the screen, connect wallet and accept the Prime Launch Policy. Afterward, select the token and amount to exchange for the project token and click the approve button in the Contribute box to start the transaction to approve these tokens to be spent inside Prime Launch. Once confirmed, click on Contribute, which will begin the transaction to swap the funding tokens for the project's tokens.

## Hosting a Launch

To host a Launch via Prime Launch, you will need to follow the application process. Please follow the below steps to apply or request support from a Prime Launch Representative by filling out [this form](https://kolektivo.typeform.com/to/TPMzQKFE).

Official Prime Launches are curated by PrimeDAO to ensure all listed projects are on par with Prime Launch's standards. After submitting the application form, the Prime DAO-appointed Prime Launch multi-sig will take up to 5 days to approve or deny the submission.

If the launch is approved, it will become visible in the Prime Launch UI, and you will be ready to continue the launch process, as described in the next section.

If your application is not accepted, consider opening a [Prime Forum](https://daotalk.org/c/primedao/38) thread to receive feedback on your application and potentially resubmit your application after incorporating feedback.

Once your launch is approved, you will need to finish setting it up using the [admin dashboard](https://admin.launch.prime.xyz/). On the dashboard, depending on the stage of your launch, you will see buttons to:

- Send the required project tokens to the launch contract
- Set up a whitelist for contributors (if applicable for your launch)
- Pause the launch
- Close the launch
- Reclaim any extra project tokens (once the launch is over)

These buttons will only work for the admin address you chose for your launch.
