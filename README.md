# [MaterialPro Lite](https://appseed.us/generator/material-wpx/) Flask

Open-Source **Flask Dashboard** coded with basic modules, database, ORM and deployment scripts on top of MaterialPro Bootstrap Lite, a modern Bootstrap dashboard design. [WrapPixel](https://appseed.us/agency/wrappixel)'s **MaterialPro Bootstrap Lite** is one of the best Bootstrap templates for admin dashboards and control admin panels. This powerful and competent Bootstrap 4 admin template is based on HTML and is built with the CSS framework. 

- 👉 [Flask MaterialPRO Lite](https://appseed.us/product/material-wpx/flask/) - product page
- 👉 [Flask MaterialPRO Lite](https://flask-materialpro-lite.appseed-srv1.com) - LIVE deployment
- 👉 [Complete documentation](https://docs.appseed.us/boilerplate-code/flask-dashboard) - `Learn how to use and update the product`
  - ✅ [Set up the environment](https://docs.appseed.us/boilerplate-code/flask-dashboard#environment)
  - ✅ [Manage App users](https://docs.appseed.us/boilerplate-code/flask-dashboard#manage-app-users)
  - ✅ [Application Bootstrap Flow](https://docs.appseed.us/boilerplate-code/flask-dashboard#application-bootstrap-flow)
  - ✅ [UI Assets and Templates](https://docs.appseed.us/boilerplate-code/flask-dashboard#ui-assets-and-templates)
  - ✅ [Set up the MySql Database](https://docs.appseed.us/boilerplate-code/flask-dashboard#set-up-the-mysql-database)
  - ✅ [Static Assets for production](https://docs.appseed.us/boilerplate-code/flask-dashboard#static-assets-for-production)  
  
<br />

> Built with [MaterialPro Lite Generator](https://appseed.us/generator/material-wpx/)

- Timestamp: `2022-06-15 14:22`
- Build ID: `5e80947b-23b2-4092-8215-ce3ecdcf4069`
- **Free [Support](https://appseed.us/support/)** (registered users) via `Email` and `Discord`

<br />

> Features

- `Up-to-date dependencies`
- Database: `sqlite`
- `DB Tools`: SQLAlchemy ORM, Flask-Migrate (schema migrations)
- Session-Based authentication (via **flask_login**), Forms validation

<br />

![MaterialPRO Lite - Starter generated by AppSeed.](https://user-images.githubusercontent.com/51070104/172007029-0e7c6df5-95d1-4b88-8831-5d35c5c37005.png)

<br />


## ✨ Start the app in Docker

> **Step 1** - Download the code from the GH repository (using `GIT`) 

```bash
$ # Get the code
$ git clone https://github.com/appseed-projects/<YOUR_BUILD_ID>.git
$ cd <YOUR_BUILD_ID>
```

<br />

> **Step 2** - Edit `.env` and set `DEBUG=True`. This will activate the `SQLite` persistance. 

```txt
DEBUG=True
```

<br />

> **Step 3** - Start the APP in `Docker`

```bash
$ docker-compose up --build 
```

Visit `http://localhost:5085` in your browser. The app should be up & running.

<br />




## ✨ How to use it

> Download the code 

```bash
$ # Get the code
$ git clone https://github.com/appseed-projects/5e80947b-23b2-4092-8215-ce3ecdcf4069.git
$ cd 5e80947b-23b2-4092-8215-ce3ecdcf4069
```

<br />

### 👉 Set Up for `Unix`, `MacOS` 

> Install modules via `VENV`  

```bash
$ virtualenv env
$ source env/bin/activate
$ pip3 install -r requirements.txt
```

<br />

> Set Up Flask Environment

```bash
$ export FLASK_APP=run.py
$ export FLASK_ENV=development
```

<br />

> Start the app

```bash
$ flask run
```

At this point, the app runs at `http://127.0.0.1:5000/`. 

<br />

### 👉 Set Up for `Windows` 

> Install modules via `VENV` (windows) 

```
$ virtualenv env
$ .\env\Scripts\activate
$ pip3 install -r requirements.txt
```

<br />

> Set Up Flask Environment

```bash
$ # CMD 
$ set FLASK_APP=run.py
$ set FLASK_ENV=development
$
$ # Powershell
$ $env:FLASK_APP = ".\run.py"
$ $env:FLASK_ENV = "development"
```

<br />

> Start the app

```bash
$ flask run
```

At this point, the app runs at `http://127.0.0.1:5000/`. 

<br />

### 👉 Create Users

By default, the app redirects guest users to authenticate. In order to access the private pages, follow this set up: 

- Start the app via `flask run`
- Access the `registration` page and create a new user:
  - `http://127.0.0.1:5000/register`
- Access the `sign in` page and authenticate
  - `http://127.0.0.1:5000/login`

<br />

## ✨ Code-base structure

The project is coded using blueprints, app factory pattern, dual configuration profile (development and production) and an intuitive structure presented bellow:

```bash
< PROJECT ROOT >
   |
   |-- apps/
   |    |
   |    |-- home/                           # A simple app that serve HTML files
   |    |    |-- routes.py                  # Define app routes
   |    |
   |    |-- authentication/                 # Handles auth routes (login and register)
   |    |    |-- routes.py                  # Define authentication routes  
   |    |    |-- models.py                  # Defines models  
   |    |    |-- forms.py                   # Define auth forms (login and register) 
   |    |
   |    |-- static/
   |    |    |-- <css, JS, images>          # CSS files, Javascripts files
   |    |
   |    |-- templates/                      # Templates used to render pages
   |    |    |-- includes/                  # HTML chunks and components
   |    |    |    |-- navigation.html       # Top menu component
   |    |    |    |-- sidebar.html          # Sidebar component
   |    |    |    |-- footer.html           # App Footer
   |    |    |    |-- scripts.html          # Scripts common to all pages
   |    |    |
   |    |    |-- layouts/                   # Master pages
   |    |    |    |-- base-fullscreen.html  # Used by Authentication pages
   |    |    |    |-- base.html             # Used by common pages
   |    |    |
   |    |    |-- accounts/                  # Authentication pages
   |    |    |    |-- login.html            # Login page
   |    |    |    |-- register.html         # Register page
   |    |    |
   |    |    |-- home/                      # UI Kit Pages
   |    |         |-- index.html            # Index page
   |    |         |-- 404-page.html         # 404 page
   |    |         |-- *.html                # All other pages
   |    |    
   |  config.py                             # Set up the app
   |    __init__.py                         # Initialize the app
   |
   |-- requirements.txt                     # App Dependencies
   |
   |-- .env                                 # Inject Configuration via Environment
   |-- run.py                               # Start the app - WSGI gateway
   |
   |-- ************************************************************************
```

<br />



## ✨ PRO Version

> For more components, pages and priority on support, feel free to take a look at this amazing starter:

MaterialPRO Dashboard is a premium Bootstrap Design now available for download in Django. Made of hundred of elements, designed blocks, and fully coded pages, Material Dashboard PRO is ready to help you create stunning websites and web apps.

- 👉 [WPX MaterialPro Flask](https://appseed.us/product/material-wpx-pro/flask/) - Product Page
- 👉 [WPX MaterialPro Flask](https://flask-material-wpx-pro.appseed-srv1.com/) - LIVE Demo

<br >

![MaterialPRO - Premium starter generated by AppSeed.](https://user-images.githubusercontent.com/51070104/172018257-c203a47a-3103-4a66-8324-f11c6aadef14.png)

<br />

---
[MaterialPro Lite](https://appseed.us/generator/material-wpx/) Flask - Open-source starter generated by **[AppSeed Generator](https://appseed.us/generator/)**.
