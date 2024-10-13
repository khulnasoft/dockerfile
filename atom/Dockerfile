# Base Docker image
FROM debian:bullseye-slim

# Set the maintainer label
LABEL maintainer="KhulnaSoft DevOps <info@khulnasoft.com>"

# Set non-interactive mode for apt-get
ENV DEBIAN_FRONTEND=noninteractive

# Install dependencies and essential packages
RUN apt-get update && apt-get install -y \
    apt-transport-https \
    ca-certificates \
    wget \
    --no-install-recommends && \
    rm -rf /var/lib/apt/lists/*

# Install Atom and additional dependencies
FROM debian:bullseye-slim AS builder
RUN apt-get update && apt-get install -y wget
RUN wget -q https://github.com/atom/atom/releases/latest/download/atom-amd64.deb -O /tmp/atom.deb

FROM debian:bullseye-slim
COPY --from=builder /tmp/atom.deb /tmp/atom.deb
RUN apt-get update && \
    apt-get install -y /tmp/atom.deb git gconf-service gconf2 gvfs-bin \
    libasound2 libcap2 libgconf-2-4 libgtk2.0-0 libnotify4 libnss3 \
    libxkbfile1 libxss1 libxtst6 libx11-xcb-dev xdg-utils --no-install-recommends && \
    rm -rf /var/lib/apt/lists/* && \
    rm /tmp/atom.deb

# Set the entrypoint to launch Atom in foreground
ENTRYPOINT ["atom", "--foreground"]
