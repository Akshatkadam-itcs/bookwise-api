# API Endpoints  

## Overview

The Bookwise API provides full CRUD operations for managing books in the systems. Below is the detailed dowcumentation for each operation.

## ✅ Create a New Book  

**Endpoint:**  

POST /books

Adds a new book to the system.

## Request Example:

{
  "title": "The Hobbit",
  "author": "J.R.R. Tolkien",
  "published_year": 1937,
  "genre": "Fantasy"
}

## Response Example:

{
  "status": "success",
  "message": "Book added successfully",
  "data": {
    "id": 201,
    "title": "The Hobbit",
    "author": "J.R.R. Tolkien",
    "published_year": 1937
  }
}

## Read (Get all books)

GET /books

Fetches a list of available books

## Response Example:

{
  "status": "success",
  "books": [
    {
      "id": 101,
      "title": "Harry Potter and the Sorcerer's Stone",
      "author": "J.K. Rowling"
    },
    {
      "id": 102,
      "title": "The Hobbit",
      "author": "J.R.R. Tolkien"
    }
  ]
}

## Read (Get books by id)

GET /books/{book_id}

Fetches book of a specific provided id

## Request Example:

GET /books/201

## Response Example:

{
  "id": 201,
  "title": "The Hobbit",
  "author": "J.R.R. Tolkien",
  "published_year": 1937
}


## Update a book

PUT /books/{book_id}

Updates book details like tile, author, publication year.

## Request example:

{
  "title": "The Hobbit (Updated Edition)",
  "published_year": 1938
}

## Response example:

{
  "status": "success",
  "message": "Book updated successfully",
  "data": {
    "id": 201,
    "title": "The Hobbit (Updated Edition)",
    "published_year": 1938
  }
}

## ❌ Delete a Book

DELETE /books/{book_id}

Deletes/ Removes a book from the system by it's id

## Request Example:

DELETE /books/201

## Response Example:

{
  "status": "success",
  "message": "Book deleted successfully"
}



