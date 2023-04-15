# syntax=docker/dockerfile:1

FROM node:16-alpine
WORKDIR /hello-world
COPY . .
RUN npm install
EXPOSE 3000
CMD ["npm", "start"]
