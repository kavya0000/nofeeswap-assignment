# nofeeswap-assignment
Full-stack Web3 DEX simulation using NoFeeSwap protocol with local deployment, Next.js dApp, and mempool sandwich attack bot.

# 🚀 NoFeeSwap Full-Stack Web3 Assignment

This project is a complete local deployment and interaction system for the NoFeeSwap protocol, built as part of a Senior Full-Stack Web3 Engineer technical assignment.

The implementation demonstrates end-to-end understanding of DeFi systems, including smart contract deployment, Web3 frontend integration, and mempool-based automated trading strategies.

---

## 🧠 Project Overview

The goal of this project is to:

- Deploy the NoFeeSwap protocol in a local blockchain environment
- Build a decentralized application (dApp) to interact with the protocol
- Develop a mempool monitoring bot that simulates sandwich attacks

This project showcases both **on-chain interaction** and **off-chain infrastructure**, focusing on real-world DeFi mechanics such as gas prioritization, nonce ordering, and transaction lifecycle management.

---

## ⚙️ Tech Stack

- Frontend: Next.js + React
- Web3 Integration: ethers.js
- Blockchain: Foundry (Anvil)
- Backend Bot: Node.js + TypeScript
- Wallet: MetaMask

---

## 🔥 Key Features

### 🧱 Local Protocol Deployment
- Deployed NoFeeSwap core & operator contracts locally
- Configured local blockchain using Anvil
- Created and minted mock ERC-20 tokens

### 🌐 Web3 Frontend (dApp)
- Wallet connection via MetaMask
- Swap interface with transaction lifecycle handling
- Basic user interaction with deployed contracts

### 🤖 Mempool Monitoring Bot
- Listens to pending transactions in the mempool
- Detects swap transactions from frontend
- Simulates sandwich attack:
  - Front-run transaction (higher gas)
  - Victim transaction
  - Back-run transaction (lower gas)

---

## ⚡ Architecture Overview

Frontend (Next.js) → ethers.js → Local Blockchain (Anvil)

Bot (Node.js) → Mempool Monitoring → Transaction Decoding → Sandwich Execution

---

## ⚠️ Transparency Statement

### ✅ Completed
- Local blockchain setup with Anvil
- Basic dApp with wallet integration
- Swap simulation
- Mempool monitoring bot
- Sandwich attack simulation using gas price ordering

### ⚠️ Partially Completed
- Calldata decoding (basic implementation)
- Profitability logic (simplified assumptions)
- UI enhancements for liquidity and pool initialization

### ❌ Not Implemented
- Full graphical kernel visualization
- Advanced MEV optimization strategies
- Production-grade contract interaction

---

## 🚧 Known Limitations

- Swap logic is simplified for demonstration purposes
- Bot uses heuristic-based detection instead of full decoding
- No real liquidity pool math from YellowPaper fully implemented
- Designed for local testing only (not mainnet-ready)

---

## 🎥 Demo

A video walkthrough demonstrating:
- Contract deployment
- dApp usage (wallet connection & swap)
- Bot detecting and executing sandwich attack

(Attach video link here)

---

## 📦 Setup Instructions

Follow the steps below to reproduce the project locally.
