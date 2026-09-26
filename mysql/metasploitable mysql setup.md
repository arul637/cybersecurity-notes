```bash
mysql --ssl-mode=DISABLED --host 192.168.1.3 --user root --password
```

- `--host` target host
- `--user` username
- `--password` ask password 
- `--ssl-mode` need to disable the ssl for mysql connection 

```bash
mysql --skip-ssl --host 192.168.1.3 --user root --password 
```

### creating the testing user 

```bash
CREATE USER 'msfadmin'@'%' IDENTIFIED BY 'msfadmin';
GRANT ALL PRIVILEGES ON *.* TO 'msfadmin'@'%' WITH GRANT OPTION;
FLUSH PRIVILEGES;
```

create the user named `msfadmin` with password `msfadmin`, grant all privilege to that created user 

flush privileges will reload the cache, so then there is no the authentication error will occur 

```
administrator@administrator:~$ mysql --ssl-mode=DISABLED --host 192.168.1.3 --user root --password
Enter password: 
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 15
Server version: 5.0.51a-3ubuntu5 (Ubuntu)

Copyright (c) 2000, 2026, Oracle and/or its affiliates.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> CREATE USER 'msfadmin'@'%' IDENTIFIED BY 'msfadmin';
Query OK, 0 rows affected (0.00 sec)

mysql> GRANT ALL PRIVILEGES ON *.* TO 'msfadmin'@'%' WITH GRANT OPTION;
Query OK, 0 rows affected (0.00 sec)

mysql> FLUSH PRIVILEGES;
Query OK, 0 rows affected (0.01 sec)

mysql> 
```

