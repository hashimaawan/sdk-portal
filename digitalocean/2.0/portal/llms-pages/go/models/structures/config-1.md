# Config 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkNvbmZpZzE

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Config1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AutovacuumAnalyzeScaleFactor` | `*float64` | Optional | Specifies a fraction, in a decimal value, of the table size to add to autovacuum_analyze_threshold when deciding whether to trigger an ANALYZE. The default is 0.2 (20% of table size).<br><br>**Constraints**: `>= 0`, `<= 1` |
| `AutovacuumAnalyzeThreshold` | `*int` | Optional | Specifies the minimum number of inserted, updated, or deleted tuples needed to trigger an ANALYZE in any one table. The default is 50 tuples.<br><br>**Constraints**: `>= 0`, `<= 2147483647` |
| `AutovacuumFreezeMaxAge` | `*int` | Optional | Specifies the maximum age (in transactions) that a table's pg_class.relfrozenxid field can attain before a VACUUM operation is forced to prevent transaction ID wraparound within the table. Note that the system will launch autovacuum processes to prevent wraparound even when autovacuum is otherwise disabled. This parameter will cause the server to be restarted.<br><br>**Constraints**: `>= 200000000`, `<= 1500000000` |
| `AutovacuumMaxWorkers` | `*int` | Optional | Specifies the maximum number of autovacuum processes (other than the autovacuum launcher) that may be running at any one time. The default is three. This parameter can only be set at server start.<br><br>**Constraints**: `>= 1`, `<= 20` |
| `AutovacuumNaptime` | `*int` | Optional | Specifies the minimum delay, in seconds, between autovacuum runs on any given database. The default is one minute.<br><br>**Constraints**: `>= 0`, `<= 86400` |
| `AutovacuumVacuumCostDelay` | `*int` | Optional | Specifies the cost delay value, in milliseconds, that will be used in automatic VACUUM operations. If -1, uses the regular vacuum_cost_delay value, which is 20 milliseconds.<br><br>**Constraints**: `>= -1`, `<= 100` |
| `AutovacuumVacuumCostLimit` | `*int` | Optional | Specifies the cost limit value that will be used in automatic VACUUM operations. If -1 is specified (which is the default), the regular vacuum_cost_limit value will be used.<br><br>**Constraints**: `>= -1`, `<= 10000` |
| `AutovacuumVacuumScaleFactor` | `*float64` | Optional | Specifies a fraction, in a decimal value, of the table size to add to autovacuum_vacuum_threshold when deciding whether to trigger a VACUUM. The default is 0.2 (20% of table size).<br><br>**Constraints**: `>= 0`, `<= 1` |
| `AutovacuumVacuumThreshold` | `*int` | Optional | Specifies the minimum number of updated or deleted tuples needed to trigger a VACUUM in any one table. The default is 50 tuples.<br><br>**Constraints**: `>= 0`, `<= 2147483647` |
| `BackupHour` | `*int` | Optional | The hour of day (in UTC) when backup for the service starts. New backup only starts if previous backup has already completed.<br><br>**Constraints**: `>= 0`, `<= 23` |
| `BackupMinute` | `*int` | Optional | The minute of the backup hour when backup for the service starts. New backup is only started if previous backup has already completed.<br><br>**Constraints**: `>= 0`, `<= 59` |
| `BgwriterDelay` | `*int` | Optional | Specifies the delay, in milliseconds, between activity rounds for the background writer. Default is 200 ms.<br><br>**Constraints**: `>= 10`, `<= 10000` |
| `BgwriterFlushAfter` | `*int` | Optional | The amount of kilobytes that need to be written by the background writer before attempting to force the OS to issue these writes to underlying storage. Specified in kilobytes, default is 512.  Setting of 0 disables forced writeback.<br><br>**Constraints**: `>= 0`, `<= 2048` |
| `BgwriterLruMaxpages` | `*int` | Optional | The maximum number of buffers that the background writer can write. Setting this to zero disables background writing. Default is 100.<br><br>**Constraints**: `>= 0`, `<= 1073741823` |
| `BgwriterLruMultiplier` | `*float64` | Optional | The average recent need for new buffers is multiplied by bgwriter_lru_multiplier to arrive at an estimate of the number that will be needed during the next round, (up to bgwriter_lru_maxpages). 1.0 represents a “just in time” policy of writing exactly the number of buffers predicted to be needed. Larger values provide some cushion against spikes in demand, while smaller values intentionally leave writes to be done by server processes. The default is 2.0.<br><br>**Constraints**: `>= 0`, `<= 10` |
| `DeadlockTimeout` | `*int` | Optional | The amount of time, in milliseconds, to wait on a lock before checking to see if there is a deadlock condition.<br><br>**Constraints**: `>= 500`, `<= 1800000` |
| `DefaultToastCompression` | [`*models.DefaultToastCompression`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/default-toast-compression.md) | Optional | Specifies the default TOAST compression method for values of compressible columns (the default is lz4). |
| `IdleInTransactionSessionTimeout` | `*int` | Optional | Time out sessions with open transactions after this number of milliseconds<br><br>**Constraints**: `>= 0`, `<= 604800000` |
| `Jit` | `*bool` | Optional | Activates, in a boolean, the system-wide use of Just-in-Time Compilation (JIT). |
| `LogAutovacuumMinDuration` | `*int` | Optional | Causes each action executed by autovacuum to be logged if it ran for at least the specified number of milliseconds. Setting this to zero logs all autovacuum actions. Minus-one (the default) disables logging autovacuum actions.<br><br>**Constraints**: `>= -1`, `<= 2147483647` |
| `LogErrorVerbosity` | [`*models.LogErrorVerbosity`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/log-error-verbosity.md) | Optional | Controls the amount of detail written in the server log for each message that is logged. |
| `LogLinePrefix` | [`*models.LogLinePrefix`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/log-line-prefix.md) | Optional | Selects one of the available log-formats. These can support popular log analyzers like pgbadger, pganalyze, etc. |
| `LogMinDurationStatement` | `*int` | Optional | Log statements that take more than this number of milliseconds to run. If -1, disables.<br><br>**Constraints**: `>= -1`, `<= 86400000` |
| `MaxFilesPerProcess` | `*int` | Optional | PostgreSQL maximum number of files that can be open per process.<br><br>**Constraints**: `>= 1000`, `<= 4096` |
| `MaxLocksPerTransaction` | `*int` | Optional | PostgreSQL maximum locks per transaction. Once increased, this parameter cannot be lowered from its set value.<br><br>**Constraints**: `>= 64`, `<= 6400` |
| `MaxLogicalReplicationWorkers` | `*int` | Optional | PostgreSQL maximum logical replication workers (taken from the pool of max_parallel_workers).<br><br>**Constraints**: `>= 4`, `<= 64` |
| `MaxParallelWorkers` | `*int` | Optional | Sets the maximum number of workers that the system can support for parallel queries.<br><br>**Constraints**: `>= 0`, `<= 96` |
| `MaxParallelWorkersPerGather` | `*int` | Optional | Sets the maximum number of workers that can be started by a single Gather or Gather Merge node.<br><br>**Constraints**: `>= 0`, `<= 96` |
| `MaxPredLocksPerTransaction` | `*int` | Optional | PostgreSQL maximum predicate locks per transaction.<br><br>**Constraints**: `>= 64`, `<= 640` |
| `MaxPreparedTransactions` | `*int` | Optional | PostgreSQL maximum prepared transactions. Once increased, this parameter cannot be lowered from its set value.<br><br>**Constraints**: `>= 0`, `<= 10000` |
| `MaxReplicationSlots` | `*int` | Optional | PostgreSQL maximum replication slots.<br><br>**Constraints**: `>= 8`, `<= 64` |
| `MaxStackDepth` | `*int` | Optional | Maximum depth of the stack in bytes.<br><br>**Constraints**: `>= 2097152`, `<= 6291456` |
| `MaxStandbyArchiveDelay` | `*int` | Optional | Max standby archive delay in milliseconds.<br><br>**Constraints**: `>= 1`, `<= 43200000` |
| `MaxStandbyStreamingDelay` | `*int` | Optional | Max standby streaming delay in milliseconds.<br><br>**Constraints**: `>= 1`, `<= 43200000` |
| `MaxWalSenders` | `*int` | Optional | PostgreSQL maximum WAL senders. Once increased, this parameter cannot be lowered from its set value.<br><br>**Constraints**: `>= 20`, `<= 64` |
| `MaxWorkerProcesses` | `*int` | Optional | Sets the maximum number of background processes that the system can support. Once increased, this parameter cannot be lowered from its set value.<br><br>**Constraints**: `>= 8`, `<= 96` |
| `PgPartmanBgwInterval` | `*int` | Optional | Sets the time interval to run pg_partman's scheduled tasks.<br><br>**Constraints**: `>= 3600`, `<= 604800` |
| `PgPartmanBgwRole` | `*string` | Optional | Controls which role to use for pg_partman's scheduled background tasks. Must consist of alpha-numeric characters, dots, underscores, or dashes. May not start with dash or dot. Maximum of 64 characters.<br><br>**Constraints**: *Maximum Length*: `64`, *Pattern*: `^[_A-Za-z0-9][-._A-Za-z0-9]{0,63}$` |
| `PgStatStatementsTrack` | [`*models.PgStatStatementsTrack`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/pg-stat-statements-track.md) | Optional | Controls which statements are counted. Specify 'top' to track top-level statements (those issued directly by clients), 'all' to also track nested statements (such as statements invoked within functions), or 'none' to disable statement statistics collection. The default value is top. |
| `Pgbouncer` | [`*models.Pgbouncer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/pgbouncer.md) | Optional | PGBouncer connection pooling settings |
| `SharedBuffersPercentage` | `*float64` | Optional | Percentage of total RAM that the database server uses for shared memory buffers.  Valid range is 20-60 (float), which corresponds to 20% - 60%.  This setting adjusts the shared_buffers configuration value.<br><br>**Constraints**: `>= 20`, `<= 60` |
| `StatMonitorEnable` | `*bool` | Optional | Enable the pg_stat_monitor extension. <b>Enabling this extension will cause the cluster to be restarted.</b> When this extension is enabled, pg_stat_statements results for utility commands are unreliable. |
| `SynchronousReplication` | [`*models.SynchronousReplication`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/synchronous-replication.md) | Optional | Synchronous replication type. Note that the service plan also needs to support synchronous replication. |
| `TempFileLimit` | `*int` | Optional | PostgreSQL temporary file limit in KiB. If -1, sets to unlimited.<br><br>**Constraints**: `>= -1`, `<= 2147483647` |
| `Timescaledb` | [`*models.Timescaledb`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/timescaledb.md) | Optional | TimescaleDB extension configuration values |
| `Timezone` | `*string` | Optional | PostgreSQL service timezone<br><br>**Constraints**: *Maximum Length*: `64` |
| `TrackActivityQuerySize` | `*int` | Optional | Specifies the number of bytes reserved to track the currently executing command for each active session.<br><br>**Constraints**: `>= 1024`, `<= 10240` |
| `TrackCommitTimestamp` | [`*models.TrackCommitTimestamp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/track-commit-timestamp.md) | Optional | Record commit time of transactions. |
| `TrackFunctions` | [`*models.TrackFunctions`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/track-functions.md) | Optional | Enables tracking of function call counts and time used. |
| `TrackIoTiming` | [`*models.TrackIoTiming`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/track-io-timing.md) | Optional | Enables timing of database I/O calls. This parameter is off by default, because it will repeatedly query the operating system for the current time, which may cause significant overhead on some platforms. |
| `WalSenderTimeout` | `*int` | Optional | Terminate replication connections that are inactive for longer than this amount of time, in milliseconds. Setting this value to zero disables the timeout. Must be either 0 or between 5000 and 10800000.<br><br>**Constraints**: `>= 0`, `<= 10800000` |
| `WalWriterDelay` | `*int` | Optional | WAL flush interval in milliseconds. Note that setting this value to lower than the default 200ms may negatively impact performance<br><br>**Constraints**: `>= 10`, `<= 200` |
| `WorkMem` | `*int` | Optional | The maximum amount of memory, in MB, used by a query operation (such as a sort or hash table) before writing to temporary disk files. Default is 1MB + 0.075% of total RAM (up to 32MB).<br><br>**Constraints**: `>= 1`, `<= 1024` |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    config1 := models.Config1{
        AutovacuumAnalyzeScaleFactor:    models.ToPointer(float64(0.2)),
        AutovacuumAnalyzeThreshold:      models.ToPointer(50),
        AutovacuumFreezeMaxAge:          models.ToPointer(200000000),
        AutovacuumMaxWorkers:            models.ToPointer(5),
        AutovacuumNaptime:               models.ToPointer(43200),
        AutovacuumVacuumCostDelay:       models.ToPointer(20),
        AutovacuumVacuumCostLimit:       models.ToPointer(-1),
        AutovacuumVacuumScaleFactor:     models.ToPointer(float64(0.2)),
        AutovacuumVacuumThreshold:       models.ToPointer(50),
        BackupHour:                      models.ToPointer(3),
        BackupMinute:                    models.ToPointer(30),
        BgwriterDelay:                   models.ToPointer(200),
        BgwriterFlushAfter:              models.ToPointer(512),
        BgwriterLruMaxpages:             models.ToPointer(100),
        BgwriterLruMultiplier:           models.ToPointer(float64(2)),
        DeadlockTimeout:                 models.ToPointer(1000),
        DefaultToastCompression:         models.ToPointer(models.DefaultToastCompression_Lz4),
        IdleInTransactionSessionTimeout: models.ToPointer(10000),
        Jit:                             models.ToPointer(true),
        LogAutovacuumMinDuration:        models.ToPointer(-1),
        LogErrorVerbosity:               models.ToPointer(models.LogErrorVerbosity_Verbose),
        LogLinePrefix:                   models.ToPointer(models.LogLinePrefix_EnumPidpuserudbdappaclienth),
        LogMinDurationStatement:         models.ToPointer(-1),
        MaxFilesPerProcess:              models.ToPointer(2048),
        MaxLocksPerTransaction:          models.ToPointer(128),
        MaxLogicalReplicationWorkers:    models.ToPointer(16),
        MaxParallelWorkers:              models.ToPointer(12),
        MaxParallelWorkersPerGather:     models.ToPointer(16),
        MaxPredLocksPerTransaction:      models.ToPointer(128),
        MaxPreparedTransactions:         models.ToPointer(20),
        MaxReplicationSlots:             models.ToPointer(16),
        MaxStackDepth:                   models.ToPointer(2097152),
        MaxStandbyArchiveDelay:          models.ToPointer(43200),
        MaxStandbyStreamingDelay:        models.ToPointer(43200),
        MaxWalSenders:                   models.ToPointer(32),
        MaxWorkerProcesses:              models.ToPointer(16),
        PgPartmanBgwInterval:            models.ToPointer(3600),
        PgPartmanBgwRole:                models.ToPointer("myrolename"),
        PgStatStatementsTrack:           models.ToPointer(models.PgStatStatementsTrack_All),
        SharedBuffersPercentage:         models.ToPointer(float64(41.5)),
        StatMonitorEnable:               models.ToPointer(false),
        SynchronousReplication:          models.ToPointer(models.SynchronousReplication_Off),
        TempFileLimit:                   models.ToPointer(5000000),
        Timezone:                        models.ToPointer("Europe/Helsinki"),
        TrackActivityQuerySize:          models.ToPointer(1024),
        TrackCommitTimestamp:            models.ToPointer(models.TrackCommitTimestamp_Off),
        TrackFunctions:                  models.ToPointer(models.TrackFunctions_All),
        TrackIoTiming:                   models.ToPointer(models.TrackIoTiming_Off),
        WalSenderTimeout:                models.ToPointer(60000),
        WalWriterDelay:                  models.ToPointer(50),
        WorkMem:                         models.ToPointer(4),
        AdditionalProperties:            map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



