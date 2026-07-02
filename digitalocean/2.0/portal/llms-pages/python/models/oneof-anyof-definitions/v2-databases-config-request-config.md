# V2 Databases Config Request Config

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyRGF0YWJhc2VzQ29uZmlnUmVxdWVzdENvbmZpZw


# Data Type

`Config | Config1 | Config2`


# Cases

| Type |
|  --- |
| [`Config`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/config.md) |
| [`Config1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/config-1.md) |
| [`Config2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/config-2.md) |


# Config

## Initialization Code

### Example

```python
value = Config(
    backup_hour=3,
    backup_minute=30,
    binlog_retention_period=600,
    connect_timeout=10,
    default_time_zone='+03:00',
    group_concat_max_len=1024,
    information_schema_stats_expiry=86400,
    innodb_ft_min_token_size=3,
    innodb_ft_server_stopword_table='db_name/table_name',
    innodb_lock_wait_timeout=50,
    innodb_log_buffer_size=16777216,
    innodb_online_alter_log_max_size=134217728,
    innodb_print_all_deadlocks=True,
    innodb_rollback_on_timeout=True,
    interactive_timeout=3600,
    internal_tmp_mem_storage_engine=InternalTmpMemStorageEngine.TEMPTABLE,
    long_query_time=10,
    max_allowed_packet=67108864,
    max_heap_table_size=16777216,
    net_read_timeout=30,
    net_write_timeout=30,
    slow_query_log=True,
    sort_buffer_size=262144,
    sql_mode='ANSI,TRADITIONAL',
    sql_require_primary_key=True,
    tmp_table_size=16777216,
    wait_timeout=28800
)
```


# Config1

## Initialization Code

### Example

```python
value = Config1(
    autovacuum_analyze_scale_factor=0.2,
    autovacuum_analyze_threshold=50,
    autovacuum_freeze_max_age=200000000,
    autovacuum_max_workers=5,
    autovacuum_naptime=43200,
    autovacuum_vacuum_cost_delay=20,
    autovacuum_vacuum_cost_limit=-1,
    autovacuum_vacuum_scale_factor=0.2,
    autovacuum_vacuum_threshold=50,
    backup_hour=3,
    backup_minute=30,
    bgwriter_delay=200,
    bgwriter_flush_after=512,
    bgwriter_lru_maxpages=100,
    bgwriter_lru_multiplier=2,
    deadlock_timeout=1000,
    default_toast_compression=DefaultToastCompression.LZ4,
    idle_in_transaction_session_timeout=10000,
    jit=True,
    log_autovacuum_min_duration=-1,
    log_error_verbosity=LogErrorVerbosity.VERBOSE,
    log_line_prefix=LogLinePrefix.ENUM_PIDPUSERUDBDAPPACLIENTH,
    log_min_duration_statement=-1,
    max_files_per_process=2048,
    max_locks_per_transaction=128,
    max_logical_replication_workers=16,
    max_parallel_workers=12,
    max_parallel_workers_per_gather=16,
    max_pred_locks_per_transaction=128,
    max_prepared_transactions=20,
    max_replication_slots=16,
    max_stack_depth=2097152,
    max_standby_archive_delay=43200,
    max_standby_streaming_delay=43200,
    max_wal_senders=32,
    max_worker_processes=16,
    pg_partman_bgw_interval=3600,
    pg_partman_bgw_role='myrolename',
    pg_stat_statements_track=PgStatStatementsTrack.ALL,
    shared_buffers_percentage=41.5,
    stat_monitor_enable=False,
    synchronous_replication=SynchronousReplication.OFF,
    temp_file_limit=5000000,
    timezone='Europe/Helsinki',
    track_activity_query_size=1024,
    track_commit_timestamp=TrackCommitTimestamp.OFF,
    track_functions=TrackFunctions.ALL,
    track_io_timing=TrackIoTiming.OFF,
    wal_sender_timeout=60000,
    wal_writer_delay=50,
    work_mem=4
)
```


# Config2

## Initialization Code

### Example

```python
value = Config2(
    redis_acl_channels_default=RedisAclChannelsDefault.ALLCHANNELS,
    redis_io_threads=1,
    redis_lfu_decay_time=1,
    redis_lfu_log_factor=10,
    redis_maxmemory_policy=RedisMaxmemoryPolicy.ALLKEYS_LRU,
    redis_notify_keyspace_events='K',
    redis_number_of_databases=16,
    redis_persistence=RedisPersistence.RDB,
    redis_pubsub_client_output_buffer_limit=64,
    redis_ssl=True,
    redis_timeout=300
)
```



