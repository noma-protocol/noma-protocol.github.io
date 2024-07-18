---
title: Feedback Burn
date: 2024-06-02 20:00:00 +/-TTTT
categories: []
tags: []
math: true
---

The burn contract is designed to optimize the use of protocol fees for continuous buybacks and burns of NOMA. It systematically supports the market price and reduces the circulating supply of NOMA through a leveraged mechanism that is triggered at regular intervals. 

The Afterburner contract's operations can be initiated by any user, with built-in safeguards like the cooldown period to prevent abuse.

## Overview
1. **Fee Accumulation:**
   - **Objective:** Collect 100% of LP fees and interest fees from the protocol.
   - **Process:** All earned fees are automatically transferred to the Afterburner contract.

2. **Token Purchase and Borrowing:**
   - **Objective:** Use accumulated fees to buy NOMA and borrow against these tokens for further purchases.
   - **Process:**
     - Fees are used to purchase NOMA.
     - The contract borrows against these NOMA to buy more, driving up the market price.

3. **Supply Reduction:**
   - **Objective:** Reduce the circulating supply of NOMA.
   - **Process:** The contract defaults on the loans, effectively burning the NOMA and removing them from circulation without impacting the market.

4. **Regular Triggers:**
   - **Objective:** Ensure continuous buyback and burn operations.
   - **Process:**
     - The Afterburner contract can be triggered every 5 minutes.
     - The triggering mechanism is public, allowing any user to initiate it.
     - A configurable cooldown period ensures controlled activation.
     - The contract burns a percentage of its assets every few minutes, following a TWAP mechanism to maintain a steady impact.
