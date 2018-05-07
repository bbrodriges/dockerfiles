FROM swift:4

MAINTAINER bbrodriges <bender.rodriges@gmail.com>

ENV PLUGIN_VERSION "1.0.3"
ENV PROTOC_VERSION "3.5.1"

RUN apt-get -q update && \
    apt-get -q install -y \
    unzip \
    && rm -r /var/lib/apt/lists/*

RUN curl -L -o plugin.zip https://github.com/apple/swift-protobuf/archive/$PLUGIN_VERSION.zip && \
	unzip plugin.zip -d ./plugin && \
	(cd plugin/swift-protobuf-$PLUGIN_VERSION && swift build -c release) && \
	cp ./plugin/swift-protobuf-$PLUGIN_VERSION/.build/x86_64-unknown-linux/release/protoc-gen-swift /usr/local/bin/protoc-gen-swift && \
	rm -rf plugin.zip plugin

RUN curl -L -o protoc.zip https://github.com/google/protobuf/releases/download/v$PROTOC_VERSION/protoc-$PROTOC_VERSION-linux-x86_64.zip && \
	unzip protoc.zip -d ./protoc && \
	cp ./protoc/bin/protoc /usr/local/bin/protoc && \
	rm -rf protoc.zip protoc

CMD ["protoc", "--help"]