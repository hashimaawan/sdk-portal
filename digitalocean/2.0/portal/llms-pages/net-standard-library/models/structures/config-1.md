# Config 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNvbmZpZzE

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Config1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AutovacuumAnalyzeScaleFactor` | `double?` | Optional | Specifies a fraction, in a decimal value, of the table size to add to autovacuum_analyze_threshold when deciding whether to trigger an ANALYZE. The default is 0.2 (20% of table size).<br><br>**Constraints**: `>= 0`, `<= 1` |
| `AutovacuumAnalyzeThreshold` | `int?` | Optional | Specifies the minimum number of inserted, updated, or deleted tuples needed to trigger an ANALYZE in any one table. The default is 50 tuples.<br><br>**Constraints**: `>= 0`, `<= 2147483647` |
| `AutovacuumFreezeMaxAge` | `int?` | Optional | Specifies the maximum age (in transactions) that a table's pg_class.relfrozenxid field can attain before a VACUUM operation is forced to prevent transaction ID wraparound within the table. Note that the system will launch autovacuum processes to prevent wraparound even when autovacuum is otherwise disabled. This parameter will cause the server to be restarted.<br><br>**Constraints**: `>= 200000000`, `<= 1500000000` |
| `AutovacuumMaxWorkers` | `int?` | Optional | Specifies the maximum number of autovacuum processes (other than the autovacuum launcher) that may be running at any one time. The default is three. This parameter can only be set at server start.<br><br>**Constraints**: `>= 1`, `<= 20` |
| `AutovacuumNaptime` | `int?` | Optional | Specifies the minimum delay, in seconds, between autovacuum runs on any given database. The default is one minute.<br><br>**Constraints**: `>= 0`, `<= 86400` |
| `AutovacuumVacuumCostDelay` | `int?` | Optional | Specifies the cost delay value, in milliseconds, that will be used in automatic VACUUM operations. If -1, uses the regular vacuum_cost_delay value, which is 20 milliseconds.<br><br>**Constraints**: `>= -1`, `<= 100` |
| `AutovacuumVacuumCostLimit` | `int?` | Optional | Specifies the cost limit value that will be used in automatic VACUUM operations. If -1 is specified (which is the default), the regular vacuum_cost_limit value will be used.<br><br>**Constraints**: `>= -1`, `<= 10000` |
| `AutovacuumVacuumScaleFactor` | `double?` | Optional | Specifies a fraction, in a decimal value, of the table size to add to autovacuum_vacuum_threshold when deciding whether to trigger a VACUUM. The default is 0.2 (20% of table size).<br><br>**Constraints**: `>= 0`, `<= 1` |
| `AutovacuumVacuumThreshold` | `int?` | Optional | Specifies the minimum number of updated or deleted tuples needed to trigger a VACUUM in any one table. The default is 50 tuples.<br><br>**Constraints**: `>= 0`, `<= 2147483647` |
| `BackupHour` | `int?` | Optional | The hour of day (in UTC) when backup for the service starts. New backup only starts if previous backup has already completed.<br><br>**Constraints**: `>= 0`, `<= 23` |
| `BackupMinute` | `int?` | Optional | The minute of the backup hour when backup for the service starts. New backup is only started if previous backup has already completed.<br><br>**Constraints**: `>= 0`, `<= 59` |
| `BgwriterDelay` | `int?` | Optional | Specifies the delay, in milliseconds, between activity rounds for the background writer. Default is 200 ms.<br><br>**Constraints**: `>= 10`, `<= 10000` |
| `BgwriterFlushAfter` | `int?` | Optional | The amount of kilobytes that need to be written by the background writer before attempting to force the OS to issue these writes to underlying storage. Specified in kilobytes, default is 512.  Setting of 0 disables forced writeback.<br><br>**Constraints**: `>= 0`, `<= 2048` |
| `BgwriterLruMaxpages` | `int?` | Optional | The maximum number of buffers that the background writer can write. Setting this to zero disables background writing. Default is 100.<br><br>**Constraints**: `>= 0`, `<= 1073741823` |
| `BgwriterLruMultiplier` | `double?` | Optional | The average recent need for new buffers is multiplied by bgwriter_lru_multiplier to arrive at an estimate of the number that will be needed during the next round, (up to bgwriter_lru_maxpages). 1.0 represents a “just in time” policy of writing exactly the number of buffers predicted to be needed. Larger values provide some cushion against spikes in demand, while smaller values intentionally leave writes to be done by server processes. The default is 2.0.<br><br>**Constraints**: `>= 0`, `<= 10` |
| `DeadlockTimeout` | `int?` | Optional | The amount of time, in milliseconds, to wait on a lock before checking to see if there is a deadlock condition.<br><br>**Constraints**: `>= 500`, `<= 1800000` |
| `DefaultToastCompression` | [`DefaultToastCompression?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/default-toast-compression.md) | Optional | Specifies the default TOAST compression method for values of compressible columns (the default is lz4). |
| `IdleInTransactionSessionTimeout` | `int?` | Optional | Time out sessions with open transactions after this number of milliseconds<br><br>**Constraints**: `>= 0`, `<= 604800000` |
| `Jit` | `bool?` | Optional | Activates, in a boolean, the system-wide use of Just-in-Time Compilation (JIT). |
| `LogAutovacuumMinDuration` | `int?` | Optional | Causes each action executed by autovacuum to be logged if it ran for at least the specified number of milliseconds. Setting this to zero logs all autovacuum actions. Minus-one (the default) disables logging autovacuum actions.<br><br>**Constraints**: `>= -1`, `<= 2147483647` |
| `LogErrorVerbosity` | [`LogErrorVerbosity?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/log-error-verbosity.md) | Optional | Controls the amount of detail written in the server log for each message that is logged. |
| `LogLinePrefix` | [`LogLinePrefix?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/log-line-prefix.md) | Optional | Selects one of the available log-formats. These can support popular log analyzers like pgbadger, pganalyze, etc. |
| `LogMinDurationStatement` | `int?` | Optional | Log statements that take more than this number of milliseconds to run. If -1, disables.<br><br>**Constraints**: `>= -1`, `<= 86400000` |
| `MaxFilesPerProcess` | `int?` | Optional | PostgreSQL maximum number of files that can be open per process.<br><br>**Constraints**: `>= 1000`, `<= 4096` |
| `MaxLocksPerTransaction` | `int?` | Optional | PostgreSQL maximum locks per transaction. Once increased, this parameter cannot be lowered from its set value.<br><br>**Constraints**: `>= 64`, `<= 6400` |
| `MaxLogicalReplicationWorkers` | `int?` | Optional | PostgreSQL maximum logical replication workers (taken from the pool of max_parallel_workers).<br><br>**Constraints**: `>= 4`, `<= 64` |
| `MaxParallelWorkers` | `int?` | Optional | Sets the maximum number of workers that the system can support for parallel queries.<br><br>**Constraints**: `>= 0`, `<= 96` |
| `MaxParallelWorkersPerGather` | `int?` | Optional | Sets the maximum number of workers that can be started by a single Gather or Gather Merge node.<br><br>**Constraints**: `>= 0`, `<= 96` |
| `MaxPredLocksPerTransaction` | `int?` | Optional | PostgreSQL maximum predicate locks per transaction.<br><br>**Constraints**: `>= 64`, `<= 640` |
| `MaxPreparedTransactions` | `int?` | Optional | PostgreSQL maximum prepared transactions. Once increased, this parameter cannot be lowered from its set value.<br><br>**Constraints**: `>= 0`, `<= 10000` |
| `MaxReplicationSlots` | `int?` | Optional | PostgreSQL maximum replication slots.<br><br>**Constraints**: `>= 8`, `<= 64` |
| `MaxStackDepth` | `int?` | Optional | Maximum depth of the stack in bytes.<br><br>**Constraints**: `>= 2097152`, `<= 6291456` |
| `MaxStandbyArchiveDelay` | `int?` | Optional | Max standby archive delay in milliseconds.<br><br>**Constraints**: `>= 1`, `<= 43200000` |
| `MaxStandbyStreamingDelay` | `int?` | Optional | Max standby streaming delay in milliseconds.<br><br>**Constraints**: `>= 1`, `<= 43200000` |
| `MaxWalSenders` | `int?` | Optional | PostgreSQL maximum WAL senders. Once increased, this parameter cannot be lowered from its set value.<br><br>**Constraints**: `>= 20`, `<= 64` |
| `MaxWorkerProcesses` | `int?` | Optional | Sets the maximum number of background processes that the system can support. Once increased, this parameter cannot be lowered from its set value.<br><br>**Constraints**: `>= 8`, `<= 96` |
| `PgPartmanBgwInterval` | `int?` | Optional | Sets the time interval to run pg_partman's scheduled tasks.<br><br>**Constraints**: `>= 3600`, `<= 604800` |
| `PgPartmanBgwRole` | `string` | Optional | Controls which role to use for pg_partman's scheduled background tasks. Must consist of alpha-numeric characters, dots, underscores, or dashes. May not start with dash or dot. Maximum of 64 characters.<br><br>**Constraints**: *Maximum Length*: `64`, *Pattern*: `^[_A-Za-z0-9][-._A-Za-z0-9]{0,63}$` |
| `PgStatStatementsTrack` | [`PgStatStatementsTrack?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/pg-stat-statements-track.md) | Optional | Controls which statements are counted. Specify 'top' to track top-level statements (those issued directly by clients), 'all' to also track nested statements (such as statements invoked within functions), or 'none' to disable statement statistics collection. The default value is top. |
| `Pgbouncer` | [`Pgbouncer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/pgbouncer.md) | Optional | PGBouncer connection pooling settings |
| `SharedBuffersPercentage` | `double?` | Optional | Percentage of total RAM that the database server uses for shared memory buffers.  Valid range is 20-60 (float), which corresponds to 20% - 60%.  This setting adjusts the shared_buffers configuration value.<br><br>**Constraints**: `>= 20`, `<= 60` |
| `StatMonitorEnable` | `bool?` | Optional | Enable the pg_stat_monitor extension. <b>Enabling this extension will cause the cluster to be restarted.</b> When this extension is enabled, pg_stat_statements results for utility commands are unreliable. |
| `SynchronousReplication` | [`SynchronousReplication?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/synchronous-replication.md) | Optional | Synchronous replication type. Note that the service plan also needs to support synchronous replication. |
| `TempFileLimit` | `int?` | Optional | PostgreSQL temporary file limit in KiB. If -1, sets to unlimited.<br><br>**Constraints**: `>= -1`, `<= 2147483647` |
| `Timescaledb` | [`Timescaledb`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/timescaledb.md) | Optional | TimescaleDB extension configuration values |
| `Timezone` | `string` | Optional | PostgreSQL service timezone<br><br>**Constraints**: *Maximum Length*: `64` |
| `TrackActivityQuerySize` | `int?` | Optional | Specifies the number of bytes reserved to track the currently executing command for each active session.<br><br>**Constraints**: `>= 1024`, `<= 10240` |
| `TrackCommitTimestamp` | [`TrackCommitTimestamp?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/track-commit-timestamp.md) | Optional | Record commit time of transactions. |
| `TrackFunctions` | [`TrackFunctions?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/track-functions.md) | Optional | Enables tracking of function call counts and time used. |
| `TrackIoTiming` | [`TrackIoTiming?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/track-io-timing.md) | Optional | Enables timing of database I/O calls. This parameter is off by default, because it will repeatedly query the operating system for the current time, which may cause significant overhead on some platforms. |
| `WalSenderTimeout` | `int?` | Optional | Terminate replication connections that are inactive for longer than this amount of time, in milliseconds. Setting this value to zero disables the timeout. Must be either 0 or between 5000 and 10800000.<br><br>**Constraints**: `>= 0`, `<= 10800000` |
| `WalWriterDelay` | `int?` | Optional | WAL flush interval in milliseconds. Note that setting this value to lower than the default 200ms may negatively impact performance<br><br>**Constraints**: `>= 10`, `<= 200` |
| `WorkMem` | `int?` | Optional | The maximum amount of memory, in MB, used by a query operation (such as a sort or hash table) before writing to temporary disk files. Default is 1MB + 0.075% of total RAM (up to 32MB).<br><br>**Constraints**: `>= 1`, `<= 1024` |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Config1 config1 = new Config1
{
    AutovacuumAnalyzeScaleFactor = 0.2,
    AutovacuumAnalyzeThreshold = 50,
    AutovacuumFreezeMaxAge = 200000000,
    AutovacuumMaxWorkers = 5,
    AutovacuumNaptime = 43200,
    AutovacuumVacuumCostDelay = 20,
    AutovacuumVacuumCostLimit = -1,
    AutovacuumVacuumScaleFactor = 0.2,
    AutovacuumVacuumThreshold = 50,
    BackupHour = 3,
    BackupMinute = 30,
    BgwriterDelay = 200,
    BgwriterFlushAfter = 512,
    BgwriterLruMaxpages = 100,
    BgwriterLruMultiplier = 2,
    DeadlockTimeout = 1000,
    DefaultToastCompression = DefaultToastCompression.Lz4,
    IdleInTransactionSessionTimeout = 10000,
    Jit = true,
    LogAutovacuumMinDuration = -1,
    LogErrorVerbosity = LogErrorVerbosity.Verbose,
    LogLinePrefix = LogLinePrefix.EnumPidpuserudbdappaclienth,
    LogMinDurationStatement = -1,
    MaxFilesPerProcess = 2048,
    MaxLocksPerTransaction = 128,
    MaxLogicalReplicationWorkers = 16,
    MaxParallelWorkers = 12,
    MaxParallelWorkersPerGather = 16,
    MaxPredLocksPerTransaction = 128,
    MaxPreparedTransactions = 20,
    MaxReplicationSlots = 16,
    MaxStackDepth = 2097152,
    MaxStandbyArchiveDelay = 43200,
    MaxStandbyStreamingDelay = 43200,
    MaxWalSenders = 32,
    MaxWorkerProcesses = 16,
    PgPartmanBgwInterval = 3600,
    PgPartmanBgwRole = "myrolename",
    PgStatStatementsTrack = PgStatStatementsTrack.All,
    SharedBuffersPercentage = 41.5,
    StatMonitorEnable = false,
    SynchronousReplication = SynchronousReplication.Off,
    TempFileLimit = 5000000,
    Timezone = "Europe/Helsinki",
    TrackActivityQuerySize = 1024,
    TrackCommitTimestamp = TrackCommitTimestamp.Off,
    TrackFunctions = TrackFunctions.All,
    TrackIoTiming = TrackIoTiming.Off,
    WalSenderTimeout = 60000,
    WalWriterDelay = 50,
    WorkMem = 4,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



