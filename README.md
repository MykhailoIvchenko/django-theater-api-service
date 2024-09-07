# Theater API
This project is a Django REST API for managing a theater's operations, including plays, 
performances, reservations, and tickets. 
The project is containerized using Docker and includes automatic API documentation 
with Swagger and Redoc.

## Installing using GitHub

Install PostgreSQL and create db

- git clone https://github.com/MykhailoIvchenko/django-theater-api-service.git
- cd django-theater-api-service
- python -m venv venv
- source venv/bin/activate
- pip install -r requirements.txt
- set POSTGRES_HOST=<your db hostname>
- set POSTGRES_DB=<your db name>
- set POSTGRES_USER=<your db username>
- set POSTGRES_PASSWORD=<your db user password>
- set PGDATA=<your link to the pg data>
- set SECRET_KEY=<your secret key>
- `python manage.py migrate`
- `python manage.py runserver`

## Run with Docker (recommended way)

Install [Docker Desktop](https://docs.docker.com/desktop/) and launch it

- `docker-compose build`
- `docker-compose up`

## Getting access

- create user via /api/user/register
- get access token via /api/user/token

## Getting access as admin
- enter container docker exec -it <container_name> sh, 
- create superuser by the command `python manage.py createsuperuser`

## Features
- JWT authenticated
- Admin panel /admin/
- Documentation is located at api/doc/swagger of at api/doc/redoc
- Creating plays with genres and actors
- Creating theater halls
- Adding performances
- Filtering plays and performances
- Managing reservations and tickets
