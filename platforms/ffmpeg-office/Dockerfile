FROM registry.supos.ai/library/supfusion-jdk-runtimes:open-8u362-b09-jdk

COPY . /tmp/

RUN set -eux; \
	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; \
	mv /tmp/sources-${arch}.list /etc/apt/sources.list; \
     apt update; \ 
     apt install -y libreoffice ffmpeg; \
     apt-get remove openjdk-11-jre openjdk-11-jre-headless -y; \
     apt autoremove -y; \
     rm -rf /var/lib/apt/lists/*; \
     rm -rf /tmp/* 
