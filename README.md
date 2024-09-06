Build the image
`sudo docker build -t xaryna/alpine-apache-php .`

Docker Compose
```
    version: '3'
    services:
      web:
        image: xaryna/alpine-apache-php
        ports:
          - "1880:80"
          - "1443:443"
        volumes:
          - /home/debian/docker/data/app/first-app/app:/htdocs
```
