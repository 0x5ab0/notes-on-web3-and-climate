# Prime Launch

**Prime Launch** is a curated token offering platform powered by [Balancer V2](https://docs.balancer.fi/) that enables fair and user-friendly token launches. It uses fully decentralized infrastructure and it is run by a DAO.

Project teams and DAOs can use Prime Launch to distribute tokens and raise capital. Users looking to acquire tokens can get access to a DAO-curated list of newly launching Web3 projects.

There are two methods for hosting a Prime Launch: Seed Launch and Liquid Launch.

## Seed Launch

A **Seed Launch** is a token offering by an early-stage project to a small group of contributors, in order to raise initial resources for the venture, carried out via a fixed swap function whereby contributors can swap the funding token for the seed token at a fixed, pre-determined price.

Seeds may specify:
- **Funding target:** if the funding target is not met, contributors can reclaim their tokens
- **Whitelist:** which addresses will be allowed to contribute to their Seed
- **Cliff:** an amount of time during which contributors who have received tokens cannot transfer them
- **Vest:** an amount of time, beginning after the cliff, during which a contributor's purchased tokens unlock linearly

## Liquid Launch

A **Liquid Launch** is a public token offering that works by attempting to bootstrap the liquidity of a new token. Liquid Launches use Balancer V2's Liquidity Bootstrapping Pools (LBPs) to facilitate fair and efficient environments for distributing tokens. The mechanism has been utilized dozens of times with promising results.

In the back end, a Liquid Launch is an adjustable Balancer V2 pool designed for initial distribution and price discovery of a new asset. The pool will generally start with a high weight of project tokens (e.g. 95%) and a small weight of funding tokens (e.g. 5% DAI). During the Liquid Launch, often 2 to 3 days, the pool weights are continuously rebalanced toward the funding token, which leads the project token's price to slowly decline. Contributors can participate at their preferred price point, while bots and arbitrageurs do not benefit from frontrunning (as buying early generally leads to overpaying).

The result is a fair and accessible token launch shown to effectively discover the market price of an asset and raise funds for the project team, without requiring prohibitive initial capital or enabling problematic frontrunning.

Balancer V2 and LBPs provide several benefits:
- **Capital-efficient:** distribute more tokens at efficient price points with less initial capital.
- **Fair:** constant downward price pressure disincentivizes front-running and large buys from whales, giving better opportunities to intended contributors
- **Multi-use:** Liquid Launch can be configured to segue directly into another use case (e.g., serve as a 50/50 AMM after the initial sale)
- **Multi-asset:** smart order routing lets users trade any token in exchange for the project token at the price of higher slippage
