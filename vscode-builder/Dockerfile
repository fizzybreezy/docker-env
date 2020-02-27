FROM node:12

RUN apt-get update -q && apt-get install -qy libx11-dev libxkbfile-dev libsecret-1-dev fakeroot rpm && \
    apt-get clean -y && \
    apt-get autoremove && \
    rm -rf /var/lib/apt/lists/* && \
    git clone https://github.com/microsoft/vscode

WORKDIR /vscode

RUN yarn
