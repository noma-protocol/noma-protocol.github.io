---
title: Concentrated Liquidity
date: 2024-06-18 14:55:00 +/-TTTT
categories: [AMM, ALM]
tags: [alm, amm, uniswap, clmm]     # TAG names should always be lowercase
mermaid: true
---

The automated tokenomics and permission-less market-making narrative was introduced by the Baseline protocol and YES token in March 2024. The project launched on the Blast layer two (L2) blockchain with the aim to provide other projects with a technology they can tap into to launch tokens with more predictable dynamics, while also benefiting from the native integration with a powerful lending/credit facility. Baseline leverages Uniswap V3 concentrated liquidity as the decentralized exchange (DEX) for its market-making strategy.

```mermaid
    xychart-beta
    title "Liquidity Distribution"
    x-axis [0, 0.1, 0.2, 0.3, 0.4, 0.5, 0.6, 0.7, 0.8, 0.9, 1, 1.1]
    y-axis "Revenue (in $)" 0.025 --> 1
    bar [0, 0, 0, 0, 0.25, 0.25, 0.25, 0.25, 0, 0, 0, 0]
    bar [1]
    bar [0, 0, 0, 0, 0, 0, 0, 0, 0.5, 0.5, 0.5, 0.5]
    bar [0]
    bar [0,1]
    bar [0,0,1]
    bar [0,0,0,1]
    bar [0,0,0,0,1]
    bar [0,0,0,0,0,1]
    bar [0,0,0,0,0,0,1]
    bar [0,0,0,0,0,0,0,1]
```