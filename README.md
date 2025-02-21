# Node.js Server Exploration

This project is designed to explore and understand fundamental server-side concepts in Node.js, focusing on how certain functionalities work under the hood. The project is primarily backend-focused and includes features such as middlewares, streams, and local file storage.

## Features

- Middleware implementation
- Stream handling for efficient data processing
- User management (CRUD operations):
  - List all users
  - Create a new user
  - Edit an existing user
  - Remove a user
- Data persistence using local file storage

## Getting Started

### Prerequisites

Ensure you have Node.js installed on your system. You can download it from [Node.js official website](https://nodejs.org/).

### Installation

1. Clone this repository:
   ```sh
   git clone https://github.com/Vih6460/MBA_Simple_Server.git
   ```
2. Navigate to the project directory:
   ```sh
   cd MBA_Simple_Server/
   ```
3. install the dependencies:
   ```sh
   npm i
   ```

### Usage

To start the server, run:
```sh
npm run dev
```
The server will be running on `http://localhost:3333`. You can change it on file 'src/server.js'

To stop the server, press `CTRL + C` in the terminal.

### API Endpoints

#### List all users
```http
GET /users
```
Retrieves a list of all users stored in the local file.

#### List especific users
```http
GET /users?search=vinicius
```
Retrieves a list of users who match with the search

#### Create a user
```http
POST /users
```
Creates a new user. Requires a JSON body with user details.
```json
{
    "name": "Vinicius",
    "email": "vini@test.com"
}
```

#### Edit a user
```http
PUT /users/:id
```
Edits an existing user based on their ID. Requires a JSON body with updated user details.
```json
{
    "name": "John Doe",
    "email": "johndoe@test.com"
}
```

#### Remove a user
```http
DELETE /users/:id
```
Removes a user from the storage by their ID.

## Contributing

Feel free to fork this repository and submit pull requests with improvements or additional features.

## License

This project is licensed under the MIT License.

---

Happy coding! 🚀
