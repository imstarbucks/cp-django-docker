FROM python:3.9
ENV PYTHONUNBUFFERED=1
ENV PYTHONDONTWRITEBYTECODE=1
WORKDIR /backend

RUN pip install pipenv
RUN pip install psycopg2
COPY Pipfile* /backend/
RUN pipenv requirements > requirements.txt
RUN pip install -r requirements.txt
COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh

COPY . /backend/
