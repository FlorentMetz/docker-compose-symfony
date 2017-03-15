### Docker Compose Symfony 3.2

This repository includes:

- [redis:latest](https://hub.docker.com/_/redis/)
- [mysql:5.7](https://hub.docker.com/_/mysql/)
- [PHP:7](https://hub.docker.com/_/php/)
- [nginx:latest](https://hub.docker.com/_/nginx/)

### Setup

Install [docker-compose](https://docs.docker.com/compose/install/) on your machine, then run:

```
docker-compose build --pull

docker-composer up -d
```

The 2 above commands will pull the right docker images, create the containers from them and run them in a detached process.

```
docker logs -f php|nginx
```

to look up the logs.

The nginx [vhost](nginx/vhost.conf) is setup to use [sf-app.local:8080](http://sf-app.local:8080) so don't forget to update your `/etc/hosts` to include

```
127.0.0.1 sf-app.local
```

and hit that up on your browser to see the default Symfony page!
