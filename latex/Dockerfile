FROM debian:jessie
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
