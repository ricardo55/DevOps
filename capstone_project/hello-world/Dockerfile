FROM node:16.13.1

# RUN apt-get update -y && apt-get install -y gnupg2
# RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 871920D1991BC93C
# RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 871920D1991BC93C

RUN apt-get update  -y \
    && apt-get upgrade -y \ 
    && apt-get install -y \
    ssh \
    sshpass \
    sudo \
    software-properties-common \
    nodejs \
    npm

# RUN add-apt-repository --yes --update ppa:ansible/ansible \
#    && apt-get install -y ansible

COPY . .
WORKDIR  /hello-world
RUN npm install

RUN useradd -rm -d /home/ansible_controller -s /bin/bash -g root -G sudo -u 1001 ansible_controller
RUN echo ansible_controller:12345 | chpasswd
RUN echo "ansible_controller ALL=(ALL:ALL) NOPASSWD: ALL" |  EDITOR="tee -a"  visudo


RUN mkdir -p /home/ansible_controller/.ssh

EXPOSE 3000

# CMD ["npm", "start"]
CMD service ssh start && npm start

