# contract-sui

A **voting smart contract** built and deployed on the **Sui blockchain** using the **Move programming language**.  
This project demonstrates how to design, publish, and interact with a Sui Move smart contract via the **Sui CLI**, with a frontend intended to be built using **React + TypeScript**.

---

## Project Overview

This repository contains the Move smart contract logic for a decentralized voting application on Sui. The contract allows users to interact with on-chain voting logic in a secure, object-oriented way using Sui’s ownership and object model.

### Key Features
- Written in **Move (Sui flavor)**
- Deployed to the **Sui network**
- CLI-based interaction using `sui client`
- Designed to integrate with a **React + TypeScript frontend**
- Includes tests for contract logic

---

## Project Structure

```text
contract-sui/
├── sources/          # Move smart contract source files
├── tests/            # Move unit tests
├── Move.toml         # Move package configuration
├── Move.lock         # Dependency lock file
├── Published.toml    # Published package IDs per network
├── .gitignore
└── README.md
```
---

## Prerequisites

Before setting up the project, ensure you have the following installed:

- Rust (required by Sui)

- Sui CLI

## Install Sui CLI

```bash
cargo install --locked --git https://github.com/MystenLabs/sui.git --branch main sui

```

**Verify Installation**

```bash
sui --version
```

## Sui Wallet Setup

1. Initialize a new wallet

```bash
sui client new-address ed25519
```

2. set the active address

```bash
sui client switch --address <YOUR_ADDRESS>
```

3. Request testnet token from SUI faucet

```bash
sui client faucet
```

4. Confirm balance

```bash
sui client balance
```

## Build & Publish the Smart Contract

1. Build the Move package

```bash
sui move build

```

2. Publish to the network

```bash
sui move publish
```

After publishing, the package ID will be stored in:

```bash
Published.toml
```

Example:
```bash
[testnet]
package_id = "0x123..."
published_at = "0x123..."

```


