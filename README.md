# [Jinja Template](https://appseed.us/jinja-template) - Gradient Dark PRO

 **Jinja Template** starter generated by the AppSeed platform on top of **[Gradient Dark PRO](https://docs.appseed.us/bootstrap-template/datta-able-pro/)** Design. The codebase is basically a simple Flask starter without a database or hard dependencies. The template can be used for UI integration into legacy Python-based products.

<br />

> Jinja Template Features

- UI Kit: **Gradient Dark PRO** by **CodedThemes**
- Render Engine: Flask / [Jinja2](https://jinja.palletsprojects.com/)
- Support via **Github** and [Discord](https://discord.gg/fZC6hup).

<br />

> Links

- [Jinja Gradient Dark PRO - Demo](https://jinja-gradient-dark-pro.appseed-srv1.com/) - LIVE Demo
- More [Jinja Templates](https://appseed.us/jinja-template) - provided by AppSeed

<br />

## Gradient Dark PRO

Gradient Able is a beautiful admin dashboard template built over the Bootstrap 4 framework. Gradient Able is well coded and well designed complete admin panel. It is elegant in visual design looks which combine soft gradient colors with well-suited typography and great cards and graphics. Which makes It a powerful tool and is very much light and flexible in use. 

With Gradient Able dashboard template we have provided all possible prebuilt admin template layouts. Which gives you the best selection choice of your backend panel need for your projects. Comes with error/bug-free, well structured, well-commented code and regularly with all latest updated code. Which saves your large amount of developing backend application time and it is fully customizable. It has enough functionality to allow you to get any project job done.

- [Gradient Dark PRO - UI Docs](https://codedthemes.com/demos/admin-templates/gradient-able/bootstrap/doc/) - Product Documentation

<br />

![Jinja Template - Gradient, Jinja seed project coded by AppSeed.](https://raw.githubusercontent.com/app-generator/jinja-gradient-dark-pro/main/media/jinja-gradient-dark-pro-screen.png)

<br />

## Build from sources

```bash
$ # Clone the sources
$ git clone https://github.com/app-generator/priv-jinja-gradient-dark-pro.git
$ cd priv-jinja-gradient-dark-pro
$
$ # Virtualenv modules installation (Unix based systems)
$ virtualenv env
$ source env/bin/activate
$
$ # Virtualenv modules installation (Windows based systems)
$ # virtualenv env
$ # .\env\Scripts\activate
$
$ # Install requirements
$ pip3 install -r requirements.txt
$
$ # Set the FLASK_APP environment variable
$ (Unix/Mac) export FLASK_APP=run.py
$ (Windows) set FLASK_APP=run.py
$ (Powershell) $env:FLASK_APP = ".\run.py"
$
$ # Set up the DEBUG environment
$ # (Unix/Mac) export FLASK_ENV=development
$ # (Windows) set FLASK_ENV=development
$ # (Powershell) $env:FLASK_ENV = "development"
$
$ # Run the Jinja Template
$ # --host=0.0.0.0 - expose the app on all network interfaces (default 127.0.0.1)
$ # --port=5000    - specify the app port (default 5000)  
$ flask run --host=0.0.0.0 --port=5000
$
$ # Access the UI in browser: http://127.0.0.1:5000/
```

<br />

## Code-base structure

The project has a simple structure, represented as bellow:

```bash
< PROJECT ROOT >
   |
   |-- app/__init__.py
   |-- app/
   |    |-- static/
   |    |    |-- <css, JS, images>         # CSS files, Javascripts files
   |    |
   |    |-- templates/
   |    |    |
   |    |    |-- includes/                 # Page chunks, components
   |    |    |    |
   |    |    |    |-- navigation.html      # Top bar
   |    |    |    |-- sidebar.html         # Left sidebar
   |    |    |    |-- scripts.html         # JS scripts common to all pages
   |    |    |    |-- footer.html          # The common footer
   |    |    |
   |    |    |-- layouts/                  # App Layouts (the master pages)
   |    |    |    |
   |    |    |    |-- base.html            # Used by common pages like index, UI
   |    |    |    |-- base-fullscreen.html # Used by auth pages (login, register)
   |    |    |
   |    |  index.html                      # The default page
   |    |  login.html                      # Auth Login Page
   |    |  register.html                   # Auth Registration Page
   |    |  page-404.html                   # Error 404 page (page not found)
   |    |  page-500.html                   # Error 500 page (server error)
   |    |    *.html                        # All other pages provided by the UI Kit
   |
   |-- requirements.txt
   |
   |-- run.py
   |
   |-- ************************************************************************
```

<br />

## Deployment

The project comes with a basic configuration for [Docker](https://www.docker.com/), [HEROKU](https://www.heroku.com/), [Gunicorn](https://gunicorn.org/), and [Waitress](https://docs.pylonsproject.org/projects/waitress/en/stable/).

<br />

### [Docker](https://www.docker.com/) execution
---

The steps to start the template using Docker:

> Get the code

```bash
$ git clone https://github.com/app-generator/priv-jinja-gradient-dark-pro.git
$ cd priv-jinja-gradient-dark-pro
```

> Start the app in Docker

```bash
$ sudo docker-compose pull && sudo docker-compose build && sudo docker-compose up -d
```

Visit `http://localhost:5005` in your browser. The app should be up & running.

<br />

### [Heroku](https://www.heroku.com/)
---

Steps to deploy on **Heroku**

- [Create a FREE account](https://signup.heroku.com/) on Heroku platform
- [Install the Heroku CLI](https://devcenter.heroku.com/articles/getting-started-with-python#set-up) that match your OS: Mac, Unix or Windows
- Open a terminal window and authenticate via `heroku login` command
- Clone the sources and push the project for LIVE deployment

```bash
$ # Clone the source code:
$ git clone https://github.com/app-generator/priv-jinja-gradient-dark-pro.git
$ cd priv-jinja-gradient-dark-pro
$
$ # Check Heroku CLI is installed
$ heroku -v
heroku/7.25.0 win32-x64 node-v12.13.0 # <-- All good
$
$ # Check Heroku CLI is installed
$ heroku login
$ # this commaond will open a browser window - click the login button (in browser)
$
$ # Create the Heroku project
$ heroku create
$
$ # Trigger the LIVE deploy
$ git push heroku master
$
$ # Open the LIVE app in browser
$ heroku open
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
$ gunicorn --bind 0.0.0.0:8001 run:app
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
$ waitress-serve --port=8001 run:app
Serving on http://localhost:8001
```

Visit `http://localhost:8001` in your browser. The app should be up & running.

<br />

## Credits & Links

- [Flask Framework](https://www.palletsprojects.com/p/flask/) - The official website

<br />

---
[Jinja Template](https://appseed.us/jinja-template) **Gradient Dark PRO** - Provided by **AppSeed** [Web App Generator](https://appseed.us/app-generator).
