# Tier

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlRpZXI

*This model accepts additional fields of type Object.*


# Class Name

`Tier`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `BuildSeconds` | `String` | Optional | - | String getBuildSeconds() | setBuildSeconds(String buildSeconds) |
| `EgressBandwidthBytes` | `String` | Optional | - | String getEgressBandwidthBytes() | setEgressBandwidthBytes(String egressBandwidthBytes) |
| `Name` | `String` | Optional | - | String getName() | setName(String name) |
| `Slug` | `String` | Optional | - | String getSlug() | setSlug(String slug) |
| `StorageBytes` | `String` | Optional | - | String getStorageBytes() | setStorageBytes(String storageBytes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Tier;
import java.io.IOException;

Tier tier = new Tier.Builder()
    .buildSeconds("233")
    .egressBandwidthBytes("123")
    .name("test")
    .slug("test")
    .storageBytes("10000000")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



