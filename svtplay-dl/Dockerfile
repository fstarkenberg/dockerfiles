FROM alpine
MAINTAINER fresta
ARG VERSION=1.9.11

run set -xe \
    && apk add --no-cache \
        ca-certificates \
        openssl \
        libc-dev \
        python-dev \
        gcc \
        py-pip \
        ffmpeg \
        rtmpdump \
        py-requests \
    && pip install pycrypto svtplay-dl==$VERSION

WORKDIR /data

ENTRYPOINT ["python", "/usr/bin/svtplay-dl"]
CMD ["--help"]
