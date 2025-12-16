# Creating NFT Collections

Learn how to create and deploy your NFT collection on Lyraverse.

## Collection Types

### Simple Collections
Perfect for beginners and straightforward drops.

**Features:**
- Single public minting phase
- Basic metadata
- Standard royalties

### Advanced Collections
For complex drops and professional projects.

**Features:**
- Multiple minting phases
- Whitelist management
- Custom timing and limits
- DAO integration options

## Step-by-Step Creation

### Simple Mode

1. **Navigate to Create**
   - Go to `/create` page
   - No advanced toggle needed

2. **Basic Information**
   ```
   Collection Name: My Awesome NFTs
   Description: A unique collection of digital art
   Symbol: MYA (optional, auto-generated)
   ```

3. **Upload Assets**
   - **Collection Image**: 1000x1000px recommended (PNG/JPG)
   - **Banner Image**: 1920x1080px for enhanced display (optional)

4. **Minting Parameters**
   ```
   Mint Price: 1 HYPE (minimum 0.01 HYPE)
   Total Supply: 1000 (max 10,000)
   Royalties: 5% (0-25% range)
   ```

5. **Deploy Collection**
   - Review all parameters
   - Click "Create Collection"
   - Confirm transaction in wallet
   - Wait for deployment (~30 seconds)

### Advanced Mode

1. **Enable Advanced Mode**
   - Toggle "Advanced Collection" at top of form

2. **Basic Setup** (Same as simple mode)

3. **Phase Configuration**
   - **Add Phases**: Click "Add Phase" button
   - **Phase Types**:
     - Public: Open to all users
     - Whitelist: Restricted access

4. **Phase Settings**
   ```json
   {
     "name": "Whitelist Phase",
     "mintPrice": "500000000000000000", // 0.5 HYPE
     "maxPerWallet": 2,
     "startTime": 1640995200,
     "endTime": 1641081600,
     "allowlistRequired": true
   }
   ```

5. **Reserve Allocation**
   - Set aside NFTs for team/giveaways
   - Define reserve amounts per phase

## Collection Metadata

### Required Fields
- **Name**: Display name (max 50 characters)
- **Description**: Detailed description (max 1000 characters)
- **Image**: Collection avatar (PNG/JPG/GIF)

### Optional Fields
- **Banner**: Hero image for collection page
- **External URL**: Link to your website
- **Symbol**: Token symbol (auto-generated if empty)

## Minting Phases Deep Dive

### Phase Types Comparison

| Feature | Public Phase | Whitelist Phase |
|---------|--------------|-----------------|
| Access | Open to all | Invite-only |
| Price | Higher | Lower (reward) |
| Timing | Flexible | Strict windows |
| Limits | Per wallet | Per wallet + total |

### Phase Timing
- **Start Time**: When minting opens
- **End Time**: When minting closes
- **Duration**: Auto-calculated
- **Buffer**: Recommended 15min between phases

### Whitelist Management
1. **Create List**: Upload CSV or manual entry
2. **Merkle Tree**: Automatic generation
3. **Verification**: On-chain proof system
4. **Updates**: Modify list before phase starts

## Best Practices

### Collection Design
- **Consistent Theme**: Unified aesthetic
- **High Quality**: 1000x1000px minimum
- **File Size**: Under 5MB per image
- **Format**: PNG for transparency, JPG for photos

### Pricing Strategy
- **Market Research**: Check similar collections
- **Phased Pricing**: Higher → Lower over time
- **Value Proposition**: Justify your price point

### Community Building
- **Social Media**: Tease collection in advance
- **Discord/Telegram**: Build community
- **Whitelist Strategy**: Reward early supporters

## Troubleshooting

### Common Issues

**Transaction Failed**
- Check HYPE balance
- Verify network connection
- Try again with higher gas

**Image Upload Issues**
- Check file format (PNG/JPG/GIF)
- Verify file size (<10MB)
- Try different browser

**Phase Configuration Errors**
- Validate dates (future dates only)
- Check phase overlaps
- Verify whitelist format

### Getting Help
- **Support Chat**: Bottom-right widget
- **Documentation**: This guide
- **Community**: Telegram group

## Advanced Features

### Phase Reordering
- Drag & drop phases
- Automatic validation
- Conflict detection

### Automated Deployment
- Batch operations
- Template reuse
- Bulk updates

---

**Ready to create?** Head to `/create` and start building your NFT collection! 🚀
