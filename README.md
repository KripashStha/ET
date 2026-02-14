# Clarity - Personal Expense Tracker

A full-stack expense tracking application to help you understand your finances better.

## Features

- **Add Expenses & Income** - Track transactions with amount, category, date, and description
- **Edit & Delete Transactions** - Modify or remove entries as needed
- **View All Transactions** - See your complete transaction history
- **Filter by Category or Date Range** - Find specific transactions easily
- **Dashboard** - Overview of your spending with summary cards and category breakdowns
- **Email-based Authentication** - Secure login with JWT tokens

## Tech Stack


**Backend:**
- Django 6.0
- Django REST Framework
- SimpleJWT for authentication
- PostgreSQL (production, Railway)
- SQLite (local development)

**Frontend:**

- React 18 with TypeScript
- Axios for API calls
- React Router for navigation

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/KripashStha/expense-tracker.git
cd expense-tracker
```

### 2. Backend Setup

```bash
cd backend

# Create virtual environment
python -m venv env

# Activate virtual environment
# Windows:
env\Scripts\activate
# macOS/Linux:
source env/bin/activate

# Install dependencies
pip install -r requirements.txt
```

# Run migrations

python manage.py migrate

# Start the backend server

python manage.py runserver

The backend will run at http://localhost:8000

### 3. Frontend Setup

cd frontend

# Install dependencies

npm install

# Start the development server

npm start

The frontend will run at http://localhost:3000

## Usage

1. Open http://localhost:3000 in your browser
2. Register a new account with your email
3. Log in with your credentials
4. Start tracking your expenses and income!


## Deployment

### Backend (Railway)

1. Push your code to GitHub.
2. Create a new Railway project and connect your repo.
3. Add a PostgreSQL plugin in Railway and copy the `DATABASE_URL` it provides.
4. Set the following environment variables in Railway:
	- `DATABASE_URL` (from Railway PostgreSQL)
	- `SECRET_KEY` (generate a secure Django secret key)
	- `DEBUG` = `False`
	- `ALLOWED_HOSTS` = `your-railway-app-url`
	- `FRONTEND_URL` = `https://your-vercel-frontend-url`
5. Deploy! Railway will use the `Procfile` and `requirements.txt` in the backend folder.

### Frontend (Vercel)

1. Push your frontend code to GitHub (in the `frontend` folder).
2. Create a new Vercel project and connect your repo, setting the root to `frontend`.
3. Set the backend API URL in your frontend's environment variables (e.g., `REACT_APP_API_URL=https://your-railway-app-url`)
4. Deploy!

---

**Note:** This project is now ready for both local development and deployment (Railway backend, Vercel frontend). See above for environment variable and deployment details.
