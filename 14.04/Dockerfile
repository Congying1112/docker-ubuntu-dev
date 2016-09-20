FROM congying/updated-ubuntu:14.04

MAINTAINER Congying <congying1112@gmail.com>

RUN apt-get install -y software-properties-common
RUN add-apt-repository ppa:ubuntu-toolchain-r/test
RUN apt-get update

RUN apt-get install -y build-essential
RUN apt-get install -y pkg-config
RUN apt-get install -y wget

RUN apt-get install -y gcc-6
RUN apt-get install -y g++-6
RUN unlink /usr/bin/gcc && ln -s /usr/bin/gcc-6 /usr/bin/gcc
RUN unlink /usr/bin/gcc-ar && ln -s /usr/bin/gcc-ar-6 /usr/bin/gcc-ar
RUN unlink /usr/bin/gcc-nm && ln -s /usr/bin/gcc-nm-6 /usr/bin/gcc-nm
RUN unlink /usr/bin/gcc-ranlib && ln -s /usr/bin/gcc-ranlib-6 /usr/bin/gcc-ranlib
RUN unlink /usr/bin/g++ && ln -s /usr/bin/g++-6 /usr/bin/g++

RUN cd /tmp && wget -O cmake-3.6.2.tar.gz https://cmake.org/files/v3.6/cmake-3.6.2.tar.gz && tar -zxvf cmake-3.6.2.tar.gz
RUN cd /tmp/cmake-3.6.2 && ./bootstrap && make -j4 && make install

RUN rm -r /tmp/*