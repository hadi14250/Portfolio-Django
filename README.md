# Portfolio-Django

A personal portfolio website built with Django to showcase my work and projects.

## About

This is my personal portfolio site where I introduce myself as a Django developer and display a gallery of jobs/projects I've worked on. Each item links to its own detail page.

## Features

- Home page with an introduction and contact link
- Dynamic gallery of jobs/projects rendered from the database
- Detail page for each job
- Light/Dark/Auto theme toggle (Bootstrap 5.3)
- Django admin for managing jobs and uploading images

## Tech Stack

- **Backend:** Django 4.2, Python
- **Database:** PostgreSQL
- **Frontend:** HTML, Bootstrap 5.3
- **Media:** Django `ImageField` with file uploads

## Project Structure

```
Portfolio-Django/
├── portfolio/        # Django project (settings, urls, wsgi/asgi)
├── jobs/             # Jobs app (models, views, templates, migrations)
├── images/           # Uploaded job images (media)
├── static/           # Static assets (e.g., profile picture)
└── manage.py
```

## Getting Started

### Prerequisites

- Python 3.x
- PostgreSQL
- pip

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/hadi14250/Portfolio-Django.git
   cd Portfolio-Django
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate   # macOS/Linux
   ```

3. Install dependencies:
   ```bash
   pip install django psycopg2-binary Pillow
   ```

4. Configure the database in `portfolio/settings.py` to match your local PostgreSQL setup.

5. Run migrations:
   ```bash
   python manage.py migrate
   ```

6. Create a superuser to access the admin:
   ```bash
   python manage.py createsuperuser
   ```

7. Start the development server:
   ```bash
   python manage.py runserver
   ```

8. Open `http://127.0.0.1:8000/` in your browser.

## Usage

- Visit `/` to see the home page with the gallery of jobs.
- Visit `/admin` to log in and add new job entries (with an image and a summary).
- Click any job card on the home page to view its detail page.

## Routes

| URL | View | Description |
|---|---|---|
| `/` | `jobs.views.hadi` | Home page / gallery |
| `/jobs/<int:job_id>` | `jobs.views.detail` | Job detail page |
| `/admin/` | Django admin | Manage jobs |

## Contact

- **Email:** hadi.hk.kaddoura2@gmail.com
- **GitHub:** [hadi14250](https://github.com/hadi14250)
