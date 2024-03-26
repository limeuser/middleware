FROM openjdk:8u342-slim

RUN apt-get update && \
    apt-get install -y --no-install-recommends fontconfig libfreetype6 ca-certificates p11-kit tzdata curl locales && \
    rm -rf /var/lib/apt/lists/*

COPY fonts/ /usr/share/fonts/wqy/

COPY security/java.security /opt/java/openjdk/jre/lib/security/

RUN  mkdir -p /home/local/bin/ && \
    mkdir -p /home/local/conf/ && \
    mkdir -p /home/local/libs/ && \
    mkdir -p /home/local/modules/ && \
    mkdir -p /home/local/tools/ && \
    mkdir -p /home/local/web/tomcat && \
    mkdir -p /home/local/web/tongweb

COPY tongweb/* /home/local/web/tongweb/
