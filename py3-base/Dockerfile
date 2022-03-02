FROM python:3.9-alpine AS base

RUN apk update \
	&& apk upgrade -U -a \
	&& apk add --no-cache git \
	&& python3 -m venv /venv \
	&& /venv/bin/pip install --quiet --no-cache-dir -U pip
