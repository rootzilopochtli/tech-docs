# Configurando un webserver con letsencrypt en Podman

## Pasos

1. Creando directorio de trabajo:
```
$ mkdir -p proyecto/letsencrypt
$ cd proyecto/letsencrypt
```
2. Crear archivo `docker-compose.yml`
```
$ vi docker-compose.yml
```
Contenido de archivo `docker-compose.yml`
```
version: '3'
services:
  webserver:
    image: nginx:latest
    ports:
      - 8080:8080
      - 8443:8443
    restart: always
    volumes:
      - ./nginx/conf/:/etc/nginx/conf.d/:ro
      - ./certbot/www/:/var/www/certbot/:ro
  certbot:
    image: certbot/certbot:latest
    volumes:
      - ./certbot/www/:/var/www/certbot/:rw
      - ./certbot/conf/:/etc/letsencrypt/:rw
```
