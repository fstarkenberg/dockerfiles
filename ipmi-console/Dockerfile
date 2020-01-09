FROM alpine:3.11

# Setup demo environment variables
ENV HOME=/root \
    LANG=en_US.UTF-8 \
    LANGUAGE=en_US.UTF-8 \
    LC_ALL=C.UTF-8 \
    DISPLAY=:0.0 \
    DISPLAY_WIDTH=1920 \
    DISPLAY_HEIGHT=1080

# x11vnc is in testing repo
RUN echo "http://dl-3.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories

RUN apk --update --upgrade add \
    bash \
    xterm \
    supervisor \
    x11vnc \
    novnc \
    xvfb \
    fluxbox \
    icedtea-web \
    firefox \
    ttf-dejavu && \
    rm -rf /var/cache/apk/*

COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf
COPY javaws.desktop /usr/share/applications/javaws.desktop
COPY mimeapps.list /root/.config/mimeapps.list
COPY deployment.properties /root/.config/icedtea-web/deployment.properties

EXPOSE 8080

CMD ["/usr/bin/supervisord", "-c", "/etc/supervisor/conf.d/supervisord.conf"]
