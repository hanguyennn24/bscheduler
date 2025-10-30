# Scheduling Application

Scheduling Application is a lightweight Flask-based web app for managing employees, collecting availability, and generating schedules. It's designed for small teams in horeca sector in Belgium who need a simple, customizable shift scheduling solution.  The application uses linear programming to minimize total cost.

## New feature
- Including example data for employees' details

## Features
- Support easy scheduling without creating account, or create manager and employee accounts for a company to save the details for next scheduling
- Schedule according to employee availability, min/max working hours allowed for an employee, wage, and role
- Several languages are supported, including English, French, Dutch, and Vietnamese

## Tech stack
- Python 3.9+
- Flask microframework
- Minimal client-side JS for UI enhancements
- PuLP as LM solver, which does not require license for public deployment

## Quickstart (local development)

1. Create a Python virtual environment and activate it:

   ```powershell
   python -m venv venv
   .\venv\Scripts\Activate.ps1
   ```

2. Install dependencies:

   ```powershell
   pip install -r venv/requirements.txt
   ```

3. Run the app in development mode:

   ```powershell
   python shift_scheduler_app/app.py
   ```

4. Open http://127.0.0.1:5000 in your browser.

## Repository layout

- `shift_scheduler_app/` — application package (Flask app, static assets, templates)
- `scripts/` — helper scripts (e.g., `reset_password.py`)
- `venv/` — local Python virtual environment (ignored)

## Deployment notes

This project is intended for small deployments. For production, run behind a WSGI server (Gunicorn/uWSGI) and use a reverse proxy (nginx). Configure secrets via environment variables and use a production-ready database instead of the default SQLite when needed.

## License

This project is licensed under the MIT License — see `LICENSE` for details.



