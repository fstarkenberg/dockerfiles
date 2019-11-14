FROM lsiobase/guacgui
LABEL maintainer="fresta"

ENV APP_NAME="subtitleedit"

ENV DEBIAN_FRONTEND noninteractive

RUN \
  echo "**** install runtime packages ****" && \
  apt-get update --quiet && \
  apt-get install --quiet --yes --no-install-recommends \
    wget \
    unzip \
    mono-xsp4 && \
  echo "**** install subtitleedit ****" && \
  mkdir /SubtitleEdit && \
  wget https://github.com/SubtitleEdit/subtitleedit/releases/download/3.5.11/SE3511.zip && \
  unzip -d /SubtitleEdit SE3511.zip && \
  echo "**** cleanup ****" && \
  apt-get clean && \
  rm -rf \
    /tmp/* \
    /var/lib/apt/lists/* \
    /var/tmp/*

RUN locale-gen en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US:en
ENV LC_ALL en_US.UTF-8

EXPOSE 3389 8080

# add local files
COPY /root /
