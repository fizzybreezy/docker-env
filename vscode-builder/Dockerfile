FROM node:12

RUN apt-get update -q && apt-get install -qy libx11-dev libxkbfile-dev libsecret-1-dev fakeroot rpm && \
    apt-get clean -y && \
    apt-get autoremove && \
    rm -rf /var/lib/apt/lists/* && \
    git clone --depth 1 https://github.com/microsoft/vscode

WORKDIR /vscode

RUN yarn install --ignore-scripts && \
    yarn compile
    
FROM node:12-slim

COPY --from=0 /vscode /
