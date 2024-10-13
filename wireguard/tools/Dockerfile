FROM debian:sid-slim

LABEL maintainer "KhulnaSoft DevOps <info@khulnasoft.com>"

RUN apt update && apt -y install \
	ca-certificates \
	libmnl-dev \
	--no-install-recommends \
	&& rm -rf /var/lib/apt/lists/*

COPY --from=khulnasoft/wireguard:install /usr/bin/wg /usr/bin/wg
COPY --from=khulnasoft/wireguard:install /usr/share/man/man8/wg.8 /usr/share/man/man8/wg.8

ENTRYPOINT ["wg"]
CMD ["--help"]
