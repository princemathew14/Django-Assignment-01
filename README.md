# Project Management System (Django + PostgreSQL)

This is a Django-based web application for managing software projects, tasks, users, comments, and time logs.  
It allows project teams to track task progress, log hours, and collaborate via comments.


##  Domain

**Application Domain:** Project Management  
This system models real-world workflows between developers, designers, project managers, and QA engineers using:

- Projects
- Users
- Tasks (assigned to users per project)
- Comments (attached to tasks)
- Time Logs (to track effort)


##  Setup Instructions

### 1. Clone the Repository

git clone https://github.com/princemathew14/Django-Assignment-01.git
cd Django-Assignment-01
 2. Create a Virtual Environment
python -m venv venv
# Activate the environment:
source venv/bin/activate  # On Unix/macOS
venv\Scripts\activate     # On Windows
3. Install Dependencies

pip install -r requirements.txt
 Environment Configuration
1. Create a .env File (in the project root)
Copy the template and fill in your actual credentials:
cp env.example .env
2. Edit .env and fill in:
SECRET_KEY='your-django-secret-key'
DEBUG=True
DATABASE_URL='postgres://your_db_user:your_db_password@localhost:5432/your_db_name'
Make sure your PostgreSQL database is created and running.

 Migrations & Superuser
 1. Apply Migrations
python manage.py makemigrations
python manage.py migrate
2. Create a Superuser
python manage.py createsuperuser
# Enter username, email, and password as prompted
Run the Development Server
python manage.py runserver
Visit: http://127.0.0.1:8000/admin/ to access the Django Admin Dashboard.

Log in with your superuser credentials to manage Projects, Users, Tasks, Comments, and Time Logs.
Admin Sample Data
Use the admin interface to add 3–5 records for each model.

Make sure relationships (like tasks to users, comments to tasks) are linked.

Project Structure Overview

myproject/

 myapp/                # App containing models, views, admin setup
 myproject/            # Settings and main config
 manage.py             # Django entry point
.env                  # Environment variables (ignored by Git)
 env.example          # Sample env file to share
requirements.txt      # All Python dependencies
 README.md             # This file








