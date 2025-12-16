# Troubleshooting Guide

Common issues and solutions for Lyraverse platform users.

## Wallet Connection Issues

### Cannot Connect Wallet
**Problem**: "Wallet not connecting to Lyraverse"
**Solutions**:
1. **Check Network**: Ensure Hyperliquid testnet selected
2. **Browser Refresh**: Hard refresh (Ctrl+F5)
3. **Extension Update**: Update wallet extension
4. **Network Addition**: Manually add Hyperliquid network

**Error**: "Unsupported network"
```
Solution: Switch to Hyperliquid Testnet in wallet
Network ID: 998
RPC URL: https://api.hyperliquid-testnet.xyz/evm
```

### Transaction Not Confirming
**Problem**: "Transaction stuck in pending"
**Solutions**:
1. **Wait Time**: Hyperliquid blocks ~3 seconds
2. **Gas Increase**: Speed up with higher gas
3. **Network Check**: Verify network connectivity
4. **Wallet Restart**: Restart wallet extension

## Minting Problems

### Mint Transaction Failed
**Problem**: "Mint failed with error message"
**Common Errors**:

**"Insufficient balance"**
```
Check HYPE balance + gas fees
Minimum: mint price + ~0.05 HYPE gas
```

**"Not whitelisted"**
```
Verify wallet address in allowlist
Check phase timing and eligibility
Contact collection creator
```

**"Phase not active"**
```
Check current date/time
Verify phase schedule
Wait for phase to begin
```

### Cannot Access Mint Page
**Problem**: "Mint button not appearing"
**Solutions**:
1. **Phase Status**: Check if minting is active
2. **Wallet Connection**: Ensure wallet is connected
3. **Network**: Confirm correct network
4. **Browser Cache**: Clear cache and refresh

## Marketplace Issues

### Listing Not Appearing
**Problem**: "NFT listed but not visible"
**Solutions**:
1. **Wait Time**: Indexer sync takes 2-3 minutes
2. **Transaction Check**: Verify transaction confirmed
3. **Contract Approval**: Ensure marketplace approved
4. **Refresh Page**: Hard refresh browser

### Purchase Failed
**Problem**: "Cannot complete NFT purchase"
**Common Issues**:

**"Price changed"**
```
Listing price updated, refresh and try again
```

**"NFT sold"**
```
Another buyer purchased first
Look for similar NFTs
```

**"Insufficient funds"**
```
Check HYPE balance includes fees
Add funds to wallet
```

## NFT Display Problems

### Image Not Loading
**Problem**: "NFT image shows as broken"
**Solutions**:
1. **IPFS Gateway**: Try different IPFS gateway
2. **Metadata Refresh**: Wait for metadata update
3. **Cache Clear**: Clear browser cache
4. **Network Issues**: Check internet connection

### Wrong NFT Information
**Problem**: "NFT shows incorrect details"
**Solutions**:
1. **Indexer Sync**: Wait 5-10 minutes
2. **Metadata Update**: Contact collection creator
3. **Cache Issues**: Hard refresh page
4. **Contract Check**: Verify contract address

## Collection Issues

### Collection Not Found
**Problem**: "Cannot find collection"
**Solutions**:
1. **Address Check**: Verify contract address
2. **Network Confirm**: Ensure correct network
3. **Deployment Status**: Check if deployed
4. **Search Function**: Use search bar

### Minting Not Working
**Problem**: "Collection shows but cannot mint"
**Solutions**:
1. **Phase Check**: Verify active mint phase
2. **Supply Check**: Confirm NFTs remaining
3. **Paused Status**: Check if minting paused
4. **Creator Contact**: Reach out to creator

## DAO and Governance

### Cannot Create Proposal
**Problem**: "Proposal creation blocked"
**Solutions**:
1. **NFT Ownership**: Must hold collection NFTs
2. **Minimum Stake**: Check proposal threshold
3. **Phase Status**: Ensure governance active
4. **Wallet Balance**: Sufficient HYPE for gas

### Vote Not Counting
**Problem**: "Vote transaction successful but not recorded"
**Solutions**:
1. **Wait Time**: Allow indexer sync (2-3 minutes)
2. **Transaction Check**: Verify on explorer
3. **Proposal Status**: Confirm proposal still active
4. **Support Contact**: Report to support team

## Performance Issues

### Slow Loading
**Problem**: "Pages loading slowly"
**Solutions**:
1. **Network Speed**: Check internet connection
2. **Browser Cache**: Clear cache and cookies
3. **Extensions**: Disable conflicting extensions
4. **Device Resources**: Close other applications

### App Crashing
**Problem**: "Application freezing or crashing"
**Solutions**:
1. **Browser Update**: Use latest browser version
2. **Memory Clear**: Close other tabs/applications
3. **Extension Conflict**: Disable wallet extensions temporarily
4. **Device Restart**: Restart computer/device

## Account and Profile

### Profile Not Updating
**Problem**: "Profile changes not saving"
**Solutions**:
1. **Save Confirmation**: Ensure save button clicked
2. **Image Size**: Check image file size limits
3. **Format Support**: Verify supported formats
4. **Network Issues**: Check connection stability

### Transaction History Missing
**Problem**: "Cannot see past transactions"
**Solutions**:
1. **Wallet Sync**: Allow full wallet synchronization
2. **Network Selection**: Confirm correct network
3. **Explorer Check**: Verify on block explorer
4. **Support Contact**: Request transaction history

## Network and Connectivity

### RPC Errors
**Problem**: "RPC endpoint issues"
**Solutions**:
1. **Network Switch**: Try different RPC endpoint
2. **Wallet Reconnect**: Disconnect and reconnect wallet
3. **Network Reset**: Reset network settings
4. **Support Check**: Verify network status

### Connection Timeouts
**Problem**: "Requests timing out"
**Solutions**:
1. **Retry Request**: Try again after delay
2. **Network Check**: Verify internet stability
3. **VPN Disable**: Turn off VPN if used
4. **Regional Issues**: Try different network

## Security Concerns

### Suspicious Transactions
**Problem**: "Unexpected transaction appeared"
**Solutions**:
1. **Verify Address**: Check recipient address
2. **Transaction Details**: Review transaction details
3. **Wallet Security**: Enable additional security
4. **Report Incident**: Contact support immediately

### Phishing Attempts
**Problem**: "Received suspicious links/messages"
**Solutions**:
1. **Verify Source**: Only use official links
2. **URL Check**: Verify lyraverse.io domain
3. **No Private Keys**: Never share private keys
4. **Report Phishing**: Alert support team

## Advanced Troubleshooting

### Developer Console
**Access Console**: Press F12 → Console tab
**Look for**: Error messages, network failures
**Report**: Copy error messages when contacting support

### Network Logs
**Check Network Tab**: F12 → Network tab
**Failed Requests**: Look for failed API calls
**Status Codes**: Note HTTP error codes

### Wallet Logs
**Extension Logs**: Check wallet extension console
**Transaction Hashes**: Save for support tickets
**Error Messages**: Copy exact error text

## Getting Help

### Self-Service Resources
- **Documentation**: Check relevant guides
- **FAQ**: Search common questions
- **Community**: Ask in Discord channels
- **Status Page**: Check platform status

### Contact Support
- **General Issues**: support@lyraverse.io
- **Technical Problems**: tech-support@lyraverse.io
- **Creator Support**: creator-support@lyraverse.io
- **Security Issues**: security@lyraverse.io

### Support Response Times
- **Urgent Issues**: < 4 hours
- **General Support**: < 24 hours
- **Technical Issues**: < 48 hours
- **Feature Requests**: 1-2 weeks

---

**Most issues can be resolved with these troubleshooting steps!** 🔧
