FROM ubuntu:focal

ENV DEBIAN_FRONTEND=noninteractive
ENV CPP_LD_FLAGS='-I/usr/include -I/usr/include/jsoncpp -lcurl -ljsoncpp'

RUN apt-get update \
    && apt-get install -y \
        g++=4:9.3.0-1ubuntu2 libcurl4=7.68.0-1ubuntu2.15 libcurl4-gnutls-dev=7.68.0-1ubuntu2.15 \
        libjsoncpp-dev=1.7.4-3.1ubuntu2 \
    && rm -rf /var/lib/apt/lists/*

RUN useradd -M -d /sandbox sandbox \
    && mkdir /sandbox \
    && chown sandbox:sandbox /sandbox
