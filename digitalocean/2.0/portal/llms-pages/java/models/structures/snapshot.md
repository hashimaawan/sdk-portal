# Snapshot

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlNuYXBzaG90

*This model accepts additional fields of type Object.*


# Class Name

`Snapshot`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `String` | Required | The unique identifier for the snapshot. | String getId() | setId(String id) |
| `CreatedAt` | `LocalDateTime` | Required | A time value given in ISO8601 combined date and time format that represents when the snapshot was created. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `MinDiskSize` | `int` | Required | The minimum size in GB required for a volume or Droplet to use this snapshot. | int getMinDiskSize() | setMinDiskSize(int minDiskSize) |
| `Name` | `String` | Required | A human-readable name for the snapshot. | String getName() | setName(String name) |
| `Regions` | `List<String>` | Required | An array of the regions that the snapshot is available in. The regions are represented by their identifying slug values. | List<String> getRegions() | setRegions(List<String> regions) |
| `SizeGigabytes` | `double` | Required | The billable size of the snapshot in gigabytes. | double getSizeGigabytes() | setSizeGigabytes(double sizeGigabytes) |
| `ResourceId` | `String` | Required | The unique identifier for the resource that the snapshot originated from. | String getResourceId() | setResourceId(String resourceId) |
| `ResourceType` | [`ResourceType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/resource-type-1.md) | Required | The type of resource that the snapshot originated from. | ResourceType1 getResourceType() | setResourceType(ResourceType1 resourceType) |
| `Tags` | `List<String>` | Required | An array of Tags the snapshot has been tagged with. | List<String> getTags() | setTags(List<String> tags) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.ResourceType1;
import com.digitalocean.api.models.Snapshot;
import java.io.IOException;
import java.util.Arrays;

Snapshot snapshot = new Snapshot.Builder(
    "6372321",
    DateTimeHelper.fromRfc8601DateTime("2020-07-28T16:47:44Z"),
    25,
    "web-01-1595954862243",
    Arrays.asList(
        "nyc3",
        "sfo3"
    ),
    2.34D,
    "200776916",
    ResourceType1.DROPLET,
    Arrays.asList(
        "web",
        "env:prod"
    )
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



