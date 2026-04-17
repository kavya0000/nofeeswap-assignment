# 🚀 NoFeeSwap Screening Assignment

## 📌 Overview

This project demonstrates a complete local implementation of the NoFeeSwap protocol, including:

* Local blockchain deployment using Hardhat
* Smart contract interaction
* Web3 frontend (dApp)
* Mempool monitoring bot simulating sandwich attacks

The system runs entirely in a local environment and showcases full-stack Web3 engineering capabilities.

---

## ⚙️ Tech Stack

* Frontend: React (Next.js)
* Blockchain: Hardhat Local Node
* Smart Contracts: Solidity (NoFeeSwap Core & Operator)
* Web3 Integration: Ethers.js
* Bot: Node.js (TypeScript)
* Wallet: MetaMask

---

## ✅ Features Implemented

* Local blockchain setup using Hardhat
* Deployment of protocol contracts
* Wallet connection via MetaMask
* Token approval system
* Swap interface (UI ready)
* Transaction lifecycle handling (pending, confirmed)
* Mempool monitoring bot (off-chain)
* Sandwich attack simulation logic (basic)

---

## ⚠️ Partially Implemented

* Liquidity pool UI (structure present, limited interaction)
* Profitability calculation (basic logic only)
* Full swap execution integration (UI + contract flow simplified)

---

## ❌ Not Implemented

* Advanced liquidity kernel visualization
* Production-level MEV optimization
* Real-world gas competition simulation

---

## 📂 Project Structure

/contracts        → Deployment scripts
/frontend         → Web3 dApp
/bot              → Mempool monitoring bot
README.md         → Documentation

---

## 🛠️ Setup Instructions

### 📌 Prerequisites

* Node.js (v16+)
* npm
* MetaMask
* Git

---

### 📥 Installation

git clone https://github.com/kavya0000/nofeeswap-assignment.git
cd nofeeswap-assignment
npm install

---

### ⛓️ Start Local Blockchain

npx hardhat node

---

### 📜 Deploy Contracts

npx hardhat run scripts/deploy.js --network localhost

---

### 🌐 Start Frontend

cd frontend
npm install
npm run dev

App runs at:
http://localhost:3000

---

### 🤖 Run Mempool Bot

cd bot
npm install
npm run start

---

## 🧠 Architecture Overview

### 1. Frontend (dApp)

* Built using React
* Connects to MetaMask
* Displays account, balances, and transaction status
* Provides UI for approvals and swaps

### 2. Local Blockchain

* Hardhat node simulates Ethereum network
* Provides test accounts with ETH
* Executes all transactions locally

### 3. Bot (Off-chain)

* Runs independently from UI
* Monitors pending transactions (mempool)
* Executes sandwich logic

Mempool contains pending transactions before confirmation ([Chainstack][1])

---

## 🤖 Mempool Bot Design

The bot listens to pending transactions using:

web3 / ethers provider → pending transaction subscription

Similar systems monitor mempool streams to detect opportunities ([GitHub][2])

### Workflow:

1. Listen for pending transactions
2. Identify swap transactions
3. Decode calldata using ABI
4. Extract:

   * Trade size
   * Slippage tolerance
5. Evaluate opportunity (basic logic)
6. Execute sandwich strategy:

   * Front-run → higher gas
   * Victim transaction
   * Back-run → lower gas

---

## 📸 Screenshots

### 🔗 Frontend UI (Running on localhost)

* NoFeeSwap Local Screening Build interface
* MetaMask connection button
* Token balance display
* Transaction feedback panel

### ⚙️ Local Blockchain (Hardhat Node)

* JSON-RPC server running
* Test accounts with ETH
* Private keys generated
* Local chain active

### 💻 Development Environment

* Frontend running on localhost:3000
* Hardhat node running in parallel
* Full integration setup working

---

## 🎥 Demo Video

https://drive.google.com/file/d/1EGn7Y4WiA0c7JcE8xBXVavViasRWYd3W/view

The video demonstrates:

* Local node startup
* Frontend execution
* Contract interaction setup
* Full system workflow

---

## 📢 Transparency Statement

This submission focuses on core system design and integration:

### ✅ Completed

* Local blockchain deployment
* Frontend UI structure
* Wallet integration
* Mempool monitoring bot structure

### ⚠️ Partial

* Swap execution flow
* Liquidity interaction UI
* Profit calculation logic

### ❌ Omitted

* Advanced visualization
* Production-grade MEV strategies

---

## ⚠️ Known Limitations

* Simplified MEV logic
* Limited UI interactivity
* No real network latency/gas competition
* Local-only environment

---

## 🙌 Final Notes

This project demonstrates:

* Understanding of EVM transaction lifecycle
* Mempool monitoring concepts
* Web3 frontend integration
* Off-chain automation design

Happy to walk through:

* Architecture decisions
* Trade-offs
* Improvements

Thank you for the opportunity.

[1]: https://chainstack.com/a-developers-guide-to-the-transactions-in-mempool-code-edition/?utm_source=chatgpt.com "Blockchain Transactions in Ethereum Mempool - Coding Edition"
[2]: https://github.com/derekzuk/mev-bot?utm_source=chatgpt.com "GitHub - derekzuk/mev-bot: MEV bot to automate sending and tracking NFT mint transactions from an array of wallets"
