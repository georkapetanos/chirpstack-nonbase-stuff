# syntax=docker/dockerfile:1

FROM --platform=linux/arm64 ubuntu:focal

RUN apt-get update && apt-get -y install --no-install-recommends \
    nano
    
COPY ./bin/chirpstack-fuota-server /usr/bin/chirpstack-fuota-server
COPY ./configuration/chirpstack-fuota-config.toml /etc/chirpstack-fuota-server/chirpstack-fuota-config.toml

ENTRYPOINT ["/usr/bin/chirpstack-fuota-server","-c", "/etc/chirpstack-fuota-server/chirpstack-fuota-config.toml"]
