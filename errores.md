# Errores encontrados

1. Error al crear el pod
```
$ podman-compose run --rm certbot certonly --webroot --webroot-path /var/www/certbot/ --dry-run -d lab.rootzilopochtli.com
/usr/lib/python3.12/site-packages/podman_compose.py:2527: RuntimeWarning: coroutine 'create_pods' was never awaited
  create_pods(compose, args)
RuntimeWarning: Enable tracemalloc to get the object allocation traceback
✔ registry.fedoraproject.org/certbot/certbot:latest
Trying to pull registry.fedoraproject.org/certbot/certbot:latest...
Error: initializing source docker://registry.fedoraproject.org/certbot/certbot:latest: reading manifest latest in registry.fedoraproject.org/certbot/certbot: manifest unknown
[acalleja@ragnarok letsencrypt]$ podman-compose run --rm certbot certonly --webroot --webroot-path /var/www/certbot/ --dry-run -d lab.rootzilopochtli.com
/usr/lib/python3.12/site-packages/podman_compose.py:2527: RuntimeWarning: coroutine 'create_pods' was never awaited
  create_pods(compose, args)
RuntimeWarning: Enable tracemalloc to get the object allocation traceback
✔ docker.io/certbot/certbot:latest
Trying to pull docker.io/certbot/certbot:latest...
Getting image source signatures
Copying blob c5689dbd1d47 done   |
Copying blob 619be1103602 done   |
Copying blob 383b91a8cb02 done   |
Copying blob 36988be9c68b done   |
Copying blob 0a1b729cd1ef done   |
Copying blob 9971f899ed93 done   |
Copying blob 944f770d6d34 done   |
Copying blob f3453e0fd1b7 done   |
Copying blob d83784b099c6 done   |
Copying blob affc648adbf9 done   |
Copying blob ae5323999d87 done   |
Copying blob 2cbac784a86e done   |
Copying config a909abdebd done   |
Writing manifest to image destination
Error: no pod with name or ID pod_letsencrypt found: no such pod  ← FIX!!
```
