
## API Response Documentation

This document outlines the expected response formats for successful and error responses from the API.

## Response Schema

The API responses follow a common schema:

## Successful Responses

There are two main types of successful responses: with pagination and without pagination. Both responses share a common structure with slight variations.

### 1. With Pagination

```json
{
  "status": 200,
  "message": "success",
  "data": {
    "products": [
      {
        "id": 1,
        "name": "Product A",
        "price": 10.99
      },
      {
        "id": 2,
        "name": "Product B",
        "price": 15.5
      },
      {
        "id": 3,
        "name": "Product C",
        "price": 7.25
      }
    ],
    "meta": {
      "current_page": 1,
      "per_page": 3,
      "total_pages": 10,
      "total_count": 30
    }
  },
  "errors": {}
}
```

### 2. Without Pagination
```json
{
  "status": 200,
  "message": "Product created sucessfully",
  "data": {
    "product": {
      "id": 1,
      "name": "Product A",
      "price": 10.99
    }
  },
  "errors": {}
}
```

## Error Response:
### 1. General 
```json
{
  "status": 400,
  "message": "Validation failed",
  "errors": {
    "name": [
      "Name cannot be empty"
    ],
    "price": [
      "Price must be a number"
    ]
  },
  "data": {}
}
```

### 1. Unauthorized Request 
```json
{
  "status": 401,
  "message": "You are not authorized to access this resource. Please login or check your credentials."
}
```

## API BEST PRACTICES

[REST API Design Best Practices Medium Blog](https://medium.com/@techworldwithmilan/rest-api-design-best-practices-2eb5e749d428)

[API Design 101: From Basics to Best Practices](https://medium.com/gitconnected/api-design-101-from-basics-to-best-practices-a0261cdf8886)
  
