# raml2md

Simple container to convert RAML files to Markdown.

# Usage

Using default template:

```
docker run --rm -v <path_to_raml_files>:/app -e "INPUT=index.raml" -e "OUTPUT=index.md" bbrodriges/raml2md
```

Using custom template:

```
docker run --rm -v <path_to_raml_files>:/app -e "INPUT=index.raml" -e "OUTPUT=index.md" -e "TPL=template.nunjucks" bbrodriges/raml2md
```

# Credits

Based on `https://github.com/raml2html/raml2md`