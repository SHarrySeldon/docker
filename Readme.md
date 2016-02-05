
Check it out,


```
docker run --rm     -v /var/run/php70:/var/run -v /var/run/mysqld:/var/run/mysqld -v /var/www:/var/www -v /etc/passwd:/etc/passwd:ro -v /etc/group:/etc/group:ro -v /etc/shadow:/etc/shadow:ro  -it ezbik/php7:0.01 bash  
```


then :
```
php-fpm7.0 -F -O
```

Or create forever:

```
docker stop php70;  docker rm php70 ; docker create  --name php70   -v /var/run/php70:/var/run -v /var/run/mysqld:/var/run/mysqld -v /var/www:/var/www -v /etc/passwd:/etc/passwd:ro -v /etc/group:/etc/group:ro -v /etc/shadow:/etc/shadow:ro ezbik/php7:latest  
docker  start php70
```


