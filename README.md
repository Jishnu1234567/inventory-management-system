# DashStack – Inventory Management System

A Django web app for managing products, suppliers, purchases, sales and staff stock requests, with low-stock email alerts, an analytics dashboard, and CSV/PDF export.

## Roles
- **Admin** – manage products, categories, suppliers and purchases; approve/reject stock requests; view dashboard and reports.
- **Staff** – browse products, raise stock requests, track and confirm deliveries.

## Setup
```bash
python -m venv env
env\Scripts\activate          # Windows  (source env/bin/activate on Linux/macOS)
pip install -r inventory_system/requirements.txt
cd inventory_system
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

## Configuration
Secrets are read from environment variables (or an untracked `inventory_system/inventory_system/local_settings.py`):

| Variable | Purpose |
|---|---|
| `DJANGO_SECRET_KEY` | Django secret key |
| `EMAIL_HOST_USER` | SMTP (Gmail) account |
| `EMAIL_HOST_PASSWORD` | Gmail app password |
| `ADMIN_EMAIL` | Address that receives alerts |

## Tech stack
Python, Django 5.2, SQLite, Chart.js, ReportLab.
