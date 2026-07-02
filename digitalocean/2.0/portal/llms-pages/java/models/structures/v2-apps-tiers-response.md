# V2 Apps Tiers Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`V2AppsTiersResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Tiers` | [`List<Tier>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/tier.md) | Optional | - | List<Tier> getTiers() | setTiers(List<Tier> tiers) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Tier;
import com.digitalocean.api.models.V2AppsTiersResponse;
import java.io.IOException;
import java.util.Arrays;

V2AppsTiersResponse v2AppsTiersResponse = new V2AppsTiersResponse.Builder()
    .tiers(Arrays.asList(
        new Tier.Builder()
            .buildSeconds("build_seconds4")
            .egressBandwidthBytes("egress_bandwidth_bytes2")
            .name("name8")
            .slug("slug8")
            .storageBytes("storage_bytes4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Tier.Builder()
            .buildSeconds("build_seconds4")
            .egressBandwidthBytes("egress_bandwidth_bytes2")
            .name("name8")
            .slug("slug8")
            .storageBytes("storage_bytes4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Tier.Builder()
            .buildSeconds("build_seconds4")
            .egressBandwidthBytes("egress_bandwidth_bytes2")
            .name("name8")
            .slug("slug8")
            .storageBytes("storage_bytes4")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



