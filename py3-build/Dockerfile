FROM python:3.6.8-alpine AS base

RUN apk update \
&& apk upgrade \
&& pip install --quiet --no-cache-dir -U pip \
&& pip install --quiet --no-cache-dir -U pipenv \
&& mkdir /build/
