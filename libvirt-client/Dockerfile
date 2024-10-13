FROM alpine:latest
LABEL maintainer "KhulnaSoft DevOps <info@khulnasoft.com>"

RUN apk --no-cache add \
	libvirt-client

ENTRYPOINT [ "virsh", "-c", "qemu:///system" ]
