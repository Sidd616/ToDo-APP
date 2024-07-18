
---

# Todo App RESTful API

This is a simple Node.js Express application that provides a RESTful API for managing Todos.

## Prerequisites

- Node.js installed on your machine ([Download Node.js](https://nodejs.org/))
- npm (Node Package Manager) installed

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/Sidd616/ToDo-APP.git
   cd repository-folder
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the server:
   ```bash
   npm start
   ```
   The server will start running on `http://localhost:3000`.

## API Endpoints

### GET /todos

Fetches all todos.

**Response**
- `200 OK`: Returns an array of all todos.

### GET /todos/:id

Fetches a specific todo by ID.

**Parameters**
- `id`: ID of the todo to fetch.

**Response**
- `200 OK`: Returns the todo object.
- `404 Not Found`: If the todo with the given ID does not exist.

### POST /todos

Creates a new todo.

**Request Body**
- `title`: Title of the todo (required).
- `description`: Description of the todo (required).

**Response**
- `201 Created`: Returns the ID of the newly created todo.
- `400 Bad Request`: If `title` or `description` is missing in the request body.

### PUT /todos/:id

Updates an existing todo by ID.

**Parameters**
- `id`: ID of the todo to update.

**Request Body**
- `title`: Updated title of the todo.
- `description`: Updated description of the todo.

**Response**
- `200 OK`: Indicates successful update.
- `404 Not Found`: If the todo with the given ID does not exist.

### DELETE /todos/:id

Deletes a todo by ID.

**Parameters**
- `id`: ID of the todo to delete.

**Response**
- `200 OK`: Indicates successful deletion.
- `404 Not Found`: If the todo with the given ID does not exist.

## Error Handling

- The API handles errors gracefully and returns appropriate HTTP status codes along with error messages when necessary (e.g., `404 Not Found`, `400 Bad Request`).

## Technologies Used

- Node.js
- Express.js
- JSON for data storage (in-memory)


---
