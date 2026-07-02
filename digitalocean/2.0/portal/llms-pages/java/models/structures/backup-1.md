# Backup 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkJhY2t1cDE

*This model accepts additional fields of type Object.*


# Class Name

`Backup1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Id` | `int` | Required | The unique identifier for the snapshot or backup. | int getId() | setId(int id) |
| `CreatedAt` | `LocalDateTime` | Required | A time value given in ISO8601 combined date and time format that represents when the snapshot was created. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `MinDiskSize` | `int` | Required | The minimum size in GB required for a volume or Droplet to use this snapshot. | int getMinDiskSize() | setMinDiskSize(int minDiskSize) |
| `Name` | `String` | Required | A human-readable name for the snapshot. | String getName() | setName(String name) |
| `Regions` | `List<String>` | Required | An array of the regions that the snapshot is available in. The regions are represented by their identifying slug values. | List<String> getRegions() | setRegions(List<String> regions) |
| `SizeGigabytes` | `double` | Required | The billable size of the snapshot in gigabytes. | double getSizeGigabytes() | setSizeGigabytes(double sizeGigabytes) |
| `Type` | [`Type13`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/type-13.md) | Required | Describes the kind of image. It may be one of `snapshot` or `backup`. This specifies whether an image is a user-generated Droplet snapshot or automatically created Droplet backup. | Type13 getType() | setType(Type13 type) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Backup1;
import com.digitalocean.api.models.Type13;
import java.io.IOException;
import java.util.Arrays;

Backup1 backup1 = new Backup1.Builder(
    6372321,
    DateTimeHelper.fromRfc8601DateTime("2020-07-28T16:47:44Z"),
    25,
    "web-01-1595954862243",
    Arrays.asList(
        "nyc3",
        "sfo3"
    ),
    2.34D,
    Type13.SNAPSHOT
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



