# REST API

Access FiveMSecure data programmatically.

## Authentication

All API requests require your license key:
```bash
curl -H "Authorization: Bearer YOUR_LICENSE_KEY" \
  https://api.fivemsecure.com/endpoint
```

## Endpoints

### Get Server Info
**Response:**
```json
{
  "server_name": "My Server",
  "server_ip": "123.456.789.0:30120",
  "license_key": "abc123",
  "status": "active"
}
```

### Get Bans