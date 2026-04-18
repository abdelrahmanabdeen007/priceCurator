# PriceCurator Backend API Documentation

## Overview
This document provides complete API documentation for the PriceCurator backend. It covers authentication, products, deals, accessories, contacts, admin functions, the database schema in SQL, error handling standards, and security requirements.

## Authentication
### Endpoints
- `POST /api/auth/register`
  - **Description**: Register a new user.
  - **Request Body**: 
    ```json
    {
      "username": "string",
      "password": "string",
      "email": "string"
    }
    ```
  - **Response**: 
    - `201 Created`: User registered successfully.

- `POST /api/auth/login`
  - **Description**: Authenticate a user and obtain a JWT token.
  - **Request Body**:
    ```json
    {
      "username": "string",
      "password": "string"
    }
    ```
  - **Response**:
    - `200 OK`: Returns JWT token.

## Products
### Endpoints
- `GET /api/products`
  - **Description**: Retrieve a list of products.
- `POST /api/products`
  - **Description**: Create a new product.

## Deals
### Endpoints
- `GET /api/deals`
  - **Description**: Retrieve a list of deals.
- `POST /api/deals`
  - **Description**: Create a new deal.

## Accessories
### Endpoints
- `GET /api/accessories`
  - **Description**: Retrieve a list of accessories.
- `POST /api/accessories`
  - **Description**: Create a new accessory.

## Contacts
### Endpoints
- `GET /api/contacts`
  - **Description**: Retrieve contact information.

## Admin Functions
### Endpoints
- `POST /api/admin/create`
  - **Description**: Create a new admin user.
- `DELETE /api/admin/remove`
  - **Description**: Remove an admin user.

## Database Schema (SQL)
```sql
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    username VARCHAR(50) NOT NULL,
    password VARCHAR(255) NOT NULL,
    email VARCHAR(100) NOT NULL UNIQUE
);

CREATE TABLE products (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    price DECIMAL(10, 2) NOT NULL
);

-- Add more tables as necessary
```

## Error Handling Standards
- All API responses should include the HTTP status code.
- Error responses should include a message with a description of the error.
- Example error response:
  ```json
  {
    "error": {
      "code": 404,
      "message": "Not Found"
    }
  }
  ```

## Security Requirements
- All endpoints require authentication via JWT.
- Sensitive data must be encrypted.
- Regular security audits should be performed.