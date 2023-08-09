FROM rust:1.71.1-bullseye
RUN apt update && \
    apt -y install git sudo&& \
    apt clean && \
    rm -rf /var/lib/apt/lists/* && \
    rustup component add rls rust-analysis rust-src rustfmt clippy && \
    cargo install cargo-edit cargo-watch

ENV SHELL bash
ARG USERNAME=node
RUN useradd -m $USERNAME && \
    echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME && \
    chmod 0440 /etc/sudoers.d/$USERNAME
RUN echo "alias c='cargo'" >> /home/node/.bashrc
RUN echo "alias cr='cargo run --release'" >> /home/node/.bashrc
RUN echo "alias crd='cargo run'" >> /home/node/.bashrc
RUN echo "alias cc='cargo check'" >> /home/node/.bashrc
RUN echo "alias cy='cargo clippy'" >> /home/node/.bashrc
USER $USERNAME
WORKDIR /home/node/works
COPY . /home/node/works
