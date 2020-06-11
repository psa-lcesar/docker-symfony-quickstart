
# How to

## Install

```bash
docker-compose -f etc/docker/docker-compose.yml up -d 
docker exec -ti docker_app_1 /bin/bash -c "cd app && composer update"
docker exec -ti docker_app_1 /bin/bash -c "cd app && php bin/console cache:clear --env=prod && php bin/console cache:clear --env=dev"
```

-----

## Clear symfony cache

```bash
docker exec -ti docker_app_1 /bin/bash -c "cd app && php bin/console cache:clear --env=prod && php bin/console cache:clear --env=dev"
```

-----

## See logs

```bash
docker logs -f docker_app_1 
```

-----

## Find docker container name

If `docker_app_1` dosen't exist find the good symfony container name with `docker ps`

```bash
docker ps
```

-----

# ressources

## Docker images

- bitnami/symfony:1
- bitnami/mariadb:10.3

## Symfony

- [https://symfony.com/doc/current/index.html](https://symfony.com/doc/current/index.html)
