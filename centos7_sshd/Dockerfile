FROM centos:centos7
MAINTAINER Albert Palau

RUN yum -y update; yum clean all
RUN yum -y install openssh-server passwd; yum clean all
RUN echo -e "r00tP4sw0rd\nr00tP4sw0rd" | (passwd --stdin root)
RUN mkdir /var/run/sshd

RUN ssh-keygen -t rsa -f /etc/ssh/ssh_host_rsa_key -N '' 

ENTRYPOINT ["/usr/sbin/sshd", "-D"]
