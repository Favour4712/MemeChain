# 🧩 MemeChain
### Decentralized Meme Battles on Base

**MemeChain** is a decentralized, time-limited meme competition platform built on **Base L2**, where communities submit, vote, and collect the best memes on-chain. Winning memes are minted as NFTs, rewards are distributed in tokens, and memecoin communities can battle for sentiment dominance.

This repo contains the smart contracts, frontend, and integration code powering MemeChain.

---

## 🚀 Core Concept

- Memes are submitted into **time-limited battles** (12–24h submissions, 12–24h voting)
- Voting uses **token-weighted influence**
- Winning memes are **minted as NFTs**
- **Prize pools** reward creators + voters
- Optional **memecoin sentiment battles**: token communities compete using memes
- Powered by **Base**: low fees, fast finality, crypto-native UX

---

## 🧠 Platform Features

### ✅ Battle System
- Create time-bound meme battles
- Open theme, memecoin sentiment battles, head-to-head token wars, sponsored contests
- Lifecycle: `UPCOMING → SUBMISSION_OPEN → VOTING_OPEN → TALLYING → FINALIZED → ARCHIVED`

### ✅ Meme Submission
- Upload images → stored on **IPFS** (via Pinata/NFT.Storage/Web3.Storage)
- On-chain reference to CID
- File types: JPG, PNG, GIF, WebP (max ~10MB)

### ✅ Token-Weighted Voting
- Stake or spend tokens to vote
- Vote weight = token amount
- Anti-spam & Sybil resistance
- Votes and tallies on-chain

### ✅ NFTs for Winners
- Winning memes minted as **ERC-721** (1/1)
- Metadata stored on IPFS
- Optional editions and royalties

### ✅ Rewards & Incentives
- Prize pools from platform treasury, submission fees, or sponsors
- Reward split:
  - 1st place – 50%
  - 2nd place – 30%
  - 3rd place – 20%
- (Optional) a share of rewards for voters of winning memes

---

## 🏗 Tech Stack

### Smart Contracts
- Solidity (BattleManager, MemeRegistry, VotingEngine, RewardDistributor, NFT contracts)
- OpenZeppelin standard libraries
- Base Testnet + Mainnet

### Frontend
- React / Next.js
- wagmi + viem / ethers.js
- RainbowKit or ConnectKit for wallet connection
- Tailwind CSS + shadcn/ui
- IPFS upload via NFT.Storage / Pinata

### Integrations
- **Dexscreener API** for memecoin market data (price, charts, sentiment)
- (Optional) Chainlink for on-chain price or oracle logic

---

## 🧪 Local Development

### Requirements
- Node.js (LTS recommended)
- pnpm / npm / yarn
- Hardhat or Foundry
- Base Sepolia testnet wallet + test ETH

### Suggested Project Structure
