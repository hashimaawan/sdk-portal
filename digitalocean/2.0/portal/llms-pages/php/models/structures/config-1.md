# Config 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkNvbmZpZzE

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Config1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `autovacuumAnalyzeScaleFactor` | `?float` | Optional | Specifies a fraction, in a decimal value, of the table size to add to autovacuum_analyze_threshold when deciding whether to trigger an ANALYZE. The default is 0.2 (20% of table size).<br><br>**Constraints**: `>= 0`, `<= 1` | getAutovacuumAnalyzeScaleFactor(): ?float | setAutovacuumAnalyzeScaleFactor(?float autovacuumAnalyzeScaleFactor): void |
| `autovacuumAnalyzeThreshold` | `?int` | Optional | Specifies the minimum number of inserted, updated, or deleted tuples needed to trigger an ANALYZE in any one table. The default is 50 tuples.<br><br>**Constraints**: `>= 0`, `<= 2147483647` | getAutovacuumAnalyzeThreshold(): ?int | setAutovacuumAnalyzeThreshold(?int autovacuumAnalyzeThreshold): void |
| `autovacuumFreezeMaxAge` | `?int` | Optional | Specifies the maximum age (in transactions) that a table's pg_class.relfrozenxid field can attain before a VACUUM operation is forced to prevent transaction ID wraparound within the table. Note that the system will launch autovacuum processes to prevent wraparound even when autovacuum is otherwise disabled. This parameter will cause the server to be restarted.<br><br>**Constraints**: `>= 200000000`, `<= 1500000000` | getAutovacuumFreezeMaxAge(): ?int | setAutovacuumFreezeMaxAge(?int autovacuumFreezeMaxAge): void |
| `autovacuumMaxWorkers` | `?int` | Optional | Specifies the maximum number of autovacuum processes (other than the autovacuum launcher) that may be running at any one time. The default is three. This parameter can only be set at server start.<br><br>**Constraints**: `>= 1`, `<= 20` | getAutovacuumMaxWorkers(): ?int | setAutovacuumMaxWorkers(?int autovacuumMaxWorkers): void |
| `autovacuumNaptime` | `?int` | Optional | Specifies the minimum delay, in seconds, between autovacuum runs on any given database. The default is one minute.<br><br>**Constraints**: `>= 0`, `<= 86400` | getAutovacuumNaptime(): ?int | setAutovacuumNaptime(?int autovacuumNaptime): void |
| `autovacuumVacuumCostDelay` | `?int` | Optional | Specifies the cost delay value, in milliseconds, that will be used in automatic VACUUM operations. If -1, uses the regular vacuum_cost_delay value, which is 20 milliseconds.<br><br>**Constraints**: `>= -1`, `<= 100` | getAutovacuumVacuumCostDelay(): ?int | setAutovacuumVacuumCostDelay(?int autovacuumVacuumCostDelay): void |
| `autovacuumVacuumCostLimit` | `?int` | Optional | Specifies the cost limit value that will be used in automatic VACUUM operations. If -1 is specified (which is the default), the regular vacuum_cost_limit value will be used.<br><br>**Constraints**: `>= -1`, `<= 10000` | getAutovacuumVacuumCostLimit(): ?int | setAutovacuumVacuumCostLimit(?int autovacuumVacuumCostLimit): void |
| `autovacuumVacuumScaleFactor` | `?float` | Optional | Specifies a fraction, in a decimal value, of the table size to add to autovacuum_vacuum_threshold when deciding whether to trigger a VACUUM. The default is 0.2 (20% of table size).<br><br>**Constraints**: `>= 0`, `<= 1` | getAutovacuumVacuumScaleFactor(): ?float | setAutovacuumVacuumScaleFactor(?float autovacuumVacuumScaleFactor): void |
| `autovacuumVacuumThreshold` | `?int` | Optional | Specifies the minimum number of updated or deleted tuples needed to trigger a VACUUM in any one table. The default is 50 tuples.<br><br>**Constraints**: `>= 0`, `<= 2147483647` | getAutovacuumVacuumThreshold(): ?int | setAutovacuumVacuumThreshold(?int autovacuumVacuumThreshold): void |
| `backupHour` | `?int` | Optional | The hour of day (in UTC) when backup for the service starts. New backup only starts if previous backup has already completed.<br><br>**Constraints**: `>= 0`, `<= 23` | getBackupHour(): ?int | setBackupHour(?int backupHour): void |
| `backupMinute` | `?int` | Optional | The minute of the backup hour when backup for the service starts. New backup is only started if previous backup has already completed.<br><br>**Constraints**: `>= 0`, `<= 59` | getBackupMinute(): ?int | setBackupMinute(?int backupMinute): void |
| `bgwriterDelay` | `?int` | Optional | Specifies the delay, in milliseconds, between activity rounds for the background writer. Default is 200 ms.<br><br>**Constraints**: `>= 10`, `<= 10000` | getBgwriterDelay(): ?int | setBgwriterDelay(?int bgwriterDelay): void |
| `bgwriterFlushAfter` | `?int` | Optional | The amount of kilobytes that need to be written by the background writer before attempting to force the OS to issue these writes to underlying storage. Specified in kilobytes, default is 512.  Setting of 0 disables forced writeback.<br><br>**Constraints**: `>= 0`, `<= 2048` | getBgwriterFlushAfter(): ?int | setBgwriterFlushAfter(?int bgwriterFlushAfter): void |
| `bgwriterLruMaxpages` | `?int` | Optional | The maximum number of buffers that the background writer can write. Setting this to zero disables background writing. Default is 100.<br><br>**Constraints**: `>= 0`, `<= 1073741823` | getBgwriterLruMaxpages(): ?int | setBgwriterLruMaxpages(?int bgwriterLruMaxpages): void |
| `bgwriterLruMultiplier` | `?float` | Optional | The average recent need for new buffers is multiplied by bgwriter_lru_multiplier to arrive at an estimate of the number that will be needed during the next round, (up to bgwriter_lru_maxpages). 1.0 represents a “just in time” policy of writing exactly the number of buffers predicted to be needed. Larger values provide some cushion against spikes in demand, while smaller values intentionally leave writes to be done by server processes. The default is 2.0.<br><br>**Constraints**: `>= 0`, `<= 10` | getBgwriterLruMultiplier(): ?float | setBgwriterLruMultiplier(?float bgwriterLruMultiplier): void |
| `deadlockTimeout` | `?int` | Optional | The amount of time, in milliseconds, to wait on a lock before checking to see if there is a deadlock condition.<br><br>**Constraints**: `>= 500`, `<= 1800000` | getDeadlockTimeout(): ?int | setDeadlockTimeout(?int deadlockTimeout): void |
| `defaultToastCompression` | [`?string(DefaultToastCompression)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/default-toast-compression.md) | Optional | Specifies the default TOAST compression method for values of compressible columns (the default is lz4). | getDefaultToastCompression(): ?string | setDefaultToastCompression(?string defaultToastCompression): void |
| `idleInTransactionSessionTimeout` | `?int` | Optional | Time out sessions with open transactions after this number of milliseconds<br><br>**Constraints**: `>= 0`, `<= 604800000` | getIdleInTransactionSessionTimeout(): ?int | setIdleInTransactionSessionTimeout(?int idleInTransactionSessionTimeout): void |
| `jit` | `?bool` | Optional | Activates, in a boolean, the system-wide use of Just-in-Time Compilation (JIT). | getJit(): ?bool | setJit(?bool jit): void |
| `logAutovacuumMinDuration` | `?int` | Optional | Causes each action executed by autovacuum to be logged if it ran for at least the specified number of milliseconds. Setting this to zero logs all autovacuum actions. Minus-one (the default) disables logging autovacuum actions.<br><br>**Constraints**: `>= -1`, `<= 2147483647` | getLogAutovacuumMinDuration(): ?int | setLogAutovacuumMinDuration(?int logAutovacuumMinDuration): void |
| `logErrorVerbosity` | [`?string(LogErrorVerbosity)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/log-error-verbosity.md) | Optional | Controls the amount of detail written in the server log for each message that is logged. | getLogErrorVerbosity(): ?string | setLogErrorVerbosity(?string logErrorVerbosity): void |
| `logLinePrefix` | [`?string(LogLinePrefix)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/log-line-prefix.md) | Optional | Selects one of the available log-formats. These can support popular log analyzers like pgbadger, pganalyze, etc. | getLogLinePrefix(): ?string | setLogLinePrefix(?string logLinePrefix): void |
| `logMinDurationStatement` | `?int` | Optional | Log statements that take more than this number of milliseconds to run. If -1, disables.<br><br>**Constraints**: `>= -1`, `<= 86400000` | getLogMinDurationStatement(): ?int | setLogMinDurationStatement(?int logMinDurationStatement): void |
| `maxFilesPerProcess` | `?int` | Optional | PostgreSQL maximum number of files that can be open per process.<br><br>**Constraints**: `>= 1000`, `<= 4096` | getMaxFilesPerProcess(): ?int | setMaxFilesPerProcess(?int maxFilesPerProcess): void |
| `maxLocksPerTransaction` | `?int` | Optional | PostgreSQL maximum locks per transaction. Once increased, this parameter cannot be lowered from its set value.<br><br>**Constraints**: `>= 64`, `<= 6400` | getMaxLocksPerTransaction(): ?int | setMaxLocksPerTransaction(?int maxLocksPerTransaction): void |
| `maxLogicalReplicationWorkers` | `?int` | Optional | PostgreSQL maximum logical replication workers (taken from the pool of max_parallel_workers).<br><br>**Constraints**: `>= 4`, `<= 64` | getMaxLogicalReplicationWorkers(): ?int | setMaxLogicalReplicationWorkers(?int maxLogicalReplicationWorkers): void |
| `maxParallelWorkers` | `?int` | Optional | Sets the maximum number of workers that the system can support for parallel queries.<br><br>**Constraints**: `>= 0`, `<= 96` | getMaxParallelWorkers(): ?int | setMaxParallelWorkers(?int maxParallelWorkers): void |
| `maxParallelWorkersPerGather` | `?int` | Optional | Sets the maximum number of workers that can be started by a single Gather or Gather Merge node.<br><br>**Constraints**: `>= 0`, `<= 96` | getMaxParallelWorkersPerGather(): ?int | setMaxParallelWorkersPerGather(?int maxParallelWorkersPerGather): void |
| `maxPredLocksPerTransaction` | `?int` | Optional | PostgreSQL maximum predicate locks per transaction.<br><br>**Constraints**: `>= 64`, `<= 640` | getMaxPredLocksPerTransaction(): ?int | setMaxPredLocksPerTransaction(?int maxPredLocksPerTransaction): void |
| `maxPreparedTransactions` | `?int` | Optional | PostgreSQL maximum prepared transactions. Once increased, this parameter cannot be lowered from its set value.<br><br>**Constraints**: `>= 0`, `<= 10000` | getMaxPreparedTransactions(): ?int | setMaxPreparedTransactions(?int maxPreparedTransactions): void |
| `maxReplicationSlots` | `?int` | Optional | PostgreSQL maximum replication slots.<br><br>**Constraints**: `>= 8`, `<= 64` | getMaxReplicationSlots(): ?int | setMaxReplicationSlots(?int maxReplicationSlots): void |
| `maxStackDepth` | `?int` | Optional | Maximum depth of the stack in bytes.<br><br>**Constraints**: `>= 2097152`, `<= 6291456` | getMaxStackDepth(): ?int | setMaxStackDepth(?int maxStackDepth): void |
| `maxStandbyArchiveDelay` | `?int` | Optional | Max standby archive delay in milliseconds.<br><br>**Constraints**: `>= 1`, `<= 43200000` | getMaxStandbyArchiveDelay(): ?int | setMaxStandbyArchiveDelay(?int maxStandbyArchiveDelay): void |
| `maxStandbyStreamingDelay` | `?int` | Optional | Max standby streaming delay in milliseconds.<br><br>**Constraints**: `>= 1`, `<= 43200000` | getMaxStandbyStreamingDelay(): ?int | setMaxStandbyStreamingDelay(?int maxStandbyStreamingDelay): void |
| `maxWalSenders` | `?int` | Optional | PostgreSQL maximum WAL senders. Once increased, this parameter cannot be lowered from its set value.<br><br>**Constraints**: `>= 20`, `<= 64` | getMaxWalSenders(): ?int | setMaxWalSenders(?int maxWalSenders): void |
| `maxWorkerProcesses` | `?int` | Optional | Sets the maximum number of background processes that the system can support. Once increased, this parameter cannot be lowered from its set value.<br><br>**Constraints**: `>= 8`, `<= 96` | getMaxWorkerProcesses(): ?int | setMaxWorkerProcesses(?int maxWorkerProcesses): void |
| `pgPartmanBgwInterval` | `?int` | Optional | Sets the time interval to run pg_partman's scheduled tasks.<br><br>**Constraints**: `>= 3600`, `<= 604800` | getPgPartmanBgwInterval(): ?int | setPgPartmanBgwInterval(?int pgPartmanBgwInterval): void |
| `pgPartmanBgwRole` | `?string` | Optional | Controls which role to use for pg_partman's scheduled background tasks. Must consist of alpha-numeric characters, dots, underscores, or dashes. May not start with dash or dot. Maximum of 64 characters.<br><br>**Constraints**: *Maximum Length*: `64`, *Pattern*: `^[_A-Za-z0-9][-._A-Za-z0-9]{0,63}$` | getPgPartmanBgwRole(): ?string | setPgPartmanBgwRole(?string pgPartmanBgwRole): void |
| `pgStatStatementsTrack` | [`?string(PgStatStatementsTrack)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/pg-stat-statements-track.md) | Optional | Controls which statements are counted. Specify 'top' to track top-level statements (those issued directly by clients), 'all' to also track nested statements (such as statements invoked within functions), or 'none' to disable statement statistics collection. The default value is top. | getPgStatStatementsTrack(): ?string | setPgStatStatementsTrack(?string pgStatStatementsTrack): void |
| `pgbouncer` | [`?Pgbouncer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/pgbouncer.md) | Optional | PGBouncer connection pooling settings | getPgbouncer(): ?Pgbouncer | setPgbouncer(?Pgbouncer pgbouncer): void |
| `sharedBuffersPercentage` | `?float` | Optional | Percentage of total RAM that the database server uses for shared memory buffers.  Valid range is 20-60 (float), which corresponds to 20% - 60%.  This setting adjusts the shared_buffers configuration value.<br><br>**Constraints**: `>= 20`, `<= 60` | getSharedBuffersPercentage(): ?float | setSharedBuffersPercentage(?float sharedBuffersPercentage): void |
| `statMonitorEnable` | `?bool` | Optional | Enable the pg_stat_monitor extension. <b>Enabling this extension will cause the cluster to be restarted.</b> When this extension is enabled, pg_stat_statements results for utility commands are unreliable. | getStatMonitorEnable(): ?bool | setStatMonitorEnable(?bool statMonitorEnable): void |
| `synchronousReplication` | [`?string(SynchronousReplication)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/synchronous-replication.md) | Optional | Synchronous replication type. Note that the service plan also needs to support synchronous replication. | getSynchronousReplication(): ?string | setSynchronousReplication(?string synchronousReplication): void |
| `tempFileLimit` | `?int` | Optional | PostgreSQL temporary file limit in KiB. If -1, sets to unlimited.<br><br>**Constraints**: `>= -1`, `<= 2147483647` | getTempFileLimit(): ?int | setTempFileLimit(?int tempFileLimit): void |
| `timescaledb` | [`?Timescaledb`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/timescaledb.md) | Optional | TimescaleDB extension configuration values | getTimescaledb(): ?Timescaledb | setTimescaledb(?Timescaledb timescaledb): void |
| `timezone` | `?string` | Optional | PostgreSQL service timezone<br><br>**Constraints**: *Maximum Length*: `64` | getTimezone(): ?string | setTimezone(?string timezone): void |
| `trackActivityQuerySize` | `?int` | Optional | Specifies the number of bytes reserved to track the currently executing command for each active session.<br><br>**Constraints**: `>= 1024`, `<= 10240` | getTrackActivityQuerySize(): ?int | setTrackActivityQuerySize(?int trackActivityQuerySize): void |
| `trackCommitTimestamp` | [`?string(TrackCommitTimestamp)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/track-commit-timestamp.md) | Optional | Record commit time of transactions. | getTrackCommitTimestamp(): ?string | setTrackCommitTimestamp(?string trackCommitTimestamp): void |
| `trackFunctions` | [`?string(TrackFunctions)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/track-functions.md) | Optional | Enables tracking of function call counts and time used. | getTrackFunctions(): ?string | setTrackFunctions(?string trackFunctions): void |
| `trackIoTiming` | [`?string(TrackIoTiming)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/track-io-timing.md) | Optional | Enables timing of database I/O calls. This parameter is off by default, because it will repeatedly query the operating system for the current time, which may cause significant overhead on some platforms. | getTrackIoTiming(): ?string | setTrackIoTiming(?string trackIoTiming): void |
| `walSenderTimeout` | `?int` | Optional | Terminate replication connections that are inactive for longer than this amount of time, in milliseconds. Setting this value to zero disables the timeout. Must be either 0 or between 5000 and 10800000.<br><br>**Constraints**: `>= 0`, `<= 10800000` | getWalSenderTimeout(): ?int | setWalSenderTimeout(?int walSenderTimeout): void |
| `walWriterDelay` | `?int` | Optional | WAL flush interval in milliseconds. Note that setting this value to lower than the default 200ms may negatively impact performance<br><br>**Constraints**: `>= 10`, `<= 200` | getWalWriterDelay(): ?int | setWalWriterDelay(?int walWriterDelay): void |
| `workMem` | `?int` | Optional | The maximum amount of memory, in MB, used by a query operation (such as a sort or hash table) before writing to temporary disk files. Default is 1MB + 0.075% of total RAM (up to 32MB).<br><br>**Constraints**: `>= 1`, `<= 1024` | getWorkMem(): ?int | setWorkMem(?int workMem): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Config1Builder;
use DigitalOceanApiLib\Models\DefaultToastCompression;
use DigitalOceanApiLib\Models\LogErrorVerbosity;
use DigitalOceanApiLib\Models\LogLinePrefix;
use DigitalOceanApiLib\Models\PgStatStatementsTrack;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\SynchronousReplication;
use DigitalOceanApiLib\Models\TrackCommitTimestamp;
use DigitalOceanApiLib\Models\TrackFunctions;
use DigitalOceanApiLib\Models\TrackIoTiming;

$config1 = Config1Builder::init()
    ->autovacuumAnalyzeScaleFactor(0.2)
    ->autovacuumAnalyzeThreshold(50)
    ->autovacuumFreezeMaxAge(200000000)
    ->autovacuumMaxWorkers(5)
    ->autovacuumNaptime(43200)
    ->autovacuumVacuumCostDelay(20)
    ->autovacuumVacuumCostLimit(-1)
    ->autovacuumVacuumScaleFactor(0.2)
    ->autovacuumVacuumThreshold(50)
    ->backupHour(3)
    ->backupMinute(30)
    ->bgwriterDelay(200)
    ->bgwriterFlushAfter(512)
    ->bgwriterLruMaxpages(100)
    ->bgwriterLruMultiplier(2)
    ->deadlockTimeout(1000)
    ->defaultToastCompression(DefaultToastCompression::LZ4)
    ->idleInTransactionSessionTimeout(10000)
    ->jit(true)
    ->logAutovacuumMinDuration(-1)
    ->logErrorVerbosity(LogErrorVerbosity::VERBOSE)
    ->logLinePrefix(LogLinePrefix::ENUM_PIDPUSERUDBDAPPACLIENTH)
    ->logMinDurationStatement(-1)
    ->maxFilesPerProcess(2048)
    ->maxLocksPerTransaction(128)
    ->maxLogicalReplicationWorkers(16)
    ->maxParallelWorkers(12)
    ->maxParallelWorkersPerGather(16)
    ->maxPredLocksPerTransaction(128)
    ->maxPreparedTransactions(20)
    ->maxReplicationSlots(16)
    ->maxStackDepth(2097152)
    ->maxStandbyArchiveDelay(43200)
    ->maxStandbyStreamingDelay(43200)
    ->maxWalSenders(32)
    ->maxWorkerProcesses(16)
    ->pgPartmanBgwInterval(3600)
    ->pgPartmanBgwRole('myrolename')
    ->pgStatStatementsTrack(PgStatStatementsTrack::ALL)
    ->sharedBuffersPercentage(41.5)
    ->statMonitorEnable(false)
    ->synchronousReplication(SynchronousReplication::OFF)
    ->tempFileLimit(5000000)
    ->timezone('Europe/Helsinki')
    ->trackActivityQuerySize(1024)
    ->trackCommitTimestamp(TrackCommitTimestamp::OFF)
    ->trackFunctions(TrackFunctions::ALL)
    ->trackIoTiming(TrackIoTiming::OFF)
    ->walSenderTimeout(60000)
    ->walWriterDelay(50)
    ->workMem(4)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



