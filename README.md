# JSONPlaceholder API Explorer

A personal API exploration project using Postman and JSONPlaceholder for learning HTTP, REST patterns, and response formats.

---

## Overview

This repository documents how I tested the JSONPlaceholder API endpoints with Postman and captured the request/response behavior.

- API: https://jsonplaceholder.typicode.com
- Focus: GET, POST, PUT, DELETE, query parameters, and nested JSON responses
- Goal: Understand request structure, response codes, and payload shape

---

## What I Learned

### HTTP basics
- HTTP is a protocol for client-server communication.
- A client sends a **request** to the server.
- The server returns a **response**.
- Common status codes: `200`, `201`, `204`, `404`.

### Postman practice
- Tested REST methods: `GET`, `POST`, `PUT`, and `DELETE`.
- Compared path parameters vs query parameters.
- Observed real JSON responses from a public API.
- Explored nested objects in resources such as `address` and `company`.

### Tools used
- Postman
- JSONPlaceholder
- Markdown

---

## API Base URL

`https://jsonplaceholder.typicode.com`

---

## Documented Endpoints

### GET /posts
- URL: `https://jsonplaceholder.typicode.com/posts`
- Method: `GET`
- Status: `200 OK`
- Returns: Array of 100 post objects
- Fields: `userId`, `id`, `title`, `body`

Example response:
```json
{
  "userId": 1,
  "id": 1,
  "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
  "body": "quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"
}
```

### GET /posts/1
- URL: `https://jsonplaceholder.typicode.com/posts/1`
- Method: `GET`
- Status: `200 OK`
- Returns: Single post object
- Fields: `userId`, `id`, `title`, `body`

Example response:
```json
{
  "userId": 1,
  "id": 1,
  "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
  "body": "quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"
}
```

### GET /posts/999
- URL: `https://jsonplaceholder.typicode.com/posts/999`
- Method: `GET`
- Status: `404 Not Found`
- Returns: Empty object

Example response:
```json
{}
```

### GET /posts?userId=1
- URL: `https://jsonplaceholder.typicode.com/posts?userId=1`
- Method: `GET`
- Status: `200 OK`
- Returns: All posts with `userId=1`

Example response:
```json
[
  {
    "userId": 1,
    "id": 1,
    "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
    "body": "quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"
  },
  {
    "userId": 1,
    "id": 2,
    "title": "qui est esse",
    "body": "est rerum tempore vitae\nsequi sint nihil reprehenderit dolor beatae ea dolores neque\nfugiat blanditiis voluptate porro vel nihil molestiae ut reiciendis\nqui aperiam non debitis possimus qui neque nisi nulla"
  }
]
```

### POST /posts
- URL: `https://jsonplaceholder.typicode.com/posts`
- Method: `POST`
- Status: `201 Created`
- Returns: Created resource data (API returns simulated ID)
- Fields: `title`, `body`, `userId`

Example response:
```json
{
  "title": "My first post",
  "body": "My first experimentation on postman.",
  "userId": 1,
  "id": 101
}
```

### PUT /posts/1
- URL: `https://jsonplaceholder.typicode.com/posts/1`
- Method: `PUT`
- Status: `200 OK`
- Returns: Updated post object
- Fields: `title`, `body`, `userId`, `id`

Example response:
```json
{
  "title": "Learning REST API with postman",
  "body": "Using PUT query to see what will be the results",
  "userId": 2,
  "id": 1
}
```

### DELETE /posts/1
- URL: `https://jsonplaceholder.typicode.com/posts/1`
- Method: `DELETE`
- Status: `200 OK`
- Returns: Empty object

Example response:
```json
{}
```

### GET /posts/1/comments
- URL: `https://jsonplaceholder.typicode.com/posts/1/comments`
- Method: `GET`
- Status: `200 OK`
- Returns: Array of comments
- Fields: `postId`, `id`, `name`, `email`, `body`

Example response:
```json
{
  "postId": 1,
  "id": 1,
  "name": "id labore ex et quam laborum",
  "email": "Eliseo@gardner.biz",
  "body": "laudantium enim quasi est quidem magnam voluptate ipsam eos\ntempora quo necessitatibus\ndolor quam autem quasi\nreiciendis et nam sapiente accusantium"
}
```

### GET /users/1
- URL: `https://jsonplaceholder.typicode.com/users/1`
- Method: `GET`
- Status: `200 OK`
- Returns: User object with nested `address`, `geo`, and `company`

Example response:
```json
{
  "id": 1,
  "name": "Leanne Graham",
  "username": "Bret",
  "email": "Sincere@april.biz",
  "address": {
    "street": "Kulas Light",
    "suite": "Apt. 556",
    "city": "Gwenborough",
    "zipcode": "92998-3874",
    "geo": {
      "lat": "-37.3159",
      "lng": "81.1496"
    }
  },
  "phone": "1-770-736-8031 x56442",
  "website": "hildegard.org",
  "company": {
    "name": "Romaguera-Crona",
    "catchPhrase": "Multi-layered client-server neural-net",
    "bs": "harness real-time e-markets"
  }
}
```

### GET /todos?completed=false
- URL: `https://jsonplaceholder.typicode.com/todos?completed=false`
- Method: `GET`
- Status: `200 OK`
- Returns: Todos where `completed=false`

Example response:
```json
[
  {
    "userId": 1,
    "id": 3,
    "title": "fugiat veniam minus",
    "completed": false
  }
]
```

---

## Notes

- JSONPlaceholder is a fake online REST API, so `POST`, `PUT`, and `DELETE` requests do not actually change data on the server.
- The responses are simulated to show how REST requests behave.
{
     "userId": 1,
     "id": 1,
     "title": "delectus aut autem",
     "completed": false
    }

## Repository Contents

- Postman collection for the JSONPlaceholder REST API
- Documentation covering basic REST operations
- Examples for using path parameters, query parameters, nested routes, and handling status codes

## Purpose
This repo is intended as a learning reference for HTTP fundamentals, proxy behavior, and REST API request methods. Further learnings will be added in the upcoming future. 
