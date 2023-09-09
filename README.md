# Tech Stack

**Backend:** FastAPI

**Frontend:** Jinja2, Pure JS

**Server:** Gunicorn

**Services:** Docker, MySQL


# Run Locally with docker-compose


```bash
  git clone -b master https://github.com/vladgenyuk/1AK_M2M
```
```bash
  cd Test1AK
```
```bash
  docker-compose up -d
```

# Run Locally without docker-compose


```bash
  git clone -b master https://github.com/vladgenyuk/1AK_M2M
```
```
  alembic upgrade head
```
```bash
  docker run --name 1AK_mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=secret -e MYSQL_USER=vlad -e MYSQL_PASSWORD=qseawdzxc1 -e MYSQL_DATABASE=library -e MYSQL_CHARACTER_SET_SERVER=utf8mb4 -e MYSQL_COLLATION_SERVER=utf8mb4_general_ci -d mysql:latest
```

```
  update DB_HOST in .env file as localhost
```

```bash
  uvicorn backend.main:app --reload
```

## Registration and Authorization

For register and authorization User needs only to Enter his name and email, email for each user is unique.
## Frontend

I used build-in in FastAPI Jinja2 template generator and pure JS to display information on web pages and add active behaviour on pages. Endpoints with pages run on the same host and port as the main application.

To imitate the suspended Frontend application, the endpoints and HTML templates makes additional requests to backend.

## Folder structure 

I tried to make a clear and expandable folder structure with methods with headen realization that easy to use and expand, Exception invokers and others to simplify the programming process.
