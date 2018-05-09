FROM node:alpine

ENV APP_BASE=/app/hello
ARG BUILD_ENV

RUN [ ! -d $APP_BASE ] && mkdir -p $APP_BASE

WORKDIR $APP_BASE
COPY src/package.json $APP_BASE/
RUN npm install
COPY src/ $APP_BASE/


#ARG BUILD_VERSION
#RUN if [ ! $BUILD_VERSION ]; then exit 1; fi
#RUN echo '{"build":{"version":"'$BUILD_VERSION'"}}' >> $APP_BASE/config/local.json

# do other things like babel here

EXPOSE 4000

COPY docker/$BUILD_ENV /docker/

CMD /docker/launch
