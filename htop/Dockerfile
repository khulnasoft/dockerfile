# htop in a container
#
# docker run --rm -it \
# 	--pid host \
# 	jess/htop
#
FROM alpine:latest
LABEL maintainer "KhulnaSoft DevOps <info@khulnasoft.com>"

RUN apk --no-cache add \
	htop

CMD [ "htop" ]
