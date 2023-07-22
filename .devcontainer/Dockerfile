FROM mcr.microsoft.com/devcontainers/typescript-node:14-bullseye

RUN apt-get update && apt-get -y upgrade \
    && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install bash-completion \
    && npm install -g npm@9.8.1 \
    && rm /etc/localtime \
    && ln -s /usr/share/zoneinfo/Asia/Tokyo /etc/localtime \
    && mkdir -p /home/node/workspace /home/node/.vscode-server/extensions \
    && chown -R node:node /home/node/workspace /home/node/.vscode-server
