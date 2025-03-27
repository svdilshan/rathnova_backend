# Rathnova Backend with FastAPI

## Overview
Rathnova is a backend system built using FastAPI, a modern and fast web framework for building APIs with Python 3. This backend serves as the core for managing API requests and responses efficiently.

## Features
- FastAPI-based backend
- Asynchronous request handling
- Database integration with SQLAlchemy
- JWT authentication
- CRUD operations for resources

## Installation

### Prerequisites
Ensure you have the following installed:
- Python 3.9+
- Virtual environment (optional but recommended)

### Steps
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/rathnova-fastapi.git
   cd rathnova-fastapi
   ```
2. Create and activate a virtual environment:
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```
3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
4. Set up environment variables:
   ```sh
   cp .env.example .env
   # Update .env with database credentials
   ```
5. Run database migrations:
   ```sh
   alembic upgrade head
   ```
6. Start the FastAPI server:
   ```sh
   uvicorn app.main:app --reload
   ```

## API Endpoints
| Method | Endpoint         | Description          |
|--------|----------------|----------------------|
| GET    | /api/v1/users  | Get all users       |
| POST   | /api/v1/users  | Create a new user   |
| GET    | /api/v1/users/{id} | Get user by ID |
| PUT    | /api/v1/users/{id} | Update user by ID |
| DELETE | /api/v1/users/{id} | Delete user by ID |

## Authentication
- JWT-based authentication is used.
- Users need to log in to get a token.
- Token is required for accessing protected routes.

## Running Tests
To run tests, use:
```sh
pytest
```

## Deployment
To deploy the application, use Docker:
```sh
docker-compose up --build -d
```

## Contributing
1. Fork the repository.
2. Create a new branch.
3. Make your changes and commit.
4. Push to your fork and submit a pull request.

## License
This project is licensed under the MIT License.
