FROM		docker.elastic.co/logstash/logstash:6.6.1
MAINTAINER	Eric Chin <ericchin90@gmail.com>

WORKDIR mkdir -p /opt/logstash/logs

WORKDIR /opt/logstash/config

COPY configurations/logstash-nginx.conf logstash-nginx.conf
COPY configurations/nginx.txt nginx.txt

ENTRYPOINT ["/usr/local/bin/docker-entrypoint"]
