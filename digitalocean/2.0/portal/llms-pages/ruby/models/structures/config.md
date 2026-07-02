# Config

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkNvbmZpZw

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Config`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `backup_hour` | `Integer` | Optional | The hour of day (in UTC) when backup for the service starts. New backup only starts if previous backup has already completed.<br><br>**Constraints**: `>= 0`, `<= 23` |
| `backup_minute` | `Integer` | Optional | The minute of the backup hour when backup for the service starts. New backup  only starts if previous backup has already completed.<br><br>**Constraints**: `>= 0`, `<= 59` |
| `binlog_retention_period` | `Float` | Optional | The minimum amount of time, in seconds, to keep binlog entries before deletion.  This may be extended for services that require binlog entries for longer than the default, for example if using the MySQL Debezium Kafka connector.<br><br>**Constraints**: `>= 600`, `<= 86400` |
| `connect_timeout` | `Integer` | Optional | The number of seconds that the mysqld server waits for a connect packet before responding with bad handshake.<br><br>**Constraints**: `>= 2`, `<= 3600` |
| `default_time_zone` | `String` | Optional | Default server time zone, in the form of an offset from UTC (from -12:00 to +12:00), a time zone name (EST), or 'SYSTEM' to use the MySQL server default.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `100` |
| `group_concat_max_len` | `Integer` | Optional | The maximum permitted result length, in bytes, for the GROUP_CONCAT() function.<br><br>**Constraints**: `>= 4`, `<= 1.8446744073709552E+19` |
| `information_schema_stats_expiry` | `Integer` | Optional | The time, in seconds, before cached statistics expire.<br><br>**Constraints**: `>= 900`, `<= 31536000` |
| `innodb_ft_min_token_size` | `Integer` | Optional | The minimum length of words that an InnoDB FULLTEXT index stores.<br><br>**Constraints**: `>= 0`, `<= 16` |
| `innodb_ft_server_stopword_table` | `String` | Optional | The InnoDB FULLTEXT index stopword list for all InnoDB tables.<br><br>**Constraints**: *Maximum Length*: `1024`, *Pattern*: `^.+/.+$` |
| `innodb_lock_wait_timeout` | `Integer` | Optional | The time, in seconds, that an InnoDB transaction waits for a row lock. before giving up.<br><br>**Constraints**: `>= 1`, `<= 3600` |
| `innodb_log_buffer_size` | `Integer` | Optional | The size of the buffer, in bytes, that InnoDB uses to write to the log files. on disk.<br><br>**Constraints**: `>= 1048576`, `<= 4294967295` |
| `innodb_online_alter_log_max_size` | `Integer` | Optional | The upper limit, in bytes, of the size of the temporary log files used during online DDL operations for InnoDB tables.<br><br>**Constraints**: `>= 65536`, `<= 1099511627776` |
| `innodb_print_all_deadlocks` | `TrueClass \| FalseClass` | Optional | When enabled, records information about all deadlocks in InnoDB user transactions  in the error log. Disabled by default. |
| `innodb_rollback_on_timeout` | `TrueClass \| FalseClass` | Optional | When enabled, transaction timeouts cause InnoDB to abort and roll back the entire transaction. |
| `interactive_timeout` | `Integer` | Optional | The time, in seconds, the server waits for activity on an interactive. connection before closing it.<br><br>**Constraints**: `>= 30`, `<= 604800` |
| `internal_tmp_mem_storage_engine` | [`InternalTmpMemStorageEngine`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/internal-tmp-mem-storage-engine.md) | Optional | The storage engine for in-memory internal temporary tables. |
| `long_query_time` | `Float` | Optional | The time, in seconds, for a query to take to execute before  being captured by slow_query_logs. Default is 10 seconds.<br><br>**Constraints**: `>= 0`, `<= 3600` |
| `max_allowed_packet` | `Integer` | Optional | The size of the largest message, in bytes, that can be received by the server. Default is 67108864 (64M).<br><br>**Constraints**: `>= 102400`, `<= 1073741824` |
| `max_heap_table_size` | `Integer` | Optional | The maximum size, in bytes, of internal in-memory tables. Also set tmp_table_size. Default is 16777216 (16M)<br><br>**Constraints**: `>= 1048576`, `<= 1073741824` |
| `net_read_timeout` | `Integer` | Optional | The time, in seconds, to wait for more data from an existing connection. aborting the read.<br><br>**Constraints**: `>= 1`, `<= 3600` |
| `net_write_timeout` | `Integer` | Optional | The number of seconds to wait for a block to be written to a connection before aborting the write.<br><br>**Constraints**: `>= 1`, `<= 3600` |
| `slow_query_log` | `TrueClass \| FalseClass` | Optional | When enabled, captures slow queries. When disabled, also truncates the mysql.slow_log table. Default is false. |
| `sort_buffer_size` | `Integer` | Optional | The sort buffer size, in bytes, for ORDER BY optimization. Default is 262144. (256K).<br><br>**Constraints**: `>= 32768`, `<= 1073741824` |
| `sql_mode` | `String` | Optional | Global SQL mode. If empty, uses MySQL server defaults. Must only include uppercase alphabetic characters, underscores, and commas.<br><br>**Constraints**: *Maximum Length*: `1024`, *Pattern*: `^[A-Z_]*(,[A-Z_]+)*$` |
| `sql_require_primary_key` | `TrueClass \| FalseClass` | Optional | Require primary key to be defined for new tables or old tables modified with ALTER TABLE and fail if missing. It is recommended to always have primary keys because various functionality may break if any large table is missing them. |
| `tmp_table_size` | `Integer` | Optional | The maximum size, in bytes, of internal in-memory tables. Also set max_heap_table_size. Default is 16777216 (16M).<br><br>**Constraints**: `>= 1048576`, `<= 1073741824` |
| `wait_timeout` | `Integer` | Optional | The number of seconds the server waits for activity on a noninteractive connection before closing it.<br><br>**Constraints**: `>= 1`, `<= 2147483` |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
config = Config.new(
  backup_hour: 3,
  backup_minute: 30,
  binlog_retention_period: 600,
  connect_timeout: 10,
  default_time_zone: '+03:00',
  group_concat_max_len: 1024,
  information_schema_stats_expiry: 86400,
  innodb_ft_min_token_size: 3,
  innodb_ft_server_stopword_table: 'db_name/table_name',
  innodb_lock_wait_timeout: 50,
  innodb_log_buffer_size: 16777216,
  innodb_online_alter_log_max_size: 134217728,
  innodb_print_all_deadlocks: true,
  innodb_rollback_on_timeout: true,
  interactive_timeout: 3600,
  internal_tmp_mem_storage_engine: InternalTmpMemStorageEngine::TEMPTABLE,
  long_query_time: 10,
  max_allowed_packet: 67108864,
  max_heap_table_size: 16777216,
  net_read_timeout: 30,
  net_write_timeout: 30,
  slow_query_log: true,
  sort_buffer_size: 262144,
  sql_mode: 'ANSI,TRADITIONAL',
  sql_require_primary_key: true,
  tmp_table_size: 16777216,
  wait_timeout: 28800,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



