---
title: Permissionless Market Making
date: 2024-06-18 14:54:00 +/-TTTT
categories: [AMM, ALM]
tags: [alm, amm, uniswap, clmm]     # TAG names should always be lowercase
mermaid: true
---

The market-making strategy used by Noma consists of three sequential positions deployed in a Uniswap V3 concentrated liquidity pool. 

```mermaid
graph TD;
    A-->B;
    B-->A;
```  

## Concentrated Liquidity Positions

The structure of the liquidity is composed as follows:

- Floor
- Anchor
- Discovery

### Floor
This position contains the majority of the reserves backing the token  concentrated in a very narrow range - the minimum width of a "tick" of liquidity on Uniswap V3. The floor position is responsible for absorbing the circulating supply during periods of high market activity and maintaining the token's intrinsic minimum value.

### Anchor
As the price leaves the IMV zone, the anchor liquidity meets demand by supplying liquidity in the price range between the token's IMV itself and the current price decided by the market. This range is wider than the floor position by design.

### Discovery
As the price keeps increasing leaving behind the anchor zone, it is served by the discovery position, which is responsible for distributing the supply into the market on a wider range. As the name suggests, this position enables the "price discovery" process of the asset.