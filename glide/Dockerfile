FROM golang:alpine
MAINTAINER bender.rodriges <bender.rodriges@gmail.com>

ENV CACHE_FOLDER /root/.glide
ENV APP_FOLDER $GOPATH/src/app
ENV GLIDE_HOME $CACHE_FOLDER

RUN set -ex \
	&& apk add --no-cache git \
	&& apk add --no-cache --virtual .build-deps curl \
	\
	&& curl https://glide.sh/get | sh \
	\
	&& rm -rf /*.patch \
	&& apk del .build-deps

RUN mkdir -p $APP_FOLDER $CACHE_FOLDER \
	&& ln -s $APP_FOLDER /src \
	&& ln -s $CACHE_FOLDER /cache

WORKDIR $APP_FOLDER

VOLUME /src
VOLUME /cache

CMD ["glide", "install"]