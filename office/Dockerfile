FROM registry.supos.ai/library/supfusion-jdk-runtimes:aarch64-open-8u362-b09-jdk

RUN apt-get update -y && \
    apt list --upgradable -y && \
    apt-get instal -y ffmpeg libreoffice && \
    apt-get clean --dry-run && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* /var/tmp/*