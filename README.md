# Craftsoft Notes API 

This is a MuleSoft application that exposes a **RESTful Notes API**, built with **RAML** and secured via **Client ID enforcement** using **API Manager Autodiscovery**.

The API supports basic CRUD operations on a `notes` database and is designed to run in different environments using externalized configuration and encrypted secure properties.

---

## Features

- RESTful API using RAML & APIkit
- Client ID/Secret enforcement via API Manager
- Secure database connectivity (MySQL)
- Environment-based configuration (`Dev.yaml`, etc.)
- Encrypted secure properties using Blowfish
- Full error handling and response transformation
- Logging for tracking operations

---


## API Endpoints

| Method | Endpoint           | Description            |
|--------|--------------------|------------------------|
| GET    | `/notes`           | Get all notes          |
| GET    | `/notes/{noteId}`  | Get a note by ID       |
| POST   | `/notes`           | Create a new note      |
| PUT    | `/notes/{noteId}`  | Update a note by ID    |
| DELETE | `/notes/{noteId}`  | Delete a note by ID    |

---

## Security

This API is protected using **Client ID Enforcement** via **API Manager Autodiscovery**.

To call this API:

1. Go to **Anypoint Platform > Exchange**
2. Locate and open this API (e.g., `Craftsoft Notes API`)
3. Click **"Request Access"**
4. Register an application
5. Copy the generated `client_id` and `client_secret`

### 🔑 Add these to your HTTP headers:

```http
client_id: <your-client-id>
client_secret: <your-client-secret>
