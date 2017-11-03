FROM alpine
MAINTAINER fresta
ARG VERSION

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
