## Overview  
This section contains practical usage examples for interacting with the Bookwise API.  

---

## ✅ Create a New Book  

### Request:  

POST /books
Content-Type: application/json

{
  "title": "The Hobbit",
  "author": "J.R.R. Tolkien",
  "published_year": 1937,
  "genre": "Fantasy"
}

{
  "status": "success",
  "message": "Book added successfully",
  "data": {
    "id": 201,
    "title": "The Hobbit",
    "author": "J.R.R. Tolkien"
  }
}

## 📘 Get a Book by ID

### Request:
GET /books/201


### Response:
{
  "id": 201,
  "title": "The Hobbit",
  "author": "J.R.R. Tolkien",
  "published_year": 1937
}



## 🔍 Search Books
### Request:

GET /books/search?q=Harry+Potter


### Response:
{
  "status": "success",
  "results": [
    {
      "id": 101,
      "title": "Harry Potter and the Sorcerer's Stone",
      "author": "J.K. Rowling"
    },
    {
      "id": 102,
      "title": "Harry Potter and the Chamber of Secrets",
      "author": "J.K. Rowling"
    }
  ]
}



### ✏️ Update a Book
### Request:

PUT /books/201

Content-Type: application/json


{
  "title": "The Hobbit (Updated Edition)",
  "published_year": 1938
}


### Response:
{
  "status": "success",
  "message": "Book updated successfully",
  "data": {
    "id": 201,
    "title": "The Hobbit (Updated Edition)",
    "published_year": 1938
  }
}



##❌ Delete a Book

### Request:
DELETE /books/201


### Response:
{
  "status": "success",
  "message": "Book deleted successfully"
}



---

