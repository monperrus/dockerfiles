FROM ubuntu:noble
RUN apt update
#RUN apt upgrade
RUN apt install -y git 
RUN apt install -y python3 python3-pip

RUN apt install -y python3-virtualenv
RUN apt install -y libleveldb-dev libffi-dev libssl-dev

RUN apt install -y  pkg-config
RUN apt install -y  vim
RUN apt install -y software-properties-common
RUN apt install -y wget curl

#RUN useradd -u1001 -r martin
RUN usermod -u 1001 ubuntu
USER ubuntu
WORKDIR /home/ubuntu
