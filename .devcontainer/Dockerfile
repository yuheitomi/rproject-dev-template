FROM rocker/rstudio:latest


RUN \
    --mount=type=cache,target=/var/lib/apt/lists \
    --mount=type=cache,target=/var/cache/apt/archives \ 
    apt-get update && apt-get install -y \
    openssh-client \
    libgit2-dev \
    fonts-ipaexfont \
    fonts-noto-cjk

# Install dependencies for tidyverse
RUN apt-get install -y \
    libfreetype6-dev \
    libfontconfig1-dev \
    libfribidi-dev \
    libharfbuzz-dev \
    libicu-dev \
    libtiff-dev \
    libxml2-dev \
    pandoc

RUN R -e "install.packages('renv')"
