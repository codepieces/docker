FROM debian

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
	dialog \
	apt-utils \
	curl \
	wget \
	git \
	libxext-dev \
	libxrender-dev \
	libxtst-dev \
	libfreetype6

RUN wget https://download.java.net/java/GA/jdk11/13/GPL/openjdk-11.0.1_linux-x64_bin.tar.gz \
	&& tar -xf openjdk-11.0.1_linux-x64_bin.tar.gz -C /opt/

RUN wget https://download.jetbrains.com/idea/ideaIU-2018.3.1.tar.gz \
	&& tar -xf ideaIU-2018.3.1.tar.gz -C /opt/

ENV DISPLAY=192.168.1.197:0.0 JAVA_HOME=/opt/jdk-11.0.1

CMD /opt/idea-IU-183.4588.61/bin/idea.sh