# mysqloffsync
Mysql/MariaDB tool for re-sync, copy and upgrate databases from one server to another.

## Requirements
[mysql](http://www.mysql.com/)

## Before start to use
1. Add with mysql_config_editor all your --login-path, source and destination
1. make sure you have a default mysql client configuration in ~/.my.cnf
1. have manual backups of your database.

## Installation

#### Clone this repo
```
$ git clone git@github.com:caherrera/mysqloffsync.git
$ ~/mysqloffsync
```

your execute file will be in 
$ ~/bin/mysqloffsync 



#### By composer
```
$ composer require caherrera/mysqloffsync
```

your execute file will be in 
```
$ ./vendor/bin/mysqloffsync 
```

## First Time

Before to start to use the software you will need to configurate some stuff

1. Setup your login-path in mysql

  ``` 
  $ mysql_config_editor set --login-path=production.server.local --user=db_owner --password

  $ mysql_config_editor set --login-path=dev.server.local --user=db_owner --password
  ```
2. Next set up your mysqloffsync.ini file
  ``` 
  $ mysqloffsync --setup 
  ```

3. And edit your file using your favorite editor

  ```
  vim ~/.mysqloffsync/mysqloffsync.ini 
  ```

## Get some help
```
$ mysqloffsync -?
```

## Usage

## Copy all tables (default)
```
$ mysqloffsync
```

## copy views|routines|functions
```
$ mysqloffsync v|r|f
```

## copy some views
```
$ mysqloffsync v view_prefix_% v_list1 v_list2
```


