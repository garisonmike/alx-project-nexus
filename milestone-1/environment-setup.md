# Environment Setup

1. Create repo + branch `nexus/init`
2. Python venv:
```
python -m venv .venv
source .venv/bin/activate
```
3. Install deps:
```
pip install django djangorestframework graphene-django psycopg2-binary python-dotenv gunicorn
```
4. Start project:
```
django-admin startproject getsocial
```
5. Apps to create:
- users  
- posts  
- interactions  
- media  
- notifications  

## .env example
```
DJANGO_SECRET_KEY=change-me
POSTGRES_DB=getsocial
POSTGRES_USER=getsocial
POSTGRES_PASSWORD=securepass
DATABASE_HOST=db
DATABASE_PORT=5432
```
