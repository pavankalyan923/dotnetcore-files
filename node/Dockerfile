# Base image
FROM node:18.14.1-alpine3.16

# Create app directory
WORKDIR /usr/src/app

COPY package.json ./

RUN npm install --force

# Bundle app source
COPY . .

# Creates a "dist" folder with the production build
RUN npm run build

CMD [ "node", "dist/main.js" ]