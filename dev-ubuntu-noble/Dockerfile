FROM ubuntu:noble
RUN apt update
#RUN apt upgrade
RUN apt install -y git
RUN apt install -y python3 python3-pip
RUN apt install -y python3-virtualenv
RUN apt install -y libleveldb-dev libffi-dev libssl-dev
RUN apt install -y pkg-config
RUN apt install -y vim
RUN apt install -y software-properties-common
RUN apt install -y wget curl
RUN apt install -y sudo

# Configure ubuntu user with sudo access
RUN usermod -u 1001 ubuntu
RUN usermod -aG sudo ubuntu
RUN echo 'ubuntu ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers.d/ubuntu
RUN chmod 0440 /etc/sudoers.d/ubuntu

USER ubuntu
WORKDIR /home/ubuntu

