# Docker-Wordpress-MySQL-Xdebug-Template

Simple Docker setup for WordPress Theme development.

* wordpress:php7.1-apache Docker image (latest WP, development only) with
* Xdebug on top (configure your IP in docker-compose.yaml *{{ip-of-machine-running-debug}}*)
* MySQL 5.7 (consistent data mounted from .data/data_db)

First run
``docker-compose up``

## Docker for Mac

Browse [http://localhost:8000/](http://localhost:8000/)

Connect to MySQL at 127.0.0.1:3306

## Visual Studio Code – launch.json example
```
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Listen for XDebug",
            "type": "php",
            "request": "launch",
            "pathMappings": {
                "/var/www/html/wp-content/themes/my-theme": "${workspaceRoot}/my-theme"
            },
            "port": 9000
        }
    ]
}
```
