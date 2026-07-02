# Config

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkNvbmZpZw

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Config`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `backupHour` | `?int` | Optional | The hour of day (in UTC) when backup for the service starts. New backup only starts if previous backup has already completed.<br><br>**Constraints**: `>= 0`, `<= 23` | getBackupHour(): ?int | setBackupHour(?int backupHour): void |
| `backupMinute` | `?int` | Optional | The minute of the backup hour when backup for the service starts. New backup  only starts if previous backup has already completed.<br><br>**Constraints**: `>= 0`, `<= 59` | getBackupMinute(): ?int | setBackupMinute(?int backupMinute): void |
| `binlogRetentionPeriod` | `?float` | Optional | The minimum amount of time, in seconds, to keep binlog entries before deletion.  This may be extended for services that require binlog entries for longer than the default, for example if using the MySQL Debezium Kafka connector.<br><br>**Constraints**: `>= 600`, `<= 86400` | getBinlogRetentionPeriod(): ?float | setBinlogRetentionPeriod(?float binlogRetentionPeriod): void |
| `connectTimeout` | `?int` | Optional | The number of seconds that the mysqld server waits for a connect packet before responding with bad handshake.<br><br>**Constraints**: `>= 2`, `<= 3600` | getConnectTimeout(): ?int | setConnectTimeout(?int connectTimeout): void |
| `defaultTimeZone` | `?string` | Optional | Default server time zone, in the form of an offset from UTC (from -12:00 to +12:00), a time zone name (EST), or 'SYSTEM' to use the MySQL server default.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `100` | getDefaultTimeZone(): ?string | setDefaultTimeZone(?string defaultTimeZone): void |
| `groupConcatMaxLen` | `?int` | Optional | The maximum permitted result length, in bytes, for the GROUP_CONCAT() function.<br><br>**Constraints**: `>= 4`, `<= 1.8446744073709552E+19` | getGroupConcatMaxLen(): ?int | setGroupConcatMaxLen(?int groupConcatMaxLen): void |
| `informationSchemaStatsExpiry` | `?int` | Optional | The time, in seconds, before cached statistics expire.<br><br>**Constraints**: `>= 900`, `<= 31536000` | getInformationSchemaStatsExpiry(): ?int | setInformationSchemaStatsExpiry(?int informationSchemaStatsExpiry): void |
| `innodbFtMinTokenSize` | `?int` | Optional | The minimum length of words that an InnoDB FULLTEXT index stores.<br><br>**Constraints**: `>= 0`, `<= 16` | getInnodbFtMinTokenSize(): ?int | setInnodbFtMinTokenSize(?int innodbFtMinTokenSize): void |
| `innodbFtServerStopwordTable` | `?string` | Optional | The InnoDB FULLTEXT index stopword list for all InnoDB tables.<br><br>**Constraints**: *Maximum Length*: `1024`, *Pattern*: `^.+/.+$` | getInnodbFtServerStopwordTable(): ?string | setInnodbFtServerStopwordTable(?string innodbFtServerStopwordTable): void |
| `innodbLockWaitTimeout` | `?int` | Optional | The time, in seconds, that an InnoDB transaction waits for a row lock. before giving up.<br><br>**Constraints**: `>= 1`, `<= 3600` | getInnodbLockWaitTimeout(): ?int | setInnodbLockWaitTimeout(?int innodbLockWaitTimeout): void |
| `innodbLogBufferSize` | `?int` | Optional | The size of the buffer, in bytes, that InnoDB uses to write to the log files. on disk.<br><br>**Constraints**: `>= 1048576`, `<= 4294967295` | getInnodbLogBufferSize(): ?int | setInnodbLogBufferSize(?int innodbLogBufferSize): void |
| `innodbOnlineAlterLogMaxSize` | `?int` | Optional | The upper limit, in bytes, of the size of the temporary log files used during online DDL operations for InnoDB tables.<br><br>**Constraints**: `>= 65536`, `<= 1099511627776` | getInnodbOnlineAlterLogMaxSize(): ?int | setInnodbOnlineAlterLogMaxSize(?int innodbOnlineAlterLogMaxSize): void |
| `innodbPrintAllDeadlocks` | `?bool` | Optional | When enabled, records information about all deadlocks in InnoDB user transactions  in the error log. Disabled by default. | getInnodbPrintAllDeadlocks(): ?bool | setInnodbPrintAllDeadlocks(?bool innodbPrintAllDeadlocks): void |
| `innodbRollbackOnTimeout` | `?bool` | Optional | When enabled, transaction timeouts cause InnoDB to abort and roll back the entire transaction. | getInnodbRollbackOnTimeout(): ?bool | setInnodbRollbackOnTimeout(?bool innodbRollbackOnTimeout): void |
| `interactiveTimeout` | `?int` | Optional | The time, in seconds, the server waits for activity on an interactive. connection before closing it.<br><br>**Constraints**: `>= 30`, `<= 604800` | getInteractiveTimeout(): ?int | setInteractiveTimeout(?int interactiveTimeout): void |
| `internalTmpMemStorageEngine` | [`?string(InternalTmpMemStorageEngine)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/internal-tmp-mem-storage-engine.md) | Optional | The storage engine for in-memory internal temporary tables. | getInternalTmpMemStorageEngine(): ?string | setInternalTmpMemStorageEngine(?string internalTmpMemStorageEngine): void |
| `longQueryTime` | `?float` | Optional | The time, in seconds, for a query to take to execute before  being captured by slow_query_logs. Default is 10 seconds.<br><br>**Constraints**: `>= 0`, `<= 3600` | getLongQueryTime(): ?float | setLongQueryTime(?float longQueryTime): void |
| `maxAllowedPacket` | `?int` | Optional | The size of the largest message, in bytes, that can be received by the server. Default is 67108864 (64M).<br><br>**Constraints**: `>= 102400`, `<= 1073741824` | getMaxAllowedPacket(): ?int | setMaxAllowedPacket(?int maxAllowedPacket): void |
| `maxHeapTableSize` | `?int` | Optional | The maximum size, in bytes, of internal in-memory tables. Also set tmp_table_size. Default is 16777216 (16M)<br><br>**Constraints**: `>= 1048576`, `<= 1073741824` | getMaxHeapTableSize(): ?int | setMaxHeapTableSize(?int maxHeapTableSize): void |
| `netReadTimeout` | `?int` | Optional | The time, in seconds, to wait for more data from an existing connection. aborting the read.<br><br>**Constraints**: `>= 1`, `<= 3600` | getNetReadTimeout(): ?int | setNetReadTimeout(?int netReadTimeout): void |
| `netWriteTimeout` | `?int` | Optional | The number of seconds to wait for a block to be written to a connection before aborting the write.<br><br>**Constraints**: `>= 1`, `<= 3600` | getNetWriteTimeout(): ?int | setNetWriteTimeout(?int netWriteTimeout): void |
| `slowQueryLog` | `?bool` | Optional | When enabled, captures slow queries. When disabled, also truncates the mysql.slow_log table. Default is false. | getSlowQueryLog(): ?bool | setSlowQueryLog(?bool slowQueryLog): void |
| `sortBufferSize` | `?int` | Optional | The sort buffer size, in bytes, for ORDER BY optimization. Default is 262144. (256K).<br><br>**Constraints**: `>= 32768`, `<= 1073741824` | getSortBufferSize(): ?int | setSortBufferSize(?int sortBufferSize): void |
| `sqlMode` | `?string` | Optional | Global SQL mode. If empty, uses MySQL server defaults. Must only include uppercase alphabetic characters, underscores, and commas.<br><br>**Constraints**: *Maximum Length*: `1024`, *Pattern*: `^[A-Z_]*(,[A-Z_]+)*$` | getSqlMode(): ?string | setSqlMode(?string sqlMode): void |
| `sqlRequirePrimaryKey` | `?bool` | Optional | Require primary key to be defined for new tables or old tables modified with ALTER TABLE and fail if missing. It is recommended to always have primary keys because various functionality may break if any large table is missing them. | getSqlRequirePrimaryKey(): ?bool | setSqlRequirePrimaryKey(?bool sqlRequirePrimaryKey): void |
| `tmpTableSize` | `?int` | Optional | The maximum size, in bytes, of internal in-memory tables. Also set max_heap_table_size. Default is 16777216 (16M).<br><br>**Constraints**: `>= 1048576`, `<= 1073741824` | getTmpTableSize(): ?int | setTmpTableSize(?int tmpTableSize): void |
| `waitTimeout` | `?int` | Optional | The number of seconds the server waits for activity on a noninteractive connection before closing it.<br><br>**Constraints**: `>= 1`, `<= 2147483` | getWaitTimeout(): ?int | setWaitTimeout(?int waitTimeout): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\ConfigBuilder;
use DigitalOceanApiLib\Models\InternalTmpMemStorageEngine;
use DigitalOceanApiLib\ApiHelper;

$config = ConfigBuilder::init()
    ->backupHour(3)
    ->backupMinute(30)
    ->binlogRetentionPeriod(600)
    ->connectTimeout(10)
    ->defaultTimeZone('+03:00')
    ->groupConcatMaxLen(1024)
    ->informationSchemaStatsExpiry(86400)
    ->innodbFtMinTokenSize(3)
    ->innodbFtServerStopwordTable('db_name/table_name')
    ->innodbLockWaitTimeout(50)
    ->innodbLogBufferSize(16777216)
    ->innodbOnlineAlterLogMaxSize(134217728)
    ->innodbPrintAllDeadlocks(true)
    ->innodbRollbackOnTimeout(true)
    ->interactiveTimeout(3600)
    ->internalTmpMemStorageEngine(InternalTmpMemStorageEngine::TEMPTABLE)
    ->longQueryTime(10)
    ->maxAllowedPacket(67108864)
    ->maxHeapTableSize(16777216)
    ->netReadTimeout(30)
    ->netWriteTimeout(30)
    ->slowQueryLog(true)
    ->sortBufferSize(262144)
    ->sqlMode('ANSI,TRADITIONAL')
    ->sqlRequirePrimaryKey(true)
    ->tmpTableSize(16777216)
    ->waitTimeout(28800)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



