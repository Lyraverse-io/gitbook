# Marketplace Fees

Complete breakdown of fees, costs, and revenue sharing on the Lyraverse marketplace.

## Fee Structure Overview

### Primary Sales (Minting)
```
Sale Price Breakdown:
├── Platform Fee: 2.5%
├── Creator Royalty: 0-25% (set by creator)
└── Creator Receives: Remaining amount
```

### Secondary Sales (Trading)
```
Sale Price Breakdown:
├── Platform Fee: 0.5%
├── Creator Royalty: 0-25% (set by creator)
└── Seller Receives: Remaining amount
```

## Platform Fee Details

### Secondary Market Fee
- **Rate**: 0.5% of total transaction value
- **Currency**: Deducted in HYPE
- **Timing**: Calculated and deducted at sale time
- **Transparency**: Fee visible before purchase

### Fee Calculation Example
```
Sale Price: 10 HYPE

Platform Fee: 0.5% = 0.05 HYPE
Creator Royalty: 5% = 0.5 HYPE
Seller Receives: 9.45 HYPE

Total Deductions: 0.55 HYPE (5.5%)
```

## Creator Royalties

### Royalty System
- **Range**: 0% to 25% (platform enforced maximum)
- **Purpose**: Ongoing creator compensation
- **Enforcement**: Smart contract level guarantee
- **Why 25% Max?**: Protects buyers from excessive fees

### Royalty Distribution
```
Creator sets 5% royalty:
- Sale #1 (10 HYPE): Creator gets 0.5 HYPE
- Sale #2 (15 HYPE): Creator gets 0.75 HYPE
- Sale #3 (8 HYPE): Creator gets 0.4 HYPE
- Total Royalties: 1.65 HYPE
```

### Royalty Management
- **Immutable**: Set at collection creation, cannot change
- **Automatic**: Paid instantly on every sale
- **Transparent**: All royalty payments visible on-chain

## Gas Fees

### Transaction Costs
- **Network**: Hyperliquid blockchain fees
- **Variable**: Depends on network congestion
- **Currency**: Paid in HYPE (network native token)
- **Estimation**: Provided before transaction

### Typical Gas Costs
```json
{
  "listing": "~0.01 HYPE",
  "purchase": "~0.02 HYPE",
  "transfer": "~0.005 HYPE",
  "minting": "~0.05-0.1 HYPE"
}
```

### Gas Optimization
- **Batch Operations**: Combine multiple actions
- **Network Timing**: Transact during low congestion
- **Fee Estimation**: Use provided gas estimates

## Fee Transparency

### Pre-Transaction Display
```
Purchase Confirmation Screen:
Sale Price: 10 HYPE
Creator Royalty (5%): 0.5 HYPE
Platform Fee (0.5%): 0.05 HYPE
Gas Fee (estimated): ~0.02 HYPE
You Pay: 10.02 HYPE
Seller Receives: 9.45 HYPE
Creator Receives: 0.5 HYPE
```

### Post-Transaction Records
- **Transaction Hash**: On-chain verification
- **Fee Breakdown**: Detailed cost analysis
- **Revenue Tracking**: Creator earnings dashboard

## Revenue Sharing

### Platform Fee Allocation
```
Platform Fee Distribution (0.5%):
├── Operations: 40%
├── Marketing: 30%
├── Development: 20%
└── Ecosystem: 10%
```

### Creator Revenue Streams
1. **Primary Sales**: 100% of mint price
2. **Secondary Royalties**: Percentage of every resale
3. **Long-term Value**: Appreciation over time

### Holder Benefits
- **No Selling Fees**: Only pay gas for transactions
- **Royalty Free**: Buy without worrying about resale costs
- **Value Appreciation**: Benefit from collection growth

## Fee Comparison

### Platform Comparison
```
Lyraverse:
- Secondary Fee: 0.5%
- Primary Fee: 2.5%
- Royalty Max: 25%

OpenSea:
- Secondary Fee: 2.5%
- Primary Fee: 0%
- Royalty Max: None

Rarible:
- Secondary Fee: 2.5%
- Primary Fee: 0%
- Royalty Max: None

Foundation:
- Secondary Fee: 5%
- Primary Fee: 5%
- Royalty: 10% (fixed)
```

### Competitive Advantages
- **Creator Protection**: 25% royalty maximum
- **Buyer Friendly**: Low 0.5% secondary fee
- **Gas Efficient**: Optimized for Hyperliquid network
- **Fair Mint Fees**: Competitive 2.5% minting fees

## Fee Optimization

### For Creators
- **Strategic Royalties**: Balance between earnings and sales
- **Value Creation**: Focus on NFT utility and community
- **Long-term Thinking**: Consider lifetime royalty potential

### For Sellers
- **Price Setting**: Factor fees into listing price
- **Market Timing**: Sell when fees are favorable
- **Bulk Operations**: Minimize per-transaction costs

### For Buyers
- **Total Cost**: Include gas in purchase decision
- **Resale Potential**: Consider future selling costs
- **Portfolio Strategy**: Diversify across collections

## Special Fee Structures

### Promotional Periods
- **Fee Waivers**: Temporary reduced fees
- **Bonus Royalties**: Increased creator earnings
- **Community Events**: Special fee structures

### Collection Tiers
```json
{
  "standard": {
    "secondaryFee": 0.005,
    "royaltyMax": 0.25
  },
  "premium": {
    "secondaryFee": 0.004,
    "royaltyMax": 0.30,
    "requirements": "10k+ volume"
  },
  "enterprise": {
    "secondaryFee": 0.003,
    "royaltyMax": 0.35,
    "requirements": "DAO governance"
  }
}
```

## Tax Considerations

### Fee Reporting
- **Business Expenses**: Platform fees as deductible costs
- **Royalty Income**: Creator earnings as taxable income
- **Record Keeping**: Maintain detailed transaction records

### Jurisdiction Compliance
- **Local Laws**: Follow regional tax regulations
- **Crypto Reporting**: Include in cryptocurrency tax reports
- **Professional Advice**: Consult tax professionals

## Future Fee Developments

### Planned Changes
- **DAO Governance**: Community-controlled fee adjustments
- **Dynamic Fees**: Market-based fee modulation
- **Fee Tokens**: Platform token rewards for active users

### Advanced Features
- **Fee Discounts**: Loyalty program benefits
- **Bulk Discounts**: Reduced fees for large transactions
- **Cross-Chain**: Unified fee structure across networks

## Support and Questions

### Fee-Related Support
- **Fee Calculations**: How fees are computed
- **Disputes**: Fee deduction disagreements
- **Refunds**: Gas fee reimbursement policies

### Contact Information
- **Fee Questions**: fees@lyraverse.io
- **Technical Support**: support@lyraverse.io
- **Creator Support**: creator-support@lyraverse.io

---

**Transparent, fair, and competitive fee structure for all participants!** 💰📊
