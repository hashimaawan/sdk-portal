# Subscription

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlN1YnNjcmlwdGlvbg

*This model accepts additional fields of type Object.*


# Class Name

`Subscription`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CreatedAt` | `LocalDateTime` | Optional, Read-only | The time at which the subscription was created. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `Tier` | [`Tier1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/tier-1.md) | Optional | - | Tier1 getTier() | setTier(Tier1 tier) |
| `UpdatedAt` | `LocalDateTime` | Optional, Read-only | The time at which the subscription was last updated. | LocalDateTime getUpdatedAt() | setUpdatedAt(LocalDateTime updatedAt) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Subscription;
import com.digitalocean.api.models.Tier1;
import java.io.IOException;

Subscription subscription = new Subscription.Builder()
    .createdAt(DateTimeHelper.fromRfc8601DateTime("2020-01-23T21:19:12Z"))
    .tier(new Tier1.Builder()
        .allowStorageOverage(false)
        .includedBandwidthBytes(46L)
        .includedRepositories(68)
        .includedStorageBytes(112L)
        .monthlyPriceInCents(110)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .updatedAt(DateTimeHelper.fromRfc8601DateTime("2020-11-05T15:53:24Z"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



