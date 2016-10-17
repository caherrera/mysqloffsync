# mysqloffsync
Mysql/MariaDB tool for re-sync, copy and upgrate databases from one server to another.

## Requirements
[mysql](http://www.mysql.com/)

## Before start to use
1. Add with mysql_config_editor all your --login-path, source and destination
1. make sure you have a default mysql client configuration in ~/.my.cnf
1. have manual backups of your database.

## Installation
```
git clone git@github.com:caherrera/mysqloffsync.git ~/mysqloffsync
cd ~/mysqloffsync && sudo ./install.sh
```

## Usage
```
mysqloffsync -?
```


## Copy all tables (default)
```
mysqloffsync
```

## copy views|routines|functions
```
mysqloffsync v|r|f
```

## copy some views
```
mysqloffsync v view_prefix_% v_list1 v_list2
```


