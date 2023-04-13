# :memo: Notes
## DJANGO
---
### Resources
- [Django](https://www.djangoproject.com/)
- [Django documentation](https://docs.djangoproject.com/)
- [Topics](https://docs.djangoproject.com/en/4.2/topics/)
- [API Reference](https://docs.djangoproject.com/en/4.2/ref/)
- [“How-to” guides](https://docs.djangoproject.com/en/4.2/howto/)
- [django-admin and manage.py](https://docs.djangoproject.com/en/4.2/ref/django-admin/)
### Requirements
- [Python](https://www.python.org/)
### Terms and concepts
1. What and why
2. What do
3. Why use
4. Getting started
5. Concepts
6. Code samples
7. API documentation
- Python web framework
- Installation
- django-admin and manage.py
- Project
- Development server
- Application
- Views
- Urls
- Database
- Models
- Super user
- Administrative interface
- Public interface
- Templates
- Forms
- Tests
- Styles
- Debug Toolbar
### Setup
Verifying  
To verify that Django can be seen by Python, type python from your shell. Then at the Python prompt, try to import Django:
```
>>> import django
>>> print(django.get_version())
4.2
```
Or you can tell Django is installed and which version by running the following command in a shell prompt:
```
python -m django --version
```
#### Create a Django project in virtual environment
Create virtual environment
```
$ python -m venv <virtual_environment_name>
```
Activate virtual environment
```
$ source <virtual_environment_name>/bin/activate
```
requirements.txt file
```
Django==4.2
```
Create project
```
$ django-admin startproject <project_name> .
```
Apply the migrations
```
$ python manage.py migrate
```
Create super user
```
$ python manage.py createsuperuser
```
Run server
```
$ python manage.py runserver
```
##### Create a Django application
Create application
```
$ python manage.py startapp <application_name>
```
Add application in settings.py file
#### Create a Django project in Docker
docker-compose.yml file
```
services:
  web:
    build: .
    command: python manage.py runserver 0.0.0.0:8000
    volumes:
      - .:/src
    ports:
      - '8000:8000'
```
Dockerfile file
```
FROM python:3.11
ENV PYTHONUNBUFFERED 1
RUN mkdir /src
WORKDIR /src
COPY requirements.txt /src/
RUN python -m pip install -r requirements.txt
COPY . /src/
```
requirements.txt file
```
Django==4.1
```
Create project
```
$ docker-compose run web django-admin startproject <project_name> .
```
Apply the migrations
```
$ docker-compose run web python manage.py migrate
```
Create super user
```
$ docker-compose run web python manage.py createsuperuser
```
Run
```
$ docker-compose up
```
Done!
- http://127.0.0.1:8000/
- http://127.0.0.1:8000/admin/
---
## Software Developer
Built by [Javi](https://javierandres.dev) :copyright: 2023
Found a bug or have an idea? [Contact me](https://javierandres.dev).
