# VERSION			0.0.1
# BUILD-USING:		docker build -t library/liferay .
# PUSH-USING:		docker tag library/liferay ericchin90/liferay && docker push ericchin90/liferay

FROM		elk_jdk:latest
MAINTAINER 	Eric Chin <ericchin90@gmail.com>

RUN mkdir /opt/apps
WORKDIR /opt/apps

COPY nginx.repo /etc/yum.repos.d/nginx.repo

RUN yum install -y nginx

EXPOSE 80

CMD ["nginx", "-g" ,"daemon off;"]