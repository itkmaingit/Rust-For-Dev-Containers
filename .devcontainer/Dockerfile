FROM node:18
RUN apt update && \
    apt install -y git build-essential cmake clang libssl-dev less man-db sudo

ARG USERNAME=node
RUN echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME && \
    chmod 0440 /etc/sudoers.d/$USERNAME

USER $USERNAME
WORKDIR /home/node/works
COPY . /home/node/works