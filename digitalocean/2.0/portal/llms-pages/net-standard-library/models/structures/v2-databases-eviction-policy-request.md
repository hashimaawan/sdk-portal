# V2 Databases Eviction Policy Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMEV2aWN0aW9uJTI1MjBQb2xpY3klMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2DatabasesEvictionPolicyRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `EvictionPolicy` | [`RedisMaxmemoryPolicy`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/redis-maxmemory-policy.md) | Required | A string specifying the desired eviction policy for the Redis cluster.<br><br>- `noeviction`: Don't evict any data, returns error when memory limit is reached.<br>- `allkeys_lru:` Evict any key, least recently used (LRU) first.<br>- `allkeys_random`: Evict keys in a random order.<br>- `volatile_lru`: Evict keys with expiration only, least recently used (LRU) first.<br>- `volatile_random`: Evict keys with expiration only in a random order.<br>- `volatile_ttl`: Evict keys with expiration only, shortest time-to-live (TTL) first. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

V2DatabasesEvictionPolicyRequest v2DatabasesEvictionPolicyRequest = new V2DatabasesEvictionPolicyRequest
{
    EvictionPolicy = RedisMaxmemoryPolicy.AllkeysLru,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



