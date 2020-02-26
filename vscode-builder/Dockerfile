FROM node:12

RUN apt install libx11-dev libxkbfile-dev libsecret-1-dev && \
    git clone https://github.com/microsoft/vscode

WORKDIR /vscode

RUN yarn
