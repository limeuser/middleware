FROM ibm-semeru-runtimes:open-8u362-b09-jdk

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
