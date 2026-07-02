# Config

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkNvbmZpZw

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Config`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `backupHour` | `number \| undefined` | Optional | The hour of day (in UTC) when backup for the service starts. New backup only starts if previous backup has already completed.<br><br>**Constraints**: `>= 0`, `<= 23` |
| `backupMinute` | `number \| undefined` | Optional | The minute of the backup hour when backup for the service starts. New backup  only starts if previous backup has already completed.<br><br>**Constraints**: `>= 0`, `<= 59` |
| `binlogRetentionPeriod` | `number \| undefined` | Optional | The minimum amount of time, in seconds, to keep binlog entries before deletion.  This may be extended for services that require binlog entries for longer than the default, for example if using the MySQL Debezium Kafka connector.<br><br>**Constraints**: `>= 600`, `<= 86400` |
| `connectTimeout` | `number \| undefined` | Optional | The number of seconds that the mysqld server waits for a connect packet before responding with bad handshake.<br><br>**Constraints**: `>= 2`, `<= 3600` |
| `defaultTimeZone` | `string \| undefined` | Optional | Default server time zone, in the form of an offset from UTC (from -12:00 to +12:00), a time zone name (EST), or 'SYSTEM' to use the MySQL server default.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `100` |
| `groupConcatMaxLen` | `number \| undefined` | Optional | The maximum permitted result length, in bytes, for the GROUP_CONCAT() function.<br><br>**Constraints**: `>= 4`, `<= 1.8446744073709552E+19` |
| `informationSchemaStatsExpiry` | `number \| undefined` | Optional | The time, in seconds, before cached statistics expire.<br><br>**Constraints**: `>= 900`, `<= 31536000` |
| `innodbFtMinTokenSize` | `number \| undefined` | Optional | The minimum length of words that an InnoDB FULLTEXT index stores.<br><br>**Constraints**: `>= 0`, `<= 16` |
| `innodbFtServerStopwordTable` | `string \| undefined` | Optional | The InnoDB FULLTEXT index stopword list for all InnoDB tables.<br><br>**Constraints**: *Maximum Length*: `1024`, *Pattern*: `^.+/.+$` |
| `innodbLockWaitTimeout` | `number \| undefined` | Optional | The time, in seconds, that an InnoDB transaction waits for a row lock. before giving up.<br><br>**Constraints**: `>= 1`, `<= 3600` |
| `innodbLogBufferSize` | `number \| undefined` | Optional | The size of the buffer, in bytes, that InnoDB uses to write to the log files. on disk.<br><br>**Constraints**: `>= 1048576`, `<= 4294967295` |
| `innodbOnlineAlterLogMaxSize` | `number \| undefined` | Optional | The upper limit, in bytes, of the size of the temporary log files used during online DDL operations for InnoDB tables.<br><br>**Constraints**: `>= 65536`, `<= 1099511627776` |
| `innodbPrintAllDeadlocks` | `boolean \| undefined` | Optional | When enabled, records information about all deadlocks in InnoDB user transactions  in the error log. Disabled by default. |
| `innodbRollbackOnTimeout` | `boolean \| undefined` | Optional | When enabled, transaction timeouts cause InnoDB to abort and roll back the entire transaction. |
| `interactiveTimeout` | `number \| undefined` | Optional | The time, in seconds, the server waits for activity on an interactive. connection before closing it.<br><br>**Constraints**: `>= 30`, `<= 604800` |
| `internalTmpMemStorageEngine` | [`InternalTmpMemStorageEngine \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/internal-tmp-mem-storage-engine.md) | Optional | The storage engine for in-memory internal temporary tables. |
| `longQueryTime` | `number \| undefined` | Optional | The time, in seconds, for a query to take to execute before  being captured by slow_query_logs. Default is 10 seconds.<br><br>**Constraints**: `>= 0`, `<= 3600` |
| `maxAllowedPacket` | `number \| undefined` | Optional | The size of the largest message, in bytes, that can be received by the server. Default is 67108864 (64M).<br><br>**Constraints**: `>= 102400`, `<= 1073741824` |
| `maxHeapTableSize` | `number \| undefined` | Optional | The maximum size, in bytes, of internal in-memory tables. Also set tmp_table_size. Default is 16777216 (16M)<br><br>**Constraints**: `>= 1048576`, `<= 1073741824` |
| `netReadTimeout` | `number \| undefined` | Optional | The time, in seconds, to wait for more data from an existing connection. aborting the read.<br><br>**Constraints**: `>= 1`, `<= 3600` |
| `netWriteTimeout` | `number \| undefined` | Optional | The number of seconds to wait for a block to be written to a connection before aborting the write.<br><br>**Constraints**: `>= 1`, `<= 3600` |
| `slowQueryLog` | `boolean \| undefined` | Optional | When enabled, captures slow queries. When disabled, also truncates the mysql.slow_log table. Default is false. |
| `sortBufferSize` | `number \| undefined` | Optional | The sort buffer size, in bytes, for ORDER BY optimization. Default is 262144. (256K).<br><br>**Constraints**: `>= 32768`, `<= 1073741824` |
| `sqlMode` | `string \| undefined` | Optional | Global SQL mode. If empty, uses MySQL server defaults. Must only include uppercase alphabetic characters, underscores, and commas.<br><br>**Constraints**: *Maximum Length*: `1024`, *Pattern*: `^[A-Z_]*(,[A-Z_]+)*$` |
| `sqlRequirePrimaryKey` | `boolean \| undefined` | Optional | Require primary key to be defined for new tables or old tables modified with ALTER TABLE and fail if missing. It is recommended to always have primary keys because various functionality may break if any large table is missing them. |
| `tmpTableSize` | `number \| undefined` | Optional | The maximum size, in bytes, of internal in-memory tables. Also set max_heap_table_size. Default is 16777216 (16M).<br><br>**Constraints**: `>= 1048576`, `<= 1073741824` |
| `waitTimeout` | `number \| undefined` | Optional | The number of seconds the server waits for activity on a noninteractive connection before closing it.<br><br>**Constraints**: `>= 1`, `<= 2147483` |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Config, InternalTmpMemStorageEngine } from 'digitalocean-apilib';

const config: Config = {
  backupHour: 3,
  backupMinute: 30,
  binlogRetentionPeriod: 600,
  connectTimeout: 10,
  defaultTimeZone: '+03:00',
  groupConcatMaxLen: 1024,
  informationSchemaStatsExpiry: 86400,
  innodbFtMinTokenSize: 3,
  innodbFtServerStopwordTable: 'db_name/table_name',
  innodbLockWaitTimeout: 50,
  innodbLogBufferSize: 16777216,
  innodbOnlineAlterLogMaxSize: 134217728,
  innodbPrintAllDeadlocks: true,
  innodbRollbackOnTimeout: true,
  interactiveTimeout: 3600,
  internalTmpMemStorageEngine: InternalTmpMemStorageEngine.TempTable,
  longQueryTime: 10,
  maxAllowedPacket: 67108864,
  maxHeapTableSize: 16777216,
  netReadTimeout: 30,
  netWriteTimeout: 30,
  slowQueryLog: true,
  sortBufferSize: 262144,
  sqlMode: 'ANSI,TRADITIONAL',
  sqlRequirePrimaryKey: true,
  tmpTableSize: 16777216,
  waitTimeout: 28800,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



