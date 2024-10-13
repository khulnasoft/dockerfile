FROM alpine:latest
LABEL maintainer "KhulnaSoft DevOps <info@khulnasoft.com>"

ENV HOME /home/gcalcli

RUN apk --no-cache add \
	python3 \
	python3-dev \
	build-base \
	&& adduser -S gcalcli \
	&& chown -R gcalcli $HOME \
	&& pip3 install vobject parsedatetime gcalcli

WORKDIR $HOME
USER gcalcli

ENTRYPOINT [ "gcalcli" ]
