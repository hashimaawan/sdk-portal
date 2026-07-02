# Config 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkNvbmZpZzE

*This model accepts additional fields of type Object.*


# Class Name

`Config1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AutovacuumAnalyzeScaleFactor` | `Double` | Optional | Specifies a fraction, in a decimal value, of the table size to add to autovacuum_analyze_threshold when deciding whether to trigger an ANALYZE. The default is 0.2 (20% of table size).<br><br>**Constraints**: `>= 0`, `<= 1` | Double getAutovacuumAnalyzeScaleFactor() | setAutovacuumAnalyzeScaleFactor(Double autovacuumAnalyzeScaleFactor) |
| `AutovacuumAnalyzeThreshold` | `Integer` | Optional | Specifies the minimum number of inserted, updated, or deleted tuples needed to trigger an ANALYZE in any one table. The default is 50 tuples.<br><br>**Constraints**: `>= 0`, `<= 2147483647` | Integer getAutovacuumAnalyzeThreshold() | setAutovacuumAnalyzeThreshold(Integer autovacuumAnalyzeThreshold) |
| `AutovacuumFreezeMaxAge` | `Integer` | Optional | Specifies the maximum age (in transactions) that a table's pg_class.relfrozenxid field can attain before a VACUUM operation is forced to prevent transaction ID wraparound within the table. Note that the system will launch autovacuum processes to prevent wraparound even when autovacuum is otherwise disabled. This parameter will cause the server to be restarted.<br><br>**Constraints**: `>= 200000000`, `<= 1500000000` | Integer getAutovacuumFreezeMaxAge() | setAutovacuumFreezeMaxAge(Integer autovacuumFreezeMaxAge) |
| `AutovacuumMaxWorkers` | `Integer` | Optional | Specifies the maximum number of autovacuum processes (other than the autovacuum launcher) that may be running at any one time. The default is three. This parameter can only be set at server start.<br><br>**Constraints**: `>= 1`, `<= 20` | Integer getAutovacuumMaxWorkers() | setAutovacuumMaxWorkers(Integer autovacuumMaxWorkers) |
| `AutovacuumNaptime` | `Integer` | Optional | Specifies the minimum delay, in seconds, between autovacuum runs on any given database. The default is one minute.<br><br>**Constraints**: `>= 0`, `<= 86400` | Integer getAutovacuumNaptime() | setAutovacuumNaptime(Integer autovacuumNaptime) |
| `AutovacuumVacuumCostDelay` | `Integer` | Optional | Specifies the cost delay value, in milliseconds, that will be used in automatic VACUUM operations. If -1, uses the regular vacuum_cost_delay value, which is 20 milliseconds.<br><br>**Constraints**: `>= -1`, `<= 100` | Integer getAutovacuumVacuumCostDelay() | setAutovacuumVacuumCostDelay(Integer autovacuumVacuumCostDelay) |
| `AutovacuumVacuumCostLimit` | `Integer` | Optional | Specifies the cost limit value that will be used in automatic VACUUM operations. If -1 is specified (which is the default), the regular vacuum_cost_limit value will be used.<br><br>**Constraints**: `>= -1`, `<= 10000` | Integer getAutovacuumVacuumCostLimit() | setAutovacuumVacuumCostLimit(Integer autovacuumVacuumCostLimit) |
| `AutovacuumVacuumScaleFactor` | `Double` | Optional | Specifies a fraction, in a decimal value, of the table size to add to autovacuum_vacuum_threshold when deciding whether to trigger a VACUUM. The default is 0.2 (20% of table size).<br><br>**Constraints**: `>= 0`, `<= 1` | Double getAutovacuumVacuumScaleFactor() | setAutovacuumVacuumScaleFactor(Double autovacuumVacuumScaleFactor) |
| `AutovacuumVacuumThreshold` | `Integer` | Optional | Specifies the minimum number of updated or deleted tuples needed to trigger a VACUUM in any one table. The default is 50 tuples.<br><br>**Constraints**: `>= 0`, `<= 2147483647` | Integer getAutovacuumVacuumThreshold() | setAutovacuumVacuumThreshold(Integer autovacuumVacuumThreshold) |
| `BackupHour` | `Integer` | Optional | The hour of day (in UTC) when backup for the service starts. New backup only starts if previous backup has already completed.<br><br>**Constraints**: `>= 0`, `<= 23` | Integer getBackupHour() | setBackupHour(Integer backupHour) |
| `BackupMinute` | `Integer` | Optional | The minute of the backup hour when backup for the service starts. New backup is only started if previous backup has already completed.<br><br>**Constraints**: `>= 0`, `<= 59` | Integer getBackupMinute() | setBackupMinute(Integer backupMinute) |
| `BgwriterDelay` | `Integer` | Optional | Specifies the delay, in milliseconds, between activity rounds for the background writer. Default is 200 ms.<br><br>**Constraints**: `>= 10`, `<= 10000` | Integer getBgwriterDelay() | setBgwriterDelay(Integer bgwriterDelay) |
| `BgwriterFlushAfter` | `Integer` | Optional | The amount of kilobytes that need to be written by the background writer before attempting to force the OS to issue these writes to underlying storage. Specified in kilobytes, default is 512.  Setting of 0 disables forced writeback.<br><br>**Constraints**: `>= 0`, `<= 2048` | Integer getBgwriterFlushAfter() | setBgwriterFlushAfter(Integer bgwriterFlushAfter) |
| `BgwriterLruMaxpages` | `Integer` | Optional | The maximum number of buffers that the background writer can write. Setting this to zero disables background writing. Default is 100.<br><br>**Constraints**: `>= 0`, `<= 1073741823` | Integer getBgwriterLruMaxpages() | setBgwriterLruMaxpages(Integer bgwriterLruMaxpages) |
| `BgwriterLruMultiplier` | `Double` | Optional | The average recent need for new buffers is multiplied by bgwriter_lru_multiplier to arrive at an estimate of the number that will be needed during the next round, (up to bgwriter_lru_maxpages). 1.0 represents a “just in time” policy of writing exactly the number of buffers predicted to be needed. Larger values provide some cushion against spikes in demand, while smaller values intentionally leave writes to be done by server processes. The default is 2.0.<br><br>**Constraints**: `>= 0`, `<= 10` | Double getBgwriterLruMultiplier() | setBgwriterLruMultiplier(Double bgwriterLruMultiplier) |
| `DeadlockTimeout` | `Integer` | Optional | The amount of time, in milliseconds, to wait on a lock before checking to see if there is a deadlock condition.<br><br>**Constraints**: `>= 500`, `<= 1800000` | Integer getDeadlockTimeout() | setDeadlockTimeout(Integer deadlockTimeout) |
| `DefaultToastCompression` | [`DefaultToastCompression`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/default-toast-compression.md) | Optional | Specifies the default TOAST compression method for values of compressible columns (the default is lz4). | DefaultToastCompression getDefaultToastCompression() | setDefaultToastCompression(DefaultToastCompression defaultToastCompression) |
| `IdleInTransactionSessionTimeout` | `Integer` | Optional | Time out sessions with open transactions after this number of milliseconds<br><br>**Constraints**: `>= 0`, `<= 604800000` | Integer getIdleInTransactionSessionTimeout() | setIdleInTransactionSessionTimeout(Integer idleInTransactionSessionTimeout) |
| `Jit` | `Boolean` | Optional | Activates, in a boolean, the system-wide use of Just-in-Time Compilation (JIT). | Boolean getJit() | setJit(Boolean jit) |
| `LogAutovacuumMinDuration` | `Integer` | Optional | Causes each action executed by autovacuum to be logged if it ran for at least the specified number of milliseconds. Setting this to zero logs all autovacuum actions. Minus-one (the default) disables logging autovacuum actions.<br><br>**Constraints**: `>= -1`, `<= 2147483647` | Integer getLogAutovacuumMinDuration() | setLogAutovacuumMinDuration(Integer logAutovacuumMinDuration) |
| `LogErrorVerbosity` | [`LogErrorVerbosity`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/log-error-verbosity.md) | Optional | Controls the amount of detail written in the server log for each message that is logged. | LogErrorVerbosity getLogErrorVerbosity() | setLogErrorVerbosity(LogErrorVerbosity logErrorVerbosity) |
| `LogLinePrefix` | [`LogLinePrefix`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/log-line-prefix.md) | Optional | Selects one of the available log-formats. These can support popular log analyzers like pgbadger, pganalyze, etc. | LogLinePrefix getLogLinePrefix() | setLogLinePrefix(LogLinePrefix logLinePrefix) |
| `LogMinDurationStatement` | `Integer` | Optional | Log statements that take more than this number of milliseconds to run. If -1, disables.<br><br>**Constraints**: `>= -1`, `<= 86400000` | Integer getLogMinDurationStatement() | setLogMinDurationStatement(Integer logMinDurationStatement) |
| `MaxFilesPerProcess` | `Integer` | Optional | PostgreSQL maximum number of files that can be open per process.<br><br>**Constraints**: `>= 1000`, `<= 4096` | Integer getMaxFilesPerProcess() | setMaxFilesPerProcess(Integer maxFilesPerProcess) |
| `MaxLocksPerTransaction` | `Integer` | Optional | PostgreSQL maximum locks per transaction. Once increased, this parameter cannot be lowered from its set value.<br><br>**Constraints**: `>= 64`, `<= 6400` | Integer getMaxLocksPerTransaction() | setMaxLocksPerTransaction(Integer maxLocksPerTransaction) |
| `MaxLogicalReplicationWorkers` | `Integer` | Optional | PostgreSQL maximum logical replication workers (taken from the pool of max_parallel_workers).<br><br>**Constraints**: `>= 4`, `<= 64` | Integer getMaxLogicalReplicationWorkers() | setMaxLogicalReplicationWorkers(Integer maxLogicalReplicationWorkers) |
| `MaxParallelWorkers` | `Integer` | Optional | Sets the maximum number of workers that the system can support for parallel queries.<br><br>**Constraints**: `>= 0`, `<= 96` | Integer getMaxParallelWorkers() | setMaxParallelWorkers(Integer maxParallelWorkers) |
| `MaxParallelWorkersPerGather` | `Integer` | Optional | Sets the maximum number of workers that can be started by a single Gather or Gather Merge node.<br><br>**Constraints**: `>= 0`, `<= 96` | Integer getMaxParallelWorkersPerGather() | setMaxParallelWorkersPerGather(Integer maxParallelWorkersPerGather) |
| `MaxPredLocksPerTransaction` | `Integer` | Optional | PostgreSQL maximum predicate locks per transaction.<br><br>**Constraints**: `>= 64`, `<= 640` | Integer getMaxPredLocksPerTransaction() | setMaxPredLocksPerTransaction(Integer maxPredLocksPerTransaction) |
| `MaxPreparedTransactions` | `Integer` | Optional | PostgreSQL maximum prepared transactions. Once increased, this parameter cannot be lowered from its set value.<br><br>**Constraints**: `>= 0`, `<= 10000` | Integer getMaxPreparedTransactions() | setMaxPreparedTransactions(Integer maxPreparedTransactions) |
| `MaxReplicationSlots` | `Integer` | Optional | PostgreSQL maximum replication slots.<br><br>**Constraints**: `>= 8`, `<= 64` | Integer getMaxReplicationSlots() | setMaxReplicationSlots(Integer maxReplicationSlots) |
| `MaxStackDepth` | `Integer` | Optional | Maximum depth of the stack in bytes.<br><br>**Constraints**: `>= 2097152`, `<= 6291456` | Integer getMaxStackDepth() | setMaxStackDepth(Integer maxStackDepth) |
| `MaxStandbyArchiveDelay` | `Integer` | Optional | Max standby archive delay in milliseconds.<br><br>**Constraints**: `>= 1`, `<= 43200000` | Integer getMaxStandbyArchiveDelay() | setMaxStandbyArchiveDelay(Integer maxStandbyArchiveDelay) |
| `MaxStandbyStreamingDelay` | `Integer` | Optional | Max standby streaming delay in milliseconds.<br><br>**Constraints**: `>= 1`, `<= 43200000` | Integer getMaxStandbyStreamingDelay() | setMaxStandbyStreamingDelay(Integer maxStandbyStreamingDelay) |
| `MaxWalSenders` | `Integer` | Optional | PostgreSQL maximum WAL senders. Once increased, this parameter cannot be lowered from its set value.<br><br>**Constraints**: `>= 20`, `<= 64` | Integer getMaxWalSenders() | setMaxWalSenders(Integer maxWalSenders) |
| `MaxWorkerProcesses` | `Integer` | Optional | Sets the maximum number of background processes that the system can support. Once increased, this parameter cannot be lowered from its set value.<br><br>**Constraints**: `>= 8`, `<= 96` | Integer getMaxWorkerProcesses() | setMaxWorkerProcesses(Integer maxWorkerProcesses) |
| `PgPartmanBgwInterval` | `Integer` | Optional | Sets the time interval to run pg_partman's scheduled tasks.<br><br>**Constraints**: `>= 3600`, `<= 604800` | Integer getPgPartmanBgwInterval() | setPgPartmanBgwInterval(Integer pgPartmanBgwInterval) |
| `PgPartmanBgwRole` | `String` | Optional | Controls which role to use for pg_partman's scheduled background tasks. Must consist of alpha-numeric characters, dots, underscores, or dashes. May not start with dash or dot. Maximum of 64 characters.<br><br>**Constraints**: *Maximum Length*: `64`, *Pattern*: `^[_A-Za-z0-9][-._A-Za-z0-9]{0,63}$` | String getPgPartmanBgwRole() | setPgPartmanBgwRole(String pgPartmanBgwRole) |
| `PgStatStatementsTrack` | [`PgStatStatementsTrack`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/pg-stat-statements-track.md) | Optional | Controls which statements are counted. Specify 'top' to track top-level statements (those issued directly by clients), 'all' to also track nested statements (such as statements invoked within functions), or 'none' to disable statement statistics collection. The default value is top. | PgStatStatementsTrack getPgStatStatementsTrack() | setPgStatStatementsTrack(PgStatStatementsTrack pgStatStatementsTrack) |
| `Pgbouncer` | [`Pgbouncer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/pgbouncer.md) | Optional | PGBouncer connection pooling settings | Pgbouncer getPgbouncer() | setPgbouncer(Pgbouncer pgbouncer) |
| `SharedBuffersPercentage` | `Double` | Optional | Percentage of total RAM that the database server uses for shared memory buffers.  Valid range is 20-60 (float), which corresponds to 20% - 60%.  This setting adjusts the shared_buffers configuration value.<br><br>**Constraints**: `>= 20`, `<= 60` | Double getSharedBuffersPercentage() | setSharedBuffersPercentage(Double sharedBuffersPercentage) |
| `StatMonitorEnable` | `Boolean` | Optional | Enable the pg_stat_monitor extension. <b>Enabling this extension will cause the cluster to be restarted.</b> When this extension is enabled, pg_stat_statements results for utility commands are unreliable. | Boolean getStatMonitorEnable() | setStatMonitorEnable(Boolean statMonitorEnable) |
| `SynchronousReplication` | [`SynchronousReplication`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/synchronous-replication.md) | Optional | Synchronous replication type. Note that the service plan also needs to support synchronous replication. | SynchronousReplication getSynchronousReplication() | setSynchronousReplication(SynchronousReplication synchronousReplication) |
| `TempFileLimit` | `Integer` | Optional | PostgreSQL temporary file limit in KiB. If -1, sets to unlimited.<br><br>**Constraints**: `>= -1`, `<= 2147483647` | Integer getTempFileLimit() | setTempFileLimit(Integer tempFileLimit) |
| `Timescaledb` | [`Timescaledb`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/timescaledb.md) | Optional | TimescaleDB extension configuration values | Timescaledb getTimescaledb() | setTimescaledb(Timescaledb timescaledb) |
| `Timezone` | `String` | Optional | PostgreSQL service timezone<br><br>**Constraints**: *Maximum Length*: `64` | String getTimezone() | setTimezone(String timezone) |
| `TrackActivityQuerySize` | `Integer` | Optional | Specifies the number of bytes reserved to track the currently executing command for each active session.<br><br>**Constraints**: `>= 1024`, `<= 10240` | Integer getTrackActivityQuerySize() | setTrackActivityQuerySize(Integer trackActivityQuerySize) |
| `TrackCommitTimestamp` | [`TrackCommitTimestamp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/track-commit-timestamp.md) | Optional | Record commit time of transactions. | TrackCommitTimestamp getTrackCommitTimestamp() | setTrackCommitTimestamp(TrackCommitTimestamp trackCommitTimestamp) |
| `TrackFunctions` | [`TrackFunctions`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/track-functions.md) | Optional | Enables tracking of function call counts and time used. | TrackFunctions getTrackFunctions() | setTrackFunctions(TrackFunctions trackFunctions) |
| `TrackIoTiming` | [`TrackIoTiming`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/track-io-timing.md) | Optional | Enables timing of database I/O calls. This parameter is off by default, because it will repeatedly query the operating system for the current time, which may cause significant overhead on some platforms. | TrackIoTiming getTrackIoTiming() | setTrackIoTiming(TrackIoTiming trackIoTiming) |
| `WalSenderTimeout` | `Integer` | Optional | Terminate replication connections that are inactive for longer than this amount of time, in milliseconds. Setting this value to zero disables the timeout. Must be either 0 or between 5000 and 10800000.<br><br>**Constraints**: `>= 0`, `<= 10800000` | Integer getWalSenderTimeout() | setWalSenderTimeout(Integer walSenderTimeout) |
| `WalWriterDelay` | `Integer` | Optional | WAL flush interval in milliseconds. Note that setting this value to lower than the default 200ms may negatively impact performance<br><br>**Constraints**: `>= 10`, `<= 200` | Integer getWalWriterDelay() | setWalWriterDelay(Integer walWriterDelay) |
| `WorkMem` | `Integer` | Optional | The maximum amount of memory, in MB, used by a query operation (such as a sort or hash table) before writing to temporary disk files. Default is 1MB + 0.075% of total RAM (up to 32MB).<br><br>**Constraints**: `>= 1`, `<= 1024` | Integer getWorkMem() | setWorkMem(Integer workMem) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Config1;
import com.digitalocean.api.models.DefaultToastCompression;
import com.digitalocean.api.models.LogErrorVerbosity;
import com.digitalocean.api.models.LogLinePrefix;
import com.digitalocean.api.models.PgStatStatementsTrack;
import com.digitalocean.api.models.SynchronousReplication;
import com.digitalocean.api.models.TrackCommitTimestamp;
import com.digitalocean.api.models.TrackFunctions;
import com.digitalocean.api.models.TrackIoTiming;
import java.io.IOException;

Config1 config1 = new Config1.Builder()
    .autovacuumAnalyzeScaleFactor(0.2D)
    .autovacuumAnalyzeThreshold(50)
    .autovacuumFreezeMaxAge(200000000)
    .autovacuumMaxWorkers(5)
    .autovacuumNaptime(43200)
    .autovacuumVacuumCostDelay(20)
    .autovacuumVacuumCostLimit(-1)
    .autovacuumVacuumScaleFactor(0.2D)
    .autovacuumVacuumThreshold(50)
    .backupHour(3)
    .backupMinute(30)
    .bgwriterDelay(200)
    .bgwriterFlushAfter(512)
    .bgwriterLruMaxpages(100)
    .bgwriterLruMultiplier(2D)
    .deadlockTimeout(1000)
    .defaultToastCompression(DefaultToastCompression.LZ4)
    .idleInTransactionSessionTimeout(10000)
    .jit(true)
    .logAutovacuumMinDuration(-1)
    .logErrorVerbosity(LogErrorVerbosity.VERBOSE)
    .logLinePrefix(LogLinePrefix.ENUM_PIDPUSERUDBDAPPACLIENTH)
    .logMinDurationStatement(-1)
    .maxFilesPerProcess(2048)
    .maxLocksPerTransaction(128)
    .maxLogicalReplicationWorkers(16)
    .maxParallelWorkers(12)
    .maxParallelWorkersPerGather(16)
    .maxPredLocksPerTransaction(128)
    .maxPreparedTransactions(20)
    .maxReplicationSlots(16)
    .maxStackDepth(2097152)
    .maxStandbyArchiveDelay(43200)
    .maxStandbyStreamingDelay(43200)
    .maxWalSenders(32)
    .maxWorkerProcesses(16)
    .pgPartmanBgwInterval(3600)
    .pgPartmanBgwRole("myrolename")
    .pgStatStatementsTrack(PgStatStatementsTrack.ALL)
    .sharedBuffersPercentage(41.5D)
    .statMonitorEnable(false)
    .synchronousReplication(SynchronousReplication.OFF)
    .tempFileLimit(5000000)
    .timezone("Europe/Helsinki")
    .trackActivityQuerySize(1024)
    .trackCommitTimestamp(TrackCommitTimestamp.OFF)
    .trackFunctions(TrackFunctions.ALL)
    .trackIoTiming(TrackIoTiming.OFF)
    .walSenderTimeout(60000)
    .walWriterDelay(50)
    .workMem(4)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



