# Config

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNvbmZpZw

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Config`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `BackupHour` | `int?` | Optional | The hour of day (in UTC) when backup for the service starts. New backup only starts if previous backup has already completed.<br><br>**Constraints**: `>= 0`, `<= 23` |
| `BackupMinute` | `int?` | Optional | The minute of the backup hour when backup for the service starts. New backup  only starts if previous backup has already completed.<br><br>**Constraints**: `>= 0`, `<= 59` |
| `BinlogRetentionPeriod` | `double?` | Optional | The minimum amount of time, in seconds, to keep binlog entries before deletion.  This may be extended for services that require binlog entries for longer than the default, for example if using the MySQL Debezium Kafka connector.<br><br>**Constraints**: `>= 600`, `<= 86400` |
| `ConnectTimeout` | `int?` | Optional | The number of seconds that the mysqld server waits for a connect packet before responding with bad handshake.<br><br>**Constraints**: `>= 2`, `<= 3600` |
| `DefaultTimeZone` | `string` | Optional | Default server time zone, in the form of an offset from UTC (from -12:00 to +12:00), a time zone name (EST), or 'SYSTEM' to use the MySQL server default.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `100` |
| `GroupConcatMaxLen` | `int?` | Optional | The maximum permitted result length, in bytes, for the GROUP_CONCAT() function.<br><br>**Constraints**: `>= 4`, `<= 1.8446744073709552E+19` |
| `InformationSchemaStatsExpiry` | `int?` | Optional | The time, in seconds, before cached statistics expire.<br><br>**Constraints**: `>= 900`, `<= 31536000` |
| `InnodbFtMinTokenSize` | `int?` | Optional | The minimum length of words that an InnoDB FULLTEXT index stores.<br><br>**Constraints**: `>= 0`, `<= 16` |
| `InnodbFtServerStopwordTable` | `string` | Optional | The InnoDB FULLTEXT index stopword list for all InnoDB tables.<br><br>**Constraints**: *Maximum Length*: `1024`, *Pattern*: `^.+/.+$` |
| `InnodbLockWaitTimeout` | `int?` | Optional | The time, in seconds, that an InnoDB transaction waits for a row lock. before giving up.<br><br>**Constraints**: `>= 1`, `<= 3600` |
| `InnodbLogBufferSize` | `int?` | Optional | The size of the buffer, in bytes, that InnoDB uses to write to the log files. on disk.<br><br>**Constraints**: `>= 1048576`, `<= 4294967295` |
| `InnodbOnlineAlterLogMaxSize` | `int?` | Optional | The upper limit, in bytes, of the size of the temporary log files used during online DDL operations for InnoDB tables.<br><br>**Constraints**: `>= 65536`, `<= 1099511627776` |
| `InnodbPrintAllDeadlocks` | `bool?` | Optional | When enabled, records information about all deadlocks in InnoDB user transactions  in the error log. Disabled by default. |
| `InnodbRollbackOnTimeout` | `bool?` | Optional | When enabled, transaction timeouts cause InnoDB to abort and roll back the entire transaction. |
| `InteractiveTimeout` | `int?` | Optional | The time, in seconds, the server waits for activity on an interactive. connection before closing it.<br><br>**Constraints**: `>= 30`, `<= 604800` |
| `InternalTmpMemStorageEngine` | [`InternalTmpMemStorageEngine?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/internal-tmp-mem-storage-engine.md) | Optional | The storage engine for in-memory internal temporary tables. |
| `LongQueryTime` | `double?` | Optional | The time, in seconds, for a query to take to execute before  being captured by slow_query_logs. Default is 10 seconds.<br><br>**Constraints**: `>= 0`, `<= 3600` |
| `MaxAllowedPacket` | `int?` | Optional | The size of the largest message, in bytes, that can be received by the server. Default is 67108864 (64M).<br><br>**Constraints**: `>= 102400`, `<= 1073741824` |
| `MaxHeapTableSize` | `int?` | Optional | The maximum size, in bytes, of internal in-memory tables. Also set tmp_table_size. Default is 16777216 (16M)<br><br>**Constraints**: `>= 1048576`, `<= 1073741824` |
| `NetReadTimeout` | `int?` | Optional | The time, in seconds, to wait for more data from an existing connection. aborting the read.<br><br>**Constraints**: `>= 1`, `<= 3600` |
| `NetWriteTimeout` | `int?` | Optional | The number of seconds to wait for a block to be written to a connection before aborting the write.<br><br>**Constraints**: `>= 1`, `<= 3600` |
| `SlowQueryLog` | `bool?` | Optional | When enabled, captures slow queries. When disabled, also truncates the mysql.slow_log table. Default is false. |
| `SortBufferSize` | `int?` | Optional | The sort buffer size, in bytes, for ORDER BY optimization. Default is 262144. (256K).<br><br>**Constraints**: `>= 32768`, `<= 1073741824` |
| `SqlMode` | `string` | Optional | Global SQL mode. If empty, uses MySQL server defaults. Must only include uppercase alphabetic characters, underscores, and commas.<br><br>**Constraints**: *Maximum Length*: `1024`, *Pattern*: `^[A-Z_]*(,[A-Z_]+)*$` |
| `SqlRequirePrimaryKey` | `bool?` | Optional | Require primary key to be defined for new tables or old tables modified with ALTER TABLE and fail if missing. It is recommended to always have primary keys because various functionality may break if any large table is missing them. |
| `TmpTableSize` | `int?` | Optional | The maximum size, in bytes, of internal in-memory tables. Also set max_heap_table_size. Default is 16777216 (16M).<br><br>**Constraints**: `>= 1048576`, `<= 1073741824` |
| `WaitTimeout` | `int?` | Optional | The number of seconds the server waits for activity on a noninteractive connection before closing it.<br><br>**Constraints**: `>= 1`, `<= 2147483` |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Config config = new Config
{
    BackupHour = 3,
    BackupMinute = 30,
    BinlogRetentionPeriod = 600,
    ConnectTimeout = 10,
    DefaultTimeZone = "+03:00",
    GroupConcatMaxLen = 1024,
    InformationSchemaStatsExpiry = 86400,
    InnodbFtMinTokenSize = 3,
    InnodbFtServerStopwordTable = "db_name/table_name",
    InnodbLockWaitTimeout = 50,
    InnodbLogBufferSize = 16777216,
    InnodbOnlineAlterLogMaxSize = 134217728,
    InnodbPrintAllDeadlocks = true,
    InnodbRollbackOnTimeout = true,
    InteractiveTimeout = 3600,
    InternalTmpMemStorageEngine = InternalTmpMemStorageEngine.TempTable,
    LongQueryTime = 10,
    MaxAllowedPacket = 67108864,
    MaxHeapTableSize = 16777216,
    NetReadTimeout = 30,
    NetWriteTimeout = 30,
    SlowQueryLog = true,
    SortBufferSize = 262144,
    SqlMode = "ANSI,TRADITIONAL",
    SqlRequirePrimaryKey = true,
    TmpTableSize = 16777216,
    WaitTimeout = 28800,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



