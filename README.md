# AI Model Project

A simple Flask web application for user authentication and personal note management. Users can sign up, log in, create notes, and delete them. The app stores data in SQLite and uses Flask-Login for session management.

## Features

- User signup and login
- Password hashing with Werkzeug
- Protected home page for authenticated users
- Add and delete notes
- SQLite database persistence
- Bootstrap-based frontend

## Tech Stack

- Python
- Flask
- Flask-Login
- Flask-SQLAlchemy
- SQLite
- Bootstrap 4

## Project Structure

```text
project_aimodel/
├── main.py
├── requirements.txt
├── instance/
├── website/
│   ├── __init__.py
│   ├── auth.py
│   ├── models.py
│   ├── views.py
│   ├── static/
│   │   └── index.js
│   └── templates/
│       ├── base.html
│       ├── home.html
│       ├── login.html
│       └── sign_up.html
└── README.md
```

## Getting Started

### 1. Clone the project

```bash
git clone <repository-url>
cd project_aimodel
```

### 2. Create and activate a virtual environment

On Windows:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

On macOS/Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the application

```bash
python main.py
```

The app will start in debug mode and run on:

```text
http://127.0.0.1:5000/
```

## Authentication and Routes

- `/` - Home page for logged-in users
- `/login` - User login page
- `/sign-up` - New user registration page
- `/logout` - Logout current user
- `/delete-note` - Delete a note via POST request

## Database

The project uses SQLite with the database file created automatically when the app starts:

```text
website/database.db
```

A database is created on first run if it does not already exist.

## Notes on Configuration

The app generates a random secret key automatically if `SECRET_KEY` is not set in the environment. For production use, it is recommended to set one explicitly:

```bash
export SECRET_KEY="your-secret-key"
```

On Windows PowerShell:

```powershell
$env:SECRET_KEY="your-secret-key"
```

## License

This project is for educational/demo purposes.

## Contribution

Feel free to fork the project and extend it with features such as:

- password reset
- note categories or tags
- search functionality
- improve UI/UX
- deployment configuration
