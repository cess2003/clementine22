# Docker Compose Guide

## What does the `services:` block do?
The `services:` block lists all the containers that make up the application.
In my file there are two: `database` (MariaDB) and `app` (Nextcloud). Each
service defines its image, ports, and environment variables. When I run
`docker-compose up -d`, Compose reads this block and creates and starts
every container in it.

## How did the Nextcloud container find the database?
Compose puts all services on one shared network, and each service name works
as a hostname on it. The app container has `MYSQL_HOST=database`, which
matches the service name `database`. Docker's built-in DNS turns that name
into the database container's IP address, so Nextcloud can connect to it.

## `docker run` vs `docker-compose up -d`
| docker run | docker-compose up -d |
|---|---|
| Starts one container per command | Starts all containers defined in the file |
| Options are typed by hand each time | Configuration is saved in docker-compose.yml |
| Networking must be set up manually | A shared network is created automatically |
| Hard to repeat and share | Repeatable, versionable, shareable (Infrastructure as Code) |
