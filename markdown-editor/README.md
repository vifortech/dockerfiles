# Docker version of (GitHub-Flavored) Markdown Editor

This is jbt's [Markdown Editor](https://github.com/jbt/markdown-editor) packaged up in a nice,
small, Alpine Linux Docker container.


#### Why?

Well, you could visit the live editor [online](http://jbt.github.com/markdown-editor), but
where's the fun when you could be running it locally?

It is also really small ~12Mb.


#### Where do I get it?

The container is available on [Docker Hub](https://hub.docker.com/r/v4tech/markdown-editor/)
and can be pulled locally by:
```
docker pull v4tech/markdown-editor
```

The Dockerfile is [on GitHub](https://github.com/v4tech/dockerfiles).


#### How do I run this?

The container automatically listens on port 80, so you need to map that (or let Docker do it
for you).

To start the container:
```
docker run -p 12345:80 --rm -it v4tech/markdown-editor
```
Then simply point your browser at: `http://<dockerIP>:12345`
