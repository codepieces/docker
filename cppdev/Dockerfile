FROM debian

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
	dialog \
	apt-utils \
	curl \
	wget \
	git \
	build-essential \
	libgtk-3-0 \
	libxss1 \
	libgconf-2-4 \
	libnss3 \
	libasound2 \
	libxkbfile1
	
RUN wget https://update.code.visualstudio.com/latest/linux-x64/stable \
	&& tar -xf stable -C /opt/

ENV DISPLAY=192.168.1.197:0.0

CMD /opt/VSCode-linux-x64/code