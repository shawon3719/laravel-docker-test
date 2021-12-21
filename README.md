# How to configure with docker

>Make sure you have `docker` and `docker-compose` installed in your machine

Set the following local dns entries in your /etc/hosts file

``` 
127.0.0.1 www.test-app.com
```

>The default password for MySQL is `password` and the username is `root`

## Update your .env

>`host.docker.internal` will be the host address for the database

## Run application
Set executable permission to the `start` file, which is located at the root directory of the project

Run below command to run application
```
./start
```
## List running docker container
```
docker ps
```

## Execute artisan command
```
docker exec -it [CONTAINER_NAME] php artisan [COMMAND]

e.g.
docker exec -it test-app php artisan migrate
```

## Execute composer command
```
docker exec -it [CONTAINER_NAME] composer install

e.g.
docker exec -it test-app composer install
```

> For this app the container name `test-app`