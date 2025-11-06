# Django Social Media Website

A simple social media website template built with Django. This project implements basic social features (posts, profiles, likes, follow, authentication) and serves static and media files in development.

It uses SQLite by default so there's no external database required for local development.

## Requirements
- Python 3.8+ (3.8–3.11 recommended)
- pip
- Windows (PowerShell) instructions are provided below. The steps are similar on macOS/Linux but activation commands differ.

Recommended (optional)
- A virtual environment (venv) to keep dependencies isolated

# check Python
python --version

# create a virtual environment
python -m venv .venv

# allow script execution for this session (temporary)
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope Process -Force

# activate the virtual environment
. .\.venv\Scripts\Activate.ps1

# upgrade pip
python -m pip install --upgrade pip

# If you have a requirements.txt file use it:
if (Test-Path .\requirements.txt) { pip install -r .\requirements.txt } else { pip install "django==3.2.6" pillow }

# run migrations
python manage.py migrate

# create an admin user (optional)
python manage.py createsuperuser

# collect static (optional for dev)
python manage.py collectstatic --noinput

# run the dev server
python manage.py runserver
```

The development server will be available at http://127.0.0.1:8000/ by default.

## License & attribution
This project was adapted from an open-source Django social media template. See the original template link in the project history for full attribution and license details.
