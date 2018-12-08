FROM debian

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
	dialog \
	apt-utils \
	curl \
	wget

RUN wget https://download.java.net/java/GA/jdk11/13/GPL/openjdk-11.0.1_linux-x64_bin.tar.gz \
	&& tar -xf openjdk-11.0.1_linux-x64_bin.tar.gz -C /opt/

RUN wget https://www-us.apache.org/dist/zookeeper/stable/zookeeper-3.4.12.tar.gz \
	&& tar -xf zookeeper-3.4.12.tar.gz -C /opt/

ENV JAVA_HOME=/opt/jdk-11.0.1

COPY zoo.cfg /opt/zookeeper-3.4.12/conf/zoo.cfg

CMD /opt/zookeeper-3.4.12/bin/zkServer.sh start-foreground