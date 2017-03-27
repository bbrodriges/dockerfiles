# raml2html

Simple container to convert RAML files to HTML documentation.

# Usage

Using default template:

```
docker run --rm -v <path_to_raml_files>:/app -e "INPUT=index.raml" -e "OUTPUT=index.html" bbrodriges/raml2html
```

Using custom template:

```
docker run --rm -v <path_to_raml_files>:/app -e "INPUT=index.raml" -e "OUTPUT=index.html" -e "FORMAT=custom" -e "TPL=template.nunjucks" bbrodriges/raml2html
```

Markdown output:

```
docker run --rm -v <path_to_raml_files>:/app -e "INPUT=index.raml" -e "OUTPUT=index.md" -e "FORMAT=md" bbrodriges/raml2html
```

Slate theme output:

```
docker run --rm -v <path_to_raml_files>:/app -e "INPUT=index.raml" -e "OUTPUT=index.html" -e "FORMAT=slate" bbrodriges/raml2html
```

# Credits

Based on `https://github.com/raml2html/raml2html`
