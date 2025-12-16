# Minting Troubleshooting

Common minting issues and their solutions.

## Transaction Failures

### "Transaction Reverted"
**Error**: Transaction fails with "reverted" status

**Possible Causes:**
1. **Insufficient Funds**: Not enough HYPE for mint price + gas
2. **Phase Not Active**: Minting phase hasn't started or has ended
3. **Supply Exhausted**: All NFTs in phase already minted
4. **Wallet Limit Reached**: Exceeded max per wallet limit

**Solutions:**
```typescript
// Check requirements before minting
const canMint = await checkMintEligibility({
  userAddress,
  collectionAddress,
  mintAmount,
  currentPrice
});
```

### "Out of Gas"
**Error**: Transaction runs out of gas

**Solutions:**
- **Increase Gas Limit**: Use higher gas limit (200,000+ recommended)
- **Gas Price**: Adjust gas price based on network congestion
- **Batch Size**: Reduce number of NFTs per transaction
- **Network Timing**: Mint during off-peak hours

### "Nonce Too Low"
**Error**: Transaction nonce issues

**Solutions:**
- **Reset Account**: Reset account in wallet
- **Clear Pending**: Clear pending transactions
- **Sequential Processing**: Wait for previous transactions to confirm

## Phase-Specific Issues

### Whitelist Problems

#### "Not Whitelisted"
```
❌ Error: Address not in allowlist
✅ Solutions:
- Verify wallet address in creator's allowlist
- Check for typos in address submission
- Contact collection creator for allowlist status
- Try different wallet address if applicable
```

#### "Invalid Merkle Proof"
```
❌ Error: Merkle proof verification failed
✅ Solutions:
- Refresh page and try again
- Ensure using correct wallet
- Check network connection
- Contact technical support
```

### Public Phase Issues

#### "Phase Ended"
```
❌ Error: Current time outside phase window
✅ Solutions:
- Check phase schedule on collection page
- Wait for next phase to begin
- Follow collection on social media for updates
```

#### "Max Per Wallet Exceeded"
```
❌ Error: Would exceed wallet limit
✅ Solutions:
- Check your current mint count
- Reduce mint amount
- Use different wallet if allowed
- Wait for limit reset (if applicable)
```

## Network Issues

### RPC Connection Problems
**Symptoms**: "RPC Error" or "Network Error"

**Solutions:**
1. **Switch RPC**: Try different RPC endpoint
2. **Network Reset**: Reset network in wallet
3. **VPN Check**: Disable VPN if interfering
4. **Browser Refresh**: Hard refresh page

### Block Confirmation Delays
**Symptoms**: Transaction pending for extended time

**Solutions:**
- **Wait Time**: Hyperliquid blocks confirm in ~3 seconds
- **Gas Boost**: Increase gas price to speed up
- **Network Check**: Verify network connectivity
- **Explorer Verify**: Check transaction on block explorer

## Contract Issues

### Contract Paused
**Error**: "Contract is currently paused"

**Solutions:**
- **Check Status**: Verify on collection page
- **Creator Contact**: Ask creator about pause reason
- **Wait Period**: Minting will resume when unpaused
- **Alternative Collections**: Explore other collections

### Invalid Contract State
**Error**: "Invalid contract state"

**Solutions:**
- **Page Refresh**: Hard refresh browser
- **Cache Clear**: Clear browser cache
- **Wallet Reconnect**: Disconnect and reconnect wallet
- **Support Contact**: Report to technical support

## Wallet-Specific Issues

### MetaMask Problems
```
❌ Common Issues:
- Network not added
- Insufficient gas
- Wrong account selected

✅ Solutions:
- Add Hyperliquid testnet manually
- Ensure sufficient HYPE balance
- Verify correct account connected
```

### Other Wallets
```
❌ Compatibility Issues:
- Unsupported wallet type
- Mobile wallet limitations
- Browser extension conflicts

✅ Solutions:
- Use MetaMask or compatible wallet
- Try desktop version
- Disable conflicting extensions
```

## Amount and Pricing Issues

### Price Mismatch
**Error**: "Price has changed" or "Insufficient payment"

**Solutions:**
- **Refresh Data**: Reload page for latest prices
- **Phase Check**: Verify current active phase
- **Calculation Verify**: Double-check total cost
- **Balance Confirm**: Ensure sufficient HYPE

### Invalid Mint Amount
**Error**: "Invalid mint amount"

**Solutions:**
- **Minimum Check**: Must mint at least 1 NFT
- **Maximum Check**: Cannot exceed max per transaction
- **Wallet Limit**: Check remaining wallet allowance
- **Phase Limits**: Verify phase-specific limits

## Timing Issues

### Phase Start/End Confusion
**Problem**: Unsure about phase timing

**Solutions:**
- **Time Zone Check**: Verify your local time zone
- **UTC Conversion**: All times are in UTC
- **Countdown Timer**: Use in-app countdown timers
- **Calendar Integration**: Add to personal calendar

### Server Time Synchronization
**Problem**: Local time doesn't match server time

**Solutions:**
- **Time Sync**: Ensure device time is accurate
- **NTP Check**: Verify internet time synchronization
- **Manual Verification**: Check against multiple time sources

## Advanced Troubleshooting

### Debug Information
**Collect Debug Data:**
```json
{
  "timestamp": "2024-01-01T12:00:00Z",
  "walletAddress": "0x1234...abcd",
  "collectionAddress": "0x5678...efgh",
  "phaseIndex": 0,
  "mintAmount": 2,
  "currentPrice": "1000000000000000000",
  "gasEstimate": "50000",
  "errorMessage": "exact error text",
  "transactionHash": "0xabcd...1234"
}
```

### Browser Console Logs
**Check Console for Errors:**
1. Press F12 to open developer tools
2. Go to Console tab
3. Look for red error messages
4. Copy error details for support

### Network Tab Analysis
**Debug Network Requests:**
1. F12 → Network tab
2. Filter by "XHR" or "Fetch"
3. Look for failed API calls
4. Check response status codes

## Prevention Best Practices

### Pre-Mint Checklist
- ✅ **Wallet Connected**: Proper wallet connection
- ✅ **Network Selected**: Hyperliquid testnet active
- ✅ **Balance Verified**: Sufficient HYPE for mint + gas
- ✅ **Phase Confirmed**: Correct phase is active
- ✅ **Limits Checked**: Within wallet and phase limits
- ✅ **Gas Estimated**: Reasonable gas costs

### During Mint Monitoring
- ✅ **Transaction Hash**: Save for tracking
- ✅ **Block Confirmation**: Wait for confirmation
- ✅ **Success Notification**: Platform confirmation
- ✅ **Wallet Balance**: Verify deduction occurred
- ✅ **NFT Receipt**: Confirm NFT in wallet

## Getting Help

### Quick Self-Help
1. **Documentation**: Check minting guides
2. **FAQ**: Search common issues
3. **Community**: Ask in Discord channels
4. **Status Page**: Check platform status

### Support Contact
- **Minting Issues**: creator-support@lyraverse.io
- **Technical Problems**: tech-support@lyraverse.io
- **General Support**: support@lyraverse.io

### Required Information for Support
```
Please include:
- Wallet address used for minting
- Collection contract address
- Exact error message
- Transaction hash (if available)
- Browser and wallet version
- Steps taken before error
- Screenshots of error
```

---

**Most minting issues can be resolved with proper preparation!** 🎯
