Job post
==========

Symfony project 3.4
-------------------

# Installation

* Git clone
``` bash
$ git clone https://github.com/kailashkds/employee.git
```
  * **NOTE**
    Before moving further we need to have docker and docker-compose installed on your pc. Kindly Google for it.

## Once docker is install follow the below steps

* **1) Inside the docker folder**
``` bash
$ cd employee/
```

* **2) Build Docker**
``` bash
$ docker-compose build
```

* **3) Start the Docker**
``` bash
$ docker-compose up -d
```

* **4) Install external packaged**
``` bash
$ docker exec -it -u www-data  sf3_php php /usr/local/bin/composer install -d /home/wwwroot/sf3/employee
```

* **5) Generate database schema**
``` bash
$ docker exec -it -u www-data  sf3_php php  /home/wwwroot/sf3/employee/bin/console d:s:u --dump-sql
```

* **6) Create database schema**
``` bash
$ docker exec -it -u www-data  sf3_php php  /home/wwwroot/sf3/employee/bin/console d:s:u --force
```

* **7) Migration Script**
``` bash
$ docker exec -it -u www-data  sf3_php php  /home/wwwroot/sf3/employee/bin/console d:m:m
```
* **8) Docker Stop**
``` bash
$ docker-compose stop
```
