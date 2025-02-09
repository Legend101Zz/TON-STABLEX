# TeleStable Hackathon Roadmap (32 Days)

## Overview

TeleStable is a CDP-based stablecoin system (StableX) on TON. Users deposit BTC (via the TON Teleport BTC bridge) to mint StableX (pegged to \$1). An extra protocol fee (collected on deposits and dApp transactions) is captured and allocated into a Fee Treasury, which is used to generate yield. A portion of the fees is also allocated to a Developer Ecosystem Fund (DEF) to reward dApp builders, especially those creating Telegram bots that drive usage.

---

## Week 1: Ideation & Architecture (Days 1-7)

### Days 1-2: Conceptualization & Research

- Finalize TeleStable core concept and unique value propositions:
  - CDP stablecoin minting with over‑collateralization (e.g., 200%).
  - Extra fee capture from deposits and dApp transactions.
  - Fee Treasury for yield generation.
  - Developer Ecosystem Fund (DEF) to incentivize Telegram bot/dApp development.
- Research TON Teleport BTC integration, fee oracles, and Telegram bot APIs.
- Hold a kickoff meeting to assign roles (Mrigesh, Abhishek, Anurag, Utkarsh).

### Days 3-4: System Architecture & Design

- Design overall system architecture with modules:
  - **CDP Vault & Minting Module:** Handles BTC deposits and StableX minting.
  - **Fee Capture Module:** Calculates extra fee using the formula:  
    `Extra Fee = Capture Rate × (Current Fee - Baseline Fee) × Tx Size`
  - **Fee Treasury & Yield Module:** Aggregates extra fees and deploys them in yield strategies.
  - **Developer Ecosystem Fund (DEF):** Allocates a percentage of extra fees from dApp transactions.
  - **Telegram Integration Module:** For user commands and analytics.
- Draw architecture diagrams (e.g., using Mermaid) and document specifications.

### Days 5-7: Environment Setup & Initial Skeleton

- Set up TON testnet environment and development tools (e.g., Tact or FunC for smart contracts).
- Create the project repository and collaboration channels.
- Build initial code skeleton:
  - Smart contract templates (CDP, Fee Capture, Yield Distribution).
  - Basic Telegram bot framework for later integration.

---

## Week 2: Smart Contract & Backend Development (Days 8-14)

### Days 8-10: Develop CDP Smart Contract

- Code the CDP contract:
  - Functions for BTC deposit, collateral tracking, minting StableX, and liquidation.
  - Integrate over‑collateralization logic (e.g., 200% ratio).
  - Implement basic fee capture logic (using mock data from an oracle).
- Write unit tests for deposit, minting, and liquidation functions.

### Days 11-12: Build Fee Treasury & Yield Modules

- Develop the Fee Capture Module:
  - Use the formula to capture extra fee during deposit transactions.
  - Store captured fees in the Fee Treasury.
- Build the Yield Module:
  - Create functions to deploy Fee Treasury funds in yield-generating strategies (simulate lending/staking).
  - Write tests to verify yield calculation and distribution logic.

### Days 13-14: Developer Ecosystem Fund (DEF) Module

- Implement logic to allocate a fixed percentage (e.g., 10%) of extra fees from dApp transactions into the DEF.
- Create functions to track dApp usage metrics (simulate usage with test data).
- Write tests for the DEF reward calculation and distribution.

---

## Week 3: Telegram Bot & dApp Integration (Days 15-21)

### Days 15-17: Telegram Bot Development

- Develop the Telegram bot (using Node.js or Python):
  - Implement commands:
    - `/deposit` to guide users through BTC deposit.
    - `/mint` to initiate StableX minting.
    - `/balance` to check collateral ratio, minted StableX, and yield accrued.
    - `/yield` to display current yield information.
- Connect the bot to TON blockchain APIs for smart contract interactions.
- Test basic interactions on the testnet.

### Days 18-19: API/SDK for dApp Integration

- Develop API endpoints or an SDK to allow developers to integrate with the TeleStable system:
  - Functions to query deposit status, fee capture, and yield data.
- Document the API for developers.
- Simulate dApp usage with test transactions to record extra fee capture.

### Days 20-21: Build a Simple Developer Dashboard

- Create a web dashboard (or extend Telegram bot capabilities) to show:
  - User CDP health: collateral value, minted StableX, yield accrued.
  - dApp usage statistics and DEF rewards.
- Integrate analytics to track transaction volumes and fee capture across dApps.

---

## Week 4: Testing, Optimization & Finalization (Days 22-32)

### Days 22-25: End-to-End Integration Testing

- Deploy smart contracts on the TON testnet.
- Run end-to-end tests simulating:
  - BTC deposit and StableX minting.
  - Extra fee capture calculations (using mock oracle data).
  - Yield generation from the Fee Treasury.
  - dApp transactions and DEF reward allocation.
- Fix any issues and optimize smart contract performance.

### Days 26-28: Security Audits & Optimization

- Conduct thorough unit and integration tests.
- Optimize gas usage and transaction response times.
- Document known risks and ensure the system meets security benchmarks.

### Days 29-30: Finalize Documentation & Presentation Materials

- Prepare detailed documentation covering:
  - System architecture and module functions.
  - Smart contract logic and calculations.
  - Telegram bot commands and API usage.
  - Test results and performance metrics.
- Develop a demo presentation video and slides.

### Days 31-32: Rehearsal & Submission

- Conduct a final demo rehearsal with the team.
- Refine any last-minute issues or bugs.
- Finalize and package the submission (code, documentation, presentation).
- Submit the project for the hackathon.

---
