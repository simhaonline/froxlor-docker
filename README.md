[![Release](https://img.shields.io/github/v/release/bloodhunterd/froxlor-docker?include_prereleases&style=for-the-badge)](https://github.com/bloodhunterd/froxlor-docker/releases)
[![Docker Build](https://img.shields.io/docker/cloud/build/bloodhunterd/froxlor?style=for-the-badge)](https://hub.docker.com/r/bloodhunterd/froxlor)
[![Docker Pulls](https://img.shields.io/docker/pulls/bloodhunterd/froxlor?style=for-the-badge)](https://hub.docker.com/r/bloodhunterd/froxlor)
[![Docker Stars](https://img.shields.io/docker/stars/bloodhunterd/froxlor?style=for-the-badge)](https://hub.docker.com/r/bloodhunterd/froxlor)
[![License](https://img.shields.io/github/license/bloodhunterd/froxlor-docker?style=for-the-badge)](https://github.com/bloodhunterd/froxlor-docker/blob/master/LICENSE)

[![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/P5P51U5SZ)

# Froxlor Docker

Docker image for Froxlor Server Management Panel.

## Installation

Download [Froxlor](https://froxlor.org/) and mount it into the container due individually setup.

## Configuration

See distribution [Docker Compose file](https://github.com/bloodhunterd/froxlor-docker/blob/master/docker-compose.dist.yml).

### Environment

| ENV | Values¹ | Default | Description
|--- |--- |--- |---
| TZ | [PHP: List of supported timezones - Manual](https://www.php.net/manual/en/timezones.php) | Europe/Berlin | Timezone.

### Volumes

Persist Froxlor, so the build in update process can be used. 

```bash
    volumes:
      - ./froxlor/:/var/www/froxlor/
```

Persist customer web, mail and log directories. 

```bash
    volumes:
      - ./customers/:/var/customers/
```

Persist SSL certificates ([Let's Encrypt](https://letsencrypt.org/)).

```bash
    volumes:
      - ./ssl/:/etc/ssl/froxlor/
```

## Update

Please note the [changelog](https://github.com/bloodhunterd/froxlor-docker/blob/master/CHANGELOG.md) to check for configuration changes before updating.

```bash
docker-compose pull
docker-compose up -d
```

## Build With

* [Froxlor](https://froxlor.org/)
* [NGINX](https://www.nginx.com/)
* [MariaDB](https://mariadb.org/)
* [PHP](https://www.php.net/)
* [BIND](https://www.isc.org/bind/)
* [Let's Encrypt](https://letsencrypt.org/)
* [Debian](https://www.debian.org/)
* [Docker](https://www.docker.com/)

## Authors

* [BloodhunterD](https://github.com/bloodhunterd)

## License

This project is licensed under the MIT - see [LICENSE.md](https://github.com/bloodhunterd/froxlor-docker/blob/master/LICENSE) file for details.
