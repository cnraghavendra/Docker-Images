# Full Developer Ubuntu (CLI-based, powerful & fast)


FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

# Update and install packages
RUN apt update && apt install -y \
    sudo curl wget git vim nano unzip zip \
    build-essential software-properties-common \
    net-tools iputils-ping dnsutils \
    python3 python3-pip \
    nodejs npm \
    openjdk-17-jdk \
    docker.io \
    && apt clean

# Create a non-root user
RUN useradd -m devuser && echo "devuser:dev123" | chpasswd && adduser devuser sudo

USER devuser
WORKDIR /home/devuser

CMD ["/bin/bash"]
