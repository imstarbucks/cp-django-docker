FROM node:16.19.0-alpine

WORKDIR /app/

COPY package.json /app/

COPY package-lock.json /app/

RUN npm i

COPY . /app/
