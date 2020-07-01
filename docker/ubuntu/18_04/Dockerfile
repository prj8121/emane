FROM ubuntu:18.04

# install EMANE build dependencies
RUN apt-get update && apt-get install --yes gcc g++ autoconf automake libtool libxml2-dev libprotobuf-dev python-protobuf libpcap-dev libpcre3-dev uuid-dev debhelper pkg-config python-setuptools protobuf-compiler git dh-python python3-protobuf python3-setuptools

# clone the emane repo
RUN git clone https://github.com/adjacentlink/emane.git

# build debs
WORKDIR emane
RUN ./autogen.sh && ./configure && make deb

# install debs
WORKDIR .debbuild
RUN dpkg -i *.deb
RUN apt-get install -f