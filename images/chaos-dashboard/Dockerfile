FROM debian:buster-slim

ARG HTTPS_PROXY
ARG HTTP_PROXY

ENV http_proxy $HTTP_PROXY
ENV https_proxy $HTTPS_PROXY

ARG UI
ARG SWAGGER

RUN apt-get update && apt-get install tzdata -y && rm -rf /var/lib/apt/lists/*

ENV http_proxy=
ENV https_proxy=

COPY --from=pingcap/chaos-binary /bin/chaos-dashboard /usr/local/bin/chaos-dashboard
