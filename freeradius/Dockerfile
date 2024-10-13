FROM alpine:latest
LABEL maintainer "KhulnaSoft DevOps <info@khulnasoft.com>"

RUN apk --no-cache add \
    freeradius \
	freeradius-python \
	freeradius-radclient \
	freeradius-sql \
	freeradius-sqlite \
	openssl-dev \
	python2 \
	sqlite

ENTRYPOINT [ "radiusd" ]
CMD [ "-xx","-f" ]
