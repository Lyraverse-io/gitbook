# Royalties System

Complete guide to creator royalties and secondary sales revenue on Lyraverse.

## Understanding Royalties

### What are Royalties?
Royalties are automatic payments made to NFT creators every time their NFTs are sold on the secondary market. They ensure creators continue to benefit from their work's long-term success.

### How Royalties Work
```
Original Sale: Creator receives 100% (minus platform fees)
Secondary Sale: Creator receives royalty percentage
Example: 5% royalty on 10 HYPE sale = 0.5 HYPE to creator
```

## Royalty Implementation

### Smart Contract Level
Royalties are enforced at the smart contract level, ensuring:
- **Automatic Payment**: No manual intervention required
- **Guaranteed Execution**: Built into every sale transaction
- **Immutable Enforcement**: Cannot be bypassed or modified

### Royalty Standards
Lyraverse follows **EIP-2981** royalty standard:
```solidity
interface IERC2981 {
    function royaltyInfo(uint256 tokenId, uint256 salePrice)
        external view returns (address receiver, uint256 royaltyAmount);
}
```

## Setting Royalties

### During Collection Creation
```json
{
  "royaltyPercentage": 5,        // 5% of secondary sales
  "royaltyRecipient": "0x1234...abcd",  // Creator's address
  "maximumRoyalties": 25        // Platform limit for user protection
}
```

### Royalty Range
- **Minimum**: 0% (no royalties)
- **Maximum**: 25% (platform enforced limit)
- **Recommended**: 5-10% (industry standard)
- **Why 25% max?**: Protects buyers from "royalty rug pulls"

### Recipient Configuration
- **Single Address**: All royalties go to one wallet
- **Split Recipients**: Distribute across multiple addresses
- **Smart Contract**: Send to DAO treasury or splitter contract

## Royalty Distribution

### Fee Breakdown Example
```
Sale Price: 10 HYPE
Platform Fee: 2.5% = 0.25 HYPE
Creator Royalty: 5% = 0.5 HYPE
Seller Receives: 9.25 HYPE
Creator Receives: 0.5 HYPE (royalty) + 10 HYPE (initial sale) = 10.5 HYPE total
```

### Multiple Sales Impact
```
Initial Sale: Creator gets 10 HYPE
Sale #1: Creator gets 0.5 HYPE (5% of 10 HYPE)
Sale #2: Creator gets 0.5 HYPE (5% of 10 HYPE)
Sale #3: Creator gets 0.5 HYPE (5% of 10 HYPE)
Total Creator Earnings: 10 + 0.5 + 0.5 + 0.5 = 11.5 HYPE
```

## Royalty Management

### Viewing Royalty Earnings
1. **Collection Dashboard**: Access creator analytics
2. **Royalty History**: Track all royalty payments
3. **Total Earnings**: Combined primary + secondary revenue
4. **Payment Status**: Confirmed on-chain transactions

### Updating Royalties
- **Creation Only**: Royalties set at collection deployment
- **Immutable**: Cannot be changed after creation
- **Planning Required**: Choose percentage carefully
- **Legal Compliance**: Consider jurisdiction requirements

## Platform Fee Structure

### Marketplace Fees
- **Primary Sales**: 0% (royalties only)
- **Secondary Sales**: 2.5% platform fee
- **Why Fees?**: Platform maintenance and development

### Fee Distribution
```
Platform Fee Breakdown:
- 40%: Development & Operations
- 30%: Marketing & User Acquisition
- 20%: Community & Ecosystem
- 10%: Reserve & Future Growth
```

## Royalty Best Practices

### Setting the Right Percentage

#### For New Creators
- **Start Low**: 2-3% for early adoption
- **Build Community**: Focus on utility over royalties
- **Gradual Increase**: Raise as collection proves value

#### For Established Creators
- **Industry Standard**: 5-7% for proven collections
- **Value-Based**: Higher for unique/artistic works
- **Market Competition**: Match similar successful collections

### Maximizing Royalty Revenue

#### Collection Value
- **Utility**: NFTs with ongoing utility earn more
- **Community**: Strong holder engagement drives sales
- **Scarcity**: Limited supply increases demand

#### Market Timing
- **Initial Hype**: High volume immediately after launch
- **Sustained Value**: Long-term holder retention
- **Market Conditions**: Benefit from NFT market growth

## Legal Considerations

### Copyright and Ownership
- **Creator Rights**: Royalties don't affect copyright
- **License Grants**: Commercial usage rights
- **Derivative Works**: Creator maintains original rights

### Tax Implications
- **Report Royalties**: Treat as business income
- **Jurisdiction**: Follow local tax laws
- **Professional Advice**: Consult tax professionals
- **Record Keeping**: Maintain detailed transaction records

## Troubleshooting Royalties

### Royalties Not Received
**Issue**: "Didn't receive royalties from sale"
**Solutions**:
- Check royalty percentage setting
- Verify recipient address
- Confirm sale was on Lyraverse marketplace
- Wait for indexer sync (2-3 minutes)

### Incorrect Royalty Amount
**Issue**: "Received less than expected"
**Solutions**:
- Verify royalty percentage in collection settings
- Check for platform fee deductions
- Confirm sale price calculation
- Contact support with transaction details

### Royalty Address Issues
**Issue**: "Royalties going to wrong address"
**Solutions**:
- Verify recipient address during creation
- Update via collection management (if available)
- Use multi-sig for shared royalties
- Contact support for address changes

## Advanced Royalty Features

### Split Royalties
```json
{
  "royaltySplits": [
    {"address": "0x1234...creator", "percentage": 70},
    {"address": "0x5678...artist", "percentage": 20},
    {"address": "0x9abc...community", "percentage": 10}
  ]
}
```

### DAO Treasury Royalties
- **Community Control**: Royalties go to DAO treasury
- **Proposal-Based Spending**: Community decides fund allocation
- **Transparent Governance**: Public treasury management

### Dynamic Royalties
- **Time-Based**: Decrease over time
- **Volume-Based**: Adjust based on sales volume
- **Holder-Based**: Different rates for different holders

## Royalty Analytics

### Creator Dashboard Metrics
- **Total Royalties Earned**: Cumulative royalty income
- **Average Royalty Rate**: Effective rate across sales
- **Top Performing NFTs**: Highest royalty-generating pieces
- **Geographic Distribution**: Sales by region/country

### Performance Insights
- **Royalty Velocity**: How quickly royalties are earned
- **Holder Retention**: Impact on long-term holding
- **Market Performance**: Royalty correlation with floor price

## Industry Comparison

### Royalty Standards by Platform
```
OpenSea: 0-10% (no maximum enforced)
Rarible: 0-50% (flexible)
Foundation: 10% (fixed)
Lyraverse: 0-25% (buyer protection)
```

### Creator Earnings Examples
```
Collection A (5% royalty):
- 1000 sales at 1 HYPE = 50 HYPE royalties

Collection B (10% royalty):
- 500 sales at 2 HYPE = 100 HYPE royalties

Collection C (1% royalty):
- 10000 sales at 0.5 HYPE = 50 HYPE royalties
```

## Future Royalty Developments

### Planned Features
- **Royalty Tokens**: Trade royalty streams as assets
- **Royalty Staking**: Stake royalties for governance
- **Cross-Platform Royalties**: Universal royalty enforcement
- **Royalty Analytics**: Advanced earning insights

### Community Governance
- **Royalty Adjustments**: Community can modify rates
- **Treasury Allocation**: Vote on royalty fund usage
- **Creator Incentives**: Reward successful creators

---

**Royalties ensure creators are rewarded for their success long after the initial sale!** 💰🎨
