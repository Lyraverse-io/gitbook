# How Minting Works

Complete guide to minting NFTs on Lyraverse.

## Minting Basics

### What is Minting?
Minting is the process of creating new NFTs from a collection's smart contract. Each mint:
- Creates a unique token on the blockchain
- Assigns metadata (image, attributes, etc.)
- Transfers ownership to the minter
- Costs the defined mint price in HYPE

### Minting Process Overview

1. **Find Collection**: Browse live collections
2. **Select Quantity**: Choose 1-10 NFTs
3. **Pay Price**: Approve transaction
4. **Receive NFTs**: Instant ownership
5. **View in Wallet**: NFTs appear immediately

## Finding Collections to Mint

### Collection Discovery
- **Browse Page**: `/collections` - All collections
- **Mint Page**: `/mint` - Currently minting only
- **Marketplace**: `/marketplace` - Listed NFTs

### Collection Status
- 🟢 **Live**: Actively minting
- 🟡 **Soon**: Upcoming mint
- 🔴 **Sold Out**: Mint completed
- ⏸️ **Paused**: Temporarily stopped

### Filtering Options
- **By Category**: Art, Gaming, Collectibles, etc.
- **By Price**: Budget-friendly to premium
- **By Popularity**: Trending collections
- **By Creator**: Follow favorite artists

## Understanding Mint Phases

### Phase Types

#### Public Phase
```
Access: Open to everyone
Timing: Flexible schedule
Price: Standard collection price
Limits: Per-wallet restrictions only
Best For: Broad community access
```

#### Whitelist Phase
```
Access: Invitation-only
Timing: Strict time windows
Price: Discounted (reward early supporters)
Limits: Additional whitelist restrictions
Best For: Building exclusive communities
```

### Phase Progression
```
Collection Launch → Whitelist Phase → Public Phase → Sold Out
                    ↓
              Early Access (Lower Price)
```

## Step-by-Step Minting Guide

### 1. Prepare Your Wallet
```javascript
// Ensure you have:
- Connected Hyperliquid-compatible wallet
- Sufficient HYPE tokens for minting
- Small amount for network fees
```

### 2. Find a Collection
1. Navigate to collection page
2. Verify "Live" status
3. Check minting requirements
4. Review collection details

### 3. Access Mint Interface
1. Click "Mint" tab on collection page
2. View current phase information
3. Check your eligibility status
4. Review pricing and limits

### 4. Configure Mint
```javascript
// Mint Settings:
Quantity: 1-10 NFTs (based on collection limits)
Total Cost: price × quantity + network fees
Estimated Time: 3-5 seconds on Hyperliquid
```

### 5. Execute Mint
1. Click "Mint X NFT(s)" button
2. Review transaction details
3. Approve in wallet popup
4. Wait for confirmation
5. Receive success notification

### 6. Verify Ownership
1. Check wallet for new NFTs
2. View in Lyraverse profile
3. Confirm transaction on explorer

## Mint Limits and Restrictions

### Per-Wallet Limits
- Set by collection creator
- Usually 1-10 NFTs per wallet
- Applies per phase
- Resets between phases

### Phase-Specific Rules
- **Whitelist**: Additional allocation limits
- **Public**: Standard wallet limits only
- **Reserve**: Creator/team allocations

### Time-Based Restrictions
- Phases have start/end times
- No minting outside active windows
- Automatic phase transitions

## Pricing and Fees

### Mint Cost Breakdown
```
Base Price: Set by collection creator
Quantity: Your selected amount
Subtotal: price × quantity
Network Fee: Minimal Hyperliquid fee
Total: subtotal + network_fee
```

### Fee Examples
```
1 NFT at 1 HYPE: ~1.0001 HYPE total
5 NFTs at 0.5 HYPE: ~2.5005 HYPE total
10 NFTs at 0.1 HYPE: ~1.001 HYPE total
```

## Mint Success and Verification

### Success Indicators
- ✅ Transaction confirmed on blockchain
- ✅ NFTs appear in your wallet
- ✅ Profile updated with new NFTs
- ✅ Collection supply updated

### Verification Steps
1. **Wallet Check**: NFTs visible in wallet
2. **Profile Check**: New NFTs in "My NFTs"
3. **Transaction Hash**: Viewable on explorer
4. **Collection Stats**: Supply counter updated

## Common Minting Scenarios

### Successful Mint
```
✅ Wallet connected
✅ Sufficient balance
✅ Within phase limits
✅ Valid timing
✅ Transaction approved
→ Mint successful!
```

### Failed Mint Scenarios

#### Insufficient Balance
```
❌ Error: "Insufficient HYPE balance"
✅ Solution: Add HYPE to wallet
```

#### Phase Not Active
```
❌ Error: "Minting not available"
✅ Solution: Wait for phase to start
```

#### Wallet Limits Exceeded
```
❌ Error: "Max mints per wallet reached"
✅ Solution: Use different wallet or wait for next phase
```

#### Network Issues
```
❌ Error: "Transaction failed"
✅ Solution: Retry with higher gas or check network
```

## Advanced Minting Strategies

### Timing Optimization
- **Early Access**: Join whitelist phases
- **Price Changes**: Monitor phase transitions
- **Supply Tracking**: Watch remaining NFTs

### Quantity Planning
- **Single Mints**: Test collections safely
- **Bulk Mints**: Save on network fees
- **Portfolio Building**: Diversify across collections

### Cost Optimization
- **Network Timing**: Mint during low congestion
- **Bulk Efficiency**: Multiple NFTs = better fee ratio
- **Phase Planning**: Cheaper whitelist vs public

## Minting Best Practices

### Preparation
- ✅ Research collection thoroughly
- ✅ Check wallet balance
- ✅ Verify whitelist eligibility
- ✅ Have backup wallet ready

### During Mint
- ✅ Double-check transaction details
- ✅ Ensure sufficient gas allocation
- ✅ Keep wallet popup open
- ✅ Don't refresh page mid-transaction

### After Mint
- ✅ Verify NFT receipt
- ✅ Save transaction hash
- ✅ Update portfolio tracking
- ✅ Follow collection announcements

## Troubleshooting Mint Issues

### Transaction Stuck
- **Wait Time**: 2-3 minutes maximum
- **Check Explorer**: Verify on Hyperliquid explorer
- **Contact Support**: If truly stuck

### Wrong NFTs Received
- **Check Contract**: Verify correct collection
- **Contact Creator**: For metadata issues
- **Report Bug**: If systematic problem

### Access Denied
- **Whitelist Check**: Verify inclusion
- **Timing Check**: Confirm phase is active
- **Wallet Check**: Ensure correct address

---

**Ready to mint?** Find your next favorite collection and start collecting! 🚀
