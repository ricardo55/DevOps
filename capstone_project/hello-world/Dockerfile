FROM node:16-alpine
COPY capstone_project/hello-world/ .
WORKDIR  /hello-world
RUN npm install
EXPOSE 3000
CMD ["npm", "start"]
