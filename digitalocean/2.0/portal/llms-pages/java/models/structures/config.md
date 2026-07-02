# Config

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkNvbmZpZw

*This model accepts additional fields of type Object.*


# Class Name

`Config`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `BackupHour` | `Integer` | Optional | The hour of day (in UTC) when backup for the service starts. New backup only starts if previous backup has already completed.<br><br>**Constraints**: `>= 0`, `<= 23` | Integer getBackupHour() | setBackupHour(Integer backupHour) |
| `BackupMinute` | `Integer` | Optional | The minute of the backup hour when backup for the service starts. New backup  only starts if previous backup has already completed.<br><br>**Constraints**: `>= 0`, `<= 59` | Integer getBackupMinute() | setBackupMinute(Integer backupMinute) |
| `BinlogRetentionPeriod` | `Double` | Optional | The minimum amount of time, in seconds, to keep binlog entries before deletion.  This may be extended for services that require binlog entries for longer than the default, for example if using the MySQL Debezium Kafka connector.<br><br>**Constraints**: `>= 600`, `<= 86400` | Double getBinlogRetentionPeriod() | setBinlogRetentionPeriod(Double binlogRetentionPeriod) |
| `ConnectTimeout` | `Integer` | Optional | The number of seconds that the mysqld server waits for a connect packet before responding with bad handshake.<br><br>**Constraints**: `>= 2`, `<= 3600` | Integer getConnectTimeout() | setConnectTimeout(Integer connectTimeout) |
| `DefaultTimeZone` | `String` | Optional | Default server time zone, in the form of an offset from UTC (from -12:00 to +12:00), a time zone name (EST), or 'SYSTEM' to use the MySQL server default.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `100` | String getDefaultTimeZone() | setDefaultTimeZone(String defaultTimeZone) |
| `GroupConcatMaxLen` | `Integer` | Optional | The maximum permitted result length, in bytes, for the GROUP_CONCAT() function.<br><br>**Constraints**: `>= 4`, `<= 1.8446744073709552E+19` | Integer getGroupConcatMaxLen() | setGroupConcatMaxLen(Integer groupConcatMaxLen) |
| `InformationSchemaStatsExpiry` | `Integer` | Optional | The time, in seconds, before cached statistics expire.<br><br>**Constraints**: `>= 900`, `<= 31536000` | Integer getInformationSchemaStatsExpiry() | setInformationSchemaStatsExpiry(Integer informationSchemaStatsExpiry) |
| `InnodbFtMinTokenSize` | `Integer` | Optional | The minimum length of words that an InnoDB FULLTEXT index stores.<br><br>**Constraints**: `>= 0`, `<= 16` | Integer getInnodbFtMinTokenSize() | setInnodbFtMinTokenSize(Integer innodbFtMinTokenSize) |
| `InnodbFtServerStopwordTable` | `String` | Optional | The InnoDB FULLTEXT index stopword list for all InnoDB tables.<br><br>**Constraints**: *Maximum Length*: `1024`, *Pattern*: `^.+/.+$` | String getInnodbFtServerStopwordTable() | setInnodbFtServerStopwordTable(String innodbFtServerStopwordTable) |
| `InnodbLockWaitTimeout` | `Integer` | Optional | The time, in seconds, that an InnoDB transaction waits for a row lock. before giving up.<br><br>**Constraints**: `>= 1`, `<= 3600` | Integer getInnodbLockWaitTimeout() | setInnodbLockWaitTimeout(Integer innodbLockWaitTimeout) |
| `InnodbLogBufferSize` | `Integer` | Optional | The size of the buffer, in bytes, that InnoDB uses to write to the log files. on disk.<br><br>**Constraints**: `>= 1048576`, `<= 4294967295` | Integer getInnodbLogBufferSize() | setInnodbLogBufferSize(Integer innodbLogBufferSize) |
| `InnodbOnlineAlterLogMaxSize` | `Integer` | Optional | The upper limit, in bytes, of the size of the temporary log files used during online DDL operations for InnoDB tables.<br><br>**Constraints**: `>= 65536`, `<= 1099511627776` | Integer getInnodbOnlineAlterLogMaxSize() | setInnodbOnlineAlterLogMaxSize(Integer innodbOnlineAlterLogMaxSize) |
| `InnodbPrintAllDeadlocks` | `Boolean` | Optional | When enabled, records information about all deadlocks in InnoDB user transactions  in the error log. Disabled by default. | Boolean getInnodbPrintAllDeadlocks() | setInnodbPrintAllDeadlocks(Boolean innodbPrintAllDeadlocks) |
| `InnodbRollbackOnTimeout` | `Boolean` | Optional | When enabled, transaction timeouts cause InnoDB to abort and roll back the entire transaction. | Boolean getInnodbRollbackOnTimeout() | setInnodbRollbackOnTimeout(Boolean innodbRollbackOnTimeout) |
| `InteractiveTimeout` | `Integer` | Optional | The time, in seconds, the server waits for activity on an interactive. connection before closing it.<br><br>**Constraints**: `>= 30`, `<= 604800` | Integer getInteractiveTimeout() | setInteractiveTimeout(Integer interactiveTimeout) |
| `InternalTmpMemStorageEngine` | [`InternalTmpMemStorageEngine`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/internal-tmp-mem-storage-engine.md) | Optional | The storage engine for in-memory internal temporary tables. | InternalTmpMemStorageEngine getInternalTmpMemStorageEngine() | setInternalTmpMemStorageEngine(InternalTmpMemStorageEngine internalTmpMemStorageEngine) |
| `LongQueryTime` | `Double` | Optional | The time, in seconds, for a query to take to execute before  being captured by slow_query_logs. Default is 10 seconds.<br><br>**Constraints**: `>= 0`, `<= 3600` | Double getLongQueryTime() | setLongQueryTime(Double longQueryTime) |
| `MaxAllowedPacket` | `Integer` | Optional | The size of the largest message, in bytes, that can be received by the server. Default is 67108864 (64M).<br><br>**Constraints**: `>= 102400`, `<= 1073741824` | Integer getMaxAllowedPacket() | setMaxAllowedPacket(Integer maxAllowedPacket) |
| `MaxHeapTableSize` | `Integer` | Optional | The maximum size, in bytes, of internal in-memory tables. Also set tmp_table_size. Default is 16777216 (16M)<br><br>**Constraints**: `>= 1048576`, `<= 1073741824` | Integer getMaxHeapTableSize() | setMaxHeapTableSize(Integer maxHeapTableSize) |
| `NetReadTimeout` | `Integer` | Optional | The time, in seconds, to wait for more data from an existing connection. aborting the read.<br><br>**Constraints**: `>= 1`, `<= 3600` | Integer getNetReadTimeout() | setNetReadTimeout(Integer netReadTimeout) |
| `NetWriteTimeout` | `Integer` | Optional | The number of seconds to wait for a block to be written to a connection before aborting the write.<br><br>**Constraints**: `>= 1`, `<= 3600` | Integer getNetWriteTimeout() | setNetWriteTimeout(Integer netWriteTimeout) |
| `SlowQueryLog` | `Boolean` | Optional | When enabled, captures slow queries. When disabled, also truncates the mysql.slow_log table. Default is false. | Boolean getSlowQueryLog() | setSlowQueryLog(Boolean slowQueryLog) |
| `SortBufferSize` | `Integer` | Optional | The sort buffer size, in bytes, for ORDER BY optimization. Default is 262144. (256K).<br><br>**Constraints**: `>= 32768`, `<= 1073741824` | Integer getSortBufferSize() | setSortBufferSize(Integer sortBufferSize) |
| `SqlMode` | `String` | Optional | Global SQL mode. If empty, uses MySQL server defaults. Must only include uppercase alphabetic characters, underscores, and commas.<br><br>**Constraints**: *Maximum Length*: `1024`, *Pattern*: `^[A-Z_]*(,[A-Z_]+)*$` | String getSqlMode() | setSqlMode(String sqlMode) |
| `SqlRequirePrimaryKey` | `Boolean` | Optional | Require primary key to be defined for new tables or old tables modified with ALTER TABLE and fail if missing. It is recommended to always have primary keys because various functionality may break if any large table is missing them. | Boolean getSqlRequirePrimaryKey() | setSqlRequirePrimaryKey(Boolean sqlRequirePrimaryKey) |
| `TmpTableSize` | `Integer` | Optional | The maximum size, in bytes, of internal in-memory tables. Also set max_heap_table_size. Default is 16777216 (16M).<br><br>**Constraints**: `>= 1048576`, `<= 1073741824` | Integer getTmpTableSize() | setTmpTableSize(Integer tmpTableSize) |
| `WaitTimeout` | `Integer` | Optional | The number of seconds the server waits for activity on a noninteractive connection before closing it.<br><br>**Constraints**: `>= 1`, `<= 2147483` | Integer getWaitTimeout() | setWaitTimeout(Integer waitTimeout) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Config;
import com.digitalocean.api.models.InternalTmpMemStorageEngine;
import java.io.IOException;

Config config = new Config.Builder()
    .backupHour(3)
    .backupMinute(30)
    .binlogRetentionPeriod(600D)
    .connectTimeout(10)
    .defaultTimeZone("+03:00")
    .groupConcatMaxLen(1024)
    .informationSchemaStatsExpiry(86400)
    .innodbFtMinTokenSize(3)
    .innodbFtServerStopwordTable("db_name/table_name")
    .innodbLockWaitTimeout(50)
    .innodbLogBufferSize(16777216)
    .innodbOnlineAlterLogMaxSize(134217728)
    .innodbPrintAllDeadlocks(true)
    .innodbRollbackOnTimeout(true)
    .interactiveTimeout(3600)
    .internalTmpMemStorageEngine(InternalTmpMemStorageEngine.TEMPTABLE)
    .longQueryTime(10D)
    .maxAllowedPacket(67108864)
    .maxHeapTableSize(16777216)
    .netReadTimeout(30)
    .netWriteTimeout(30)
    .slowQueryLog(true)
    .sortBufferSize(262144)
    .sqlMode("ANSI,TRADITIONAL")
    .sqlRequirePrimaryKey(true)
    .tmpTableSize(16777216)
    .waitTimeout(28800)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



