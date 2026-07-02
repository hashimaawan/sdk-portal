# Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlZvbHVtZQ

*This model accepts additional fields of type Object.*


# Class Name

`Volume`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CreatedAt` | `String` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the block storage volume was created. | String getCreatedAt() | setCreatedAt(String createdAt) |
| `Description` | `String` | Optional | An optional free-form text field to describe a block storage volume. | String getDescription() | setDescription(String description) |
| `DropletIds` | `List<Integer>` | Optional, Read-only | An array containing the IDs of the Droplets the volume is attached to. Note that at this time, a volume can only be attached to a single Droplet. | List<Integer> getDropletIds() | setDropletIds(List<Integer> dropletIds) |
| `Id` | `String` | Optional, Read-only | The unique identifier for the block storage volume. | String getId() | setId(String id) |
| `Name` | `String` | Optional | A human-readable name for the block storage volume. Must be lowercase and be composed only of numbers, letters and "-", up to a limit of 64 characters. The name must begin with a letter. | String getName() | setName(String name) |
| `SizeGigabytes` | `Integer` | Optional | The size of the block storage volume in GiB (1024^3). | Integer getSizeGigabytes() | setSizeGigabytes(Integer sizeGigabytes) |
| `Tags` | `List<String>` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. | List<String> getTags() | setTags(List<String> tags) |
| `FilesystemLabel` | `String` | Optional | The label currently applied to the filesystem. | String getFilesystemLabel() | setFilesystemLabel(String filesystemLabel) |
| `FilesystemType` | `String` | Optional | The type of filesystem currently in-use on the volume. | String getFilesystemType() | setFilesystemType(String filesystemType) |
| `Region` | [`Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/region.md) | Optional, Read-only | - | Region getRegion() | setRegion(Region region) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Region;
import com.digitalocean.api.models.Volume;
import java.io.IOException;
import java.util.Arrays;

Volume volume = new Volume.Builder()
    .createdAt("2020-03-02T17:00:49Z")
    .description("Block store for examples")
    .dropletIds(Arrays.asList(

    ))
    .id("506f78a4-e098-11e5-ad9f-000f53306ae1")
    .name("example")
    .sizeGigabytes(10)
    .tags(Arrays.asList(
        "base-image",
        "prod"
    ))
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
    .build();
```



