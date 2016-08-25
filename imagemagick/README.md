# Docker install of imagemagick in Alpine Linux

This is [imagemagick](https://en.wikipedia.org/wiki/ImageMagick) packaged up in a nice,
small, Alpine Linux Docker container.


#### Where do I get it?

The container is available on [Docker Hub](https://hub.docker.com/r/v4tech/imagemagick/)
and can be pulled locally by:
```
docker pull v4tech/imagemagick
```

The Dockerfile is [on GitHub](https://github.com/v4tech/dockerfiles).


#### How do I run this?

To start the container:
```
docker run -v /path/to/images:/images --rm -it v4tech/imagemagick /bin/sh
```

...or get fancy and try:
```
docker run -v /path/to/images:/images --rm -it v4tech/imagemagick \
    convert /images/input.png /images/output.jpg
```
