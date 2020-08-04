![License MIT](https://img.shields.io/badge/license-MIT-blue.svg)

# MODX-DOCKER

modx-docker sets up a container running nginx, mysql and modx. The container will expose port 80 and you will require a running nginx-proxy container to forward request to the MODX container.
Please see NGINX-PROXY section to start your nginx-proxy container.


### PHP-open-redirect Usage

```Dockerfile
docker build  https://github.com/ankh2054/php-open-redirect.git  -t php-open-redirect 
```

To run it:

```Dockerfile
docker run  --name php-open-redirect --expose 80 \
-d -e 'VIRTUAL_HOST=avatar.sentnl.io' \
-e "LETSENCRYPT_HOST=avatar.sentnl.io" \
-e "LETSENCRYPT_EMAIL=charles.holtzkampf@gmail.com" \
php-open-redirect 
```

