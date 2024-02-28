# Simple Node.js Server with Express

This is a simple Node.js server built with Express framework, implementing CRUD operations for managing users.

## Getting Started

### Prerequisites

Ensure you have Node.js installed on your machine.

### Installation

1. Clone the repository:

    ```bash
    git clone <repository_url>
    ```

2. Navigate to the project directory:

    ```bash
    cd <project_directory>
    ```

3. Install dependencies:

    ```bash
    npm install
    ```

## Usage

To start the server, run:

```bash
npm start
```

The server will start running on `http://localhost:PORT`, where `PORT` is the port number specified in the environment or defaulting to 3000.

## Routes

- **GET /users**: Get all users.
- **POST /users**: Create a new user.
- **GET /users/:id**: Get a user by ID.
- **DELETE /users/:id**: Delete a user by ID.
- **PATCH /users/:id**: Update a user by ID.

## Sample Request and Response

### Create a User

- **Request**:

    ```http
    POST /users
    Content-Type: application/json

    {
        "firstName": "John",
        "lastName": "Doe",
        "age": 30
    }
    ```

- **Response**:

    ```json
    "User with the name John added to the database."
    ```

### Get a User

- **Request**:

    ```http
    GET /users/:id
    ```

- **Response**:

    ```json
    {
        "id": "sample_id",
        "firstName": "John",
        "lastName": "Doe",
        "age": 30
    }
    ```

### Delete a User

- **Request**:

    ```http
    DELETE /users/:id
    ```

- **Response**:

    ```json
    "User with the id sample_id deleted from the database."
    ```

### Update a User

- **Request**:

    ```http
    PATCH /users/:id
    Content-Type: application/json

    {
        "firstName": "Jane"
    }
    ```

- **Response**:

    ```json
    "User with the id sample_id has been updated"
    ```

## Contributing

Contributions are welcome! If you find any issues or want to enhance the functionality, feel free to open a pull request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
