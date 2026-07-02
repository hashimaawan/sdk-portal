# V2 Databases Config Response Config

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyRGF0YWJhc2VzQ29uZmlnUmVzcG9uc2VDb25maWc


# Class Name

`V2DatabasesConfigResponseConfig`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`Config`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/config.md) | V2DatabasesConfigResponseConfig.FromConfig(Config config) |
| [`Config1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/config-1.md) | V2DatabasesConfigResponseConfig.FromConfig1(Config1 config1) |
| [`Config2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/config-2.md) | V2DatabasesConfigResponseConfig.FromConfig2(Config2 config2) |


# Config

## Initialization Code

### Example

```csharp
V2DatabasesConfigResponseConfig value = V2DatabasesConfigResponseConfig.FromConfig(
    new Config
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
    }
);
```


# Config1

## Initialization Code

### Example

```csharp
V2DatabasesConfigResponseConfig value = V2DatabasesConfigResponseConfig.FromConfig1(
    new Config1
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
    }
);
```


# Config2

## Initialization Code

### Example

```csharp
V2DatabasesConfigResponseConfig value = V2DatabasesConfigResponseConfig.FromConfig2(
    new Config2
    {
        RedisAclChannelsDefault = RedisAclChannelsDefault.Allchannels,
        RedisIoThreads = 1,
        RedisLfuDecayTime = 1,
        RedisLfuLogFactor = 10,
        RedisMaxmemoryPolicy = RedisMaxmemoryPolicy.AllkeysLru,
        RedisNotifyKeyspaceEvents = "K",
        RedisNumberOfDatabases = 16,
        RedisPersistence = RedisPersistence.Rdb,
        RedisPubsubClientOutputBufferLimit = 64,
        RedisSsl = true,
        RedisTimeout = 300,
    }
);
```



