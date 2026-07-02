# V2 Apps Tiers Instance Sizes Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwSW5zdGFuY2UlMjUyMFNpemVzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`V2AppsTiersInstanceSizesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DiscountPercent` | `Double` | Optional | - | Double getDiscountPercent() | setDiscountPercent(Double discountPercent) |
| `InstanceSizes` | [`List<InstanceSize>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/instance-size.md) | Optional | - | List<InstanceSize> getInstanceSizes() | setInstanceSizes(List<InstanceSize> instanceSizes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.InstanceSize;
import com.digitalocean.api.models.MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores;
import com.digitalocean.api.models.V2AppsTiersInstanceSizesResponse;
import java.io.IOException;
import java.util.Arrays;

V2AppsTiersInstanceSizesResponse v2AppsTiersInstanceSizesResponse = new V2AppsTiersInstanceSizesResponse.Builder()
    .discountPercent(2.32D)
    .instanceSizes(Arrays.asList(
        new InstanceSize.Builder()
            .cpuType(MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores.DEDICATED)
            .cpus("cpus4")
            .memoryBytes("memory_bytes8")
            .name("name8")
            .slug("slug8")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



