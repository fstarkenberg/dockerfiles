FROM alpine
MAINTAINER fresta
ARG VERSION=1.9.6

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
    && pip install pycrypto svtplay-dl==$VERSION

WORKDIR /data

ENTRYPOINT ["python", "/usr/bin/svtplay-dl"]
CMD ["--help"]
