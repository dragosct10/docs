title: Django Dashboard Light

# [Django Dashboard Light](https://appseed.us/admin-dashboards/django-dashboard-light)

**Open-Source Admin Dashboard** coded in **[Django Framework](https://www.djangoproject.com/)** on top of **Light Dashboard** design (free version) - Provided by **AppSeed** [Web App Generator](https://appseed.us/app-generator).

<br />

## Dashboard Features
---

- UI-Ready app, SQLite Database, Django Native ORM
- Modular design, clean code-base
- Session-Based Authentication, Forms validation
- Deployment scripts: Heroku, Docker, Gunicorn / Nginx
- UI Kit: **[Light Dashboard](https://django-dashboard-light.appseed.us/login/)** (Free version) provided by **Creative-Tim**
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

- [Django Dashboard Light](https://appseed.us/admin-dashboards/django-dashboard-light) - Product page
- [Django Dashboard Light](https://github.com/app-generator/django-dashboard-light) - Source code (published on Github)
- [Django Dashboard Light](https://django-dashboard-light.appseed.us/login) - LIVE demo
- [Django Admin Dashboards](https://appseed.us/admin-dashboards/django) - UI-ready admin dashboards generated in Django by **AppSeed**
- **[Django Dashboard Light PRO](https://appseed.us/admin-dashboards/django-dashboard-light-pro)** - Premium Version - [LIVE Demo](https://django-dashboard-light-pro.appseed.us/login/)

<br />

![Django Dashboard Light - Open-Source Admin Panel](https://raw.githubusercontent.com/app-generator/static/master/products/django-dashboard-light-screen.png)

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
$ git clone https://github.com/app-generator/django-dashboard-light.git
$ cd django-dashboard-light
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
$ git clone https://github.com/app-generator/django-dashboard-light.git
$ cd django-dashboard-light
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
$ git clone https://github.com/app-generator/django-dashboard-light.git
$ cd django-dashboard-light
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

## [Django Light](https://appseed.us/admin-dashboards/django-dashboard-light) - App screens
---

<br />

![Django Dashboard Light - UI Notifications Page.](https://raw.githubusercontent.com/app-generator/static/master/products/django-dashboard-light-screen-1.png)

<br />

![Django Dashboard Light - User Profile Page.](https://raw.githubusercontent.com/app-generator/static/master/products/django-dashboard-light-screen-2.png)

<br />

![Django Dashboard Light - UI Modals Page.](https://raw.githubusercontent.com/app-generator/static/master/products/django-dashboard-light-screen-3.png)

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

### [What is a dashboard](https://en.wikipedia.org/wiki/Dashboard_(business))

A dashboard is a set of pages that are easy to read and offer information to the user in real-time regarding his business. A dashboard usually consists of graphical representations of the current status and trends within an organization. Having a well-designed dashboard will give you the possibility to act and make informed decisions based on the data that your business provides - *definition provided by [Creative-Tim - Free Dashboard Templates](https://www.creative-tim.com/blog/web-design/free-dashboard-templates/?ref=appseed)*.

<br />

### [Light Bootstrap Dashboard](https://www.creative-tim.com/product/light-bootstrap-dashboard?ref=appseed)

[Light Bootstrap Dashboard](https://www.creative-tim.com/product/light-bootstrap-dashboard?ref=appseed) is bootstrap 4 admin dashboard template designed to be beautiful and simple. It is built on top of Bootstrap 4 and it is fully responsive. It comes with a big collections of elements that will offer you multiple possibilities to create the app that best fits your needs. It can be used to create admin panels, project management systems, web applications backend, CMS or CRM  - provided by **Creative-Tim**.

<br />

---
[Django Dashboard Light](https://appseed.us/admin-dashboards/django-dashboard-light) - Provided by **AppSeed** [Web App Generator](https://appseed.us/app-generator).
