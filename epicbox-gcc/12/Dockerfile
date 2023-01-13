FROM ubuntu:lunar

ENV DEBIAN_FRONTEND=noninteractive
ENV CPP_LD_FLAGS='-lcurl -ljsoncpp'

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        g++-12=12.2.0-9ubuntu1 libcurl4=7.86.0-2 libcurl4-gnutls-dev=7.86.0-2 \
        libjsoncpp-dev=1.9.5-4 libjsoncpp25=1.9.5-4 \
    && rm -rf /var/lib/apt/lists/*

RUN useradd -M -d /sandbox sandbox \
    && mkdir /sandbox \
    && chown sandbox:sandbox /sandbox
