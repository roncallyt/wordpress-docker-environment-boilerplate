# wordpress-docker-environment-boilerplate
Wordpress Docker Environment Boilerplate

## Clone this repository

```bash
git clone https://github.com/roncallyt/wordpress-docker-environment-boilerplate.git
```

## Enter in directory and create **.env** from example

```bash
cp .docker/.env.example .docker/.env
```

## Fill the environment variables

```text
# Project
COMPOSE_PROJECT_NAME=

# Nginx
NGINX_PORT=
NGINX_ALIAS=

# Database
MYSQL_DATABASE=
MYSQL_ROOT_PASSWORD=
MYSQL_PORT=
```

The alias defined in this file MUST be addicted to hosts file in your machine.

## Build the images

```bash
./develop build --no-cache
```

## Turn up the containers

To run in foreground:
```bash
./develop up
```

To run in background:
```bash
./develop up -d
```

## Turn down the containers

```bash
./develop stop
```

## To destroy the containers

Without destroy volumes:
```bash
./develop down
```

Destroing volumes:
```bash
./develop down -v
```
