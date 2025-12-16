# Staking NFTs

Learn how to stake your NFTs for governance rewards and enhanced voting power.

## What is NFT Staking?

### Overview
NFT staking allows you to lock your NFTs in a smart contract to earn rewards and gain governance benefits. It's like depositing your NFTs to participate more actively in the DAO.

### Benefits of Staking
- **Governance Rewards**: Earn tokens for participation
- **Boosted Voting Power**: Increased influence in proposals
- **Community Status**: Recognition as active member
- **Long-term Incentives**: Aligned with collection success

## Staking Requirements

### Basic Requirements
- ✅ **NFT Ownership**: Hold NFTs from the collection
- ✅ **DAO Membership**: Collection must have active DAO
- ✅ **Wallet Connection**: Connected Hyperliquid wallet
- ✅ **Gas Fees**: Small amount for staking transactions

### Staking Parameters
```json
{
  "minimumStake": 1,              // Minimum NFTs to stake
  "lockPeriod": 604800,           // 7 days minimum
  "rewardRate": "0.001",          // Daily reward rate
  "boostMultiplier": 2,           // 2x voting power when staked
  "unstakeCooldown": 86400        // 24h cooldown period
}
```

## How to Stake NFTs

### Step-by-Step Process

#### 1. Access Staking Interface
1. **Go to Collection Page**: Navigate to your DAO-enabled collection
2. **Click "DAO" Tab**: Access governance section
3. **Find "Staking" Section**: Located in DAO interface
4. **Connect Wallet**: Ensure proper wallet connection

#### 2. Select NFTs to Stake
```typescript
// Staking Interface Options
- Individual Selection: Choose specific NFTs
- Bulk Selection: Stake multiple NFTs at once
- All NFTs: Stake entire collection holding
- Custom Amount: Specify exact number to stake
```

#### 3. Configure Staking
```json
{
  "selectedNFTs": ["#123", "#456", "#789"],
  "stakingDuration": "flexible",  // or fixed period
  "autoCompound": true,           // Reinvest rewards automatically
  "notificationSettings": {
    "rewards": true,
    "governance": true
  }
}
```

#### 4. Confirm Staking Transaction
1. **Review Details**: Confirm NFTs and parameters
2. **Check Gas Estimate**: Review transaction costs
3. **Approve Transaction**: Sign staking transaction
4. **Wait Confirmation**: ~30 seconds on Hyperliquid

### Post-Staking Actions
- **Verify Staking**: Check staked NFTs in your profile
- **Monitor Rewards**: Track accumulating rewards
- **Voting Power**: Confirm boosted governance rights

## Staking Rewards

### Reward Structure
- **Base Rate**: Daily rewards based on staked NFTs
- **Bonus Multipliers**: Additional rewards for long-term staking
- **Community Pool**: Shared rewards from DAO treasury

### Reward Calculation
```
Daily Rewards = (Staked NFTs × Base Rate × Time Multiplier)
Time Multiplier = 1.0 (normal) to 2.0 (long-term staking)
```

### Reward Distribution
- **Automatic**: Rewards credited daily to staked position
- **Claimable**: Withdraw rewards anytime
- **Compounding**: Option to reinvest rewards automatically

## Enhanced Governance

### Voting Power Boost
```typescript
// Voting Power Calculation
baseVotingPower = numberOfNFTs
stakedVotingPower = baseVotingPower × boostMultiplier
totalVotingPower = baseVotingPower + stakedVotingPower
```

### Staking Benefits
- **Increased Influence**: Higher voting weight on proposals
- **Priority Access**: Early access to new features
- **Exclusive Proposals**: Special staking-related governance
- **Community Recognition**: Staker status and badges

## Managing Stakes

### Viewing Your Stakes
1. **Profile Section**: Check "Staked NFTs" in your profile
2. **DAO Dashboard**: View staking status and rewards
3. **Transaction History**: Track staking/unstaking history

### Claiming Rewards
1. **Access Staking Dashboard**: Go to DAO staking section
2. **View Accumulated Rewards**: Check available rewards
3. **Claim Rewards**: Withdraw to wallet
4. **Confirm Transaction**: Approve claim transaction

### Modifying Stakes
- **Add NFTs**: Stake additional NFTs to existing position
- **Partial Unstaking**: Unstake some NFTs while keeping others
- **Duration Extension**: Extend staking period for bonus rewards

## Unstaking Process

### Unstaking Requirements
- ✅ **Lock Period Passed**: Minimum staking time completed
- ✅ **Cooldown Period**: 24-48 hour waiting period
- ✅ **Gas Fees**: Small amount for unstaking transaction

### Step-by-Step Unstaking

#### 1. Initiate Unstaking
1. **Go to Staking Dashboard**: Access your staked positions
2. **Select NFTs to Unstake**: Choose which NFTs to withdraw
3. **Confirm Unstaking**: Start the unstaking process

#### 2. Cooldown Period
```typescript
// Cooldown Timeline
Day 1: Unstaking initiated
Days 1-2: Cooldown period (cannot access NFTs)
Day 3: NFTs become available for withdrawal
```

#### 3. Complete Withdrawal
1. **Return to Dashboard**: After cooldown period
2. **Confirm Withdrawal**: Finalize NFT return
3. **Receive NFTs**: NFTs back in your wallet
4. **Rewards Claimed**: Any pending rewards automatically claimed

## Staking Strategies

### Short-term Staking (1-3 months)
- **Purpose**: Participate in specific governance votes
- **Benefits**: Quick rewards, flexible exit
- **Risk**: Lower reward multipliers

### Medium-term Staking (3-6 months)
- **Purpose**: Balance flexibility and rewards
- **Benefits**: Moderate multipliers, community influence
- **Risk**: Some opportunity cost

### Long-term Staking (6+ months)
- **Purpose**: Maximum governance participation
- **Benefits**: Highest reward multipliers, maximum influence
- **Risk**: Locked capital, less flexibility

## Risk Considerations

### Smart Contract Risks
- **Audit Status**: Ensure staking contract is audited
- **Emergency Controls**: Check for emergency withdrawal options
- **Upgradeability**: Understand contract update processes

### Opportunity Costs
- **Liquidity**: Staked NFTs cannot be traded
- **Market Movements**: Cannot sell during price increases
- **New Opportunities**: Missing other collection launches

### Reward Sustainability
- **Treasury Health**: Monitor DAO treasury capacity
- **Inflation Concerns**: Watch for reward dilution
- **Economic Balance**: Ensure rewards don't harm tokenomics

## Troubleshooting Staking

### Cannot Stake NFTs
**Issue**: "Staking contract not available"
**Solution**: Ensure collection has active DAO staking

**Issue**: "Insufficient balance for gas"
**Solution**: Add HYPE to wallet for transaction fees

### Rewards Not Appearing
**Issue**: "No rewards after staking period"
**Solution**: Check reward distribution schedule, contact support

### Cannot Unstake
**Issue**: "Still in lock period"
**Solution**: Wait for minimum staking time to pass

**Issue**: "Cooldown period active"
**Solution**: Wait 24-48 hours after initiating unstaking

## Staking Analytics

### Performance Metrics
- **Total Staked**: Percentage of circulating supply staked
- **Average Duration**: Typical staking periods
- **Reward Distribution**: Historical payout data
- **Participation Rate**: Community staking engagement

### Personal Dashboard
- **Staking History**: Past staking/unstaking transactions
- **Reward History**: Detailed reward earning records
- **Voting Activity**: Governance participation while staked
- **Performance Comparison**: Your staking vs community averages

## Advanced Features

### Auto-Compounding
- **Automatic Reinvestment**: Rewards restaked automatically
- **Maximize Returns**: Compound interest effect
- **Set and Forget**: Minimal maintenance required

### Staking Pools
- **Community Pools**: Group staking for shared rewards
- **Themed Pools**: Special interest staking groups
- **Boosted Pools**: Higher rewards for specific goals

### Governance Integration
- **Proposal Boosting**: Stakers can boost proposal visibility
- **Delegate Voting**: Allow stakers to delegate voting power
- **Emergency Voting**: Special voting rights for stakers

---

**Staking your NFTs is the ultimate commitment to your collection's success!** 🚀🔒
