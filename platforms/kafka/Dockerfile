FROM ibm-semeru-runtimes:open-8u362-b09-jdk

ENV KAFKA_USER=kafka KAFKA_DATA_DIR=/var/lib/kafka/data KAFKA_HOME=/opt/kafka PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/kafka/bin

RUN set -eux; \
     KAFKA_DIST=kafka_2.12-3.7.0; KAFKA_VERSION=3.7.0; \
     curl -O "http://archive.apache.org/dist/kafka/$KAFKA_VERSION/$KAFKA_DIST.tgz"; \
     curl -O "http://archive.apache.org/dist/kafka/$KAFKA_VERSION/$KAFKA_DIST.tgz.asc"; \
     tar -xzf "$KAFKA_DIST.tgz" -C /opt; \
     ln -s /opt/$KAFKA_DIST $KAFKA_HOME ; \
     useradd $KAFKA_USER; \ 
     [ `id -u $KAFKA_USER` -eq 1000 ]; \ 
     [ `id -g $KAFKA_USER` -eq 1000 ]; \ 
     mkdir -p $KAFKA_DATA_DIR; \ 
     chown -R "$KAFKA_USER:$KAFKA_USER" /opt/$KAFKA_DIST; \ 
     chown -R "$KAFKA_USER:$KAFKA_USER" $KAFKA_DATA_DIR; \
     rm -rf /var/lib/apt/lists/*; \
     rm -rf /tmp/* 
