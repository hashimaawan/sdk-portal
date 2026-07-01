# Volume 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlZvbHVtZTE

*This model accepts additional fields of type Object.*


# Class Name

`Volume1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) | String getCreated() | setCreated(String created) |
| `Format` | `String` | Required | Filesystem of the Volume if formatted on creation, null if not formatted on creation | String getFormat() | setFormat(String format) |
| `Id` | `int` | Required | ID of the Resource | int getId() | setId(int id) |
| `Labels` | `Map<String, String>` | Required | User-defined labels (key-value pairs) | Map<String, String> getLabels() | setLabels(Map<String, String> labels) |
| `LinuxDevice` | `String` | Required | Device path on the file system for the Volume | String getLinuxDevice() | setLinuxDevice(String linuxDevice) |
| `Location` | [`Location16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/location-16.md) | Required | Location of the Volume. Volume can only be attached to Servers in the same Location. | Location16 getLocation() | setLocation(Location16 location) |
| `Name` | `String` | Required | Name of the Resource. Must be unique per Project. | String getName() | setName(String name) |
| `Protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/protection.md) | Required | Protection configuration for the Resource | Protection getProtection() | setProtection(Protection protection) |
| `Server` | `Integer` | Required | ID of the Server the Volume is attached to, null if it is not attached at all | Integer getServer() | setServer(Integer server) |
| `Size` | `double` | Required | Size in GB of the Volume | double getSize() | setSize(double size) |
| `Status` | [`Status113`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/status-113.md) | Required | Current status of the Volume | Status113 getStatus() | setStatus(Status113 status) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Location16;
import cloud.hetzner.api.models.Protection;
import cloud.hetzner.api.models.Status113;
import cloud.hetzner.api.models.Volume1;
import java.io.IOException;
import java.util.LinkedHashMap;

Volume1 volume1 = new Volume1.Builder(
    "2016-01-30T23:55:00+00:00",
    "xfs",
    42,
    new LinkedHashMap<String, String>() {{
        put("key0", "labels8");
    }},
    "/dev/disk/by-id/scsi-0HC_Volume_4711",
    new Location16.Builder(
        "Falkenstein",
        "DE",
        "Falkenstein DC Park 1",
        1D,
        50.47612D,
        12.370071D,
        "fsn1",
        "eu-central"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build(),
    "my-resource",
    new Protection.Builder(
        false
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build(),
    12,
    42D,
    Status113.AVAILABLE
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



