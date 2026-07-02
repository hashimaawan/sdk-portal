# V2 Databases Eviction Policy Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMEV2aWN0aW9uJTI1MjBQb2xpY3klMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2DatabasesEvictionPolicyRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `evictionPolicy` | [`RedisMaxmemoryPolicy`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/redis-maxmemory-policy.md) | Required | A string specifying the desired eviction policy for the Redis cluster.<br><br>- `noeviction`: Don't evict any data, returns error when memory limit is reached.<br>- `allkeys_lru:` Evict any key, least recently used (LRU) first.<br>- `allkeys_random`: Evict keys in a random order.<br>- `volatile_lru`: Evict keys with expiration only, least recently used (LRU) first.<br>- `volatile_random`: Evict keys with expiration only in a random order.<br>- `volatile_ttl`: Evict keys with expiration only, shortest time-to-live (TTL) first. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  RedisMaxmemoryPolicy,
  V2DatabasesEvictionPolicyRequest,
} from 'digitalocean-apilib';

const v2DatabasesEvictionPolicyRequest: V2DatabasesEvictionPolicyRequest = {
  evictionPolicy: RedisMaxmemoryPolicy.AllkeysLru,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



