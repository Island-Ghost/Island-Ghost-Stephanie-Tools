# API Reference

Welcome to the IslandGhost Stephanie Tools API documentation. This section provides detailed information about the available API endpoints, request/response formats, and authentication methods.

## Base URL

```
https://api.islandghost.dev/v1
```

## Authentication

```http
Authorization: Bearer YOUR_API_KEY
```

## Endpoints

### Authentication
- `POST /auth/login` - Authenticate and get an access token
- `POST /auth/refresh` - Refresh an access token

### Core Features
- `GET /features` - List all available features
- `GET /features/:id` - Get details about a specific feature

### Data Operations
- `GET /data` - Query data with filters
- `POST /data` - Create new data
- `PUT /data/:id` - Update existing data
- `DELETE /data/:id` - Remove data

## Rate Limiting
- 100 requests per minute per IP address
- 1,000 requests per hour per API key

## Error Handling

All error responses follow this format:

```json
{
  "error": {
    "code": "error_code",
    "message": "Human-readable error message",
    "details": {
      "field": "Additional error details"
    }
  },
  "request_id": "unique_request_identifier"
}
```

## SDKs

Official client libraries are available for:

- [JavaScript/Node.js](https://github.com/Island-Ghost/sdk-js)
- [Python](https://github.com/Island-Ghost/sdk-python)
- [Java](https://github.com/Island-Ghost/sdk-java)

## Changelog

See [CHANGELOG.md](../../CHANGELOG.md) for version history and changes.
