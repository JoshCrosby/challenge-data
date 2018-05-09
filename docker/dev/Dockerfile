FROM node:alpine

ENV APP_BASE=/app/hello
ARG BUILD_ENV

WORKDIR $APP_BASE

EXPOSE 4000

COPY docker/$BUILD_ENV /docker/

CMD /docker/launch
