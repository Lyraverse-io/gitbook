# API Documentation - Lyraverse.io Indexer

## Base URL
```
http://localhost:3001/api
```

## Authentification
L'API ne nécessite pas d'authentification pour les endpoints publics. Les endpoints protégés utiliseront JWT dans le futur.

## Endpoints

### Collections

#### GET /collections
Récupérer toutes les collections

**Paramètres de requête:**
- `page` (number, optionnel): Numéro de page (défaut: 1)
- `limit` (number, optionnel): Nombre d'éléments par page (défaut: 20)
- `verified` (boolean, optionnel): Filtrer par statut de vérification
- `sortBy` (string, optionnel): Champ de tri (défaut: createdAt)
- `sortOrder` (string, optionnel): Ordre de tri (asc/desc, défaut: desc)

**Réponse:**
```json
{
  "data": [
    {
      "id": "string",
      "address": "string",
      "name": "string",
      "symbol": "string",
      "description": "string",
      "image": "string",
      "banner": "string",
      "owner": "string",
      "totalSupply": 1000,
      "mintedSupply": 500,
      "mintPrice": "1000000000000000000",
      "royaltyPercentage": 500,
      "isVerified": true,
      "baseURI": "string",
      "createdAt": "2024-01-01T00:00:00Z",
      "updatedAt": "2024-01-01T00:00:00Z",
      "_count": {
        "nfts": 500,
        "listings": 50,
        "sales": 100
      }
    }
  ],
  "pagination": {
    "page": 1,
    "limit": 20,
    "total": 100,
    "totalPages": 5
  }
}
```

#### GET /collections/{address}
Récupérer une collection spécifique

**Paramètres de chemin:**
- `address` (string): Adresse du contrat de la collection

**Réponse:**
```json
{
  "data": {
    "id": "string",
    "address": "string",
    "name": "string",
    "symbol": "string",
    "description": "string",
    "image": "string",
    "banner": "string",
    "owner": "string",
    "totalSupply": 1000,
    "mintedSupply": 500,
    "mintPrice": "1000000000000000000",
    "royaltyPercentage": 500,
    "isVerified": true,
    "baseURI": "string",
    "createdAt": "2024-01-01T00:00:00Z",
    "updatedAt": "2024-01-01T00:00:00Z",
    "_count": {
      "nfts": 500,
      "listings": 50,
      "sales": 100
    }
  }
}
```

#### GET /collections/{address}/nfts
Récupérer les NFTs d'une collection

**Paramètres de requête:**
- `page` (number, optionnel): Numéro de page (défaut: 1)
- `limit` (number, optionnel): Nombre d'éléments par page (défaut: 20)
- `owner` (string, optionnel): Filtrer par propriétaire
- `listed` (boolean, optionnel): Filtrer par statut de listing
- `sortBy` (string, optionnel): Champ de tri (défaut: tokenId)
- `sortOrder` (string, optionnel): Ordre de tri (asc/desc, défaut: asc)

#### GET /collections/{address}/sales
Récupérer les ventes d'une collection

#### GET /collections/{address}/stats
Récupérer les statistiques d'une collection

### NFTs

#### GET /nfts
Récupérer tous les NFTs

**Paramètres de requête:**
- `page` (number, optionnel): Numéro de page (défaut: 1)
- `limit` (number, optionnel): Nombre d'éléments par page (défaut: 20)
- `collection` (string, optionnel): Filtrer par collection
- `owner` (string, optionnel): Filtrer par propriétaire
- `listed` (boolean, optionnel): Filtrer par statut de listing
- `sortBy` (string, optionnel): Champ de tri (défaut: createdAt)
- `sortOrder` (string, optionnel): Ordre de tri (asc/desc, défaut: desc)

#### GET /nfts/{contract}/{tokenId}
Récupérer un NFT spécifique

**Paramètres de chemin:**
- `contract` (string): Adresse du contrat NFT
- `tokenId` (number): ID du token

#### GET /nfts/owner/{address}
Récupérer les NFTs d'un propriétaire

#### GET /nfts/search
Rechercher des NFTs

**Paramètres de requête:**
- `q` (string, optionnel): Terme de recherche
- `page` (number, optionnel): Numéro de page (défaut: 1)
- `limit` (number, optionnel): Nombre d'éléments par page (défaut: 20)
- `collection` (string, optionnel): Filtrer par collection
- `owner` (string, optionnel): Filtrer par propriétaire
- `listed` (boolean, optionnel): Filtrer par statut de listing

### Listings

#### GET /listings
Récupérer tous les listings actifs

**Paramètres de requête:**
- `page` (number, optionnel): Numéro de page (défaut: 1)
- `limit` (number, optionnel): Nombre d'éléments par page (défaut: 20)
- `collection` (string, optionnel): Filtrer par collection
- `priceMin` (string, optionnel): Prix minimum
- `priceMax` (string, optionnel): Prix maximum
- `seller` (string, optionnel): Filtrer par vendeur
- `sortBy` (string, optionnel): Champ de tri (défaut: createdAt)
- `sortOrder` (string, optionnel): Ordre de tri (asc/desc, défaut: desc)

#### GET /listings/{id}
Récupérer un listing spécifique

#### GET /listings/nft/{contract}/{tokenId}
Récupérer le listing d'un NFT spécifique

#### GET /listings/seller/{address}
Récupérer les listings d'un vendeur

#### GET /listings/collection/{address}
Récupérer les listings d'une collection

#### GET /listings/stats/overview
Récupérer les statistiques des listings

### Sales

#### GET /sales
Récupérer toutes les ventes

**Paramètres de requête:**
- `page` (number, optionnel): Numéro de page (défaut: 1)
- `limit` (number, optionnel): Nombre d'éléments par page (défaut: 20)
- `collection` (string, optionnel): Filtrer par collection
- `buyer` (string, optionnel): Filtrer par acheteur
- `seller` (string, optionnel): Filtrer par vendeur
- `sortBy` (string, optionnel): Champ de tri (défaut: timestamp)
- `sortOrder` (string, optionnel): Ordre de tri (asc/desc, défaut: desc)

#### GET /sales/{id}
Récupérer une vente spécifique

#### GET /sales/buyer/{address}
Récupérer les achats d'un utilisateur

#### GET /sales/seller/{address}
Récupérer les ventes d'un utilisateur

#### GET /sales/stats/overview
Récupérer les statistiques générales des ventes

#### GET /sales/stats/daily
Récupérer les statistiques quotidiennes des ventes

**Paramètres de requête:**
- `days` (number, optionnel): Nombre de jours (défaut: 7)

### Statistiques

#### GET /stats/overview
Récupérer les statistiques générales du marketplace

#### GET /stats/trending
Récupérer les collections tendance

**Paramètres de requête:**
- `period` (string, optionnel): Période (24h, 7d, 30d, défaut: 7d)

#### GET /stats/activity
Récupérer l'activité récente

**Paramètres de requête:**
- `limit` (number, optionnel): Nombre d'éléments (défaut: 20)

#### GET /stats/volume
Récupérer le volume par période

**Paramètres de requête:**
- `period` (string, optionnel): Période (24h, 7d, 30d, 90d, défaut: 7d)

#### GET /stats/collections
Récupérer les statistiques des collections

**Paramètres de requête:**
- `limit` (number, optionnel): Nombre d'éléments (défaut: 10)

#### GET /stats/users
Récupérer les statistiques des utilisateurs

**Paramètres de requête:**
- `limit` (number, optionnel): Nombre d'éléments (défaut: 10)

## Codes d'erreur

- `200` - Succès
- `400` - Requête invalide
- `404` - Ressource non trouvée
- `500` - Erreur interne du serveur

## Rate Limiting

L'API applique un rate limiting de 100 requêtes par fenêtre de 15 minutes par IP.

## Pagination

Tous les endpoints qui retournent des listes supportent la pagination avec les paramètres `page` et `limit`.

## Format des réponses

Toutes les réponses sont au format JSON et incluent :
- `data`: Les données demandées
- `pagination`: Informations de pagination (si applicable)
- `error`: Message d'erreur (en cas d'erreur)

## Exemples d'utilisation

### Récupérer les collections les plus populaires
```bash
curl "http://localhost:3001/api/collections?sortBy=totalSales&sortOrder=desc&limit=10"
```

### Rechercher des NFTs
```bash
curl "http://localhost:3001/api/nfts/search?q=dragon&collection=0x123..."
```

### Récupérer les ventes récentes
```bash
curl "http://localhost:3001/api/sales?sortBy=timestamp&sortOrder=desc&limit=20"
```

### Obtenir les statistiques du marketplace
```bash
curl "http://localhost:3001/api/stats/overview"
```
