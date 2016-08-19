# gear-visor

Simple container to run gear-visor Web UI service.

# Usage

This docker image is ment to be used in `docker-compose.yml` alongside with gearmand docker image.
Mount `/app/gear_visor_settings.py` to override default visor settings.


```
gearman:
  image: pataquets/gearmand
  user: nobody
  restart: always

visor:
  image: bbrodriges/gear-visor
  restart: always
  ports:
  - "127.0.0.1:8840:5000"
  volumes:
  - "./gear_visor_settings.py:/app/gear_visor_settings.py"

```

# Source
See [github](https://github.com/bbrodriges/gear-visor)