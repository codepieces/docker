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

RUN wget https://github.com/oracle/graal/releases/download/vm-1.0.0-rc10/graalvm-ce-1.0.0-rc10-linux-amd64.tar.gz \
	&& tar -xf graalvm-ce-1.0.0-rc10-linux-amd64.tar.gz -C /opt/

RUN wget https://download.jetbrains.com/idea/ideaIU-2018.3.1.tar.gz \
	&& tar -xf ideaIU-2018.3.1.tar.gz -C /opt/

ENV DISPLAY=192.168.1.197:0.0 JAVA_HOME=/opt/graalvm-ce-1.0.0-rc10

CMD /opt/idea-IU-183.4588.61/bin/idea.sh