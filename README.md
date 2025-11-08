# CLOUD_WORDPRESS

##CODIGO
```
services:
  db:
    image: mariadb:11
    environment:
      - MYSQL_ROOT_PASSWORD=12345
      - MYSQL_DATABASE=wordpress
      - MYSQL_USER=wordpress
      - MYSQL_PASSWORD=wordpress123
    volumes:
      - wp_db:/var/lib/mysql
    restart: unless-stopped
  wordpress:
    image: wordpress:6-apache
      - WORDPRESS_MYSQL_TYPE= mysql
      - WORDPRESS_MYSQL_DB_NAME=wordpress
      - WORDPRESS_MYSQL_USER=wordpress
      - WORDPRESS_MYSQL_PASSWORD=wordpress123
      - WORDPRESS_MYSQL_HOST=db
      - WORDPRESS_ADMIN_USERNAME=admin
      - WORDPRESS_ADMIN_PASSWORD=admin123
      - WORDPRESS_DOMAIN=localhost
    ports:
    environment:
    volumes:
      - wp_files:/mnt/data
    restart: unless-stopped
volumes:
  wp_db:
  wp_files:

```


##EVIDENCIAS
