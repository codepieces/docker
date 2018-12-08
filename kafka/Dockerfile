FROM debian

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
	dialog \
	apt-utils \
	curl \
	wget

RUN wget https://download.java.net/java/GA/jdk11/13/GPL/openjdk-11.0.1_linux-x64_bin.tar.gz \
	&& tar -xf openjdk-11.0.1_linux-x64_bin.tar.gz -C /opt/

RUN wget https://www-us.apache.org/dist/kafka/2.1.0/kafka_2.11-2.1.0.tgz \
	&& tar -xf kafka_2.11-2.1.0.tgz -C /opt/

ENV JAVA_HOME=/opt/jdk-11.0.1

COPY server.properties /opt/kafka_2.11-2.1.0/config/server.properties

WORKDIR /opt/kafka_2.11-2.1.0

CMD ./bin/kafka-server-start.sh config/server.properties