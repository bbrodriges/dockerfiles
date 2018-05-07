# swift-protobuf

Container to produce Swift source code from Protobuf files.

# Usage

```
docker run --rm -v <path_to_protos>:/proto bbrodriges/swift-protobuf:latest protoc -I /proto --swift_out=/proto /proto/index.proto
```

# Credits

Based on `https://github.com/muukii/docker-protobuf`
