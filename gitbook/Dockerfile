FROM node:6-alpine

MAINTAINER yzhao <zhaoyijun1987@hotmail.com>

ARG VERSION=3.2.3

LABEL version=$VERSION

RUN npm install --global gitbook-cli &&\
	gitbook fetch ${VERSION} &&\
	npm install http-server -g &&\
	npm cache clear &&\
	rm -rf /tmp/*

WORKDIR /srv/gitbook

VOLUME /srv/gitbook /srv/html
