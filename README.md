# Lyraverse Documentation

> Complete guide to using Lyraverse - Your NFT platform on Hyperliquid

[![Lyraverse](https://img.shields.io/badge/Lyraverse-Hyperliquid-blue)](https://lyraverse.io)
[![Platform](https://img.shields.io/badge/Platform-Web3-green)](https://lyraverse.io)

## 📋 Table of Contents

- [🚀 Getting Started](#-getting-started)
- [🎨 Creating NFT Collections](#-creating-nft-collections)
- [⚡ Minting NFTs](#-minting-nfts)
- [🏪 Marketplace](#-marketplace)
- [👤 Profile Management](#-profile-management)
- [🏛️ DAO Features](#️-dao-features)
- [💰 Royalties](#-royalties)
- [🔍 Rarity System](#-rarity-system)
- [❓ FAQ](#-faq)
- [🔧 Troubleshooting](#-troubleshooting)

---

## 🚀 Getting Started

### What is Lyraverse?

Lyraverse is a comprehensive NFT platform built on **Hyperliquid**, featuring:

- **Collection Creation**: Simple and advanced NFT collection creation
- **Multi-Phase Minting**: Public and whitelist minting phases
- **Marketplace**: Buy and sell NFTs with HYPE tokens
- **DAO Integration**: Decentralized governance for collections
- **Wallet Integration**: Seamless Hyperliquid wallet connection

### Connecting Your Wallet

1. **Install a Web3 Wallet**: MetaMask, Coinbase Wallet, or any Hyperliquid-compatible wallet
2. **Connect to Hyperliquid Network**: Ensure your wallet is connected to the Hyperliquid testnet
3. **Connect to Lyraverse**: Click "Connect Wallet" in the top-right corner
4. **Authorize**: Approve the connection in your wallet

> 💡 **Tip**: Lyraverse works exclusively with Hyperliquid for maximum speed and low fees.

---

## 🎨 Creating NFT Collections

### Simple Mode (Recommended for beginners)

1. **Navigate to Create**: Go to `/create` page
2. **Fill Basic Info**:
   - Collection name
   - Description
   - Upload collection image (recommended: 1000x1000px)
3. **Set Parameters**:
   - Mint price in HYPE
   - Total supply (max 10,000)
   - Royalties (0-25%)
4. **Create Collection**: Click "Create Collection"

### Advanced Mode (For complex drops)

1. **Enable Advanced Mode**: Toggle "Advanced Collection"
2. **Configure Multiple Phases**:
   - **Public Phase**: Open to everyone
   - **Whitelist Phase**: Limited to authorized addresses
3. **Phase Settings**:
   - Start/End dates
   - Price per phase
   - Max mints per wallet
   - Reserve amounts

### Phase Management

```typescript
// Example phase configuration
{
  name: "Public Sale",
  mintPrice: "1000000000000000000", // 1 HYPE
  maxPerWallet: 5,
  startTime: 1640995200, // Unix timestamp
  endTime: 1641081600,
  reserveAmount: 1000
}
```

### Collection Images

- **Format**: PNG, JPG, GIF (max 10MB)
- **Recommended Size**: 1000x1000px for square collections
- **Banner**: Optional 1920x1080px banner image

---

## ⚡ Minting NFTs

### Finding Collections to Mint

1. **Browse Collections**: Visit `/collections` or `/mint`
2. **Filter by Status**:
   - 🟢 **Live**: Currently minting
   - 🟡 **Soon**: Upcoming mint
   - 🔴 **Sold Out**: Completed

### Minting Process

1. **Select Collection**: Click on any live collection
2. **Choose Quantity**: Select 1-10 NFTs (depending on collection limits)
3. **Connect Wallet**: Ensure your Hyperliquid wallet is connected
4. **Approve Transaction**: Confirm the mint transaction
5. **Wait for Confirmation**: Transaction completes in ~3-5 seconds on Hyperliquid

### Understanding Mint Phases

#### Public Phase
- Open to all users
- First-come, first-served
- Usually higher price

#### Whitelist Phase
- Invitation-only
- Lower price as reward
- Limited spots

### Mint Limits

- **Per Wallet**: Set by collection creator (usually 1-10)
- **Per Transaction**: Max 10 NFTs at once
- **Time Windows**: Phases have specific start/end times

---

## 🏪 Marketplace

### Buying NFTs

1. **Browse Listings**: Visit `/marketplace`
2. **Filter Results**:
   - By collection
   - By price range
   - By traits
3. **Select NFT**: Click on any listed NFT
4. **Purchase**: Click "Buy for [price] HYPE"
5. **Confirm Transaction**: Approve in your wallet

### Selling NFTs

1. **Navigate to NFT**: Go to your NFT's detail page
2. **List for Sale**: Click "List for Sale" (if you own it)
3. **Set Price**: Enter price in HYPE
4. **Confirm Listing**: Approve the transaction

### Canceling Listings

1. **Go to NFT Page**: Find your listed NFT
2. **Cancel Listing**: Click "Cancel Listing"
3. **Confirm**: Approve the cancellation transaction

### Marketplace Fees

- **Platform Fee**: 2.5% on all sales
- **Creator Royalties**: 0-25% (set by collection creator)
- **Network Fees**: Minimal on Hyperliquid

---

## 👤 Profile Management

### Viewing Your Profile

1. **Access Profile**: Click your avatar or "Profile" in navigation
2. **Profile Sections**:
   - **Overview**: Your stats and activity
   - **NFTs**: NFTs you own
   - **Collections**: Collections you've created
   - **Activity**: Transaction history

### Profile Customization

1. **Edit Profile**: Click "Edit Profile"
2. **Update Info**:
   - Display name
   - Bio
   - Avatar image
   - Social links

### Managing Collections

1. **Go to Collections Tab**: In your profile
2. **Collection Management**:
   - View analytics
   - Update settings
   - Manage DAO (if applicable)

---

## 🏛️ DAO Features

### What is a DAO?

A DAO (Decentralized Autonomous Organization) allows community governance of NFT collections through token voting.

### Creating a DAO

1. **Collection Ownership**: You must own the collection
2. **Navigate to Collection**: Go to your collection page
3. **Create DAO**: Click "Create DAO" in collection actions
4. **Configure Settings**:
   - Voting parameters
   - Treasury management
   - Proposal settings

### DAO Governance

#### Proposal Types
- **Parameter Changes**: Update collection settings
- **Treasury Actions**: Spend or receive funds
- **Minting Decisions**: Adjust future mints

#### Voting Process
1. **Create Proposal**: Submit via DAO interface
2. **Community Voting**: Token holders vote
3. **Execution**: Successful proposals are executed

### Staking NFTs

1. **Stake NFTs**: Lock your NFTs in the DAO
2. **Earn Rewards**: Receive governance tokens
3. **Voting Power**: Increased influence in decisions

---

## 💰 Royalties

### How Royalties Work

- **Creator Royalties**: Percentage of secondary sales paid to creator
- **Platform**: Lyraverse takes 2.5% platform fee
- **Royalties**: Creator receives their set percentage

### Setting Royalties

When creating a collection:
- **Range**: 0-25% (recommended: 5-10%)
- **Why 25% max?**: Protects buyers from "rug pulls"
- **Platform fees**: Separate from royalties

### Royalty Distribution

```
Sale Price: 10 HYPE
Platform Fee (2.5%): 0.25 HYPE
Creator Royalty (10%): 1.0 HYPE
Seller Receives: 8.75 HYPE
```

---

## 🔍 Rarity System

### Understanding Rarity

Lyraverse uses a sophisticated rarity system based on trait frequency:

| Rarity Grade | Threshold | Color | Description |
|-------------|-----------|-------|-------------|
| **Legendary** | ≤ 2% | 🟡 Gold | Ultra rare |
| **Epic** | ≤ 5% | 🟣 Purple | Very rare |
| **Rare** | ≤ 8% | 🟢 Green | Rare |
| **Uncommon** | ≤ 12% | 🔵 Blue | Moderately rare |
| **Common** | > 12% | ⚪ Gray | Common |

### How Rarity is Calculated

1. **Trait Analysis**: System analyzes all minted NFTs in collection
2. **Frequency Counting**: Counts occurrences of each trait value
3. **Percentage Calculation**: Rarity = (trait count / total NFTs) × 100
4. **Ranking**: NFTs ranked by combined trait rarity

### Rarity Visualization

- **Progress Bars**: Colored bars showing rarity percentage
- **Grade Labels**: Text labels (Legendary, Epic, etc.)
- **Hover Effects**: Dynamic border colors based on rarity

---

## ❓ FAQ

### General Questions

**Q: What blockchain does Lyraverse use?**
A: Lyraverse runs exclusively on Hyperliquid for speed and low fees.

**Q: What token do I need?**
A: HYPE tokens for all transactions (minting, buying, selling).

**Q: Are there gas fees?**
A: Minimal network fees on Hyperliquid (much lower than Ethereum).

### Collection Creation

**Q: What's the difference between simple and advanced mode?**
A: Simple mode creates one public minting phase. Advanced mode allows multiple phases with different rules.

**Q: Can I change settings after creation?**
A: Some settings can be modified through DAO governance if enabled.

### Minting

**Q: Why can't I mint?**
A: Check if the collection is live, you have enough HYPE, and haven't reached wallet limits.

**Q: What happens if mint fails?**
A: Funds are returned automatically. Try again or contact support.

### Marketplace

**Q: How long do listings take to appear?**
A: Usually instant, but up to 30 seconds during high network activity.

**Q: Can I trade NFTs directly?**
A: Yes, through the marketplace or direct transfers.

---

## 🔧 Troubleshooting

### Common Issues

#### Wallet Connection Issues
- **Solution**: Refresh page and reconnect wallet
- **Check**: Ensure you're on Hyperliquid network

#### Transaction Stuck
- **Solution**: Wait 2-3 minutes, check Hyperliquid explorer
- **Recovery**: Transactions are final once confirmed

#### Images Not Loading
- **Solution**: Check IPFS gateway, try refreshing
- **Format**: Ensure PNG/JPG under 10MB

#### Minting Limits Reached
- **Check**: Wallet limits per phase
- **Solution**: Wait for next phase or different collection

### Getting Help

1. **Documentation**: This guide (comprehensive help)
2. **Community**: Join Discord for community support
3. **Support**: Contact via email for technical issues

---

## 📞 Support

- **Email**: contact@lyraverse.io
- **Documentation**: You're reading it! 📚
- **Community**: Join our Telegram

---

*Last updated: December 2025*
*Version: 1.0.0*
*Platform: Hyperliquid Network*
