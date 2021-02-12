[<img src="https://hotio.dev/img/lidarr.png" alt="logo" height="130" width="130">](https://github.com/lidarr/Lidarr)

[![GitHub Source](https://img.shields.io/badge/github-source-ffb64c?style=flat-square&logo=github&logoColor=white&labelColor=757575)](https://github.com/hotio/lidarr)
[![GitHub Registry](https://img.shields.io/badge/github-registry-ffb64c?style=flat-square&logo=github&logoColor=white&labelColor=757575)](https://github.com/orgs/hotio/packages/container/package/lidarr)
[![Docker Pulls](https://img.shields.io/docker/pulls/hotio/lidarr?color=ffb64c&style=flat-square&label=pulls&logo=docker&logoColor=white&labelColor=757575)](https://hub.docker.com/r/hotio/lidarr)
[![Discord](https://img.shields.io/discord/610068305893523457?style=flat-square&color=ffb64c&label=discord&logo=discord&logoColor=white&labelColor=757575)](https://hotio.dev/discord)
[![Upstream](https://img.shields.io/badge/upstream-project-ffb64c?style=flat-square&labelColor=757575)](https://github.com/lidarr/Lidarr)
[![Website](https://img.shields.io/badge/website-hotio.dev-ffb64c?style=flat-square&labelColor=757575)](https://hotio.dev/containers/lidarr)

## Starting the container

CLI:

```shell
docker run --rm \
    --name lidarr \
    -p 8686:8686 \
    -e PUID=1000 \
    -e PGID=1000 \
    -e UMASK=002 \
    -e TZ="Etc/UTC" \
    -v /<host_folder_config>:/config \
    hotio/lidarr
```

Compose:

```yaml
version: "3.7"

services:
  lidarr:
    container_name: lidarr
    image: hotio/lidarr
    ports:
      - "8686:8686"
    environment:
      - PUID=1000
      - PGID=1000
      - UMASK=002
      - TZ=Etc/UTC
    volumes:
      - /<host_folder_config>:/config
```

In most cases you'll need to add additional volumes, depending on your own personal preference, to get access to your files.

## Tags

Go [here](https://hotio.dev/tags-overview/#hotiolidarr) to see all available tags.
