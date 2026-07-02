# V2 Apps Tiers Instance Sizes Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwSW5zdGFuY2UlMjUyMFNpemVzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type Object.*


# Class Name

`V2AppsTiersInstanceSizesResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `InstanceSize` | [`InstanceSize`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/instance-size.md) | Optional | - | InstanceSize getInstanceSize() | setInstanceSize(InstanceSize instanceSize) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.InstanceSize;
import com.digitalocean.api.models.MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores;
import com.digitalocean.api.models.V2AppsTiersInstanceSizesResponse1;
import java.io.IOException;

V2AppsTiersInstanceSizesResponse1 v2AppsTiersInstanceSizesResponse1 = new V2AppsTiersInstanceSizesResponse1.Builder()
    .instanceSize(new InstanceSize.Builder()
        .cpuType(MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores.DEDICATED)
        .cpus("cpus4")
        .memoryBytes("memory_bytes8")
        .name("name8")
        .slug("slug2")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



