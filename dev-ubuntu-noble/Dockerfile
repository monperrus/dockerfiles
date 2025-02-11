FROM ubuntu:noble
RUN apt update
#RUN apt upgrade
# low level
# for gpus and ollamas
RUN apt install -y lshw libleveldb-dev libffi-dev libssl-dev libc-bin file
RUN apt install -y sudo git vim tmux wget curl
RUN apt install -y python3 python3-pip python3-virtualenv
RUN apt install -y pkg-config software-properties-common
# user facing

# Configure ubuntu user with sudo access
RUN usermod -u 1001 ubuntu
RUN usermod -aG sudo ubuntu
RUN echo 'ubuntu ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers.d/ubuntu
RUN chmod 0440 /etc/sudoers.d/ubuntu
ENV LANG C.UTF-8
USER ubuntu
WORKDIR /home/ubuntu

