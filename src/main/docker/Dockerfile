FROM openjdk:8-jdk-alpine

MAINTAINER javaansehz

RUN apk --no-cache add openssl wget tar bash curl nano
RUN wget -q http://packages.confluent.io/archive/4.0/confluent-oss-4.0.0-2.11.tar.gz
RUN tar -xzf confluent-oss-4.0.0-2.11.tar.gz
RUN rm confluent-oss-4.0.0-2.11.tar.gz

EXPOSE 2181:2181
EXPOSE 8081:8081
EXPOSE 9092:9092

CMD /confluent-4.0.0/bin/confluent start && tail -F /confluent-4.0.0/log/server.log
