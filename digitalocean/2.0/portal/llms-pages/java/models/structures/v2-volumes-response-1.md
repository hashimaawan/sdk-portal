# V2 Volumes Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type Object.*


# Class Name

`V2VolumesResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Volume` | [`Volume`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/volume.md) | Optional | - | Volume getVolume() | setVolume(Volume volume) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Region;
import com.digitalocean.api.models.V2VolumesResponse1;
import com.digitalocean.api.models.Volume;
import java.io.IOException;
import java.util.Arrays;

V2VolumesResponse1 v2VolumesResponse1 = new V2VolumesResponse1.Builder()
    .volume(new Volume.Builder()
        .createdAt("2020-03-02T17:00:49Z")
        .description("Block store for examples")
        .dropletIds(Arrays.asList(

        ))
        .id("506f78a4-e098-11e5-ad9f-000f53306ae1")
        .name("example")
        .sizeGigabytes(10)
        .filesystemLabel("example")
        .filesystemType("ext4")
        .region(new Region.Builder(
            true,
            Arrays.asList(
                "private_networking",
                "backups",
                "ipv6",
                "metadata"
            ),
            "New York 1",
            Arrays.asList(
                "s-1vcpu-1gb",
                "s-1vcpu-2gb",
                "s-1vcpu-3gb",
                "s-2vcpu-2gb",
                "s-3vcpu-1gb",
                "s-2vcpu-4gb",
                "s-4vcpu-8gb",
                "s-6vcpu-16gb",
                "s-8vcpu-32gb",
                "s-12vcpu-48gb",
                "s-16vcpu-64gb",
                "s-20vcpu-96gb",
                "s-24vcpu-128gb",
                "s-32vcpu-192gb"
            ),
            "nyc1"
        )
        .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



