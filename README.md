# docker mysql test

```
docker run --name mysql-container -e MYSQL_ROOT_PASSWORD=1234 -e MYSQL_DATABASE=app -e MYSQL_USER=app -e MYSQL_PASSWORD=1234 -d -p 3306:3306 mysql:latest
```
