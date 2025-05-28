# Authentication  

## Overview  

The Bookwise API uses secure authentication methods to ensure that only authorized users get to access resources. Authentication is required for all the endpoints.

## Authentication Methods  

- **API Key Authentication** (recommended)  
- **OAuth 2.0** (for third-party integrations)

## API Key Authentication  

To access protected endpoints, users must include theri API keysin the request header

### Request Example:

GET /books/search?q=Harry+Potter
Header: Authorization: Bearer <YOUR_API_KEY>

### Response Example:
```json

{
  "status": "success",
  "data": [
    {
      "id": 101,
      "title": "Harry Potter and the Sorcerer's Stone",
      "author": "J.K. Rowling",
      "published_year": 1997
    }
  ]
}

## OAuth 2.0

For users integrating with third-party applications, OAuth 2.0 is available.

### Token Generation:

POST /auth/token
Body: {"client_id": "your_client_id", "client_secret": "your_client_secret"}

### Response Example:
'''json

{
  "access_token": "eyJhbGciOiJIUzI1NiIsIn...",
  "expires_in": 3600
}

##Error handling:

If you encounter '401 Unauthorized', this means you are not authorized and need to have an API key for accessing resources.