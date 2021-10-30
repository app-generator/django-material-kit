# [Django Boilerplate](https://appseed.us/boilerplate-code/django-boilerplate)

> Template [boilerplate code](https://appseed.us/boilerplate-code) used by [AppSeed](https://appseed.us) to generate simple admin dashboards coded in [Django](https://www.djangoproject.com/) - Features:

<br />

- Up-to-date [dependencies](./requirements.txt): **Django 3.2.6 LTS**
- [SCSS compilation](#recompile-css) via **Gulp**
- UI Kit: **Pixel UI Kit** (Free Version) by **Themesberg**
- SQLite Database, Django Native ORM
- Modular design, clean codebase
- Session-Based Authentication, Forms validation
- Deployment scripts: Docker, Gunicorn / Nginx
- Support via **Github** (issues tracker) and [Discord](https://discord.gg/fZC6hup).

<br />

> Links

- [Boierplate Code Django](https://appseed.us/django/django-pixel-bootstrap-uikit) - Product page
- [Boierplate Code Django](https://docs.appseed.us/boilerplate-code/django/) - Documentation

<br />

## Want more? Go PRO!

PRO versions include **Premium UI Kits**, Lifetime updates and **24/7 LIVE Support** (via [Discord](https://discord.gg/fZC6hup))

| [Django Datta PRO](https://appseed.us/admin-dashboards/django-dashboard-dattaable-pro) | [Django Material PRO](https://appseed.us/admin-dashboards/django-dashboard-material-pro) | [Django Volt PRO](https://appseed.us/admin-dashboards/django-dashboard-volt-pro) |
| --- | --- | --- |
| [![Django Datta PRO](https://raw.githubusercontent.com/app-generator/django-dashboard-dattaable-pro/master/media/django-dashboard-dattaable-pro-screen.png)](https://appseed.us/admin-dashboards/django-dashboard-dattaable-pro) | [![Django Material PRO](https://raw.githubusercontent.com/app-generator/django-dashboard-material-pro/master/media/django-dashboard-material-pro-screen.png)](https://appseed.us/admin-dashboards/django-dashboard-material-pro) | [![Django Volt PRO](https://raw.githubusercontent.com/app-generator/django-dashboard-volt-pro/master/media/django-dashboard-volt-pro-screen.png)](https://appseed.us/admin-dashboards/django-dashboard-volt-pro)

<br />

![Boierplate Code Django - Template project provided by AppSeed.](https://user-images.githubusercontent.com/51070104/132866430-46a91bcd-98dd-44ba-9e9c-acbd5e8f1156.png)

<br />

## How to use it

```bash
$ # Get the code
$ git clone https://github.com/app-generator/boilerplate-code-django.git
$ cd boilerplate-code-django
$
$ # Virtualenv modules installation (Unix based systems)
$ virtualenv env
$ source env/bin/activate
$
$ # Virtualenv modules installation (Windows based systems)
$ # virtualenv env
$ # .\env\Scripts\activate
$
$ # Install modules - SQLite Storage
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

> Note: To use the app, please access the registration page and create a new user. After authentication, the app will unlock the private pages.

<br />

## Code-base structure

The project is coded using a simple and intuitive structure presented bellow:

```bash
< PROJECT ROOT >
   |
   |-- core/                               # Implements app configuration
   |    |-- settings.py                    # Defines Global Settings
   |    |-- wsgi.py                        # Start the app in production
   |    |-- urls.py                        # Define URLs served by all apps/nodes
   |
   |-- apps/
   |    |
   |    |-- home/                          # A simple app that serve HTML files
   |    |    |-- views.py                  # Serve HTML pages for authenticated users
   |    |    |-- urls.py                   # Define some super simple routes  
   |    |
   |    |-- authentication/                # Handles auth routes (login and register)
   |    |    |-- urls.py                   # Define authentication routes  
   |    |    |-- views.py                  # Handles login and registration  
   |    |    |-- forms.py                  # Define auth forms (login and register) 
   |    |
   |    |-- static/
   |    |    |-- <css, JS, images>         # CSS files, Javascripts files
   |    |
   |    |-- templates/                     # Templates used to render pages
   |         |-- includes/                 # HTML chunks and components
   |         |    |-- navigation.html      # Top menu component
   |         |    |-- sidebar.html         # Sidebar component
   |         |    |-- footer.html          # App Footer
   |         |    |-- scripts.html         # Scripts common to all pages
   |         |
   |         |-- layouts/                   # Master pages
   |         |    |-- base-fullscreen.html  # Used by Authentication pages
   |         |    |-- base.html             # Used by common pages
   |         |
   |         |-- accounts/                  # Authentication pages
   |         |    |-- login.html            # Login page
   |         |    |-- register.html         # Register page
   |         |
   |         |-- home/                      # UI Kit Pages
   |              |-- index.html            # Index page
   |              |-- 404-page.html         # 404 page
   |              |-- *.html                # All other pages
   |
   |-- requirements.txt                     # Development modules - SQLite storage
   |
   |-- .env                                 # Inject Configuration via Environment
   |-- manage.py                            # Start the app - Django default start script
   |
   |-- ************************************************************************
```

<br />

> The bootstrap flow

- Django bootstrapper `manage.py` uses `core/settings.py` as the main configuration file
- `core/settings.py` loads the app magic from `.env` file
- Redirect the guest users to Login page
- Unlock the pages served by *app* node for authenticated users

<br />

## Recompile CSS

To recompile SCSS files, follow this setup:

<br />

**Step #1** - Install tools

- [NodeJS](https://nodejs.org/en/) 12.x or higher
- [Gulp](https://gulpjs.com/) - globally 
    - `npm install -g gulp-cli`
- [Yarn](https://yarnpkg.com/) (optional) 

<br />

**Step #2** - Change the working directory to `assets` folder

```bash
$ cd apps/static/assets
```

<br />

**Step #3** - Install modules (this will create a classic `node_modules` directory)

```bash
$ npm install
// OR
$ yarn
```

<br />

**Step #4** - Edit & Recompile SCSS files 

```bash
$ gulp scss
```

The generated file is saved in `static/assets/css` directory.

<br /> 

## Deployment

The app is provided with a basic configuration to be executed in [Docker](https://www.docker.com/), [Gunicorn](https://gunicorn.org/), and [Waitress](https://docs.pylonsproject.org/projects/waitress/en/stable/).

### [Docker](https://www.docker.com/) execution
---

The application can be easily executed in a docker container. The steps:

> Get the code

```bash
$ git clone https://github.com/app-generator/boilerplate-code-django.git
$ cd boilerplate-code-django
```

> Start the app in Docker

```bash
$ sudo docker-compose pull && sudo docker-compose build && sudo docker-compose up -d
```

Visit `http://localhost:85` in your browser. The app should be up & running.

> Create Django `superuser` 

```bash
$ # Get Container ID
$ docker ps
$ 
$ # Call docker exec and CREATE the Superuser
$ docker exec -it <APPSEED_CONTAINER_ID> python manage.py createsuperuser
```

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

## Credits & Links

- [Django](https://www.djangoproject.com/) - The official website
- [Boilerplate Code](https://appseed.us/boilerplate-code) - Index provided by **AppSeed**
- [Boilerplate Code](https://github.com/app-generator/boilerplate-code) - Index published on Github

<br />

---
[Django Boilerplate](https://appseed.us/boilerplate-code/django-boilerplate) - Provided by **AppSeed** [App Generator](https://appseed.us/app-generator).
