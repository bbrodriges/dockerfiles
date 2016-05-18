# raml2html

Simple container to convert RAML files to HTML documentation.

# Usage

```
docker run --rm -v <path_to_raml_files>:/app -e "INPUT=index.raml" -e "OUTPUT=index.html" bbrodriges/raml2html
```