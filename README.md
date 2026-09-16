# PMP — Project Management Platform
A full-stack, multi-tenant project management platform with an integrated AI Assistant. The project includes a Next.js frontend, FastAPI backend, PostgreSQL database, authentication, role-based access control, project and task management, and AI-powered tools.

## About the Project
I completed this project within 15–20 days, covering the frontend, backend, database integration, authentication, project and task management, AI Assistant, and Docker setup.
The platform is designed to provide a project management experience similar to modern tools such as Jira and Linear, with additional AI capabilities for managing projects and tasks.

## Key Features
* User registration and login
* JWT-based authentication
* Multi-tenant organization structure
* Tenant-level data isolation
* Role-based access control
* Organization management
* Team member management
* Project creation and management
* Task creation and management
* Task status and assignment
* Comments and activity tracking
* Project and task details
* Dashboard with project and task information
* AI Assistant
* AI-powered project and task operations
* Docker-based development setup
* PostgreSQL database
* Frontend and backend integration

## AI Assistant
The project includes an AI Assistant that can interact with the project management system through defined tools.

The AI Assistant can help with operations such as:
* Create tasks
* Update tasks
* List projects
* Get project summaries
* Assign users
* Generate reports

AI was used during development mainly as a guidance and learning tool. I used it to understand concepts, debug errors, explore solutions, and improve implementation approaches.

I did not copy and paste the complete project code from AI. I implemented, tested, understood, and modified the code myself.

## Technology Stack

### Frontend
* Next.js
* React
* TypeScript
* Tailwind CSS
* Axios
* Redux Toolkit
* Lucide React
* Sonner

### Backend
* Python
* FastAPI
* SQLAlchemy
* Pydantic
* JWT Authentication
* Argon2 Password Hashing
* Async PostgreSQL
* Uvicorn

### Database
* PostgreSQL

### DevOps / Deployment
* Docker
* Docker Compose
* Docker Desktop
* WSL

## Project Architecture

```text
PMP-project
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── Dockerfile
│   ├── .dockerignore
│   ├── package.json
│   └── ...
│
├── backend/
│   ├── app/
│   ├── requirements.txt
│   ├── Dockerfile
│   ├── .dockerignore
│   └── ...
│
├── docker-compose.yml
├── .gitignore
├── .env.example
└── README.md
```

## Application Architecture

```text
             ┌─────────────────────┐
             │   Next.js Frontend  │
             │      Port 3000      │
             └──────────┬──────────┘
                        │
                        │ HTTP / API
                        ▼
             ┌─────────────────────┐
             │   FastAPI Backend   │
             │      Port 8000      │
             └───────┬───────┬─────┘
                     │       │
                     │       │
                     ▼       ▼
              PostgreSQL   OpenAI API
```

## Authentication

The application uses JWT-based authentication.

The basic authentication flow is:

```text
User
 ↓
Login / Register
 ↓
FastAPI Authentication
 ↓
JWT Token
 ↓
Frontend stores token
 ↓
Token sent with API requests
 ↓
Protected Backend Routes
```

Passwords are securely hashed before being stored in the database.

## Multi-Tenant Architecture

The platform supports multiple organizations/tenants.

Users belong to organizations, and application data is scoped to the user's organization.

The goal is to prevent users from accessing data belonging to another organization.

Tenant-scoped resources include:

* Projects
* Tasks
* Team members
* Comments
* Activity data
* Other organization-related information

## User Roles

The platform supports different roles:

* Owner
* Admin
* Manager
* Developer
* Viewer

Permissions are based on the user's role.

For example, users with management permissions can manage projects and team members, while viewers have more limited access.

## Docker Setup

The project can be run locally using Docker Compose.

Docker Compose starts three main services:

```text
Frontend
   ↓
Backend
   ↓
PostgreSQL
```

### Services

| Service    | Port | Purpose              |
| ---------- | ---: | -------------------- |
| Frontend   | 3000 | Next.js application  |
| Backend    | 8000 | FastAPI API          |
| PostgreSQL | 5432 | Application database |

## Running with Docker

Make sure Docker Desktop is installed and running.

Clone the repository:

```bash
git clone <your-PMP-project-repository-url>
```

Move into the project directory:

```bash
cd PMP-project
```

Create your environment file:

```bash
.env
```

Add the required environment variables.

Then build and start the containers:

```bash
docker compose up -d --build
```

Check running containers:

```bash
docker ps
```

Stop the application:

```bash
docker compose down
```

View backend logs:

```bash
docker compose logs backend --tail=50
```

View frontend logs:

```bash
docker compose logs frontend --tail=50
```

## Environment Variables

Create a `.env` file in the project root.

Example:

```env
OPENAI_API_KEY=your_openai_api_key
```

Never commit the real `.env` file or API keys to GitHub.

An `.env.example` file can be used to show the required variables without exposing secrets.

Example:

```env
OPENAI_API_KEY=
```

## Local URLs

After starting Docker Compose:

Frontend:

```text
http://localhost:3000
```

Backend:

```text
http://localhost:8000
```

FastAPI Swagger documentation:

```text
http://localhost:8000/docs
```

## GitHub Repository Structure

The project was initially maintained in two separate repositories:

### Frontend Repository

`frontend-PMP-project`

Contains the complete Next.js frontend source code.

### Backend Repository

`backend-PMP-project`

Contains the complete FastAPI backend source code.

### Combined Repository

`PMP-project`

This repository contains both frontend and backend source code together.

The combined repository was created to make project management and deployment easier after facing challenges while deploying the frontend and backend from separate repositories.

The original frontend and backend repositories are still maintained separately.

## Development Process

The project was developed over approximately **15–20 days**.

The development included:

1. Project setup
2. Database configuration
3. Backend API development
4. Authentication
5. Organization and tenant management
6. Project management
7. Task management
8. Role and permission system
9. Team management
10. Dashboard
11. AI Assistant
12. Frontend-backend integration
13. Docker configuration
14. Testing and debugging
15. Deployment preparation

## Learning and AI-Assisted Development

During development, AI tools were used as a support resource.

AI was mainly used for:

* Understanding new concepts
* Explaining errors
* Debugging
* Finding possible solutions
* Learning FastAPI and Docker concepts
* Improving development approaches

The project was not created by simply copying AI-generated code. The implementation was reviewed, understood, modified, tested, and integrated manually.

## Future Improvements

Possible future improvements include:

* Production deployment with HTTPS
* Custom domain
* Improved CI/CD pipeline
* Automated testing
* Better monitoring and logging
* More advanced AI tools
* AI-generated project insights
* Notifications
* File attachments
* Advanced project analytics
* Production database management

## Author

**Muhammad Junaid**

BS Software Engineering
Full-Stack / MERN Developer

### Related Repositories

* `frontend-PMP-project` — Next.js frontend
* `backend-PMP-project` — FastAPI backend
* `PMP-project` — Combined project and deployment repository
