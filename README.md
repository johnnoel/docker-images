# Docker images

[hub.docker.com/r/johnnoel](https://hub.docker.com/r/johnnoel)

## PHP

[hub.docker.com/r/johnnoel/php](https://hub.docker.com/r/johnnoel/php/tags)

PHP Docker images built on top of the [circleci/php:*-cli](https://hub.docker.com/r/circleci/php) ones to add some commonly used modules as well as some tools used during CI.

`johnnoel/php:7.4-cli`

Adds the `gd` and `pdo_pgsql` modules as well as the [Digital Ocean CLI](https://docs.digitalocean.com/reference/doctl/) and the [Sentry CLI](https://docs.sentry.io/product/cli/).

`johnnoel/php:8.0-cli`

The same as the `7.4-cli` tag but also adds the [`redis` PECL extension](https://github.com/phpredis/phpredis).