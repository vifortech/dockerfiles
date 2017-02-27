FROM alpine:latest
MAINTAINER Stewart V. Wright <v4tech@users.noreply.github.com>


ENV PDFTK_VERSION=2.02-r1 

# Alpine Install URL
ENV AI_URL=http://dl-cdn.alpinelinux.org/alpine
RUN echo -e "\n@edge ${AI_URL}/edge/main\n@testing ${AI_URL}/edge/testing\n@community ${AI_URL}/edge/community" >> /etc/apk/repositories

RUN apk update && \
    apk add libgcj@edge && \
    apk add pdftk@community && \
    rm -rf /var/cache/apk/*


# The directory containing the PDF files to be processed is expected to be mounted here
# as a docker volume when running the container.
# (from https://github.com/mnuessler/docker-pdftk)
RUN mkdir /work
WORKDIR /work
VOLUME ["/work"]


ENTRYPOINT ["/usr/local/bin/pdftk"]
