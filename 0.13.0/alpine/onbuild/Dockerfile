FROM nimlang/nim:0.13.0-alpine

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

ONBUILD COPY . /usr/src/app
ONBUILD RUN nimble build
