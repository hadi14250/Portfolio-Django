# Portfolio-Django

> A personal portfolio website built with Django — a place to introduce myself and showcase the projects I've worked on.

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Django](https://img.shields.io/badge/Django-4.2-092E20?logo=django&logoColor=white)](https://www.djangoproject.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-4169E1?logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3-7952B3?logo=bootstrap&logoColor=white)](https://getbootstrap.com/)

---

## Overview

This is my personal portfolio site. The home page introduces me as a Django developer and renders a dynamic gallery of jobs/projects pulled from the database. Each card links through to its own detail page, and everything is managed from the Django admin — no code changes needed to add new work.

## Features

- **Home page** with a personal intro and a contact link
- **Dynamic project gallery** rendered from the database
- **Per-project detail pages** with images and descriptions
- **Light / Dark / Auto theme toggle** (Bootstrap 5.3)
- **Django admin** for managing jobs and uploading images

## Tech Stack

| Layer       | Technology                              |
| ----------- | --------------------------------------- |
| Backend     | Django 4.2, Python 3.x                  |
| Database    | PostgreSQL                              |
| Frontend    | HTML, Bootstrap 5.3                     |
| Media       | Django `ImageField` with file uploads   |

## Project Structure

```
Portfolio-Django/
├── portfolio/        # Django project (settings, urls, wsgi/asgi)
├── jobs/             # Jobs app (models, views, templates, migrations)
├── images/           # Uploaded job images (media)
├── static/           # Static assets (e.g. profile picture)
└── manage.py
```

## Getting Started

### Prerequisites

- Python 3.x
- PostgreSQL
- pip

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/hadi14250/Portfolio-Django.git
   cd Portfolio-Django
   ```

2. **Create and activate a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate   # macOS/Linux
   ```

3. **Install dependencies**
   ```bash
   pip install django psycopg2-binary Pillow
   ```

4. **Configure the database**
   Update `portfolio/settings.py` to match your local PostgreSQL setup.

5. **Apply migrations**
   ```bash
   python manage.py migrate
   ```

6. **Create a superuser** (for admin access)
   ```bash
   python manage.py createsuperuser
   ```

7. **Run the development server**
   ```bash
   python manage.py runserver
   ```

8. Open [http://127.0.0.1:8000/](http://127.0.0.1:8000/) in your browser.

## Usage

- Visit `/` to see the home page with the gallery of jobs.
- Visit `/admin` to log in and add new job entries (with an image and a summary).
- Click any job card on the home page to view its detail page.

## Routes

| URL                    | View                  | Description           |
| ---------------------- | --------------------- | --------------------- |
| `/`                    | `jobs.views.hadi`     | Home page / gallery   |
| `/jobs/<int:job_id>`   | `jobs.views.detail`   | Job detail page       |
| `/admin/`              | Django admin          | Manage jobs           |

## Contact

- **Email:** hadi.hk.kaddoura2@gmail.com
- **GitHub:** [@hadi14250](https://github.com/hadi14250)

---

<p align="center">Built with Django ✨</p>
