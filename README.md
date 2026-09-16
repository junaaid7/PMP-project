PMP — Project Management Platform:
A full-stack, multi-tenant project management platform with an integrated AI Assistant.
The project includes a Next.js frontend, FastAPI backend, PostgreSQL database, authentication, role-based access control, project and task management, and AI-powered tools.
**********************
**********************
About the Project:
I completed this project within 15–20 days, covering the frontend, backend, database integration, authentication, project and task management, AI Assistant, and Docker setup.
The platform is designed to provide a project management experience similar to modern tools such as Jira and Linear, with additional AI capabilities for managing projects and tasks.
***********************
***********************
Key Features:
User registration and login
JWT-based authentication
Multi-tenant organization structure
Tenant-level data isolation
Role-based access control
Organization management
Team member management
Project creation and management
Task creation and management
Task status and assignment
Comments and activity tracking
Project and task details
Dashboard with project and task information
AI Assistant
AI-powered project and task operations
Docker-based development setup
PostgreSQL database
Frontend and backend integration
**********************
**********************
AI Assistant:
The project includes an AI Assistant that can interact with the project management system through defined tools.

The AI Assistant can help with operations such as:
Create tasks
Update tasks
List projects
Get project summaries
Assign users
Generate reports
**************************
**************************
Technology Stack:

Frontend:
Next.js
React
TypeScript
Tailwind CSS
Axios
Redux Toolkit
Lucide React
Sonner

Backend:
Python
FastAPI
SQLAlchemy
Pydantic
JWT Authentication
Argon2 Password Hashing
Async PostgreSQL
Uvicorn

Database:
PostgreSQL

DevOps / Deployment:
Docker
Docker Compose
Docker Desktop
WSL
************************
************************
Multi-Tenant Architecture:
The platform supports multiple organizations/tenants.
Users belong to organizations, and application data is scoped to the user's organization.
The goal is to prevent users from accessing data belonging to another organization.

Tenant-scoped resources include:
Projects
Tasks
Team members
Comments
Activity data
Other organization-related information
User Roles

The platform supports different roles:
Owner
Admin
Manager
Developer
Viewer

Permissions are based on the user's role.
For example, users with management permissions can manage projects and team members, while viewers have more limited access.
*******************************
*******************************
GitHub Repository Structure:
The project was initially maintained in two separate repositories:
Frontend Repository:
frontend-PMP-project
Contains the complete Next.js frontend source code.

Backend Repository:
backend-PMP-project
Contains the complete FastAPI backend source code.

Combined Repository:
PMP-project
This repository contains both frontend and backend source code together.
The combined repository was created to make project management and deployment easier after facing challenges while deploying the frontend and backend from separate repositories.
The original frontend and backend repositories are still maintained separately.

Development Process:
The project was developed over approximately 15–20 days.

The development included:
Project setup
Database configuration
Backend API development
Authentication
Organization and tenant management
Project management
Task management
Role and permission system
Team management
Dashboard
AI Assistant
Frontend-backend integration
Docker configuration
Testing and debugging
Deployment preparation
**************************************
**************************************
Author
Muhammad Junaid
BS Software Engineering
Full-Stack / MERN Developer
**************************************
**************************************
Related Repositories:
frontend-PMP-project — Next.js frontend
backend-PMP-project — FastAPI backend
PMP-project — Combined project and deployment repository
