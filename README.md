# Employee Management System (Flask + RBAC)

## Tech Stack
- Backend: Flask
- Frontend: HTML, CSS, Bootstrap 5, Chart.js
- Database: SQLite
- ORM: SQLAlchemy
- Auth: Session based
- Password Hashing: werkzeug.security

## Roles
- Admin
- HR
- Manager
- Employee

## Run Instructions
1. Open terminal in `employee-management`.
2. Create virtual environment:
   - `python -m venv venv`
3. Activate environment:
   - Windows PowerShell: `./venv/Scripts/activate`
4. Install dependencies:
   - `pip install -r requirements.txt`
5. Run app:
   - `python app.py`
6. Open browser:
   - `http://127.0.0.1:5000`

## Sample Logins
- Admin: `admin / admin123`
- HR: `hr / hr123`
- Manager: `manager / manager123`
- Employee: `employee / employee123`

## Notes
- Database tables are auto-created on first run.
- Old schema is auto-rebuilt for compatibility in this demo setup.
- Uploaded files are stored in `static/uploads/`.

## REST API (JSON + JWT)
- Base path: `/api`
- Login: `POST /api/auth/login` with JSON body `{"username":"...","password":"..."}`
- Use token in header: `Authorization: Bearer <token>`
- Health: `GET /api/health`
- Employees:
  - `GET /api/employees`
  - `GET /api/employees/<id>`
  - `POST /api/employees`
  - `PUT /api/employees/<id>`
  - `DELETE /api/employees/<id>`
- Tasks:
  - `GET /api/tasks`
  - `POST /api/tasks`
  - `PUT /api/tasks/<id>`
  - `DELETE /api/tasks/<id>`

The UI remains session-based, and task update forms now also support Fetch API when `localStorage.ems_api_token` is available.
