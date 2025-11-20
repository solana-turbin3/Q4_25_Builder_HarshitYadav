# Decentralized Lend and Borrow System

A secure, transparent, and user-friendly decentralized finance (DeFi) protocol built on the Solana blockchain for seamless lending and borrowing of digital assets.

---

## Project Documentation & Diagrams

The following documents and diagrams were **created specifically for this project** to support its design, planning, and implementation:

* SRS Document:
  [https://drive.google.com/file/d/1xaPzXe70YgVkHRmb8qAa3M_LEVi3Chnu/view?usp=sharing](https://drive.google.com/file/d/1xaPzXe70YgVkHRmb8qAa3M_LEVi3Chnu/view?usp=sharing)
* System Diagrams & Architecture (Excalidraw):
  [https://excalidraw.com/#json=v0vRE3XmlTIUKHpM3PTWY,B6AK6g6iPVOS5lKNkk4FFQ](https://excalidraw.com/#json=v0vRE3XmlTIUKHpM3PTWY,B6AK6g6iPVOS5lKNkk4FFQ)

---

## Overview

The Decentralized Lend and Borrow System allows users to lend their crypto assets to earn interest or borrow liquidity by providing collateral, all without traditional financial intermediaries. The system leverages Solana's high-speed and low-cost infrastructure along with smart contracts built using the Anchor framework to ensure automation, transparency, and security.

Users interact with the platform through an intuitive web interface connected to their wallets, allowing them to manage deposits, loans, and repayments efficiently.

---

## Key Features

* Trustless lending and borrowing
* Collateral-backed loan mechanism
* Simple interest calculation (current implementation)
* Secure PDA-based account architecture
* Real-time wallet connectivity
* Modular and scalable design

---

## System Architecture

### On-Chain Program

Developed using Rust and the Anchor framework, the on-chain program manages all critical protocol logic, including:

* Treasury initialization and configuration
* Liquidity deposits and withdrawals
* Borrowing and loan lifecycle management
* Interest computation (simple model for now)
* Repayment and liquidation handling

Program Derived Addresses (PDAs) are used to guarantee secure and deterministic state management across the protocol.

### Off-Chain Interface

The front-end interface is built with React and TypeScript, providing smooth interaction with the blockchain via:

* @solana/web3.js
* Anchor client libraries
* Solana Wallet Adapter

Supported wallets include Phantom, Solflare, and Backpack, ensuring accessibility for a wide range of users.

---

## User Roles

| Role               | Responsibility                         |
| ------------------ | -------------------------------------- |
| Liquidity Provider | Supplies tokens and earns interest     |
| Borrower           | Provides collateral to borrow assets   |
| Protocol Admin     | Manages treasury and system parameters |
| Liquidator         | Handles liquidation of risky positions |
| Auditor            | Reviews protocol operations and logic  |

---

## Technology Stack

* Blockchain: Solana (Devnet and Mainnet)
* Smart Contracts: Rust + Anchor
* Frontend: React + TypeScript
* Wallets: Phantom, Solflare, Backpack
* Oracles: Pyth / Switchboard (Optional)
* Development Tools: Solana CLI, Anchor CLI, GitHub Actions

---

## Installation and Setup

### Prerequisites

* Node.js
* Solana CLI
* Anchor Framework
* Solana-compatible wallet (Phantom recommended)

### Steps

```bash
# Clone the repository
git clone <repository-url>

# Install dependencies
npm install

# Build the Solana program
anchor build

# Deploy to Devnet
anchor deploy

# Run the frontend application
npm start
```

---

## Usage Flow

1. Connect your wallet
2. Deposit tokens as liquidity or lock collateral
3. Borrow assets within allowed LTV ratio
4. Repay borrowed funds with interest
5. Withdraw funds at any time

---

## Security Measures

* PDA and signer validation
* Ownership and access verification
* Rent-exempt account enforcement
* Oracle-based price validation
* SPL Token standard compliance

---

## Future Enhancements

* Implementation of compound interest algorithms
* Advanced risk assessment model
* DAO-based governance integration
* Real-time analytics dashboard
* Automated liquidation bots

---

## Version

Current Version: 1.0

---

## Author

Harshit Yadav

---

## License

This project is developed strictly for academic and research purposes under institutional guidelines.

---

For issues, suggestions, or contributions, feel free to open an issue or submit a pull request. Your feedback is always welcome.
