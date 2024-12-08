# MySite Project

A full-stack web application with a containerized architecture using Docker, featuring a Python backend, frontend web interface, and MongoDB database.

## Project Structure

```
mysite/
├── backend/         # Python backend service
├── frontend/        # Frontend web application
├── mongodb/         # MongoDB database configuration
├── mongo-express/   # MongoDB web-based admin interface
└── docker-compose.yml
```

## Prerequisites

- Docker
- Docker Compose

## Environment Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/amirulabdlatib/docker-basic.git
   cd mysite
   ```

2. Set up environment variables:
   - Create `.env` files in the following directories:
     - `backend/.env`
     - `mongodb/.env`
     - `mongo-express/.env`

## Running the Application

1. Build and start all services:
   ```bash
   # Run in foreground (see logs in terminal)
   docker-compose up --build

   # Run in detached mode (run in background)
   docker-compose up --build -d
   ```

2. Access the applications:
   - Frontend: http://localhost:80 or http://localhost
   - Backend API: http://localhost:8000
   - MongoDB Express (Database Admin): http://localhost:8081

## Services

### Backend
- Built with Python Fast API
- Runs on port 8000
- Contains the API endpoints and business logic
-  http://localhost:8000/docs to view the endpoints

### Frontend
- Web interface
- Runs on port 80
- Provides the user interface for interacting with the application

### MongoDB
- Database service
- Persistent data storage using Docker volumes
- Version: 7.0.12

### Mongo Express
- MongoDB web-based admin interface
- Runs on port 8081
- Version: 1.0.2

## Development

To modify the application:
1. Make changes to the source code
2. Rebuild the containers:
   ```bash
   docker-compose down
   docker-compose up --build
   ```

## Stopping the Application

To stop all services:
```bash
docker-compose down
```

To stop all services and remove volumes:
```bash
docker-compose down -v