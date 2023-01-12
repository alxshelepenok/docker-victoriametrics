# docker-grafana

Ready-to-run Docker image with VictoriaMetrics.

## Quickstart

```bash
$ docker run --name victoriametrics -e waterscape/victoriametrics:latest
```

## Building

```bash
$ ./build.sh latest
```

## Usage

```yaml
version: "3.9"

victoriametrics:
  image: waterscape/victoriametrics
  volumes:
    - victoriametrics-data:/storage
  command:
    - --storageDataPath=/storage

volumes:
  victoriametrics-data:
    external: false
```
