FROM debian:bullseye

RUN dpkg --add-architecture arm64 && \
    apt-get update && \
    apt-get full-upgrade --no-install-recommends -y \
        build-essential crossbuild-essential-arm64 git \
        cmake debhelper devscripts lintian libx11-dev:arm64 && \
    adduser --gecos runner --disabled-password runner && \
    rm -rf /var/lib/apt/lists/*
