# docker_laravel
Setup PHP Laravel into Docker with NGINX and MariaDB/MySQL

Edit ``.env`` 

```
DB_HOST=db
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=root
```
After run command

```
docker-compose up -d
docker-compose exec app php artisan key:generate
docker-compose exec app php artisan config:cache
docker-compose exec app php artisan migrate
```
