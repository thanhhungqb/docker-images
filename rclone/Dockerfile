FROM ubuntu:16.04

MAINTAINER thanhhungqb <thanhhungqb@gmail.com>

RUN 	apt-get update && \
	apt-get install -y curl unzip && \
	curl https://rclone.org/install.sh | bash ; \
	echo 'done'
	
ENV	PATH	/bin:/usr/bin:/usr/local/bin:/sbin:/usr/sbin

CMD 	["rclone"]

