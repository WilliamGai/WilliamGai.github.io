估算批处理限制
```
mysql> show VARIABLES like '%max_allowed_packet%';
+--------------------------+------------+
| Variable_name            | Value      |
+--------------------------+------------+
| max_allowed_packet       | 1024       |
| slave_max_allowed_packet | 1073741824 |
+--------------------------+------------+
```
