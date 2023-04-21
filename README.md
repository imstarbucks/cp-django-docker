# Capstone Django-Docker Project Setup Documentation

# Capstone Django-Docker Project Setup Documentation

This document outlines the steps required to set up the Capstone Django-Docker project. The project is composed of the following technologies:

- Django as the backend framework
- PostgreSQL as the database
- Nginx as the web server
- Gunicorn as the WSGI HTTP Server
- Vite-React as the front-end framework

## Prerequisites

Before proceeding with the setup, ensure that you have the following installed on your system:

- Docker Desktop
- Docker-compose

## Getting Started

1. Clone the Capstone Django-Docker project to your local machine.
    
    ```
    git clone https://github.com/imstarbucks/cp-django-docker.git {project_name}
    ```
    
2. Navigate to the root directory of the project.
3. Create a `.env` file in the root directory of the project if it does not exist.
4. Add the following environment variables to the `.env` file:

```
DJANGO_ALLOWED_HOSTS=localhost 127.0.0.1 [::1]
SQL_ENGINE=django.db.backends.postgresql
SQL_DATABASE={datebase name}
SQL_USER={datebase user}
SQL_PASSWORD={datebase password}
SQL_HOST=db
SQL_PORT=5432

```

1. Run the following command to start the project:

```bash
# For starter run:
docker-compose up --build -d

# For non-starter run:
docker-compose up -d

# Note:
#  - Use -d flag for detached mode
#  - It is recommended to use docker compose v2 in this project
#  - To ensure docker compose v2 is enabled, go to Docker Desktop > Setting >
#    check docker-compose v2 checkbox   
```

1. Once the project has started, open your browser and navigate to 
    1. `[http://localhost:3000](http://localhost:3000)` for front-end
    2. `[http://localhost:8000](http://localhost:8000)` for django panel
    3. `[http://localhost:5050](http://localhost:5050)` for pgadmin4 panel

## Reference:

1. [Dockerizing Django with Postgres, Gunicorn, and Nginx | TestDriven.io](https://testdriven.io/blog/dockerizing-django-with-postgres-gunicorn-and-nginx/)
2. [Dockerize your React, Django Rest Api Application and serve using nginx | by Parth Koshta | Medium](https://parthkoshta.medium.com/dockerize-your-react-django-rest-api-application-and-serve-using-nginx-6f9ccf17105b)
3. [Docker | Towards serving React (Nginx) with Django API (gunicorn) - YouTube](https://www.youtube.com/watch?v=e63EBEFJkH0)
4. Notion Link: [https://wild-park-b26.notion.site/Capstone-Django-Docker-Project-Setup-Documentation-aa471f3444f24eb5a2282ff4c3b849ea](https://www.notion.so/Capstone-Django-Docker-Project-Setup-Documentation-aa471f3444f24eb5a2282ff4c3b849ea)