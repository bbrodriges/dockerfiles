FROM golang:alpine
MAINTAINER bender.rodriges <bender.rodriges@gmail.com>

RUN set -ex \
	&& apk add --no-cache --virtual .build-deps \
		curl \
	\
	&& curl https://glide.sh/get | sh \
	\
	&& rm -rf /*.patch \
	&& apk del .build-deps

RUN mkdir -p /src /cache /root/.glide && \
	ln -s /root/.glide /cache

WORKDIR /src

VOLUME /src
VOLUME /cache

CMD ["glide", "install"]