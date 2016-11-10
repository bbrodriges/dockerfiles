# glide

Package Management for Golang in container.

# Usage

Default:

```
docker run --rm -v <path_to_source_root>:/src bbrodriges/glide
```

With reusable cache:

```
docker run --rm -v <path_to_source_root>:/src -v <path_to_glide_cache>:/cache bbrodriges/glide
```