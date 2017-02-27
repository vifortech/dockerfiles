FROM alpine:latest
MAINTAINER Stewart V. Wright <stewart@vifortech.com>

RUN apk --update add exiftool \
    && rm -rf /var/cache/apk/*

RUN mkdir /root/pub
WORKDIR /root/pub
