# Config 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkNvbmZpZzI

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Config2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `RedisAclChannelsDefault` | [`*models.RedisAclChannelsDefault`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/redis-acl-channels-default.md) | Optional | Determines default pub/sub channels' ACL for new users if ACL is not supplied. When this option is not defined, all_channels is assumed to keep backward compatibility. This option doesn't affect Redis configuration acl-pubsub-default. |
| `RedisIoThreads` | `*int` | Optional | Redis IO thread count<br><br>**Constraints**: `>= 1`, `<= 32` |
| `RedisLfuDecayTime` | `*int` | Optional | LFU maxmemory-policy counter decay time in minutes<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1`, `<= 120` |
| `RedisLfuLogFactor` | `*int` | Optional | Counter logarithm factor for volatile-lfu and allkeys-lfu maxmemory-policies<br><br>**Default**: `10`<br><br>**Constraints**: `>= 0`, `<= 100` |
| `RedisMaxmemoryPolicy` | [`*models.RedisMaxmemoryPolicy`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/redis-maxmemory-policy.md) | Optional | A string specifying the desired eviction policy for the Redis cluster.<br><br>- `noeviction`: Don't evict any data, returns error when memory limit is reached.<br>- `allkeys_lru:` Evict any key, least recently used (LRU) first.<br>- `allkeys_random`: Evict keys in a random order.<br>- `volatile_lru`: Evict keys with expiration only, least recently used (LRU) first.<br>- `volatile_random`: Evict keys with expiration only in a random order.<br>- `volatile_ttl`: Evict keys with expiration only, shortest time-to-live (TTL) first. |
| `RedisNotifyKeyspaceEvents` | `*string` | Optional | Set notify-keyspace-events option<br><br>**Constraints**: *Maximum Length*: `32`, *Pattern*: `^[KEg\$lshzxeA]*$` |
| `RedisNumberOfDatabases` | `*int` | Optional | Set number of redis databases. Changing this will cause a restart of redis service.<br><br>**Constraints**: `>= 1`, `<= 128` |
| `RedisPersistence` | [`*models.RedisPersistence`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/redis-persistence.md) | Optional | When persistence is 'rdb', Redis does RDB dumps each 10 minutes if any key is changed. Also RDB dumps are done according to backup schedule for backup purposes. When persistence is 'off', no RDB dumps and backups are done, so data can be lost at any moment if service is restarted for any reason, or if service is powered off. Also service can't be forked. |
| `RedisPubsubClientOutputBufferLimit` | `*int` | Optional | Set output buffer limit for pub / sub clients in MB. The value is the hard limit, the soft limit is 1/4 of the hard limit. When setting the limit, be mindful of the available memory in the selected service plan.<br><br>**Constraints**: `>= 32`, `<= 512` |
| `RedisSsl` | `*bool` | Optional | Require SSL to access Redis<br><br>**Default**: `true` |
| `RedisTimeout` | `*int` | Optional | Redis idle connection timeout in seconds<br><br>**Default**: `300`<br><br>**Constraints**: `>= 0`, `<= 31536000` |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    config2 := models.Config2{
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
        AdditionalProperties:               map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



