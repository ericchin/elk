# VERSION			0.0.1
# BUILD-USING:		docker build -t library/jdk8 .
# PUSH-USING:		docker tag library/jdk8 ericchin90/jdk8 && docker push ericchin90/jdk8

FROM		centos:centos7
MAINTAINER 	Eric Chin <ericchin90@gmail.com>

RUN yum -y install wget tar unzip

RUN wget --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" "https://download.oracle.com/otn-pub/java/jdk/8u201-b09/42970487e3af4f5aa5bca3f542482c60/jdk-8u201-linux-x64.rpm"

RUN rpm -Uvh jdk-8u201-linux-x64.rpm
RUN rm jdk-8u201-linux-x64.rpm

RUN echo 'fs.file-max = 100000' >> /etc/sysctl.conf

RUN sed -i.bak '$ i \*\t\thard\tnofile\t\t8192\n\*\t\tsoft\tnofile\t\t8192' /etc/security/limits.conf

CMD ["/bin/bash"]