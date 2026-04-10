# 🎬 Drishya – Decentralized Film Distribution Platform

Drishya is a **next-generation decentralized film distribution and rental platform** built on the **Ethereum Blockchain**.
It reshapes the relationship between filmmakers and their audience by **removing centralized intermediaries**, ensuring **fair monetization**, and offering a **censorship-resistant home** for creative work.

---

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Powered by: Ethereum Blockchain](https://img.shields.io/badge/Powered%20by-Ethereum%20Blockchain-627EEA?logo=ethereum)
![Deployment: Vercel](https://img.shields.io/badge/Deployment-Vercel-black?logo=vercel)
![Meme Spotlight: Chainlink VRF](https://img.shields.io/badge/Meme%20Spotlight-Chainlink%20VRF-375BD2?logo=chainlink)

---

## 🌟 The Problem

The modern digital media landscape is dominated by centralized platforms that act as **powerful gatekeepers**.
This creates a severe **power imbalance** for independent creators:

- **💸 Extractive Fees** – Platforms often take **30–55%** of revenue with **opaque, delayed payments**.
- **🚫 Censorship & Loss of Control** – Arbitrary “community guidelines” can **deplatform** creators without recourse.
- **🛑 High Barriers to Entry** – Securing distribution deals is a **major hurdle** for many talented filmmakers.
- **⚠ Platform Risk** – Sudden changes in terms of service can **destroy a creator’s livelihood** overnight.

---

## ✨ The Drishya Solution

Drishya solves these problems by leveraging **Web3 technology** and the **Ethereum Blockchain**:

| Feature | Benefit |
|---------|---------|
| **🎥 Creator Sovereignty** | Immutable smart contracts remove Drishya as the intermediary. |
| **⚡ Fair & Instant Payments** | 90% of rental revenue paid instantly to creators’ wallets. |
| **🛡 Censorship Resistance** | Films stored on IPFS via specialized storage solutions – resilient & tamper-proof. |
| **🌍 Permissionless Access** | Anyone can upload films and monetize globally. |
| **🎁 Community Rewards** | Participate in the **Meme Spotlight** to win a 20% rental discount. |

---

## 🚀 Key Features

- **Dual-Portal Architecture**
  - 🎬 **Creator Portal** – Upload films, manage profiles, track on-chain earnings in real time.
  - 🍿 **Viewer Portal** – Discover, rent, and watch indie films with a **modern streaming experience**.

- **Web3-First Design**
  - Decentralized storage (IPFS + Pinata fallback)
  - Automated smart contract rental lifecycle
  - Wallet-based identity (MetaMask, RainbowKit)

- **New Feature: Meme Spotlight**
  -The Meme Spotlight feature is a blockchain-based system that randomly selects a winning meme in a fair, transparent, and verifiable way using Chainlink VRF (Verifiable Random Function).

  - **User-Submitted Memes:** Viewers can upload relevant memes *free of cost* for community enjoyment.
  - **Random Selection:** The platform **admin** can trigger the **Spotlight of the Day** to randomly select a winning meme.
  - **Decentralized Randomness:** The selection process uses **Chainlink VRF (Verifiable Random Function)** for provably fair, tamper-proof randomness.
  - **Reward:** The creator of the selected meme wins a **20% discount** on their next film rental transaction.

  -**HOW IT WORKS**
   -**Request Randomness:**The smart contract sends a request to Chainlink VRF.
   -**VRF Fulfillment:**Chainlink VRF generates a secure random number. It sends request back to smart contract via callback function.
   -**Winner Selection:**Smart contract uses random number to select a meme from pool and declare it as spotlight winner.

  -**Required Configuration:**
    -**1.VRF Coordinator Address:** This is Chainlink  VRF contract address for your network.
    -**2.Subscription ID:** It is created from Chainlink VRF to pay for randomness request.
    -**3.Key Hash(gas lane):** Controls maximum gas price for requests.
    -**4.Callback Gas Limit:**Maximum gas allowed for the VRF callback function.
    -**5.Request Confirmations:**Number of block confirmations before VRF responds.

  -**Official Documentation:**
      For more details on setup and configuration, refer to the official Chainlink documentation
      For more details:
      - Learn how VRF works in the [official Chainlink VRF docs](https://docs.chain.link/vrf/v2-5/getting-started)
      - Create and manage subscriptions using the [VRF Subscription Manager](https://vrf.chain.link/)
      - See implementation examples in the [VRF examples guide](https://docs.chain.link/vrf/v1/examples/get-a-random-number)

  -**Setup & Integration:**
   -1.Create a VRF Subscription:
     -[Go to the Chainlink VRF Subscription Manager](https://vrf.chain.link/)
     -Connect your wallet and create new subscription.

   -2.Fund the Subscription:  
    -Add link tokens to your subscription.

   -3.Add Your Contract as Consumer
    -After deploying, add its address to VRF subscription as consumer.
   
   -4.Configure Contract Parameters
   -5.Deploy the Smart Contract:
    -use your preferred environment(Hardhat, Foundry)
   -6.Trigger Meme Spotlight:
    -Call the required functions in your contract.


- **Modern UI/UX**
  - Built with **Next.js**, **Tailwind CSS**, **Framer Motion**, **shadcn/ui**
  - Fully **responsive** and **mobile-friendly**

---

## 🛠 Tech Stack & Tools

**Frontend**
- Framework: `Next.js (React)`
- Styling: `Tailwind CSS`
- UI Components: `shadcn/ui`
- Animations: `Framer Motion`

**Web3 Integration**
- Blockchain: `Ethereum`
- Wallet: `RainbowKit`
- Contract Interaction: `wagmi`, `viem`
- Randomness: `Chainlink VRF`

**Smart Contract**
- Language: `Solidity`
- Dev Environment: `Hardhat` / `Foundry`

**Storage**
- Primary: `IPFS (via specialized SDK/Gateway)`
- Fallback: `Pinata`

**Deployment**
- Platform: `Vercel`

---

## 🏁 Getting Started

### 📋 Prerequisites
- Node.js v18+
- `pnpm` / `npm` / `yarn`
- Web3 wallet (e.g., MetaMask)

### 📦 Installation
```bash
# Clone the repository
git clone [https://github.com/your-username/Drishya.git](https://github.com/your-username/Drishya.git)
cd Drishya

# Install dependencies
pnpm install
