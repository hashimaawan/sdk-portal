# V2 Volumes Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBSZXF1ZXN0MQ

*This model accepts additional fields of type Object.*


# Class Name

`V2VolumesRequest1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CreatedAt` | `String` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the block storage volume was created. | String getCreatedAt() | setCreatedAt(String createdAt) |
| `Description` | `String` | Optional | An optional free-form text field to describe a block storage volume. | String getDescription() | setDescription(String description) |
| `DropletIds` | `List<Integer>` | Optional, Read-only | An array containing the IDs of the Droplets the volume is attached to. Note that at this time, a volume can only be attached to a single Droplet. | List<Integer> getDropletIds() | setDropletIds(List<Integer> dropletIds) |
| `Id` | `String` | Optional, Read-only | The unique identifier for the block storage volume. | String getId() | setId(String id) |
| `Name` | `String` | Required | A human-readable name for the block storage volume. Must be lowercase and be composed only of numbers, letters and "-", up to a limit of 64 characters. The name must begin with a letter. | String getName() | setName(String name) |
| `SizeGigabytes` | `int` | Required | The size of the block storage volume in GiB (1024^3). | int getSizeGigabytes() | setSizeGigabytes(int sizeGigabytes) |
| `Tags` | `List<String>` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. | List<String> getTags() | setTags(List<String> tags) |
| `SnapshotId` | `String` | Optional | The unique identifier for the volume snapshot from which to create the volume. | String getSnapshotId() | setSnapshotId(String snapshotId) |
| `FilesystemType` | `String` | Optional | The name of the filesystem type to be used on the volume. When provided, the volume will automatically be formatted to the specified filesystem type. Currently, the available options are `ext4` and `xfs`. Pre-formatted volumes are automatically mounted when attached to Ubuntu, Debian, Fedora, Fedora Atomic, and CentOS Droplets created on or after April 26, 2018. Attaching pre-formatted volumes to other Droplets is not recommended. | String getFilesystemType() | setFilesystemType(String filesystemType) |
| `FilesystemLabel` | `String` | Optional | **Constraints**: *Maximum Length*: `12` | String getFilesystemLabel() | setFilesystemLabel(String filesystemLabel) |
| `Region` | [`Region2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/region-2.md) | Required | The slug identifier for the region where the resource will initially be  available. | Region2 getRegion() | setRegion(Region2 region) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Region2;
import com.digitalocean.api.models.V2VolumesRequest1;
import java.io.IOException;
import java.util.Arrays;

V2VolumesRequest1 v2VolumesRequest1 = new V2VolumesRequest1.Builder(
    "example",
    10,
    Region2.NYC3
)
.createdAt("2020-03-02T17:00:49Z")
.description("Block store for examples")
.dropletIds(Arrays.asList(

    ))
.id("506f78a4-e098-11e5-ad9f-000f53306ae1")
.tags(Arrays.asList(
        "base-image",
        "prod"
    ))
.snapshotId("b0798135-fb76-11eb-946a-0a58ac146f33")
.filesystemType("ext4")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



