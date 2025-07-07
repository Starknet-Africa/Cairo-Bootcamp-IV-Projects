# Obscura

## 🧠 Project Description

**Obscura** is a shielded UTXO pool for Starknet enabling private, anonymous asset transfers via zero-knowledge cryptography.  
It acts as a privacy-preserving layer that abstracts sensitive user information and transactions, using NOIR to ensure secure, unlinkable transfers on Starknet.  
The goal is to provide Ethereum-like privacy infrastructure to Starknet users through a simple, intuitive interface.

## 🧪 Project Category

DeFi / Privacy / ZK

## 🌐 Project Link

🔗 [https://obscura-app.vercel.app](https://obscura-app.vercel.app)

## 🧑‍💻 Project Codebase

💻 [https://github.com/truthixify/obscura](https://github.com/truthixify/obscura)  

## 📹 Project Video

🎥 [https://www.youtube.com/watch?v=vVEz_tNnDgM](https://www.youtube.com/watch?v=vVEz_tNnDgM)

## 📋 Tech Stack

- **Starknet** — for building and deploying Cairo contracts
- **Noir** — for writing the ZK circuit
- **Garaga** - for generating Cairo smart contract verifier for the Noir circuit 
- **Scaffold Stark** - project bootstrap
- **React + Vite** — frontend app
- **TypeScript** — frontend language
- **Node.js / Express** — backend integration for paymaster and account handling
- **MongoDB** — to store shielded account metadata
- **Avnu Paymaster API** — to handle sponsored transactions

## 🔐 Features

- Anonymous deposits and withdrawals using UTXOs
- Shielded balances, unlinkable to original wallet address
- Paymaster integration for gasless transactions
- Zero-knowledge proof verification (client-side + contract-side)
- Clean UI/UX to handle shielded transactions easily

## 🚧 Future Improvements

- ✨ Full integration of **paymaster flow** for sponsored gasless transactions
- 🎨 UI/UX overhaul for improved privacy experience and onboarding
- 🧪 More robust circuit testing and edge case handling
- 🔄 Multi-asset pool support and token wrapping integration

## 👤 Author

- **truthixify** — [@truthixify](https://github.com/truthixify)

---

> **Note:** Submission for Cairo Bootcamp IV — July 2025.