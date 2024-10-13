# command to run Telnet
# docker run -it --rm \
#	--log-driver none \
#	jess/telnet towel.blinkenlights.nl
#
FROM alpine:latest
LABEL maintainer "KhulnaSoft DevOps <info@khulnasoft.com>"

RUN apk add --no-cache --virtual \
	busybox-extras

ENTRYPOINT [ "telnet" ]
