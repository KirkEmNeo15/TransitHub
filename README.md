# TransitHub: Transportation Management and Route Mapping System

> **Demo data notice:** All routes, stops, fares and schedules in this project are
> fictional sample data for a school project. They are **not** official transportation
> information. TransitHub does **not** provide live GPS tracking.

## Project Description
TransitHub is a full-stack web application where commuters can explore public
transportation routes (bus, jeepney, van, shuttle, train) on an interactive map,
search routes between two places, and view stops, fares and operating hours.
Administrators manage routes, stops, transportation and alerts.

## Problem Being Addressed
Commuters may have difficulty finding transportation route information because details about routes, stops, fares and operating hours can be scattered across different sources. This can make it difficult to determine which transportation option to take, especially when users are unfamiliar with an area.

TransitHub addresses this problem by providing a centralized system where sample transportation information can be organized, searched and displayed on an interactive map. The system allows commuters to easily explores available routes and transportation details in one place, while administrators can be update and manage the information.

## Project Objectives
- Build a Java (Spring Boot) application that demonstrates abstraction, encapsulation, inheritance and polymorphism.
- Let users view routes and stops on an OpenStreetMap-based map.
- Let users search for routes by origin and destination.
- Let administrators keep route information up to date.

## Target Users
- **Commuters:** view and search routes, save favorites, report wrong information.
- **Administrators:** manage routes, stops, transportation, alerts and users.

## Main Features
_Filled in as features are built (Phases 3–16)._

## Technologies Used
| Layer | Technology |
|---|---|
| Frontend | React, TypeScript, Tailwind CSS, React Router, Axios, Leaflet, React Leaflet |
| Backend | Java, Spring Boot, Spring Web, Spring Data JPA, Spring Security (JWT), Maven |
| Database | PostgreSQL |
| Map | Leaflet + OpenStreetMap |
| Tools | Git, GitHub, Docker Compose, VS Code

## Project Structure
```
transithub/
├── frontend/     React + TypeScript (Vite)
├── backend/      Spring Boot (Maven)
├── database/seed/  Sample SQL/data notes
├── docs/         OOP-DESIGN.md and other documents
├── .env.example  Template for environment variables
├── docker-compose.yml  Local PostgreSQL
└── README.md
```

## Setup (so far: database only)

### 1. Prerequisites
- Git
- Docker Desktop (for PostgreSQL) **or** a local PostgreSQL installation
- Java 17+ and Maven (needed from Phase 3)
- Node.js 18+ (needed from Phase 11)

### 2. Environment variables
```bash
cp .env.example .env     # Windows CMD: copy .env.example .env
```
Open `.env` and set your own values.

| Variable | Meaning |
|---|---|
| `DATABASE_NAME` | Database name (used by Docker to create the DB) |
| `DATABASE_USERNAME` | Database user |
| `DATABASE_PASSWORD` | Database password (choose your own, never commit it) |
| `DATABASE_URL` | JDBC address used by Spring Boot |
| `JWT_SECRET` | Long random string that signs login tokens |
| `JWT_EXPIRATION_MS` | Token lifetime in milliseconds |
| `CORS_ALLOWED_ORIGINS` | Frontend address allowed to call the API |

### 3. Start the database
```bash
docker compose up -d
docker compose ps        # STATUS should become "healthy"
```

## OOP Principles Demonstrated
_Completed in Phase 18. See [docs/OOP-DESIGN.md](docs/OOP-DESIGN.md)._

## API Documentation
_Completed in Phase 18._

## Sample Accounts
_Added in Phase 10 (demo accounts for development only)._

## Screenshots
_Placeholders to be replaced with real screenshots._

## Known Limitations
- Sample data only; not official transit information.
- Routes are stored coordinates; no live GPS, traffic or ETA.
- Route search finds direct routes only (no transfers).

## Future Improvements
Real-time GPS tracking, traffic information, ETA, route optimization with transfers,
mobile app, public transportation API integration.

## Team Members and Roles
| Name | Role |
|---|---|
| _TODO_ | _TODO_ |

## GitHub Workflow
Branches:
```
main                 stable, demo-ready code only
develop              integration branch
feature/backend      Spring Boot work
feature/frontend     React work
feature/maps         Leaflet map
feature/auth         login / JWT
feature/admin        admin dashboard
```
Flow: create a feature branch from `develop` → commit small changes → open a Pull Request into `develop` → teammate reviews → merge. Merge `develop` into `main` only when it works.

Commit message examples:
```
feat: create route entity
feat: add route REST API
feat: implement map view
feat: add JWT authentication
feat: create admin route management
fix: validate route coordinates
docs: update README setup steps
```

## Contributors
_TODO_
