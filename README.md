# JSONPlaceholder API Explorer

Personal API exploration project. 
Making real HTTP requests with Postman and documenting every endpoint I did. 

## What I Learned

### HTTP (Hypertext Transfer Protocol)
- HTTP is a protocol designed for client-server communication.
- A client sends a **request** to the server.
- The server sends a **response** back to the client.
- The client is typically a **user agent** such as a web browser.

### Postman Experimentation 
- How GET, POST, PUT DELETE works 
- Difference between path param and query params 
- What 200, 201, 204, 404 actually look like in a real response 
- How nested routes works,
 - need to write more content 


### Tools I used 
 - Postman (for request testing and collection export)
 - JSONPlaceholder (free fake REST API)
 - Markdown (documentation)

 ### API base URL
 `https://jsonplaceholder.typicode.com` 

 ## Endpoints 

 ### GET /posts 
 URL : https://jsonplaceholder.typicode.com/posts
 Method : GET 
 Status : 200 OK 
 Returns : Array of 100 posts objects 
 Fileds : userId, id, title, body

 Example response: 
 {
        "userId": 1,
        "id": 1,
        "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
        "body": "quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum   
        rerum est autem sunt rem eveniet architecto"

   }

### GET /posts/1 
 URL : https://jsonplaceholder.typicode.com/posts/1
 Method : GET 
 Status : 200 OK 
 Returns : Detail of user having id 1
 Fileds : userId, id, title, body

 Example response :
 {
    "userId": 1,
    "id": 1,
    "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
    "body": "quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"
}

### GET /posts/999 
-userId 999 does not exists.

 URL : https://jsonplaceholder.typicode.com/posts/999
 Method : GET 
 Status : 404 Not Found  
 Returns : {}
 Fields : None

 Example response:
  {}

### GET /posts?userId=1
 URL : https://jsonplaceholder.typicode.com/posts?userId=1
 Method : GET 
 Status : 200 OK
 Returns : Details of users having userId === 1 
 Fields : None

 Example response:
  
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
    },
    {
        "userId": 1,
        "id": 3,
        "title": "ea molestias quasi exercitationem repellat qui ipsa sit aut",
        "body": "et iusto sed quo iure\nvoluptatem occaecati omnis eligendi aut ad\nvoluptatem doloribus vel accusantium quis pariatur\nmolestiae porro eius odio et labore et velit aut"
    },


### POST /posts
 URL : https://jsonplaceholder.typicode.com/posts/
 Method : POST 
 Status : 201 Created 
 Returns : Entered data by me
 Fileds : title, body, userId

 Example response:
{
    "title": "My first post",
    "body": "My first experimentation on postman.",
    "userId": 1,
    "id": 101
}

### PUT /posts/1
 URL : https://jsonplaceholder.typicode.com/posts/1
 Method : PUT
 Status : 200 OK
 Returns : Updated the data.
 Fileds : title, body, userId, id

 Example response:
 {
    "title": "Learning REST API with postman",
    "body": "Using PUT Query to see what well be the results",
    "userId": 2,
    "id": 1
}

### DELETE /posts/1
URL : https://jsonplaceholder.typicode.com/posts/1
Method : DELETE
Status : 200 OK 
Fields : None 

Example response 
{}


### GET /posts/1/comments
 URL : https://jsonplaceholder.typicode.com/posts/1/comments
 Method : GET
 Status : 200 OK
 Returns : Comments in the content 
 Fileds : postId, id, name, email, body

 Example response 
 {
        "postId": 1,
        "id": 1,
        "name": "id labore ex et quam laborum",
        "email": "Eliseo@gardner.biz",
        "body": "laudantium enim quasi est quidem magnam voluptate ipsam eos\ntempora quo necessitatibus\ndolor quam autem quasi\nreiciendis et nam sapiente accusantium"
    },


### GET /users/1
URL : https://jsonplaceholder.typicode.com/users/1
Method : GET
Status : 200 OK 
Fields : Response contains nested objects — address, geo, company

Example response 
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

### GET /todos?completed=false
URL : https://jsonplaceholder.typicode.com/todos?completed=false
Method : GET
Status : 200 OK 
Fields : Response contains which have not completed todos

Example response 
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
