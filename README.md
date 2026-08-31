# Zomato Clone

A full-stack food delivery web application developed as an assignment project using Django REST Framework for the backend and Vue 3 (Vite) for the frontend. The system includes restaurant discovery with category/dietary filters, a cart that restricts items to a single restaurant at a time, promotional coupon application, simulated payment processing, and order status tracking.

## Tech Stack

- **Backend:** Python 3.10+, Django 5, Django REST Framework, SimpleJWT, django-filter, SQLite / PostgreSQL
- **Frontend:** Vue 3 (Composition API), Vite, Pinia, Vue Router 4, Axios, Tailwind CSS

---

## Setup Instructions

### 1. Backend Setup (Django REST Framework)

Navigate to the `backend` directory, set up a Python virtual environment, install dependencies, and run the database migrations:

```bash
cd backend

# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
.\venv\Scripts\activate
# On Linux / macOS:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Create .env file in backend folder for database 
DATABASE_URL=postgresql://postgres:password@host:5432/postgres?sslmode=require
DEBUG=True
SECRET_KEY=django-insecure-change-this-in-production-long-secure-key-50-characters

# Run database migrations
python manage.py migrate

# Seed initial restaurant, menu, and coupon data
python manage.py seed_restaurants

# Start the development server
python manage.py runserver
```

- Backend API: `http://localhost:8000/api/`
- Interactive API Docs (Swagger): `http://localhost:8000/api/docs/`

To run backend automated tests:

```bash
python manage.py test api
```

---

### 2. Frontend Setup (Vue 3 + Vite)

Navigate to the `frontend` directory, install the required npm packages, and start the local development server:

```bash
cd frontend

# Install node dependencies
npm install

# Start Vite development server
npm run dev
```

- Frontend App: `http://localhost:5173`
