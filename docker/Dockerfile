#################################################################
# Dockerfile to build Zimbra Collaboration 8.8.12 container images
# Based on CentOS 7
# Created by Alan Denniston
# Editado por Michael Robert
#################################################################
FROM centos:7
MAINTAINER Alan Denniston <alan.denniston@gmail.com>

RUN yum update -y --nogpgcheck && yum install -y --nogpgcheck \
  wget \
  dialog \
  sqlite \
  bind \
  bind-chroot \
  bind-libs
  bind-utils \
  nc \
  sudo \
  sysstat \
  unzip \
  perl \
  perl-core \
  ntpl \
  nmap \ 
  libidn \
  gmp \
  libaio \ 
  libstdc++ \ 
  unzip \
  telnet \
  net-tools \
  openssh \
  openssh-server \
  && yum clean all \
  && yum clean metadata
VOLUME ["/opt/zimbra"]

EXPOSE 22 25 465 587 110 143 993 995 80 443 8080 8443 7071

COPY opt /opt/

CMD ["/bin/bash", "/opt/start.sh", "-bash"]
