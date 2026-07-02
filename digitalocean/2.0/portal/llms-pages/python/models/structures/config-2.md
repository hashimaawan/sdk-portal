# Config 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkNvbmZpZzI

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Config2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `redis_acl_channels_default` | [`RedisAclChannelsDefault`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/redis-acl-channels-default.md) | Optional | Determines default pub/sub channels' ACL for new users if ACL is not supplied. When this option is not defined, all_channels is assumed to keep backward compatibility. This option doesn't affect Redis configuration acl-pubsub-default. |
| `redis_io_threads` | `int` | Optional | Redis IO thread count<br><br>**Constraints**: `>= 1`, `<= 32` |
| `redis_lfu_decay_time` | `int` | Optional | LFU maxmemory-policy counter decay time in minutes<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1`, `<= 120` |
| `redis_lfu_log_factor` | `int` | Optional | Counter logarithm factor for volatile-lfu and allkeys-lfu maxmemory-policies<br><br>**Default**: `10`<br><br>**Constraints**: `>= 0`, `<= 100` |
| `redis_maxmemory_policy` | [`RedisMaxmemoryPolicy`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/redis-maxmemory-policy.md) | Optional | A string specifying the desired eviction policy for the Redis cluster.<br><br>- `noeviction`: Don't evict any data, returns error when memory limit is reached.<br>- `allkeys_lru:` Evict any key, least recently used (LRU) first.<br>- `allkeys_random`: Evict keys in a random order.<br>- `volatile_lru`: Evict keys with expiration only, least recently used (LRU) first.<br>- `volatile_random`: Evict keys with expiration only in a random order.<br>- `volatile_ttl`: Evict keys with expiration only, shortest time-to-live (TTL) first. |
| `redis_notify_keyspace_events` | `str` | Optional | Set notify-keyspace-events option<br><br>**Constraints**: *Maximum Length*: `32`, *Pattern*: `^[KEg\$lshzxeA]*$` |
| `redis_number_of_databases` | `int` | Optional | Set number of redis databases. Changing this will cause a restart of redis service.<br><br>**Constraints**: `>= 1`, `<= 128` |
| `redis_persistence` | [`RedisPersistence`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/redis-persistence.md) | Optional | When persistence is 'rdb', Redis does RDB dumps each 10 minutes if any key is changed. Also RDB dumps are done according to backup schedule for backup purposes. When persistence is 'off', no RDB dumps and backups are done, so data can be lost at any moment if service is restarted for any reason, or if service is powered off. Also service can't be forked. |
| `redis_pubsub_client_output_buffer_limit` | `int` | Optional | Set output buffer limit for pub / sub clients in MB. The value is the hard limit, the soft limit is 1/4 of the hard limit. When setting the limit, be mindful of the available memory in the selected service plan.<br><br>**Constraints**: `>= 32`, `<= 512` |
| `redis_ssl` | `bool` | Optional | Require SSL to access Redis<br><br>**Default**: `True` |
| `redis_timeout` | `int` | Optional | Redis idle connection timeout in seconds<br><br>**Default**: `300`<br><br>**Constraints**: `>= 0`, `<= 31536000` |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.config_2 import Config2
from digitaloceanapi.models.redis_acl_channels_default import RedisAclChannelsDefault
from digitaloceanapi.models.redis_maxmemory_policy import RedisMaxmemoryPolicy
from digitaloceanapi.models.redis_persistence import RedisPersistence

config_2 = Config2(
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
    redis_timeout=300,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



