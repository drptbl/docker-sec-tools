FROM cimg/node:14.13
# FROM cimg/node:12.18

# USER root

RUN apk add --no-cache --virtual .tools git curl

RUN npm install -g audit-ci@3.1.1 lockfile-lint@4.3.7

RUN curl -LO "https://storage.googleapis.com/container-diff/v0.15.0/container-diff-linux-amd64" && chmod +x container-diff-linux-amd64 && mv container-diff-linux-amd64 /usr/local/bin/container-diff

RUN apk del .tools

# USER node

# ENV HOME /home/node

# WORKDIR ${HOME}/app

CMD ["bash"]
