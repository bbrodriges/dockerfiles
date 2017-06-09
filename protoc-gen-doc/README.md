# protoc-gen-doc

Simple container to generate documentation from .proto files.

# Usage

Suppose you have your proto files in ~/proto and you want to generate HTML documentation:

```
docker run --rm -v $HOME/proto:/src -v $HOME/docs:/docs bbrodriges/protoc-gen-doc sh -c "protoc --doc_out=html,index.html:/docs *.proto"
```

Running above command will create folder named `docs` and put `index.html` file into it.

# Other formats

See [https://github.com/pseudomuto/protoc-gen-doc#invoking-the-plugin](https://github.com/pseudomuto/protoc-gen-doc#invoking-the-plugin)

# Credits

Inspired by `https://github.com/sashabaranov/protoc-gen-doc/blob/master/Dockerfile`