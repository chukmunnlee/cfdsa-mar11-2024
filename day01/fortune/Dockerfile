FROM node:21

# create the /app directory, cd into /app
WORKDIR /app

# How to build the application
# inside /app
# copy files from local into the container
COPY main.js .
COPY package-lock.json .
COPY package.json .

COPY public public
COPY views views

# Install dependencies
RUN npm ci

# How to run the application

# Environment variables
ENV APP_PORT=3000

# Tell the container what port the application need
EXPOSE ${APP_PORT}

ENTRYPOINT node main.js

