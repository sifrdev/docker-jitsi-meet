FROM jitsi/base

RUN \
	apt-dpkg-wrap apt-get update && \
	apt-dpkg-wrap apt-get install -y cron nginx-extras jitsi-meet-web && \
	apt-dpkg-wrap apt-get install -y -t stretch-backports certbot && \
	apt-dpkg-wrap apt-get install -y wget && \
	wget -q https://www.sifr.no/all.css -O /usr/share/jitsi-meet/css/all.css && \
	apt-cleanup && \
	rm -f /etc/nginx/conf.d/default.conf && \
	rm -f /usr/share/jitsi-meet/interface_config.js

COPY rootfs/ /

EXPOSE 80 443

VOLUME /config

