FROM node:alpine

ENV APP_BASE=/app
ARG BUILD_ENV

WORKDIR $APP_BASE

COPY docker/$BUILD_ENV /docker/

ENTRYPOINT /bin/bash
