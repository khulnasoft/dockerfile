FROM debian:sid-slim
LABEL maintainer "KhulnaSoft DevOps <info@khulnasoft.com>"

RUN apt-get update && apt-get install -y \
	netcat \
	--no-install-recommends \
	&& rm -rf /var/lib/apt/lists/*

ENTRYPOINT [ "netcat" ]
