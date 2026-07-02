# V2 Databases Config Request Config

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyRGF0YWJhc2VzQ29uZmlnUmVxdWVzdENvbmZpZw


# Class Name

`V2DatabasesConfigRequestConfig`


# Cases

| Type | Factory Method |
|  --- | --- |
| [`models.Config`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/config.md) | models.V2DatabasesConfigRequestConfigContainer.FromConfig(models.Config config) |
| [`models.Config1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/config-1.md) | models.V2DatabasesConfigRequestConfigContainer.FromConfig1(models.Config1 config1) |
| [`models.Config2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/config-2.md) | models.V2DatabasesConfigRequestConfigContainer.FromConfig2(models.Config2 config2) |


# models.Config

## Initialization Code

### Example

```go
value := models.V2DatabasesConfigRequestConfigContainer.FromConfig(models.Config{
    BackupHour:                   models.ToPointer(3),
    BackupMinute:                 models.ToPointer(30),
    BinlogRetentionPeriod:        models.ToPointer(float64(600)),
    ConnectTimeout:               models.ToPointer(10),
    DefaultTimeZone:              models.ToPointer("+03:00"),
    GroupConcatMaxLen:            models.ToPointer(1024),
    InformationSchemaStatsExpiry: models.ToPointer(86400),
    InnodbFtMinTokenSize:         models.ToPointer(3),
    InnodbFtServerStopwordTable:  models.ToPointer("db_name/table_name"),
    InnodbLockWaitTimeout:        models.ToPointer(50),
    InnodbLogBufferSize:          models.ToPointer(16777216),
    InnodbOnlineAlterLogMaxSize:  models.ToPointer(134217728),
    InnodbPrintAllDeadlocks:      models.ToPointer(true),
    InnodbRollbackOnTimeout:      models.ToPointer(true),
    InteractiveTimeout:           models.ToPointer(3600),
    InternalTmpMemStorageEngine:  models.ToPointer(models.InternalTmpMemStorageEngine_Temptable),
    LongQueryTime:                models.ToPointer(float64(10)),
    MaxAllowedPacket:             models.ToPointer(67108864),
    MaxHeapTableSize:             models.ToPointer(16777216),
    NetReadTimeout:               models.ToPointer(30),
    NetWriteTimeout:              models.ToPointer(30),
    SlowQueryLog:                 models.ToPointer(true),
    SortBufferSize:               models.ToPointer(262144),
    SqlMode:                      models.ToPointer("ANSI,TRADITIONAL"),
    SqlRequirePrimaryKey:         models.ToPointer(true),
    TmpTableSize:                 models.ToPointer(16777216),
    WaitTimeout:                  models.ToPointer(28800),
})
```


# models.Config1

## Initialization Code

### Example

```go
value := models.V2DatabasesConfigRequestConfigContainer.FromConfig1(models.Config1{
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
})
```


# models.Config2

## Initialization Code

### Example

```go
value := models.V2DatabasesConfigRequestConfigContainer.FromConfig2(models.Config2{
    RedisAclChannelsDefault:            models.ToPointer(models.RedisAclChannelsDefault_Allchannels),
    RedisIoThreads:                     models.ToPointer(1),
    RedisLfuDecayTime:                  models.ToPointer(1),
    RedisLfuLogFactor:                  models.ToPointer(10),
    RedisMaxmemoryPolicy:               models.ToPointer(models.RedisMaxmemoryPolicy_AllkeysLru),
    RedisNotifyKeyspaceEvents:          models.ToPointer("K"),
    RedisNumberOfDatabases:             models.ToPointer(16),
    RedisPersistence:                   models.ToPointer(models.RedisPersistence_Rdb),
    RedisPubsubClientOutputBufferLimit: models.ToPointer(64),
    RedisSsl:                           models.ToPointer(true),
    RedisTimeout:                       models.ToPointer(300),
})
```



