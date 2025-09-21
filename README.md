NestCare - Household Services Marketplace

A full-stack platform connecting customers with professionals for household services, with role-based dashboards and automated workflows.

About the Project

NestCare is a full-stack web application designed to connect customers with skilled professionals for a variety of household services. It provides a seamless, role-based experience for customers, professionals, and administrators, ensuring efficient service management and communication.

The platform features distinct dashboards for each user role, an admin-controlled approval process for professionals, and an integrated system for managing service requests from creation to completion.

Features
👨‍💼 Admin Features

Secure Admin Login with separate authentication.

Comprehensive Dashboard: Manage users, services, and requests.

User Management: Approve/reject professionals, flag/unflag users.

Service Management (CRUD): Add, update, delete, and view services.

Analytics Summary with data visualizations (users, requests).

CSV Export: Export closed requests via background tasks and email.

🙋 Customer Features

Easy Registration.

Browse & Search Services.

Service Request Management: Create, track, and close requests.

Monthly Email Reports for service activity.

👷 Professional Features

Specialized Registration with portfolio upload.

Approval Workflow (requires admin approval).

Request Dashboard (Pending, Active, Completed, Rejected).

Daily Email Reminders for pending requests.

Tech Stack
Area	Technology
Backend	Python, Flask, Flask-RESTful, SQLAlchemy, Celery, Redis, Flask-JWT-Extended, Flask-Mail, Flask-Caching
Frontend	Vue.js 3 (Composition API), Vite, Vue Router, Chart.js, Bootstrap 5
Database	SQLAlchemy ORM (agnostic, works with PostgreSQL, SQLite, etc.)
Project Setup
Prerequisites

Python 3.8+

Node.js 18+ and npm

Redis Server (for caching & Celery tasks)

Backend Setup

Navigate to the backend directory:

cd backend


Create and activate a virtual environment:

python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate


Install dependencies:

pip install -r requirements.txt


Run backend services:

Flask App:

python main.py


Celery Worker:

celery -A main.celery worker -l info


Celery Beat Scheduler:

celery -A main.celery beat -l info

Frontend Setup

Navigate to the frontend directory:

cd frontend


Install dependencies:

npm install


Run development server:

npm run dev


Access the app:
Open http://localhost:5173
 (proxied to Flask backend).

File Structure
HouseholdServices_2/
├── backend/
│   ├── apps/
│   ├── main.py
│   ├── requirements.txt
├── frontend/
│   ├── src/
│   ├── package.json
├── README.md

Author

Developed by Nv1023
