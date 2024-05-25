## Vendor Management Project

Develop a Vendor Management System using Django and Django REST Framework. This system will handle vendor profiles, track purchase orders, and calculate vendor performance metrics.

### Steps to install and run vendor app on your local machine
* Run `$ pip install virtualenv` command to install virtual environment
* Run `$ pip install venv env` command to Create Virtual environment
* Run `$ source env/bin/activate` command to activate virtual environment # For Linux/Mac4
* Run `$ venv\Scripts\activate` command to activate virtual environment # For Windows
* Run `$ git clone https://github.com/garg-shefali/task-vendor` command for cloning the project
* Run `$ cd vendorProject` command for jump into the project directory
* Run `$ pip install -r requirements.txt` command to Install project requirement file
* Set variable in .env.dev according to .env.template
* Set database name and password on your project Setting file
    * Go to setting.py file and update database connection in your setting file
        `DATABASES = {`
            `'default': {`
               ` 'ENGINE': 'django.db.backends.sqlite3',`
                `'NAME': BASE_DIR / "db.sqlite3",`
            `}`
        `}`
* Run `$ python manage.py migrate` command to apply migrations on your local machine
* Run `$ python manage.py runserver` command to run project on your local machine

## Set up a new project with a single application

* django-admin startproject vendorProject
* cd Vendor
* django-admin startapp vendor_app

## Superuser creation and Token generation

* python manage.py createsuperuser
* "username=your_superuser_username&password=your_superuser_password" http://localhost:8000/api-token-auth/
* '/api-token-auth/' #provide username and password in json eg. { "username":"superuser","password":"superuser" }
I used Postman to test API
once Token is created or received provide it to HEADER
with key as Authorization (eg. key : Authorization) and value as token

## Run the server

* python manage.py runserver

## Access Django Admin:

* Open the Django admin at http://127.0.0.1:8000/admin/ and log in using the superuser credentials. this is to access the database as a admin user.

## How to run a api endpoint:

* first we need to make sure that we migrated the models to database then we need to start the server using "python manage.py runserver" command.








