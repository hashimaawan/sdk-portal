# Tier 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlRpZXIx

*This model accepts additional fields of type Object.*


# Class Name

`Tier1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AllowStorageOverage` | `Boolean` | Optional | A boolean indicating whether the subscription tier supports additional storage above what is included in the base plan at an additional cost per GiB used. | Boolean getAllowStorageOverage() | setAllowStorageOverage(Boolean allowStorageOverage) |
| `IncludedBandwidthBytes` | `Long` | Optional | The amount of outbound data transfer included in the subscription tier in bytes. | Long getIncludedBandwidthBytes() | setIncludedBandwidthBytes(Long includedBandwidthBytes) |
| `IncludedRepositories` | `Integer` | Optional | The number of repositories included in the subscription tier. `0` indicates that the subscription tier includes unlimited repositories. | Integer getIncludedRepositories() | setIncludedRepositories(Integer includedRepositories) |
| `IncludedStorageBytes` | `Long` | Optional | The amount of storage included in the subscription tier in bytes. | Long getIncludedStorageBytes() | setIncludedStorageBytes(Long includedStorageBytes) |
| `MonthlyPriceInCents` | `Integer` | Optional | The monthly cost of the subscription tier in cents. | Integer getMonthlyPriceInCents() | setMonthlyPriceInCents(Integer monthlyPriceInCents) |
| `Name` | `String` | Optional | The name of the subscription tier. | String getName() | setName(String name) |
| `Slug` | `String` | Optional | The slug identifier of the subscription tier. | String getSlug() | setSlug(String slug) |
| `StorageOveragePriceInCents` | `Integer` | Optional | The price paid in cents per GiB for additional storage beyond what is included in the subscription plan. | Integer getStorageOveragePriceInCents() | setStorageOveragePriceInCents(Integer storageOveragePriceInCents) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Tier1;
import java.io.IOException;

Tier1 tier1 = new Tier1.Builder()
    .allowStorageOverage(true)
    .includedBandwidthBytes(5368709120L)
    .includedRepositories(5)
    .includedStorageBytes(5368709120L)
    .monthlyPriceInCents(500)
    .name("Basic")
    .slug("basic")
    .storageOveragePriceInCents(2)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



