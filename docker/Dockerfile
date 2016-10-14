FROM scratch
MAINTAINER The CentOS Project <cloud-ops@centos.org>
#ADD centos-7.2.1511-docker.tar.xz /
ADD http://x3193-www.daoapp.io/ubt1404.tar.gz.xz /

LABEL name="CentOS Base Image"
LABEL vendor="CentOS"
LABEL license=GPLv2

# Volumes for systemd
# VOLUME ["/run", "/tmp"]

# Environment for systemd
# ENV container=docker

# For systemd usage this changes to /usr/sbin/init
# Keeping it as /bin/bash for compatability with previous
CMD /run.sh full
