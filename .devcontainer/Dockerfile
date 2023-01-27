FROM mcr.microsoft.com/devcontainers/typescript-node:0-18

RUN apt-get update && apt-get install -y xz-utils
# Install basic development tools
RUN apt update && apt install -y less man-db sudo

# Ensure default `node` user has access to `sudo`
ARG USERNAME=node
RUN echo $USERNAME ALL=\(root\) NOPASSWD:ALL > /etc/sudoers.d/$USERNAME \
    && chmod 0440 /etc/sudoers.d/$USERNAME

# Set `DEVCONTAINER` environment variable to help with orientation
ENV DEVCONTAINER=true

RUN npm i -g @types/node
RUN npm i -g vite
RUN npm i -g bootstrap


