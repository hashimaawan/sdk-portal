# V2 Databases Config Response Config

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyRGF0YWJhc2VzQ29uZmlnUmVzcG9uc2VDb25maWc


# Data Type

`Config|Config1|Config2`


# Cases

| Type |
|  --- |
| [`Config`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/config.md) |
| [`Config1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/config-1.md) |
| [`Config2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/config-2.md) |


# Config

## Initialization Code

### Example

```php
$value = ConfigBuilder::init()
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
    ->build();
```


# Config1

## Initialization Code

### Example

```php
$value = Config1Builder::init()
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
    ->build();
```


# Config2

## Initialization Code

### Example

```php
$value = Config2Builder::init()
    ->redisAclChannelsDefault(RedisAclChannelsDefault::ALLCHANNELS)
    ->redisIoThreads(1)
    ->redisLfuDecayTime(1)
    ->redisLfuLogFactor(10)
    ->redisMaxmemoryPolicy(RedisMaxmemoryPolicy::ALLKEYS_LRU)
    ->redisNotifyKeyspaceEvents('K')
    ->redisNumberOfDatabases(16)
    ->redisPersistence(RedisPersistence::RDB)
    ->redisPubsubClientOutputBufferLimit(64)
    ->redisSsl(true)
    ->redisTimeout(300)
    ->build();
```



