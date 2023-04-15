# syntax=docker/dockerfile:1

FROM node:16-alpine
WORKDIR /hello-world
COPY package*.json ./
RUN npm install
EXPOSE 3000
CMD ["npm", "start"]
