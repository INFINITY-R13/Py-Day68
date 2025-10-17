# Flask Authentication App

A complete Flask web application with user authentication, registration, login, and protected routes.

## Features

- User registration with email and password
- Secure password hashing using Werkzeug
- User login/logout functionality
- Protected routes requiring authentication
- Session management with Flask-Login
- File download for authenticated users
- SQLite database for user storage
- Bootstrap styling

## Installation

1. Clone the repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Run the application:
   ```bash
   python main.py
   ```

2. Open your browser and navigate to: `http://localhost:5000`

3. Register a new account or login with existing credentials

4. Access protected content and download files

## Project Structure

```
├── main.py              # Main Flask application
├── requirements.txt     # Python dependencies
├── templates/           # HTML templates
│   ├── base.html       # Base template
│   ├── index.html      # Home page
│   ├── login.html      # Login form
│   ├── register.html   # Registration form
│   └── secrets.html    # Protected content
├── static/             # Static files
│   ├── css/
│   │   └── styles.css  # Styling
│   └── files/
│       └── cheat_sheet.pdf  # Downloadable file
└── users.db            # SQLite database (created automatically)
```

## Security Features

- Password hashing with PBKDF2-SHA256
- Session management
- CSRF protection
- Environment-based secret key configuration

## Dependencies

- **Flask 3.1.2** - Web framework
- **Flask-Login 0.6.3** - User session management
- **Flask-SQLAlchemy 3.1.1** - Database ORM integration
- **SQLAlchemy 2.0.44** - Database toolkit and ORM
- **Werkzeug 3.1.3** - WSGI utilities and security functions

## Environment Variables

Set `SECRET_KEY` environment variable for production deployment:

**Linux/Mac:**
```bash
export SECRET_KEY="your-secret-key-here"
```

**Windows:**
```cmd
set SECRET_KEY=your-secret-key-here
```

**PowerShell:**
```powershell
$env:SECRET_KEY="your-secret-key-here"
```

## Development Notes

- The app runs in debug mode by default for development
- Database file (`users.db`) is created automatically on first run
- All passwords are securely hashed using PBKDF2-SHA256
- Session cookies are used for user authentication
