http://www.e-agency.co.jp/column/20121220.html

```
$ ./mysqltuner.pl --user root
General recommendations:
    Run OPTIMIZE TABLE to defragment tables for better performance
    Set up a Password for user with the following SQL statement ( SET PASSWORD FOR 'user'@'SpecificDNSorIp' = PASSWORD('secure_password'); )
    Set up a Secure Password for user@host ( SET PASSWORD FOR 'user'@'SpecificDNSorIp' = PASSWORD('secure_password'); )
    Reduce or eliminate unclosed connections and network issues
    When making adjustments, make tmp_table_size/max_heap_table_size equal
    Reduce your SELECT DISTINCT queries which have no LIMIT clause
Variables to adjust:
    query_cache_type (=1)
    tmp_table_size (> 16M)
    max_heap_table_size (> 16M)
    innodb_buffer_pool_size (>= 2G) if possible.
    innodb_buffer_pool_instances(=2)
```

みたいに教えてくれるので、闇雲に設定するより良いかも。
