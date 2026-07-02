# Config 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkNvbmZpZzE

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Config1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `autovacuum_analyze_scale_factor` | `float` | Optional | Specifies a fraction, in a decimal value, of the table size to add to autovacuum_analyze_threshold when deciding whether to trigger an ANALYZE. The default is 0.2 (20% of table size).<br><br>**Constraints**: `>= 0`, `<= 1` |
| `autovacuum_analyze_threshold` | `int` | Optional | Specifies the minimum number of inserted, updated, or deleted tuples needed to trigger an ANALYZE in any one table. The default is 50 tuples.<br><br>**Constraints**: `>= 0`, `<= 2147483647` |
| `autovacuum_freeze_max_age` | `int` | Optional | Specifies the maximum age (in transactions) that a table's pg_class.relfrozenxid field can attain before a VACUUM operation is forced to prevent transaction ID wraparound within the table. Note that the system will launch autovacuum processes to prevent wraparound even when autovacuum is otherwise disabled. This parameter will cause the server to be restarted.<br><br>**Constraints**: `>= 200000000`, `<= 1500000000` |
| `autovacuum_max_workers` | `int` | Optional | Specifies the maximum number of autovacuum processes (other than the autovacuum launcher) that may be running at any one time. The default is three. This parameter can only be set at server start.<br><br>**Constraints**: `>= 1`, `<= 20` |
| `autovacuum_naptime` | `int` | Optional | Specifies the minimum delay, in seconds, between autovacuum runs on any given database. The default is one minute.<br><br>**Constraints**: `>= 0`, `<= 86400` |
| `autovacuum_vacuum_cost_delay` | `int` | Optional | Specifies the cost delay value, in milliseconds, that will be used in automatic VACUUM operations. If -1, uses the regular vacuum_cost_delay value, which is 20 milliseconds.<br><br>**Constraints**: `>= -1`, `<= 100` |
| `autovacuum_vacuum_cost_limit` | `int` | Optional | Specifies the cost limit value that will be used in automatic VACUUM operations. If -1 is specified (which is the default), the regular vacuum_cost_limit value will be used.<br><br>**Constraints**: `>= -1`, `<= 10000` |
| `autovacuum_vacuum_scale_factor` | `float` | Optional | Specifies a fraction, in a decimal value, of the table size to add to autovacuum_vacuum_threshold when deciding whether to trigger a VACUUM. The default is 0.2 (20% of table size).<br><br>**Constraints**: `>= 0`, `<= 1` |
| `autovacuum_vacuum_threshold` | `int` | Optional | Specifies the minimum number of updated or deleted tuples needed to trigger a VACUUM in any one table. The default is 50 tuples.<br><br>**Constraints**: `>= 0`, `<= 2147483647` |
| `backup_hour` | `int` | Optional | The hour of day (in UTC) when backup for the service starts. New backup only starts if previous backup has already completed.<br><br>**Constraints**: `>= 0`, `<= 23` |
| `backup_minute` | `int` | Optional | The minute of the backup hour when backup for the service starts. New backup is only started if previous backup has already completed.<br><br>**Constraints**: `>= 0`, `<= 59` |
| `bgwriter_delay` | `int` | Optional | Specifies the delay, in milliseconds, between activity rounds for the background writer. Default is 200 ms.<br><br>**Constraints**: `>= 10`, `<= 10000` |
| `bgwriter_flush_after` | `int` | Optional | The amount of kilobytes that need to be written by the background writer before attempting to force the OS to issue these writes to underlying storage. Specified in kilobytes, default is 512.  Setting of 0 disables forced writeback.<br><br>**Constraints**: `>= 0`, `<= 2048` |
| `bgwriter_lru_maxpages` | `int` | Optional | The maximum number of buffers that the background writer can write. Setting this to zero disables background writing. Default is 100.<br><br>**Constraints**: `>= 0`, `<= 1073741823` |
| `bgwriter_lru_multiplier` | `float` | Optional | The average recent need for new buffers is multiplied by bgwriter_lru_multiplier to arrive at an estimate of the number that will be needed during the next round, (up to bgwriter_lru_maxpages). 1.0 represents a “just in time” policy of writing exactly the number of buffers predicted to be needed. Larger values provide some cushion against spikes in demand, while smaller values intentionally leave writes to be done by server processes. The default is 2.0.<br><br>**Constraints**: `>= 0`, `<= 10` |
| `deadlock_timeout` | `int` | Optional | The amount of time, in milliseconds, to wait on a lock before checking to see if there is a deadlock condition.<br><br>**Constraints**: `>= 500`, `<= 1800000` |
| `default_toast_compression` | [`DefaultToastCompression`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/default-toast-compression.md) | Optional | Specifies the default TOAST compression method for values of compressible columns (the default is lz4). |
| `idle_in_transaction_session_timeout` | `int` | Optional | Time out sessions with open transactions after this number of milliseconds<br><br>**Constraints**: `>= 0`, `<= 604800000` |
| `jit` | `bool` | Optional | Activates, in a boolean, the system-wide use of Just-in-Time Compilation (JIT). |
| `log_autovacuum_min_duration` | `int` | Optional | Causes each action executed by autovacuum to be logged if it ran for at least the specified number of milliseconds. Setting this to zero logs all autovacuum actions. Minus-one (the default) disables logging autovacuum actions.<br><br>**Constraints**: `>= -1`, `<= 2147483647` |
| `log_error_verbosity` | [`LogErrorVerbosity`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/log-error-verbosity.md) | Optional | Controls the amount of detail written in the server log for each message that is logged. |
| `log_line_prefix` | [`LogLinePrefix`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/log-line-prefix.md) | Optional | Selects one of the available log-formats. These can support popular log analyzers like pgbadger, pganalyze, etc. |
| `log_min_duration_statement` | `int` | Optional | Log statements that take more than this number of milliseconds to run. If -1, disables.<br><br>**Constraints**: `>= -1`, `<= 86400000` |
| `max_files_per_process` | `int` | Optional | PostgreSQL maximum number of files that can be open per process.<br><br>**Constraints**: `>= 1000`, `<= 4096` |
| `max_locks_per_transaction` | `int` | Optional | PostgreSQL maximum locks per transaction. Once increased, this parameter cannot be lowered from its set value.<br><br>**Constraints**: `>= 64`, `<= 6400` |
| `max_logical_replication_workers` | `int` | Optional | PostgreSQL maximum logical replication workers (taken from the pool of max_parallel_workers).<br><br>**Constraints**: `>= 4`, `<= 64` |
| `max_parallel_workers` | `int` | Optional | Sets the maximum number of workers that the system can support for parallel queries.<br><br>**Constraints**: `>= 0`, `<= 96` |
| `max_parallel_workers_per_gather` | `int` | Optional | Sets the maximum number of workers that can be started by a single Gather or Gather Merge node.<br><br>**Constraints**: `>= 0`, `<= 96` |
| `max_pred_locks_per_transaction` | `int` | Optional | PostgreSQL maximum predicate locks per transaction.<br><br>**Constraints**: `>= 64`, `<= 640` |
| `max_prepared_transactions` | `int` | Optional | PostgreSQL maximum prepared transactions. Once increased, this parameter cannot be lowered from its set value.<br><br>**Constraints**: `>= 0`, `<= 10000` |
| `max_replication_slots` | `int` | Optional | PostgreSQL maximum replication slots.<br><br>**Constraints**: `>= 8`, `<= 64` |
| `max_stack_depth` | `int` | Optional | Maximum depth of the stack in bytes.<br><br>**Constraints**: `>= 2097152`, `<= 6291456` |
| `max_standby_archive_delay` | `int` | Optional | Max standby archive delay in milliseconds.<br><br>**Constraints**: `>= 1`, `<= 43200000` |
| `max_standby_streaming_delay` | `int` | Optional | Max standby streaming delay in milliseconds.<br><br>**Constraints**: `>= 1`, `<= 43200000` |
| `max_wal_senders` | `int` | Optional | PostgreSQL maximum WAL senders. Once increased, this parameter cannot be lowered from its set value.<br><br>**Constraints**: `>= 20`, `<= 64` |
| `max_worker_processes` | `int` | Optional | Sets the maximum number of background processes that the system can support. Once increased, this parameter cannot be lowered from its set value.<br><br>**Constraints**: `>= 8`, `<= 96` |
| `pg_partman_bgw_interval` | `int` | Optional | Sets the time interval to run pg_partman's scheduled tasks.<br><br>**Constraints**: `>= 3600`, `<= 604800` |
| `pg_partman_bgw_role` | `str` | Optional | Controls which role to use for pg_partman's scheduled background tasks. Must consist of alpha-numeric characters, dots, underscores, or dashes. May not start with dash or dot. Maximum of 64 characters.<br><br>**Constraints**: *Maximum Length*: `64`, *Pattern*: `^[_A-Za-z0-9][-._A-Za-z0-9]{0,63}$` |
| `pg_stat_statements_track` | [`PgStatStatementsTrack`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/pg-stat-statements-track.md) | Optional | Controls which statements are counted. Specify 'top' to track top-level statements (those issued directly by clients), 'all' to also track nested statements (such as statements invoked within functions), or 'none' to disable statement statistics collection. The default value is top. |
| `pgbouncer` | [`Pgbouncer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/pgbouncer.md) | Optional | PGBouncer connection pooling settings |
| `shared_buffers_percentage` | `float` | Optional | Percentage of total RAM that the database server uses for shared memory buffers.  Valid range is 20-60 (float), which corresponds to 20% - 60%.  This setting adjusts the shared_buffers configuration value.<br><br>**Constraints**: `>= 20`, `<= 60` |
| `stat_monitor_enable` | `bool` | Optional | Enable the pg_stat_monitor extension. <b>Enabling this extension will cause the cluster to be restarted.</b> When this extension is enabled, pg_stat_statements results for utility commands are unreliable. |
| `synchronous_replication` | [`SynchronousReplication`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/synchronous-replication.md) | Optional | Synchronous replication type. Note that the service plan also needs to support synchronous replication. |
| `temp_file_limit` | `int` | Optional | PostgreSQL temporary file limit in KiB. If -1, sets to unlimited.<br><br>**Constraints**: `>= -1`, `<= 2147483647` |
| `timescaledb` | [`Timescaledb`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/timescaledb.md) | Optional | TimescaleDB extension configuration values |
| `timezone` | `str` | Optional | PostgreSQL service timezone<br><br>**Constraints**: *Maximum Length*: `64` |
| `track_activity_query_size` | `int` | Optional | Specifies the number of bytes reserved to track the currently executing command for each active session.<br><br>**Constraints**: `>= 1024`, `<= 10240` |
| `track_commit_timestamp` | [`TrackCommitTimestamp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/track-commit-timestamp.md) | Optional | Record commit time of transactions. |
| `track_functions` | [`TrackFunctions`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/track-functions.md) | Optional | Enables tracking of function call counts and time used. |
| `track_io_timing` | [`TrackIoTiming`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/track-io-timing.md) | Optional | Enables timing of database I/O calls. This parameter is off by default, because it will repeatedly query the operating system for the current time, which may cause significant overhead on some platforms. |
| `wal_sender_timeout` | `int` | Optional | Terminate replication connections that are inactive for longer than this amount of time, in milliseconds. Setting this value to zero disables the timeout. Must be either 0 or between 5000 and 10800000.<br><br>**Constraints**: `>= 0`, `<= 10800000` |
| `wal_writer_delay` | `int` | Optional | WAL flush interval in milliseconds. Note that setting this value to lower than the default 200ms may negatively impact performance<br><br>**Constraints**: `>= 10`, `<= 200` |
| `work_mem` | `int` | Optional | The maximum amount of memory, in MB, used by a query operation (such as a sort or hash table) before writing to temporary disk files. Default is 1MB + 0.075% of total RAM (up to 32MB).<br><br>**Constraints**: `>= 1`, `<= 1024` |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.config_1 import Config1
from digitaloceanapi.models.default_toast_compression import DefaultToastCompression
from digitaloceanapi.models.log_error_verbosity import LogErrorVerbosity
from digitaloceanapi.models.log_line_prefix import LogLinePrefix
from digitaloceanapi.models.pg_stat_statements_track import PgStatStatementsTrack
from digitaloceanapi.models.synchronous_replication import SynchronousReplication
from digitaloceanapi.models.track_commit_timestamp import TrackCommitTimestamp
from digitaloceanapi.models.track_functions import TrackFunctions
from digitaloceanapi.models.track_io_timing import TrackIoTiming

config_1 = Config1(
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
    work_mem=4,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



