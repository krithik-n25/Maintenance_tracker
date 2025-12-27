# GearGuard Maintenance Tracker

## Project Overview
GearGuard is a full-stack maintenance management system built with FastAPI (Backend) and Vanilla HTML/JS (Frontend).

## Features Implemented
- **Authentication**: Secure Signup and Login with JWT and Argon2 hashing.
- **Dashboard**: Real-time overview of equipment, requests, and teams.
- **Equipment Management**: CRUD operations for assets, tracking warranty, and status.
- **Team Management**: Create and manage maintenance teams.
- **Request System**: Kanban-style maintenance request tracking with smart auto-fill.
- **Security**: Role-Based Access Control (RBAC) and protected frontend routes.

## Setup Instructions

### Backend
1. Navigate to the `backend` directory.
2. Create virtual environment and install dependencies:
   ```bash
   python -m venv venv
   source venv/bin/activate  # or venv\Scripts\activate on Windows
   pip install -r requirements.txt
   ```
3. Run the server:
   ```bash
   uvicorn app.main:app --reload
   ```
   Server will start at `http://127.0.0.1:8000`.

### Frontend
1. Navigate to the `frontend` directory.
2. Serve the files using any static file server (e.g., Live Server in VS Code):
   - Right-click `index.html` -> "Open with Live Server".
   - Or use python: `python -m http.server 5500`
3. Access the app at `http://127.0.0.1:5500`.

## Implementation Details
- **API Configuration**: `frontend/js/config.js` handles API base URL and auth headers.
- **UI**: Uses a modern dark theme with Spline 3D background components.
- **State Management**: Uses `localStorage` for tokens and Vanilla JS for state.

## Recent Updates
- Integrated `equipment.html`, `teams.html`, and `request.html` with the backend.
- Added Dashboard logic to `index.html`.
- Implemented Kanban board for requests with drag-and-drop support.
