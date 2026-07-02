# V2 Databases Config Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMENvbmZpZyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DatabasesConfigResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `config` | [Config](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/config.md) \| [Config1](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/config-1.md) \| [Config2](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/config-2.md) | Required | This is a container for any-of cases. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.config import Config
from digitaloceanapi.models.internal_tmp_mem_storage_engine import InternalTmpMemStorageEngine
from digitaloceanapi.models.v_2_databases_config_response import V2DatabasesConfigResponse

v_2_databases_config_response = V2DatabasesConfigResponse(
    config=Config(
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
        wait_timeout=28800,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



