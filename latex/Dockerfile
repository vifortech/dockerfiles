FROM debian:latest
MAINTAINER Stewart V. Wright <stewart@vifortech.com>

# all TeX runtime requirements
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        texlive \
        texinfo \
        texlive-latex-extra \
        texlive-pictures\
        latex-beamer && \
    rm -rf /var/lib/apt/lists/*

# If you don't understand why I'm using this path...
# Read:  http://tex.stackexchange.com/a/31415
COPY additional-style-files /root/texmf/tex/latex

RUN mkdir /root/pub
WORKDIR /root/pub
