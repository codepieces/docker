FROM debian

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
	dialog \
	apt-utils \
	curl \
	wget \
	git \
  vim \
	build-essential \
  clang \
  clang-format \
  libboost-dev \
  cmake \
  cppcheck \
	gdb \
  doxygen

ENV DISPLAY=192.168.1.197:0.0

CMD /bin/bash
