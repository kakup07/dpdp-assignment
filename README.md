# dpdp-assignment
================================
JOB PORTAL – README
================================

Job Portal is a Python Flask web application that supports three types of users:

Job Seekers

Employers

Admin

The system allows job posting, job applications, resume uploads, application tracking, admin management, and a fully responsive mobile-friendly UI.

PROJECT STRUCTURE

project/
│
├── app.py → Flask app entry point
├── db.py → SQLite connection + helper functions
├── schema.sql → Database schema (tables, triggers, indexes)
├── init_db.py → Script to initialize database
├── requirements.txt → Python dependencies
├── README.txt → This file
│
├── routes/ → Blueprints for different roles
│ ├── users.py
│ ├── employers.py
│ ├── job_seekers.py
│ └── admin.py
│
├── services/ → Business logic
├── repository/ → Database layer (SQL queries)
│
├── templates/ → Jinja2 HTML templates
│ ├── layout.html
│ ├── login.html
│ ├── register.html
│ ├── employer_home.html
│ ├── jb_home.html
│ ├── applied_jobs.html
│ ├── job_detail.html
│ └── error.html
│
└── static/
├── style.css → Custom styles (sidebar + responsive)
└── uploads/ → Resume upload folder (contains .gitkeep)

PREREQUISITES

Make sure you have:

Python 3.8+

pip installed

SQLite3 installed (usually pre-installed)

SETUP INSTRUCTIONS

Create a virtual environment:

  python3 -m venv env
  source env/bin/activate (Linux or macOS)
  env\Scripts\activate (Windows)

Install dependencies:

  pip install -r requirements.txt

Initialize the database:

  python3 init_db.py

Run the flask server:

  export FLASK_APP=app.py
  export FLASK_ENV=development
  flask run

OR simply:

  python3 app.py

The application will start at:

  http://127.0.0.1:5000/

SECTION 5 — ENVIRONMENT VARIABLES

You should create a .env file in the project root with:

  SECRET_KEY=your-secret-key-here

A file named .env.example may be provided to show required variables.