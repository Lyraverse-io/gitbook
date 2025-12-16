# Mint Phases

Comprehensive guide to configuring and managing different mint phases for your NFT collection.

## Phase Types Overview

### Available Phase Types
1. **Public Phase**: Open to all wallets
2. **Whitelist Phase**: Restricted to approved wallets
3. **Dutch Auction**: Decreasing price over time
4. **English Auction**: Increasing bid system

## Phase Configuration

### Basic Phase Structure
```json
{
  "index": 0,
  "name": "Public Sale",
  "type": "public",
  "mintPrice": "1000000000000000000",
  "maxPerWallet": 5,
  "startTime": 1640995200,
  "endTime": 1641081600,
  "allowlistRoot": null,
  "reserveAmount": 1000,
  "maxSupply": 5000
}
```

### Phase Parameters

#### Timing
- **Start Time**: Unix timestamp when phase begins
- **End Time**: Unix timestamp when phase ends
- **Duration**: Calculated automatically
- **Buffer Time**: Gap between phases

#### Pricing
- **Fixed Price**: Set HYPE amount per NFT
- **Dynamic Pricing**: Auction-based pricing
- **Discount Tiers**: Volume-based discounts

#### Limits
- **Max Per Wallet**: NFTs per address limit
- **Reserve Amount**: Guaranteed NFTs for phase
- **Total Allocation**: Phase supply cap

## Public Phase Setup

### Standard Configuration
```json
{
  "type": "public",
  "mintPrice": "2000000000000000000",
  "maxPerWallet": 10,
  "startTime": 1640995200,
  "endTime": 1641081600,
  "allowlistRoot": null
}
```

### Use Cases
- **Fair Launch**: Equal opportunity for all
- **Community Building**: Broad participation
- **Price Discovery**: Market-determined value

## Whitelist Phase Setup

### Creating Allowlists

#### Manual List Creation
```json
{
  "allowlistAddresses": [
    "0x1234567890123456789012345678901234567890",
    "0x0987654321098765432109876543210987654321"
  ],
  "maxPerWallet": 2,
  "mintPrice": "1000000000000000000"
}
```

#### Merkle Tree Generation
```javascript
import { MerkleTree } from 'merkletreejs';
import { keccak256 } from 'viem';

// Generate leaf nodes
const leaves = addresses.map(addr => keccak256(addr));
const tree = new MerkleTree(leaves, keccak256, { sortPairs: true });
const root = tree.getHexRoot();

// Generate proof for specific address
const proof = tree.getHexProof(keccak256(userAddress));
```

### Whitelist Management
- **Address Verification**: On-chain proof validation
- **Dynamic Updates**: Add/remove addresses
- **Tiered Access**: Different limits per tier

## Advanced Phase Strategies

### Phase Sequencing
```
Phase 1: Whitelist (24h) - Early supporters
Phase 2: Public (48h) - General community
Phase 3: Dutch Auction (24h) - Price discovery
```

### Overlapping Phases
- **Concurrent Access**: Multiple phases active simultaneously
- **Priority System**: Whitelist gets first access
- **Fallback Mechanism**: Public phase as safety net

## Phase Timing Best Practices

### Launch Schedule
- **Pre-Announcement**: Build hype beforehand
- **Soft Launch**: Small whitelist phase first
- **Main Launch**: Public phase with marketing push
- **Post-Launch**: Dutch auction for remaining NFTs

### Time Zone Considerations
- **Global Accessibility**: Consider different time zones
- **Peak Hours**: Launch during active periods
- **Weekend Launches**: Higher participation rates

## Phase Monitoring

### Real-time Metrics
- **Mint Progress**: NFTs minted vs allocated
- **Participation Rate**: Active minters
- **Gas Competition**: Network congestion monitoring
- **Error Tracking**: Failed transaction analysis

### Phase Analytics
```json
{
  "phaseMetrics": {
    "totalMinted": 850,
    "uniqueMinters": 420,
    "averageGasPrice": "50000000000",
    "failedTransactions": 12,
    "peakConcurrentMints": 150
  }
}
```

## Troubleshooting Phase Issues

### Common Problems

#### Phase Not Starting
**Issue**: "Phase shows as future when it should be active"
**Solutions**:
- Check server time synchronization
- Verify timestamp format (Unix seconds)
- Confirm contract deployment status

#### Mint Rejections
**Issue**: "Transactions failing during mint"
**Solutions**:
- Verify phase is active
- Check wallet balance and allowances
- Confirm whitelist status
- Monitor gas prices

#### Supply Issues
**Issue**: "Phase selling out too quickly/slowly"
**Solutions**:
- Adjust phase duration
- Modify allocation amounts
- Consider additional phases

## Phase Optimization

### Performance Tuning
- **Gas Optimization**: Efficient contract calls
- **Batch Minting**: Multiple NFTs per transaction
- **Queue Management**: Handle high concurrent load

### User Experience
- **Clear Communication**: Phase schedule transparency
- **Progress Indicators**: Real-time mint progress
- **Error Handling**: User-friendly error messages

## Advanced Features

### Dynamic Phases
- **Conditional Logic**: Phase activation based on conditions
- **Adaptive Pricing**: Price adjustment based on demand
- **Smart Allocation**: Dynamic supply distribution

### Integration Features
- **Cross-Platform**: Phase data for external tools
- **Analytics Export**: Detailed phase performance data
- **Automation**: Smart contract triggers for phase changes

## Legal Considerations

### Compliance Requirements
- **Fair Access**: Equal opportunity principles
- **Transparency**: Clear phase rules and timing
- **Consumer Protection**: Clear terms and conditions

### Regulatory Aspects
- **Security Laws**: Token distribution compliance
- **Consumer Rights**: Refund and cancellation policies
- **Tax Reporting**: Mint activity documentation

## Phase Examples

### Simple Launch
```
Phase 1: Public Phase
- Duration: 48 hours
- Price: 1 HYPE
- Max per wallet: 5 NFTs
- Supply: 2000 NFTs
```

### Complex Launch
```
Phase 1: OG Whitelist (12h)
- Price: 0.5 HYPE
- Max per wallet: 2 NFTs
- Supply: 500 NFTs

Phase 2: Public Sale (36h)
- Price: 1 HYPE
- Max per wallet: 5 NFTs
- Supply: 3000 NFTs

Phase 3: Dutch Auction (24h)
- Start Price: 2 HYPE
- End Price: 0.8 HYPE
- Supply: Remaining NFTs
```

## Future Phase Developments

### Planned Features
- **Automated Phase Creation**: AI-assisted configuration
- **Cross-Chain Phases**: Multi-network launches
- **Dynamic Allowlists**: Real-time eligibility updates
- **Advanced Auctions**: More auction types

---

**Master phase configuration for successful NFT launches!** 🚀
