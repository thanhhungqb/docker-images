FROM ubuntu:16.04

MAINTAINER thanhhungqb

RUN 	apt-get update && \
	apt-get -y install python curl wget && \
	apt-get -y install supervisor && \
	mkdir -p /etc/supervisord.d && \
	mv /etc/supervisor/supervisord.conf /etc/ && \
	echo "files = /etc/supervisord.d/*.conf" >> /etc/supervisord.conf

CMD 	["supervisord", "-n", "-c", "/etc/supervisord.conf"]

