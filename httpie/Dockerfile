FROM alpine:latest
LABEL maintainer "KhulnaSoft DevOps <info@khulnasoft.com>"

RUN apk --no-cache add \
	ca-certificates \
	python \
	py2-pip \
	&& pip install httpie httpie-unixsocket

ENTRYPOINT [ "http" ]
