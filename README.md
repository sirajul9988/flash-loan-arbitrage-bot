# Flash Loan Arbitrage Bot

This repository provides a smart contract template for executing **Flash Loans**. It is designed to borrow liquidity from a provider (e.g., Aave), execute a trade on Uniswap, and repay the loan within a single transaction.

## Workflow
1. **Request Loan:** The contract requests a specific asset from the provider.
2. **Execute Trade:** The `executeOperation` callback is triggered.
3. **Arbitrage:** The contract swaps assets on DEX A and DEX B.
4. **Repayment:** The loan + premium is returned; profit remains in the contract.

## Prerequisites
* Solidity ^0.8.10
* Knowledge of Flash Loan premiums (typically 0.05% - 0.09%).
* An EOA with enough gas to deploy and trigger the transaction.

## Disclaimer
Arbitrage opportunities are highly competitive. Ensure you have calculated gas fees and slippage before execution.
