FROM ubuntu:jammy
RUN apt update
#RUN apt upgrade
# low level
# for gpus and ollamas
RUN apt install -y lshw libleveldb-dev libffi-dev libssl-dev pkg-config software-properties-common libc-bin file
RUN apt install -y sudo git vim tmux wget curl

# minimum python
RUN apt install -y python3 python3-pip python3-virtualenv

RUN apt install -y maven

# bazel
RUN apt install apt-transport-https curl gnupg -y
RUN curl -fsSL https://bazel.build/bazel-release.pub.gpg | gpg --dearmor >bazel-archive-keyring.gpg
RUN mv bazel-archive-keyring.gpg /usr/share/keyrings
RUN echo "deb [arch=amd64 signed-by=/usr/share/keyrings/bazel-archive-keyring.gpg] https://storage.googleapis.com/bazel-apt stable jdk1.8" | sudo tee /etc/apt/sources.list.d/bazel.list
RUN apt update && apt install -y bazel

# Configure ubuntu user with sudo access
RUN useradd -u 1001 ubuntu
#RUN usermod -u 1001 ubuntu
RUN usermod -aG sudo ubuntu
RUN echo 'ubuntu ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers.d/ubuntu
RUN chmod 0440 /etc/sudoers.d/ubuntu
ENV LANG C.UTF-8
USER ubuntu
WORKDIR /home/ubuntu
CMD bash -i

