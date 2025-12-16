# Selling NFTs

Complete guide to listing and selling your NFTs on the Lyraverse marketplace.

## Getting Started

### Prerequisites
- ✅ **NFT Ownership**: Own the NFT you want to sell
- ✅ **Wallet Connected**: Hyperliquid-compatible wallet
- ✅ **Marketplace Access**: Navigate to NFT detail page
- ✅ **Gas Fees**: Small amount for listing transactions

### Access Points
1. **NFT Detail Page**: "List for Sale" button
2. **Profile Dashboard**: Bulk listing options
3. **Collection Page**: Quick listing for owned NFTs

## Creating a Listing

### Step-by-Step Process

#### 1. Navigate to NFT
```typescript
// Go to NFT detail page
/nfts/{contractAddress}/{tokenId}
```

#### 2. Initiate Listing
- **Click "List for Sale"**: Opens listing modal
- **Verify Ownership**: System confirms NFT ownership
- **Check Approvals**: Marketplace contract approval status

#### 3. Set Listing Parameters
```json
{
  "price": "2000000000000000000",    // Price in wei (2 HYPE)
  "currency": "HYPE",                // Only HYPE supported
  "duration": null,                  // No expiration on Lyraverse
  "royalties": 5                     // Creator royalty percentage
}
```

#### 4. Confirm Listing
- **Review Details**: Price, fees, royalties
- **Estimate Gas**: Transaction cost preview
- **Sign Transaction**: Approve listing creation

### Listing Types

#### Fixed Price Listing
- **Set Price**: Fixed HYPE amount
- **Instant Sale**: Immediate purchase possible
- **No Expiration**: Listing remains active until sold/cancelled

#### Auction Listing (Coming Soon)
- **Starting Price**: Minimum bid amount
- **Duration**: Auction time period
- **Reserve Price**: Hidden minimum price

## Managing Listings

### Active Listings View
1. **Profile Page**: "My Listings" section
2. **Dashboard**: Overview of all active listings
3. **Collection Filter**: View listings by collection

### Listing Analytics
```json
{
  "views": 1250,
  "favorites": 45,
  "offers": 8,
  "timeListed": "7 days",
  "estimatedValue": "2.1 HYPE"
}
```

## Pricing Strategy

### Setting the Right Price

#### Research Market Value
- **Floor Price**: Collection minimum price
- **Recent Sales**: Similar NFT transaction history
- **Rarity Factor**: Adjust based on NFT rarity
- **Market Trends**: Overall NFT market conditions

#### Pricing Examples
```
Common NFT: Floor price = 1.5 HYPE → List at 1.8 HYPE
Rare NFT: Floor price = 5 HYPE → List at 6.5 HYPE
Legendary NFT: Floor price = 50 HYPE → List at 65 HYPE
```

### Dynamic Pricing
- **Start Higher**: Price above floor for negotiation room
- **Gradual Reduction**: Lower price if no sales
- **Market Adjustment**: Update based on collection performance

## Offers and Negotiation

### Receiving Offers
- **Offer Notifications**: Real-time offer alerts
- **Offer Management**: View all offers on NFT
- **Counter Offers**: Propose different terms

### Accepting Offers
1. **Review Offer**: Check buyer, price, conditions
2. **Accept Transaction**: Confirm sale
3. **Automatic Transfer**: NFT moves to buyer wallet

### Declining Offers
- **Soft Decline**: No response (offer expires)
- **Hard Decline**: Explicit rejection
- **Counter Offer**: Propose alternative price

## Transaction Process

### Sale Completion
```
1. Buyer initiates purchase
2. Smart contract verification
3. Payment transfer (HYPE)
4. Royalty payment (automatic)
5. Platform fee deduction
6. NFT transfer to buyer
7. Listing automatically removed
```

### Fee Structure
```
Sale Price: 10 HYPE
Platform Fee: 2.5% = 0.25 HYPE
Creator Royalty: 5% = 0.5 HYPE
Seller Receives: 9.25 HYPE
```

## Advanced Selling Features

### Bulk Listing
- **Multiple NFTs**: List several NFTs simultaneously
- **Batch Operations**: Set prices for entire collection
- **Automated Pricing**: Algorithm-based price suggestions

### Collection Management
- **Collection Floor**: Maintain above collection floor
- **Portfolio Strategy**: Balance across different rarities
- **Market Timing**: Optimal selling periods

## Optimizing Sales

### NFT Presentation
- **High-Quality Images**: Best possible NFT display
- **Detailed Description**: Compelling NFT story
- **Trait Highlighting**: Emphasize rare attributes

### Timing and Strategy
- **Peak Hours**: List during high activity periods
- **Market Momentum**: Sell during positive trends
- **Holder Engagement**: Build community around NFT

### Marketing Tactics
- **Social Sharing**: Promote listing on social media
- **Community Forums**: Post in relevant Discord channels
- **Cross-Platform**: List on multiple marketplaces

## Troubleshooting Sales

### Common Issues

#### Listing Not Appearing
**Issue**: "NFT listed but not showing in marketplace"
**Solutions**:
- Wait for indexer sync (2-3 minutes)
- Check transaction confirmation
- Verify contract approval status

#### Sale Not Processing
**Issue**: "Buyer paid but NFT not transferred"
**Solutions**:
- Check transaction status on explorer
- Contact support with transaction hash
- Verify wallet balance and allowances

#### Incorrect Pricing
**Issue**: "Listed at wrong price"
**Solutions**:
- Cancel current listing
- Create new listing with correct price
- Double-check price input format

## Analytics and Insights

### Seller Dashboard
- **Sales History**: Past transaction records
- **Revenue Tracking**: Total earnings over time
- **Performance Metrics**: Average sale price, time to sell

### Market Intelligence
- **Price Trends**: Historical price movements
- **Buyer Behavior**: Popular price points and timing
- **Competition Analysis**: How your listings compare

## Legal and Tax Considerations

### Seller Obligations
- **Ownership Verification**: Prove legitimate NFT ownership
- **Transfer Rights**: Ensure NFT can be legally transferred
- **Platform Terms**: Comply with marketplace rules

### Tax Reporting
- **Capital Gains**: Report profits from NFT sales
- **Record Keeping**: Maintain detailed transaction records
- **Jurisdiction**: Follow local tax regulations

## Best Practices

### For New Sellers
- **Start Small**: Begin with one or two NFTs
- **Research Pricing**: Study similar sales extensively
- **Patient Approach**: Don't rush into low offers

### For Experienced Sellers
- **Portfolio Management**: Diversify across collections
- **Market Timing**: Understand optimal selling windows
- **Relationship Building**: Network with potential buyers

### General Tips
- **Professional Communication**: Respond promptly to inquiries
- **Fair Pricing**: Set realistic expectations
- **Continuous Learning**: Study successful selling strategies

## Future Developments

### Planned Features
- **Advanced Auctions**: Dutch and English auction support
- **Scheduled Listings**: Set future listing times
- **Automated Selling**: AI-powered pricing optimization
- **Cross-Marketplace**: Unified multi-platform selling

---

**Master the art of NFT selling and maximize your returns!** 💰🚀
