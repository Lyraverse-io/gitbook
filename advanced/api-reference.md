# API Reference

Technical documentation for Lyraverse API endpoints and integration.

## Base URL
```
https://api.lyraverse.io
```

## Authentication

### No Authentication Required
Most endpoints are public and don't require authentication.

### Rate Limiting
- **100 requests per minute** per IP
- **1000 requests per hour** per IP
- Headers included in responses:
  ```
  X-RateLimit-Limit: 100
  X-RateLimit-Remaining: 95
  X-RateLimit-Reset: 1638360000
  ```

## Collections API

### Get All Collections
```http
GET /api/collections
```

**Query Parameters:**
- `limit` (number): Number of results (default: 50, max: 1000)
- `offset` (number): Pagination offset (default: 0)
- `sortBy` (string): Sort field (volume30d, mintedSupply, createdAt)
- `sortOrder` (string): Sort order (asc, desc)
- `search` (string): Search term for collection names

**Response:**
```json
{
  "success": true,
  "data": [
    {
      "id": "collection-id",
      "address": "0x1234...abcd",
      "name": "Collection Name",
      "symbol": "SYMB",
      "description": "Collection description",
      "image": "ipfs://...",
      "bannerImage": "ipfs://...",
      "mintPrice": "1000000000000000000",
      "royaltyPercentage": 5,
      "totalSupply": 10000,
      "mintedSupply": 2500,
      "floorPrice": "2000000000000000000",
      "createdAt": "2024-01-01T00:00:00.000Z"
    }
  ],
  "total": 150,
  "hasMore": true
}
```

### Get Collection by Address
```http
GET /api/collections/{address}
```

**Response:** Single collection object (same format as above)

### Get Collection Phases
```http
GET /api/collections/{address}/phases
```

**Response:**
```json
{
  "success": true,
  "data": {
    "phases": [
      {
        "index": 0,
        "name": "Public Sale",
        "mintPrice": "1000000000000000000",
        "maxPerWallet": 5,
        "startTime": 1640995200,
        "endTime": 1641081600,
        "allowlistRoot": "0x...",
        "reserveAmount": 1000
      }
    ]
  }
}
```

## NFTs API

### Get NFTs by Collection
```http
GET /api/nfts?collection={address}
```

**Query Parameters:**
- `collection` (string, required): Collection contract address
- `limit` (number): Results per page (default: 20, max: 100)
- `offset` (number): Pagination offset
- `sortBy` (string): Sort field (tokenId, price)
- `sortOrder` (string): Sort order (asc, desc)

### Get NFT Details
```http
GET /api/nfts/{contractAddress}/{tokenId}
```

**Response:**
```json
{
  "success": true,
  "data": {
    "id": "nft-id",
    "tokenId": 1234,
    "contractAddress": "0x1234...abcd",
    "name": "NFT Name #1234",
    "description": "NFT description",
    "image": "ipfs://...",
    "owner": "0x5678...efgh",
    "isListed": true,
    "price": "2000000000000000000",
    "listingId": "listing-id",
    "metadata": {
      "attributes": [
        {
          "trait_type": "Background",
          "value": "Blue",
          "rarity": 25.5
        }
      ]
    },
    "collection": {
      "name": "Collection Name",
      "address": "0x1234...abcd"
    },
    "rarityRank": 42,
    "createdAt": "2024-01-01T00:00:00.000Z"
  }
}
```

## Marketplace API

### Get Listed NFTs
```http
GET /api/listings
```

**Query Parameters:**
- `collection` (string): Filter by collection
- `minPrice` (string): Minimum price in wei
- `maxPrice` (string): Maximum price in wei
- `traits` (array): Filter by traits
- `limit` (number): Results per page
- `offset` (number): Pagination offset

### Get NFT Listing
```http
GET /api/listings/nft/{contractAddress}/{tokenId}
```

## Transactions API

### Get NFT History
```http
GET /api/nfts/{contractAddress}/{tokenId}/history
```

**Response:**
```json
{
  "success": true,
  "data": [
    {
      "type": "sale",
      "price": "2000000000000000000",
      "buyer": "0x1234...abcd",
      "seller": "0x5678...efgh",
      "timestamp": "2024-01-01T00:00:00.000Z",
      "txHash": "0xabcd...1234"
    },
    {
      "type": "listing",
      "price": "2000000000000000000",
      "seller": "0x5678...efgh",
      "status": "active",
      "timestamp": "2024-01-01T00:00:00.000Z",
      "txHash": "0xabcd...1234"
    }
  ]
}
```

## Offers API

### Get NFT Offers
```http
GET /api/nfts/{contractAddress}/{tokenId}/offers
```

### Create Offer (POST)
```http
POST /api/nfts/{contractAddress}/{tokenId}/offers
Content-Type: application/json

{
  "userAddress": "0x1234...abcd",
  "price": "1500000000000000000",
  "message": "Great NFT, willing to pay premium"
}
```

## User API

### Get User Profile
```http
GET /api/profile/{address}
```

### Get User NFTs
```http
GET /api/profile/{address}/nfts
```

### Get User Collections
```http
GET /api/profile/{address}/collections
```

## Analytics API

### Collection Stats
```http
GET /api/analytics/collection/{address}
```

**Response:**
```json
{
  "success": true,
  "data": {
    "totalVolume": "50000000000000000000",
    "floorPrice": "2000000000000000000",
    "holders": 1250,
    "listedCount": 89,
    "volume24h": "2000000000000000000",
    "volume7d": "15000000000000000000",
    "volume30d": "45000000000000000000"
  }
}
```

## Search API

### Global Search
```http
GET /api/search?q={query}
```

**Query Parameters:**
- `q` (string, required): Search term
- `type` (string): Filter by type (collection, nft, user)
- `limit` (number): Results per page

## Error Handling

### Standard Error Response
```json
{
  "success": false,
  "error": {
    "code": "VALIDATION_ERROR",
    "message": "Invalid request parameters",
    "details": {
      "field": "address",
      "issue": "Invalid contract address format"
    }
  }
}
```

### Common Error Codes
- `VALIDATION_ERROR`: Invalid request parameters
- `NOT_FOUND`: Resource not found
- `RATE_LIMITED`: Too many requests
- `SERVER_ERROR`: Internal server error

## Rate Limiting Headers

All responses include rate limiting information:
```
X-RateLimit-Limit: 100
X-RateLimit-Remaining: 95
X-RateLimit-Reset: 1638360000
```

## SDK and Libraries

### JavaScript SDK
```javascript
import { LyraverseAPI } from '@lyraverse/sdk';

const api = new LyraverseAPI();

// Get collections
const collections = await api.getCollections({ limit: 20 });

// Get NFT details
const nft = await api.getNFT('0x1234...abcd', 1234);
```

### Webhooks
Subscribe to real-time events:
- NFT sales
- New listings
- Price changes
- Collection updates

## Best Practices

### Efficient API Usage
- Use appropriate `limit` and `offset` for pagination
- Cache responses when possible
- Implement exponential backoff for retries
- Monitor rate limits

### Error Handling
```javascript
try {
  const response = await fetch('/api/collections');
  const data = await response.json();

  if (!data.success) {
    handleError(data.error);
  } else {
    processData(data.data);
  }
} catch (error) {
  handleNetworkError(error);
}
```

## Support

- **API Issues**: api-support@lyraverse.io
- **Rate Limiting**: Contact for increased limits
- **Integration Help**: Developer documentation
- **Bug Reports**: GitHub issues

---

**Happy building with Lyraverse API!** 🚀
