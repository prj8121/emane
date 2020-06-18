FROM fedora:31

# install EMANE build dependencies
# RUN dnf install gcc-c++ autoconf automake libtool libxml2-devel protobuf-devel python2-protobuf python3-protobuf libpcap-devel pcre-devel libuuid-devel rpm-build python2-setuptools python3-setuptoo
# ls  python2-devel python3-devel git make -y

# clone the emane repo  (?)
# RUN git clone https://github.com/adjacentlink/emane.git

# build RPMs
# WORKDIR emane
# RUN ./autogen.sh && ./configure 
# RUN ./autogen.sh && ./configure && make rpm

# install RPMs
# WORKDIR emane/.rpmbuild
# RUN dnf install $(ls RPMS/x86_64/*.rpm RPMS/noarch/*.rpm | grep -v debuginfo) -y

RUN echo 'fake fedora31 ran'