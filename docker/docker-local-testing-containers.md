Testing mysql Docker [[docker]] container
```
docker run --name mysql8.4 -d -e MYSQL_ROOT_PASSWORD=rootie-mcroot-face -p 13306:3306 -v mysql8-data:/var/lib/mysql mysql:8.4.0
```


#local-dev #docker 