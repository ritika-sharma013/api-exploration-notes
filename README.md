# api-exploration-notes

This repository contains notes and examples for exploring HTTP and REST API concepts, with a focus on the JSONPlaceholder REST API.

## What I Learned

### HTTP (Hypertext Transfer Protocol)
- HTTP is a protocol designed for client-server communication.
- A client sends a **request** to the server.
- The server sends a **response** back to the client.
- The client is typically a **user agent** such as a web browser.

### Proxies and Network Layers
- Between the client and server, there are many entities called **proxies**.
- Proxies operate at the application layer and help route, transform, or inspect traffic.
- Common proxy functions include:
  - **Caching**: storing responses for faster reuse (public or private cache, including browser cache)
  - **Filtering**: scanning traffic for security or content restrictions (e.g., antivirus, parental control)
  - **Load balancing**: distributing requests among multiple servers
  - **Authentication**: controlling access to protected resources
  - **Logging**: recording request and response history for analysis and troubleshooting

### HTTP Methods
- **GET**: retrieve data from a server
- **PUT**: update or replace existing data on the server
- **POST**: create new data or submit information
- **DELETE**: remove data from the server

### HTTP Request 







### HTTP Response








## Repository Contents
- Postman collection for the JSONPlaceholder REST API
- Documentation covering basic REST operations
- Examples for using path parameters, query parameters, nested routes, and handling status codes

## Purpose
This repo is intended as a learning reference for HTTP fundamentals, proxy behavior, and REST API request methods. Further learnings will be added in the upcoming future. 
