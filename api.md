# REST API

Access FiveMSecure data programmatically.

## Authentication

All API requests require your license key in the Authorization header:
```bash
Authorization: Bearer YOUR_LICENSE_KEY
```

## Base URL

## Endpoints

### Get Server Info

Retrieve server information and status.
```http
POST /api/server-info
Content-Type: application/json

{
  "licenseKey": "your-license-key"
}
```

**Response**:
```json
{
  "serverInfo": {
    "server_name": "My FiveM Server",
    "server_ip": "123.456.789.0:30120",
    "license_key": "abc123...",
    "status": "active",
    "expires_at": "2026-01-01T00:00:00Z"
  }
}
```

### Get Bans

Retrieve all bans for your server.
```http
POST /api/bans
Content-Type: application/json

{
  "action": "get_bans",
  "licenseKey": "your-license-key"
}
```

**Response**:
```json
{
  "bans": [
    {
      "ban_id": "ban_abc123",
      "reason": "Cheating",
      "discordId": "123456789",
      "steamid": "steam:110000abc",
      "banEndDate": "2025-12-31T23:59:59Z"
    }
  ]
}
```

### Get Active Players

Retrieve currently connected players.
```http
GET /api/monitoring?license=your-license-key
```

**Response**:
```json
{
  "players": [
    {
      "id": 1,
      "name": "PlayerName",
      "steam": "steam:110000abc",
      "discord": "discord:123456",
      "license": "license:abc123",
      "ip": "123.456.789.0",
      "ping": 45,
      "health": 200,
      "armor": 100
    }
  ]
}
```

### Create Ban

Ban a player via API.
```http
POST /api/monitoring/actions
Content-Type: application/json

{
  "license": "your-license-key",
  "action": {
    "type": "ban",
    "playerId": "1",
    "reason": "API ban test",
    "duration": "permanent"
  }
}
```

**Response**:
```json
{
  "success": true,
  "message": "Player banned successfully"
}
```

### Unban Player

Remove a ban via API.
```http
POST /api/bans
Content-Type: application/json

{
  "action": "unban",
  "banId": "ban_abc123"
}
```

**Response**:
```json
{
  "success": true,
  "message": "Player unbanned successfully"
}
```

## Rate Limits

- **100 requests per minute**
- **1000 requests per hour**

Rate limit headers are included in responses: