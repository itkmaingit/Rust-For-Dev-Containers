# Overview

This is a Dev Container (in VSCode features.) template repository for Rust. You have to execute commands below.

## Requirements

OS: Windows 10/11
Docker
VSCode

- Extensions -> Dev Containers, Docker

You can build dev container and start to develop Rust project after you press F1 and choice "Dev Container: Reopen in container".

In Dockerfile, we set alias (ex. cargo -> c). So, if you don't want to set that, you delete line in Dockerfile that writes `RUN echo "alias c='cargo'" >> /home/node/.bashrc`.

## Caution

This repository has .gitignore, but **doesn't** add `.env`. If you want to use .env, you must add .env(.env.local, etc...) to .gitignore.
