# Docker node + ngnix + monogoDB

## Servislar /api/Dockerfile
``` 
FROM node:13

WORKDIR /usr/src/app

COPY package*.json ./

RUN  npm install

COPY . .
```

## docker-compose.yml
``` 
version: '3'
services: 
  api: 
    build: ./api
    command: npm run start
    ports:
      - "3000:3000"
```
