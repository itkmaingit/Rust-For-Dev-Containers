FROM node:18
RUN apt update && \
    apt install -y git build-essential cmake clang libssl-dev less man-db sudo
ENV SHELL bash
ARG USERNAME=node
RUN useradd -m $USERNAME && \
    echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME && \
    chmod 0440 /etc/sudoers.d/$USERNAME

USER $USERNAME
WORKDIR /home/node/works
COPY . /home/node/works
