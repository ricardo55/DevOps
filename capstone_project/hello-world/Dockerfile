FROM node:16-alpine
COPY . .
WORKDIR  /hello-world
RUN npm install
# Install Ansible
RUN apt-get update && \
    apt-get install -y ansible
EXPOSE 3000
CMD ["npm", "start"]
