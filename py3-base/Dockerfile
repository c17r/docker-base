FROM alpine:3.19 AS base

RUN apk update \
	&& apk upgrade -U -a \
	&& apk add --no-cache git python3 \
	&& python3 -m venv /venv \
	&& /venv/bin/pip install --quiet --no-cache-dir -U pip
