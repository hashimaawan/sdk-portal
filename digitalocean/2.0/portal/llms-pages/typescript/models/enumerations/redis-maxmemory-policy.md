# Redis Maxmemory Policy

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlZGlzTWF4bWVtb3J5UG9saWN5

A string specifying the desired eviction policy for the Redis cluster.

- `noeviction`: Don't evict any data, returns error when memory limit is reached.
- `allkeys_lru:` Evict any key, least recently used (LRU) first.
- `allkeys_random`: Evict keys in a random order.
- `volatile_lru`: Evict keys with expiration only, least recently used (LRU) first.
- `volatile_random`: Evict keys with expiration only in a random order.
- `volatile_ttl`: Evict keys with expiration only, shortest time-to-live (TTL) first.


# Enum Type Name

`RedisMaxmemoryPolicy`


# Fields

| Name |
|  --- |
| `Noeviction` |
| `AllkeysLru` |
| `AllkeysRandom` |
| `VolatileLru` |
| `VolatileRandom` |
| `VolatileTtl` |


# Example

```ts
import { RedisMaxmemoryPolicy } from 'digitalocean-apilib';

const redisMaxmemoryPolicy = RedisMaxmemoryPolicy.AllkeysRandom;
```



