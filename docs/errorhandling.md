# Error Handling  

## Overview 

The Bookwise API follows standard error responses to codes to ensure proper debugging and issue resolution. Below are some common errors and hoe to handle them.

## 🔹 400 - Bad Request 

Occurs when something is icorrectly requested or request is formatted incorrectly or missing required parameters.

### Response Example:
```json
{
  "status": "error",
  "code": 400,
  "message": "Invalid request format. Missing required field: 'title'."
}

## 🔹 401 - Unauthorized

Occurs when authentication fails due to an invalid or missing API key.

### Response Example
{
  "status": "error",
  "code": 401,
  "message": "Unauthorized access. Please provide a valid API key."
}



##🔹 403 - Forbidden

Occurs when the request is valid but the user lacks the necessary permissions.

### Response example
{
  "status": "error",
  "code": 403,
  "message": "Access denied. You do not have permission to modify this resource."
}


##🔹 404 - Not Found

Occurs when the requested resource or endpoint does not exist.

###Response Example:
{
  "status": "error",
  "code": 404,
  "message": "Book with ID 999 not found."
}



##🔹 500 - Internal Server Error

Occurs when the server encounters an unexpected issue.

###Response Example:
{
  "status": "error",
  "code": 500,
  "message": "An unexpected error occurred. Please try again later."
}




