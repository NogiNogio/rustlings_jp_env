FROM mcr.microsoft.com/devcontainers/base:ubuntu-24.04

RUN apt update -y
RUN apt install -y curl ca-certificates git build-essential pkg-config libssl-dev

SHELL ["/bin/bash", "-lc"]

USER vscode
WORKDIR /home/vscode

RUN curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y
RUN echo 'source "$HOME/.cargo/env"' >> ~/.bashrc

RUN source "$HOME/.cargo/env"
RUN cargo install rustlings
