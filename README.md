# Task Management API

## Overview

This Task Management API is a RESTful service built with Node.js and Express.js, allowing users to manage their tasks efficiently. It provides endpoints for user authentication, task creation, retrieval, updating, and deletion.

## Features

- User registration and authentication
- CRUD operations for tasks
- Task prioritization
- Secure API with JWT authentication
- MongoDB integration for data persistence
- Docker support for easy development setup
- API documentation with Swagger

## Prerequisites

- Node.js (v14 or later)
- Docker and Docker Compose (for running MongoDB)
- npm or yarn

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/task-management-api.git
cd task-management-api
```

### 2. Install dependencies

```bash
npm install
```

### 3. Set up environment variables

Create a `.env` file in the root directory and add the following:

```
PORT=3000
MONGODB_URI=mongodb://root:rootpassword@localhost:27017/taskmanagement?authSource=admin
JWT_SECRET=your_jwt_secret_here
```

Replace `your_jwt_secret_here` with a secure random string.

### 4. Start MongoDB using Docker

```bash
docker-compose up -d
```

This command starts MongoDB and MongoDB Express. You can access MongoDB Express at `http://localhost:8081`.

### 5. Run the application

For development:

```bash
npm run dev
```

For production:

```bash
npm start
```

The API will be available at `http://localhost:3000`.

## API Documentation

Once the application is running, you can access the Swagger UI documentation at:

```
http://localhost:3000/api-docs
```

This provides an interactive interface to explore and test the API endpoints.

## API Endpoints

Here's a brief overview of the available endpoints:

### Authentication

- `POST /api/auth/register`: Register a new user
- `POST /api/auth/login`: Login and receive a JWT

### Tasks

- `GET /api/tasks`: Get all tasks for the authenticated user
- `POST /api/tasks`: Create a new task
- `GET /api/tasks/:id`: Get a specific task by ID
- `PUT /api/tasks/:id`: Update a specific task
- `DELETE /api/tasks/:id`: Delete a specific task

## Running Tests

To run the test suite:

```bash
npm test
```

## Docker

The project includes a `docker-compose.yml` file for easy MongoDB setup. To start the MongoDB service:

```bash
docker-compose up -d
```

To stop the service:

```bash
docker-compose down
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgments

- Express.js
- MongoDB
- Swagger UI
- JSON Web Tokens
