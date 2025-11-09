# Access Job Recommendation System (Web)

A prototype Django-based web application that provides AI-powered job recommendations for job seekers and an admin dashboard to manage job listings and users.

Key features (prototype):
- User registration & login (Django + DRF + JWT)
- Profile management (resume upload, skills, education, experience)
- Job posting CRUD for admins
- Simple TF-IDF recommender (text similarity between profile+resume and job descriptions)
- Admin site for management

Quick setup (PowerShell):

1. Create and activate virtualenv

```powershell
python -m venv .venv; .\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

2. Set environment (optional): create a `.env` file with SECRET_KEY and DEBUG=1
3. Apply migrations and create superuser

```powershell
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

4. Open http://127.0.0.1:8000/

Notes:
- This is a minimal prototype focused on architecture and a simple recommender. For production, secure secrets, use HTTPS, add rate-limiting, background tasks, and robust resume parsing.
