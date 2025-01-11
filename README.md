# Phonebook Application

## Overview
This Phonebook Application uses **Python 3.10**, the latest libraries, and runs entirely in **Docker** (no Docker Compose). It provides a **Vue.js** frontend (served as a single page by Flask) for contact management, including searching, tagging, photo uploads, and **Redis** caching for fast lookups.

## Key Requirements
- **Python 3.10**  
- **Docker** (single container build & run)
- **Flask** (backend API + serves Vue.js single page)
- **Vue.js** (frontend logic, making API calls to Flask)
- **PostgreSQL** (contact data persistence)
- **Redis** (caching partial search results)
- **Alembic** (database creation & migrations)
- **Bootstrap** (HTML/CSS for responsive UI)

## Features
1. **Contact Management**: Create, read, update, and delete contacts (first name, last name, phone, email, etc.).  
2. **Partial Search**: Redis caching for efficient partial string matching (names or phone numbers).  
3. **Tags**: Associate tags (e.g., "Work," "Family") with each contact and filter by tags.  
4. **Photo Upload**: Attach a photo to a contact; served via Flask and displayed in the Vue.js UI.  
5. **Single-Page Vue.js App**: All interactions happen via RESTful APIs (Flask routes), with Bootstrap for styling.  
6. **Testing**: Unittests for CRUD operations, tagging, photo upload, and cache functionality.

## Running the Application
1. **Build** the Docker image (using the provided `Dockerfile`).
2. **Run** the container, ensuring PostgreSQL and Redis are accessible (inside or external to the container).
3. **Alembic** handles creating and migrating the database schema automatically.
4. **Flask** serves the Vue.js assets and exposes RESTful endpoints.

Use and modify the repository to explore or expand the Phonebook Application’s code and features. All dependencies and configuration run within Docker—no additional installation steps needed.

