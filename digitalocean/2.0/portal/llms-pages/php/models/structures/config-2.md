# Config 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkNvbmZpZzI

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Config2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `redisAclChannelsDefault` | [`?string(RedisAclChannelsDefault)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/redis-acl-channels-default.md) | Optional | Determines default pub/sub channels' ACL for new users if ACL is not supplied. When this option is not defined, all_channels is assumed to keep backward compatibility. This option doesn't affect Redis configuration acl-pubsub-default. | getRedisAclChannelsDefault(): ?string | setRedisAclChannelsDefault(?string redisAclChannelsDefault): void |
| `redisIoThreads` | `?int` | Optional | Redis IO thread count<br><br>**Constraints**: `>= 1`, `<= 32` | getRedisIoThreads(): ?int | setRedisIoThreads(?int redisIoThreads): void |
| `redisLfuDecayTime` | `?int` | Optional | LFU maxmemory-policy counter decay time in minutes<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1`, `<= 120` | getRedisLfuDecayTime(): ?int | setRedisLfuDecayTime(?int redisLfuDecayTime): void |
| `redisLfuLogFactor` | `?int` | Optional | Counter logarithm factor for volatile-lfu and allkeys-lfu maxmemory-policies<br><br>**Default**: `10`<br><br>**Constraints**: `>= 0`, `<= 100` | getRedisLfuLogFactor(): ?int | setRedisLfuLogFactor(?int redisLfuLogFactor): void |
| `redisMaxmemoryPolicy` | [`?string(RedisMaxmemoryPolicy)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/redis-maxmemory-policy.md) | Optional | A string specifying the desired eviction policy for the Redis cluster.<br><br>- `noeviction`: Don't evict any data, returns error when memory limit is reached.<br>- `allkeys_lru:` Evict any key, least recently used (LRU) first.<br>- `allkeys_random`: Evict keys in a random order.<br>- `volatile_lru`: Evict keys with expiration only, least recently used (LRU) first.<br>- `volatile_random`: Evict keys with expiration only in a random order.<br>- `volatile_ttl`: Evict keys with expiration only, shortest time-to-live (TTL) first. | getRedisMaxmemoryPolicy(): ?string | setRedisMaxmemoryPolicy(?string redisMaxmemoryPolicy): void |
| `redisNotifyKeyspaceEvents` | `?string` | Optional | Set notify-keyspace-events option<br><br>**Constraints**: *Maximum Length*: `32`, *Pattern*: `^[KEg\$lshzxeA]*$` | getRedisNotifyKeyspaceEvents(): ?string | setRedisNotifyKeyspaceEvents(?string redisNotifyKeyspaceEvents): void |
| `redisNumberOfDatabases` | `?int` | Optional | Set number of redis databases. Changing this will cause a restart of redis service.<br><br>**Constraints**: `>= 1`, `<= 128` | getRedisNumberOfDatabases(): ?int | setRedisNumberOfDatabases(?int redisNumberOfDatabases): void |
| `redisPersistence` | [`?string(RedisPersistence)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/redis-persistence.md) | Optional | When persistence is 'rdb', Redis does RDB dumps each 10 minutes if any key is changed. Also RDB dumps are done according to backup schedule for backup purposes. When persistence is 'off', no RDB dumps and backups are done, so data can be lost at any moment if service is restarted for any reason, or if service is powered off. Also service can't be forked. | getRedisPersistence(): ?string | setRedisPersistence(?string redisPersistence): void |
| `redisPubsubClientOutputBufferLimit` | `?int` | Optional | Set output buffer limit for pub / sub clients in MB. The value is the hard limit, the soft limit is 1/4 of the hard limit. When setting the limit, be mindful of the available memory in the selected service plan.<br><br>**Constraints**: `>= 32`, `<= 512` | getRedisPubsubClientOutputBufferLimit(): ?int | setRedisPubsubClientOutputBufferLimit(?int redisPubsubClientOutputBufferLimit): void |
| `redisSsl` | `?bool` | Optional | Require SSL to access Redis<br><br>**Default**: `true` | getRedisSsl(): ?bool | setRedisSsl(?bool redisSsl): void |
| `redisTimeout` | `?int` | Optional | Redis idle connection timeout in seconds<br><br>**Default**: `300`<br><br>**Constraints**: `>= 0`, `<= 31536000` | getRedisTimeout(): ?int | setRedisTimeout(?int redisTimeout): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Config2Builder;
use DigitalOceanApiLib\Models\RedisAclChannelsDefault;
use DigitalOceanApiLib\Models\RedisMaxmemoryPolicy;
use DigitalOceanApiLib\Models\RedisPersistence;
use DigitalOceanApiLib\ApiHelper;

$config2 = Config2Builder::init()
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
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



