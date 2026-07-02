# V2 Droplets Destroy with Associated Resources Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`V2DropletsDestroyWithAssociatedResourcesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FloatingIps` | [`List<FloatingIp>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/floating-ip.md) | Optional | - | List<FloatingIp> getFloatingIps() | setFloatingIps(List<FloatingIp> floatingIps) |
| `ReservedIps` | [`List<FloatingIp>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/floating-ip.md) | Optional | - | List<FloatingIp> getReservedIps() | setReservedIps(List<FloatingIp> reservedIps) |
| `Snapshots` | [`List<FloatingIp>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/floating-ip.md) | Optional | - | List<FloatingIp> getSnapshots() | setSnapshots(List<FloatingIp> snapshots) |
| `VolumeSnapshots` | [`List<FloatingIp>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/floating-ip.md) | Optional | - | List<FloatingIp> getVolumeSnapshots() | setVolumeSnapshots(List<FloatingIp> volumeSnapshots) |
| `Volumes` | [`List<FloatingIp>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/floating-ip.md) | Optional | - | List<FloatingIp> getVolumes() | setVolumes(List<FloatingIp> volumes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.FloatingIp;
import com.digitalocean.api.models.V2DropletsDestroyWithAssociatedResourcesResponse;
import java.io.IOException;
import java.util.Arrays;

V2DropletsDestroyWithAssociatedResourcesResponse v2DropletsDestroyWithAssociatedResourcesResponse = new V2DropletsDestroyWithAssociatedResourcesResponse.Builder()
    .floatingIps(Arrays.asList(
        new FloatingIp.Builder()
            .cost("cost0")
            .id("id2")
            .name("name2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new FloatingIp.Builder()
            .cost("cost0")
            .id("id2")
            .name("name2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .reservedIps(Arrays.asList(
        new FloatingIp.Builder()
            .cost("cost8")
            .id("id0")
            .name("name0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .snapshots(Arrays.asList(
        new FloatingIp.Builder()
            .cost("cost0")
            .id("id2")
            .name("name2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new FloatingIp.Builder()
            .cost("cost0")
            .id("id2")
            .name("name2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .volumeSnapshots(Arrays.asList(
        new FloatingIp.Builder()
            .cost("cost6")
            .id("id8")
            .name("name8")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .volumes(Arrays.asList(
        new FloatingIp.Builder()
            .cost("cost4")
            .id("id6")
            .name("name6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new FloatingIp.Builder()
            .cost("cost4")
            .id("id6")
            .name("name6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



