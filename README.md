# Cinema API Service
<hr>
API service for cinema management written on DRF.

## Features
<hr>

- JWT authenticated;
- Admin panel/admin/;
- Documentation is located at /api/doc/swagger/ or /api/doc/redoc/;
- Managing orders and tickets;
- Creating movies with genres, actors;
- Creating cinema halls;
- Adding movie sessions;
- Filtering movies and movie sessions.

## Installing using GitHub
<hr>
Install PostgresSQL and create DB.

Run the commands below:

```shell
git clone https://github.com/Vasyl-Poremchuk/cinema-api
cd cinema-api
python -m venv venv
venv\Scripts\activate (Windows) or source venv/bin/activate (Linux or macOS)
pip install -r requirements.txt
```

Create an .env file in which write the commands below:

```shell
set DB_HOST=<your DB host>
set DB_NAME=<your DB name>
set DB_USER=<your DB username>
set DB_PASSWORD=<your DB user password>
set DJANGO_SECRET_KEY=<your secret key>
```

Run migrations and run server:

```shell
python manage.py migrate
python manage.py runserver
```

## Getting access
<hr>

- Create user via/api/user/register/
- Get access token via/api/user/token/

## Also, you can run project using docker container
<hr>

Docker should be installed on your machine.

```shell
docker-compose build
docker-compose up
```

## Follow the instructions below to access the docker container
<hr>

- Go to `127.0.0.1:8000/api/` and check project endpoints via DRF interface;
- Create new admin user. Enter container `docker exec -it <container_name> bash`, and create in from there.