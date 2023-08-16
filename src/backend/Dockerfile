FROM node:lts-buster-slim AS development

# Create app directory
WORKDIR /usr/src/app

# Copy dependency definitions
COPY package.json /usr/src/app/package.json
COPY package-lock.json /usr/src/app/package-lock.json

# Install dependecies
RUN npm ci

COPY . /usr/src/app

EXPOSE 3000

CMD [ "npm", "run", "dev" ]
