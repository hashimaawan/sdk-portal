# Registry

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlJlZ2lzdHJ5

*This model accepts additional fields of type Object.*


# Class Name

`Registry`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CreatedAt` | `LocalDateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the registry was created. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `Name` | `String` | Optional | A globally unique name for the container registry. Must be lowercase and be composed only of numbers, letters and `-`, up to a limit of 63 characters.<br><br>**Constraints**: *Maximum Length*: `63`, *Pattern*: `^[a-z0-9-]{1,63}$` | String getName() | setName(String name) |
| `Region` | `String` | Optional | Slug of the region where registry data is stored | String getRegion() | setRegion(String region) |
| `StorageUsageBytes` | `Integer` | Optional, Read-only | The amount of storage used in the registry in bytes. | Integer getStorageUsageBytes() | setStorageUsageBytes(Integer storageUsageBytes) |
| `StorageUsageBytesUpdatedAt` | `LocalDateTime` | Optional, Read-only | The time at which the storage usage was updated. Storage usage is calculated asynchronously, and may not immediately reflect pushes to the registry. | LocalDateTime getStorageUsageBytesUpdatedAt() | setStorageUsageBytesUpdatedAt(LocalDateTime storageUsageBytesUpdatedAt) |
| `Subscription` | [`Subscription`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/subscription.md) | Optional | - | Subscription getSubscription() | setSubscription(Subscription subscription) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Registry;
import java.io.IOException;

Registry registry = new Registry.Builder()
    .createdAt(DateTimeHelper.fromRfc8601DateTime("2020-03-21T16:02:37Z"))
    .name("example")
    .region("fra1")
    .storageUsageBytes(29393920)
    .storageUsageBytesUpdatedAt(DateTimeHelper.fromRfc8601DateTime("2020-11-04T21:39:49.530562231Z"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



