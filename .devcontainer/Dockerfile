FROM mcr.microsoft.com/devcontainers/base:bullseye

ARG DEBIAN_FRONTEND=noninteractive

# Install nodejs and npm
RUN apt update && \
    apt install -y \
    nodejs \
    npm

# Install go-task
RUN npm install -g @go-task/cli
