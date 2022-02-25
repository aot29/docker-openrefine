Docker image for OpenRefine

[![docker-openrefine-actions-workflow](https://github.com/aot29/docker-openrefine/actions/workflows/master.yml/badge.svg)](https://github.com/aot29/docker-openrefine/actions/workflows/master.yml)

# Usage
Add this to a docker-compose.yml services section

```
  openrefine:
    image: ghcr.io/aot29/docker-openrefine:master
    ports:
      - "3333:3333"
    volumes:
      - ./data:/data
    environment:
      - REFINE_INTERFACE=0.0.0.0
      - REFINE_PORT=3333
      - REFINE_MEMORY=1024M
      - REFINE_DATA_DIR=/data
```
