FROM congying/updated-ubuntu:16.10

MAINTAINER Congying <congying1112@gmail.com>

RUN apt-get install -y build-essential
RUN apt-get install -y pkg-config
RUN apt-get install -y wget

RUN cd /tmp && wget -O cmake-3.6.2.tar.gz https://cmake.org/files/v3.6/cmake-3.6.2.tar.gz && tar -zxvf cmake-3.6.2.tar.gz
RUN cd /tmp/cmake-3.6.2 && ./bootstrap && make -j4 && make install

RUN rm -r /tmp/*