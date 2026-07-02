# V2 Apps Tiers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type Object.*


# Class Name

`V2AppsTiersResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Tier` | [`Tier`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/tier.md) | Optional | - | Tier getTier() | setTier(Tier tier) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Tier;
import com.digitalocean.api.models.V2AppsTiersResponse1;
import java.io.IOException;

V2AppsTiersResponse1 v2AppsTiersResponse1 = new V2AppsTiersResponse1.Builder()
    .tier(new Tier.Builder()
        .buildSeconds("build_seconds0")
        .egressBandwidthBytes("egress_bandwidth_bytes6")
        .name("name2")
        .slug("slug4")
        .storageBytes("storage_bytes0")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



