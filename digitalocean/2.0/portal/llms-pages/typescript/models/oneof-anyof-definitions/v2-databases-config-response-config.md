# V2 Databases Config Response Config

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyRGF0YWJhc2VzQ29uZmlnUmVzcG9uc2VDb25maWc


# Class Name

`V2DatabasesConfigResponseConfig`


# Cases

| Type |
|  --- |
| [`Config`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/config.md) |
| [`Config1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/config-1.md) |
| [`Config2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/config-2.md) |


# Config

## Initialization Code

### Example

```ts
const value: V2DatabasesConfigResponseConfig = {
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
};
```


# Config1

## Initialization Code

### Example

```ts
const value: V2DatabasesConfigResponseConfig = {
  autovacuumAnalyzeScaleFactor: 0.2,
  autovacuumAnalyzeThreshold: 50,
  autovacuumFreezeMaxAge: 200000000,
  autovacuumMaxWorkers: 5,
  autovacuumNaptime: 43200,
  autovacuumVacuumCostDelay: 20,
  autovacuumVacuumCostLimit: -1,
  autovacuumVacuumScaleFactor: 0.2,
  autovacuumVacuumThreshold: 50,
  backupHour: 3,
  backupMinute: 30,
  bgwriterDelay: 200,
  bgwriterFlushAfter: 512,
  bgwriterLruMaxpages: 100,
  bgwriterLruMultiplier: 2,
  deadlockTimeout: 1000,
  defaultToastCompression: DefaultToastCompression.Lz4,
  idleInTransactionSessionTimeout: 10000,
  jit: true,
  logAutovacuumMinDuration: -1,
  logErrorVerbosity: LogErrorVerbosity.Verbose,
  logLinePrefix: LogLinePrefix.EnumPidpuserudbdappaclienth,
  logMinDurationStatement: -1,
  maxFilesPerProcess: 2048,
  maxLocksPerTransaction: 128,
  maxLogicalReplicationWorkers: 16,
  maxParallelWorkers: 12,
  maxParallelWorkersPerGather: 16,
  maxPredLocksPerTransaction: 128,
  maxPreparedTransactions: 20,
  maxReplicationSlots: 16,
  maxStackDepth: 2097152,
  maxStandbyArchiveDelay: 43200,
  maxStandbyStreamingDelay: 43200,
  maxWalSenders: 32,
  maxWorkerProcesses: 16,
  pgPartmanBgwInterval: 3600,
  pgPartmanBgwRole: 'myrolename',
  pgStatStatementsTrack: PgStatStatementsTrack.All,
  sharedBuffersPercentage: 41.5,
  statMonitorEnable: false,
  synchronousReplication: SynchronousReplication.Off,
  tempFileLimit: 5000000,
  timezone: 'Europe/Helsinki',
  trackActivityQuerySize: 1024,
  trackCommitTimestamp: TrackCommitTimestamp.Off,
  trackFunctions: TrackFunctions.All,
  trackIoTiming: TrackIoTiming.Off,
  walSenderTimeout: 60000,
  walWriterDelay: 50,
  workMem: 4,
};
```


# Config2

## Initialization Code

### Example

```ts
const value: V2DatabasesConfigResponseConfig = {
  redisAclChannelsDefault: RedisAclChannelsDefault.Allchannels,
  redisIoThreads: 1,
  redisLfuDecayTime: 1,
  redisLfuLogFactor: 10,
  redisMaxmemoryPolicy: RedisMaxmemoryPolicy.AllkeysLru,
  redisNotifyKeyspaceEvents: 'K',
  redisNumberOfDatabases: 16,
  redisPersistence: RedisPersistence.Rdb,
  redisPubsubClientOutputBufferLimit: 64,
  redisSsl: true,
  redisTimeout: 300,
};
```



