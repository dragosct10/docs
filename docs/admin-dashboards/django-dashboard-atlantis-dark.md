title: Django Dashboard Atlantis Dark

# [Django Dashboard Atlantis Dark](https://appseed.us/admin-dashboards/django-dashboard-atlantis-dark)

**Open-Source Admin Dashboard** coded in **[Django Framework](https://www.djangoproject.com/)** on top of **Atlantis Dark Dashboard** design (free version) - Provided by **AppSeed** [Web App Generator](https://appseed.us/app-generator).

<br />

## Dashboard Features
---

- SQLite, PostgreSQL, SQLAlchemy ORM
- Alembic (DB schema migrations)
- Modular design with **Blueprints**
- Session-Based authentication (via **flask_login**), Forms validation
- Deployment scripts: Docker, Gunicorn / Nginx
- UI Kit: **[Atlantis Dark Dashboard](https://django-dashboard-atlantis-dark.appseed.us/login/)** (Free version) provided by **ThemeKita**
- **MIT License**
- Support: Free support via **Github** and (Paid) **24/7 LIVE Support** via [Discord](https://discord.gg/fZC6hup)

<br />

## Dashboard technology stack
---

- Used Language: [Python3](https://www.python.org/)
- Web Framework: [Django](https://www.djangoproject.com/)
- CSS Framework: [Bootstrap CSS](https://getbootstrap.com/)
- Javascript: [jQuery](https://jquery.com/)

<br />

## Dashboard Links
---

- [Django Dashboard Atlantis Dark](https://appseed.us/admin-dashboards/django-dashboard-atlantis-dark) - Product page
- [Django Dashboard Atlantis Dark](https://github.com/app-generator/django-dashboard-atlantis-dark) - Source code (published on Github)
- [Django Dashboard Atlantis Dark](https://django-dashboard-atlantis-dark.appseed.us/login) - LIVE demo
- [Django Admin Dashboards](https://appseed.us/admin-dashboards/django) - UI-ready admin dashboards generated in Django by **AppSeed**

<br />

![Django Dashboard Atlantis Dark - Open-Source Admin Panel](https://raw.githubusercontent.com/app-generator/static/master/products/django-dashboard-atlantis-dark-screen.png)

<br />

## Prepare your environment
---

The product is built on top of [Django](https://www.djangoproject.com/), a popular Python Web Framework. To build the app, Python3 should be installed properly in the workstation. If you are not sure if Python is properly installed, please open a terminal and type `python --version`. The full-list with dependencies and tools required to build the app:

- [Python3](https://www.python.org/) - the programming language used to code the app
- [Git](https://git-scm.com/) - used to clone the source code from the Github repository
- A [Github](https://github.com/) account - the invitation to the source code, will be sent on your account.
- Basic development tools (g++ compiler, python development libraries ..etc) used by Python to compile the app dependencies in your environment.

<br />

> Check Python (using the terminal)

```bash
$ # Check Python version
$ python --version
Python 3.7 # <--- All good
```

<br />

> Check GIT command tool (using the terminal)

```bash
$ # Check git
$ git --version
$ git version 2.10 # <--- All good
```

<br />

For more information on how to set up your environment please access the resources listed below. In case we've missed something, contact us on Discord.

- [How to set up Python](/how-to/install-python)
- [Setup CentOS for development](/how-to/setup-centos-for-development/)
- [Setup Ubuntu for development](/how-to/setup-ubuntu-for-development/)
- [Setup Windows for development](/how-to/setup-windows-for-development/)

<br />

## Project Structure
---

The boilerplate code is built with a modular structure that follows the recommended pattern used by many open-source projects. The most important files and  directories are shown below:

<br />

```bash
< PROJECT ROOT >                               # application root folder
    |
    |--- core/__init__.py                      # Handles the core features
    |--- core/                                 # define app settings and serve statis assets and pages
    |      | --- <templates>
    |      |        |---<includes>             # Page chunks, components
    |      |        |---<layouts>              # App Layouts (the master pages)
    |      |        |---<account>              # Auth Pages (login, register)
    |      |        |---<pages>                # App Pages
    |      |
    |      | --- views.py
    |      | --- urls.py
    |      | --- models.py
    |
    |--- app/__init__.py                       # Django app that serve the pages
    |--- app/                                  # for authenticated users
    |      | --- views.py
    |      | --- urls.py
    |      | --- models.py
    |
    |--- authentication/__init__.py            # Django app that serve the pages
    |--- authentication/                       # for authenticated users
    |      | --- forms.py                      # Login, Register forms
    |      | --- views.py
    |      | --- urls.py
    |      | --- models.py
    |
    |--- requirements.txt                      # Requirements - SQLite storage
    |
    |--- manage.py                             # bootstrap the app
    |
    |-----------------------------
```

<br />

## Build from sources
---

```bash
$ # Get the code
$ git clone https://github.com/app-generator/django-dashboard-atlantis-dark.git
$ cd django-dashboard-atlantis-dark
$
$ # Virtualenv modules installation (Unix based systems)
$ virtualenv --no-site-packages env
$ source env/bin/activate
$
$ # Virtualenv modules installation (Windows based systems)
$ # virtualenv --no-site-packages env
$ # .\env\Scripts\activate
$
$ # Install modules - SQLite Database
$ pip3 install -r requirements.txt
$
$ # Create tables
$ python manage.py makemigrations
$ python manage.py migrate
$
$ # Start the application (development mode)
$ python manage.py runserver # default port 8000
$
$ # Start the app - custom port 
$ # python manage.py runserver 0.0.0.0:<your_port>
$
$ # Access the web app in browser: http://127.0.0.1:8000/
```

<br />

## Deployment

The app is provided with a basic configuration to be executed in [Heroku](https://heroku.com/), [Docker](https://www.docker.com/), [Gunicorn](https://gunicorn.org/), and [Waitress](https://docs.pylonsproject.org/projects/waitress/en/stable/).

### [Heroku](https://heroku.com/) platform

```bash
$ # Get the code
$ git clone https://github.com/app-generator/django-dashboard-atlantis-dark.git
$ cd django-dashboard-atlantis-dark
$
$ # Heroku Login
$ heroku login
$
$ # Create the app in Heroku platform
$ heroku create # a random name will be generated by Heroku
$
$ # Disable collect static
$ heroku config:set DISABLE_COLLECTSTATIC=1
$
$ # Push the source code and trigger the deploy
$ git push heroku master
$
$ # Execute DBSchema Migration
$ heroku run python manage.py makemigrations
$ heroku run python manage.py migrate
$
$ # Visit the deployed app in browser.
$ heroku open
$
$ # Create a superuser
$ heroku run python manage.py createsuperuser
```

<br />

### [Docker](https://www.docker.com/) execution
---

The application can be easily executed in a docker container. The steps:

> Get the code

```bash
$ git clone https://github.com/app-generator/django-dashboard-atlantis-dark.git
$ cd django-dashboard-atlantis-dark
```

> Start the app in Docker

```bash
$ sudo docker-compose pull && sudo docker-compose build && sudo docker-compose up -d
```

Visit `http://localhost:5005` in your browser. The app should be up & running. 

<br />

### [Gunicorn](https://gunicorn.org/)
---

Gunicorn 'Green Unicorn' is a Python WSGI HTTP Server for UNIX.

> Install using pip

```bash
$ pip install gunicorn
```
> Start the app using gunicorn binary

```bash
$ gunicorn --bind=0.0.0.0:8001 core.wsgi:application
Serving on http://localhost:8001
```

Visit `http://localhost:8001` in your browser. The app should be up & running.


<br />

### [Waitress](https://docs.pylonsproject.org/projects/waitress/en/stable/)
---

Waitress (Gunicorn equivalent for Windows) is meant to be a production-quality pure-Python WSGI server with very acceptable performance. It has no dependencies except ones that live in the Python standard library.

> Install using pip

```bash
$ pip install waitress
```
> Start the app using [waitress-serve](https://docs.pylonsproject.org/projects/waitress/en/stable/runner.html)

```bash
$ waitress-serve --port=8001 core.wsgi:application
Serving on http://localhost:8001
```

Visit `http://localhost:8001` in your browser. The app should be up & running.

<br />

## [Django Atlantis Dark](https://appseed.us/admin-dashboards/django-dashboard-atlantis-dark) - App screens
---

<br />

![Django Dashboard Atlantis Dark - Charts Page.](https://raw.githubusercontent.com/app-generator/static/master/products/django-dashboard-atlantis-dark-screen-1.png)

<br />

![Django Dashboard Atlantis Dark - UI Tables Page.](https://raw.githubusercontent.com/app-generator/static/master/products/django-dashboard-atlantis-dark-screen-2.png)

<br />

![Django Dashboard Atlantis Dark - Main Dashboard Page.](https://raw.githubusercontent.com/app-generator/static/master/products/django-dashboard-atlantis-dark-screen-3.png)

<br />

## Credits & Links
---

<br />

### [Django Admin Dashboards](https://appseed.us/admin-dashboards/django)

Index with UI-ready **admin dashboards** generated by the AppSeed platform in [Django Framework](https://www.djangoproject.com/).
Start fast your next Django project by using functional admin dashboards enhanced with Database, ORM, authentication flow, helpers and deployment scripts.

<br />

### What is [Django](https://www.djangoproject.com/)

[Django](https://www.djangoproject.com/) is a Python-based free and open-source web framework, which follows the model-template-view architectural pattern. It is maintained by the Django Software Foundation, an independent organization established as a 501 non-profit. Django's primary goal is to ease the creation of complex, database-driven websites.

<br />

### [What is dashboard](https://en.wikipedia.org/wiki/Dashboard_(business))

In information technology, a **[dashboard](https://en.wikipedia.org/wiki/Dashboard_(business))** is a user interface that, somewhat resembling an automobile's dashboard, organizes and presents information in a way that is easy to read. However, a computer dashboard is more likely to be interactive than an automobile dashboard (unless it is also computer-based). To some extent, most graphical user interfaces (GUIs) resemble a dashboard - by [Techtarget](https://searchcio.techtarget.com/definition/dashboard)

<br />

### [Atlantis Dark Dashboard](https://www.themekita.com/atlantis-lite-bootstrap-dashboard.html)

Atlantis Dark is a free bootstrap 4 admin dashboard that is beautifully and elegantly designed to display various metrics, numbers or data visualization. Atlantis Dark admin dashboard has 2 layouts, many plugins and UI components to help developers create dashboards quickly and effectively so they can save development time and also help users to make the right and fast decisions based on existing data. - provided by **ThemeKita**.

<br />

---
[Django Dashboard Atlantis Dark](https://appseed.us/admin-dashboards/django-dashboard-atlantis-dark-dark) - Provided by **AppSeed** [Web App Generator](https://appseed.us/app-generator).