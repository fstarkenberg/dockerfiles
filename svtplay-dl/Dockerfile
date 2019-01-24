FROM alpine
MAINTAINER fresta
ARG VERSION=2.1

run set -xe \
    && apk add --no-cache \
        ca-certificates \
        openssl \
        libc-dev \
        python3-dev \
        gcc \
        py3-pip \
        ffmpeg \
        rtmpdump \
        py-requests \
    && pip3 install pycrypto svtplay-dl==$VERSION

WORKDIR /data

ENTRYPOINT ["python", "/usr/bin/svtplay-dl"]
CMD ["--help"]
