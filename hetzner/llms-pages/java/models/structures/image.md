# Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkltYWdl


# Class Name

`Image`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `BoundTo` | `Integer` | Required | ID of Server the Image is bound to. Only set for Images of type `backup`. | Integer getBoundTo() | setBoundTo(Integer boundTo) |
| `Created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) | String getCreated() | setCreated(String created) |
| `CreatedFrom` | [`CreatedFrom`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/created-from.md) | Required | Information about the Server the Image was created from | CreatedFrom getCreatedFrom() | setCreatedFrom(CreatedFrom createdFrom) |
| `Deleted` | `String` | Required | Point in time where the Image was deleted (in ISO-8601 format) | String getDeleted() | setDeleted(String deleted) |
| `Deprecated` | `String` | Required | Point in time when the Image is considered to be deprecated (in ISO-8601 format) | String getDeprecated() | setDeprecated(String deprecated) |
| `Description` | `String` | Required | Description of the Image | String getDescription() | setDescription(String description) |
| `DiskSize` | `double` | Required | Size of the disk contained in the Image in GB | double getDiskSize() | setDiskSize(double diskSize) |
| `Id` | `int` | Required | ID of the Resource | int getId() | setId(int id) |
| `ImageSize` | `Double` | Required | Size of the Image file in our storage in GB. For snapshot Images this is the value relevant for calculating costs for the Image. | Double getImageSize() | setImageSize(Double imageSize) |
| `Labels` | `Map<String, String>` | Required | User-defined labels (key-value pairs) | Map<String, String> getLabels() | setLabels(Map<String, String> labels) |
| `Name` | `String` | Required | Unique identifier of the Image. This value is only set for system Images. | String getName() | setName(String name) |
| `OsFlavor` | [`OsFlavorEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/enumerations/os-flavor.md) | Required | Flavor of operating system contained in the Image | OsFlavorEnum getOsFlavor() | setOsFlavor(OsFlavorEnum osFlavor) |
| `OsVersion` | `String` | Required | Operating system version | String getOsVersion() | setOsVersion(String osVersion) |
| `Protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/protection.md) | Required | Protection configuration for the Resource | Protection getProtection() | setProtection(Protection protection) |
| `RapidDeploy` | `Boolean` | Optional | Indicates that rapid deploy of the Image is available | Boolean getRapidDeploy() | setRapidDeploy(Boolean rapidDeploy) |
| `Status` | [`Status24Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/enumerations/status-24.md) | Required | Whether the Image can be used or if it's still being created or unavailable | Status24Enum getStatus() | setStatus(Status24Enum status) |
| `Type` | [`Type22Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/enumerations/type-22.md) | Required | Type of the Image | Type22Enum getType() | setType(Type22Enum type) |


# Example

```java
import cloud.hetzner.api.models.CreatedFrom;
import cloud.hetzner.api.models.Image;
import cloud.hetzner.api.models.OsFlavorEnum;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.Status24Enum;
import cloud.hetzner.api.models.Type22Enum;
import java.util.LinkedHashMap;

Image image = new Image.Builder(
    null,
    "2016-01-30T23:55:00+00:00",
    new CreatedFrom.Builder(
        1,
        "Server"
    )
    .build(),
    null,
    "2018-02-28T00:00:00+00:00",
    "Ubuntu 20.04 Standard 64 bit",
    10D,
    42,
    2.3D,
    new LinkedHashMap<String, String>() {{
        put("key0", "labels4");
    }},
    "ubuntu-20.04",
    OsFlavorEnum.UBUNTU,
    "20.04",
    new Protection.Builder(
        false
    )
    .build(),
    Status24Enum.UNAVAILABLE,
    Type22Enum.SNAPSHOT
)
.rapidDeploy(false)
.build();
```



