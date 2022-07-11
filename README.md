# hta-db-schema

Document DB Schema for Oracle/Mysql (using hta script)

This is a simple hta script to show/document oracle tables/views. 

* For Oracle, it use OLEDB (driver=MSDAORA)
* For MySql, it use ODBC for mysql

no more dependance.

![](hta-db-schema-oracle.jpg)

## Features

1. single hta scripting file
2. no dependance without any css/js lib
3. document oracle/mysql using built-in "comments" feature.
4. classify tables/views into "folder"
4. show/edit/print table summary (for classified table/view only)
5. show/edit/print table definition 

## Usage Guide

just download file [db-schema-oracle.hta](srouce\db-schema-oracle.hta) 
or [db-schema-mysql.hta](srouce\db-schema-mysql.hta) to local, and click to run.

![](hta-db-schema-login.jpg)

1. input the oracle database connection parametes, and click "connect" button
1. by default, tables/views will show in folder of "TABLE/VIEW" in grey color
1. click on folder to toggle table list
1. click on table to show table definition
1. DoubleClick on table description to edit (and setup folder)
1. DoubleClick on column description to edit (ps: for oracle only!)
1. Click "print" button to print table definition
1. input keyword and press enter (or click on "search" button) to search name+comments

You may edit below script (bottom of file, line 262) to setup the default DB connection.

~~~
  //===== initial db connection parameters =====
  app('dbtitle').value = 'Database Schema of Oracle DB'
  app('dbserver').value = '192.168.0.211'
  app('dbname').value = 'XE'
  app('dbuser').value = 'hr'
  app('dbpass').value = 'password'
  //app.connectdb()
  //===== end of db parameters ====================
~~~  

For MySql, 

{{
  //===== initial db connection parameters =====
  app('dbtitle').value = 'Database Schema of MySql'
  app('dbodbc').value = 'mysqlDSN'
  //app.connectdb()
  //===== end of db parameters ====================
}}


## Modification Log

* 2022/07/06, v0.70, initial version, for oracle DB
* 2022/07/11, v0.80, add mysql version
