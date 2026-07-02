# V2 Databases Eviction Policy Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMEV2aWN0aW9uJTI1MjBQb2xpY3klMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesEvictionPolicyRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `EvictionPolicy` | [`RedisMaxmemoryPolicy`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/redis-maxmemory-policy.md) | Required | A string specifying the desired eviction policy for the Redis cluster.<br><br>- `noeviction`: Don't evict any data, returns error when memory limit is reached.<br>- `allkeys_lru:` Evict any key, least recently used (LRU) first.<br>- `allkeys_random`: Evict keys in a random order.<br>- `volatile_lru`: Evict keys with expiration only, least recently used (LRU) first.<br>- `volatile_random`: Evict keys with expiration only in a random order.<br>- `volatile_ttl`: Evict keys with expiration only, shortest time-to-live (TTL) first. | RedisMaxmemoryPolicy getEvictionPolicy() | setEvictionPolicy(RedisMaxmemoryPolicy evictionPolicy) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.RedisMaxmemoryPolicy;
import com.digitalocean.api.models.V2DatabasesEvictionPolicyRequest;
import java.io.IOException;

V2DatabasesEvictionPolicyRequest v2DatabasesEvictionPolicyRequest = new V2DatabasesEvictionPolicyRequest.Builder(
    RedisMaxmemoryPolicy.ALLKEYS_LRU
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



