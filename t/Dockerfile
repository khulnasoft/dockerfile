FROM	ruby:alpine
LABEL maintainer "KhulnaSoft DevOps <info@khulnasoft.com>"

RUN	apk add --no-cache \
	ca-certificates

RUN	set -x \
	&& apk add --no-cache --virtual .build-deps \
	build-base \
	&& gem install io-console t --no-document \
	&& apk del .build-deps

ENTRYPOINT	["t"]
