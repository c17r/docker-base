FROM python:3.6.8-alpine AS base

RUN apk update \
&& apk upgrade \
&& apk add --no-cache git uwsgi-python3 \
&& python3 -m venv /venv \
&& /venv/bin/pip install --quiet --no-cache-dir -U pip \
&& mkdir /code/

EXPOSE 8000

ENV \
PYTHONUNBUFFERED=1 \
UWSGI_GID=2000 \
UWSGI_HTTP_AUTO_CHUNKED=1 \
UWSGI_HTTP_KEEPALIVE=1 \
UWSGI_HTTP_SOCKET=0.0.0.0:8000 \
UWSGI_LAZY_APPS=1 \
UWSGI_MASTER=1 \
UWSGI_PLUGINS=python3 \
UWSGI_THREADS=3 \
UWSGI_UID=1000 \
UWSGI_VIRTUALENV=/venv \
UWSGI_WORKERS=1 \
UWSGI_WSGI_ENV_BEHAVIOR=holy
