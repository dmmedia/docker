FROM local/c7-systemd
RUN wget https://ast.tucny.com/repo/tucny-asterisk.repo -O /etc/yum.repos.d/tucny-asterisk.repo && \
rpm --import https://ast.tucny.com/repo/RPM-GPG-KEY-dtucny && \
yum-config-manager --enable repository asterisk-common && \
yum-config-manager --enable repository asterisk-13 && \
yum -y install epel-release && \
yum -y install asterisk asterisk-mp3 asterisk-pjsip asterisk-sounds-core-ru asterisk-sounds-core-ru-ulaw && \
yum clean all && \
systemctl enable asterisk.service
CMD ["/usr/sbin/init"]
