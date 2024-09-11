Build the image
`sudo docker build -t xaryna/alpine-apache-php-mariadb .`

Docker Compose
```
    version: '3'
    services:
      web:
        image: xaryna/alpine-apache-php-mariadb
        restart: always
        ports:
          - "1880:80"
         # - "1443:443"
        volumes:
          - /home/debian/docker/data/app/first-app/app:/htdocs
          - /home/debian/docker/data/app/first-app/data:/var/lib/mysql
          - /home/debian/docker/data/app/first-app/logs:/var/lib/mysql/mysql-bin
        environment:
          SERVER_ADMIN: test@localhost.me
          SERVER_NAME: localhost
          # MYSQL_ROOT_PASSWORD: 
          # MYSQL_DATABASE: 
          # MYSQL_USER: 
          # MYSQL_PASSWORD: 
          # MYSQL_CHARSET: 
          # MYSQL_COLLATION: 
```
