```
mysql> show variables like 'log_%';
+----------------------------------------+---------------------+
| Variable_name                          | Value               |
+----------------------------------------+---------------------+
| log_bin                                | OFF                 |
| log_bin_basename                       |                     |
| log_bin_index                          |                     |
| log_bin_trust_function_creators        | OFF                 |
| log_bin_use_v1_row_events              | OFF                 |
| log_error                              | /var/log/mysqld.log |
| log_output                             | FILE                |
| log_queries_not_using_indexes          | OFF                 |
| log_slave_updates                      | OFF                 |
| log_slow_admin_statements              | OFF                 |
| log_slow_slave_statements              | OFF                 |
| log_throttle_queries_not_using_indexes | 0                   |
| log_warnings                           | 1                   |
+----------------------------------------+---------------------+
13 rows in set (0.00 sec)
```



设置 /etc/my.cf后
```
mysql> show variables like 'log_%';
+----------------------------------------+--------------------------------+
| Variable_name                          | Value                          |
+----------------------------------------+--------------------------------+
| log_bin                                | ON                             |
| log_bin_basename                       | /var/lib/mysql/mysql-bin       |
| log_bin_index                          | /var/lib/mysql/mysql-bin.index |
| log_bin_trust_function_creators        | OFF                            |
| log_bin_use_v1_row_events              | OFF                            |
| log_error                              | /var/log/mysqld.log            |
| log_output                             | FILE                           |
| log_queries_not_using_indexes          | OFF                            |
| log_slave_updates                      | OFF                            |
| log_slow_admin_statements              | OFF                            |
| log_slow_slave_statements              | OFF                            |
| log_throttle_queries_not_using_indexes | 0                              |
| log_warnings                           | 1                              |
+----------------------------------------+--------------------------------+
13 rows in set (0.00 sec)

mysql> show master status;
+------------------+----------+--------------+------------------+-------------------+
| File             | Position | Binlog_Do_DB | Binlog_Ignore_DB | Executed_Gtid_Set |
+------------------+----------+--------------+------------------+-------------------+
| mysql-bin.000001 |      120 |              |                  |                   |
+------------------+----------+--------------+------------------+-------------------+
1 row in set (0.00 sec)

[root@rabbit1 mysql]# ll
total 176172
-rw-rw---- 1 mysql mysql       56 Jan  8  2017 auto.cnf
drwx------ 2 mysql mysql     4096 Feb 26 17:35 canal_test
drwx------ 2 mysql mysql     4096 Feb 26 17:47 canal_test2
drwx------ 2 mysql mysql     4096 May 19  2017 db_demo
-rw-rw---- 1 mysql mysql 79691776 Feb 26 19:29 ibdata1
-rw-rw---- 1 mysql mysql 50331648 Feb 26 19:29 ib_logfile0
-rw-rw---- 1 mysql mysql 50331648 Jan  8  2017 ib_logfile1
drwx------ 2 mysql mysql     4096 Feb 26 03:16 mysql
-rw-rw---- 1 mysql mysql      120 Feb 26 19:29 mysql-bin.000001
-rw-rw---- 1 mysql mysql       19 Feb 26 19:29 mysql-bin.index
srwxrwxrwx 1 mysql mysql        0 Feb 26 19:29 mysql.sock
drwx------ 2 mysql mysql     4096 Jan  8  2017 performance_schema
drwx------ 2 mysql mysql     4096 Oct 27 10:01 test


```





