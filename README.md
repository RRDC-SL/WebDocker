# WebDocker for RRDC

This docker contain a LAMP stack installed from scratch for RRDC

### Run you own image

```  
git clone https://github.com/RRDC-SL/WebDocker && cd WebDocker/
```

### Build the image
```
docker build -t $USER/WebDocker .
```

### Run it
Note dest:source on ports
```
docker run -d -v /path/to/project:/var/www/localhost/htdocs/ -e MYSQL_ROOT_PASSWORD=password -p 8000:80 -p 13306:3306 --name RRDC-HTTP $USER/WebDocker
```

### Connect to MariaDB
To use this you need to install mysql/mariadb cli client
```
mysql -uroot -ppassword -h 127.0.0.1
```

## Troubleshooting

### Forbidden error 403 
```
sudo chmod -Rf 755 /path/to/project
``` 

## Repos
https://github.com/RRDC-SL/WebDocker
