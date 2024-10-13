FROM khulnasoft/curl
LABEL maintainer "KhulnaSoft DevOps <info@khulnasoft.com>"

RUN apk add --no-cache \
	bash

COPY sendemail /usr/bin/sendemail

ENTRYPOINT [ "sendemail" ]
