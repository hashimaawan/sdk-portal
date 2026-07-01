# Create Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZVZvbHVtZVJlcXVlc3Q


# Class Name

`CreateVolumeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Automount` | `Boolean` | Optional | Auto-mount Volume after attach. `server` must be provided. | Boolean getAutomount() | setAutomount(Boolean automount) |
| `Format` | `String` | Optional | Format Volume after creation. One of: `xfs`, `ext4` | String getFormat() | setFormat(String format) |
| `Labels` | `Object` | Optional | User-defined labels (key-value pairs) | Object getLabels() | setLabels(Object labels) |
| `Location` | `String` | Optional | Location to create the Volume in (can be omitted if Server is specified) | String getLocation() | setLocation(String location) |
| `Name` | `String` | Required | Name of the volume | String getName() | setName(String name) |
| `Server` | `Integer` | Optional | Server to which to attach the Volume once it's created (Volume will be created in the same Location as the server) | Integer getServer() | setServer(Integer server) |
| `Size` | `int` | Required | Size of the Volume in GB | int getSize() | setSize(int size) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.CreateVolumeRequest;
import java.io.IOException;

CreateVolumeRequest createVolumeRequest = new CreateVolumeRequest.Builder(
    "databases-storage",
    42
)
.automount(false)
.format("xfs")
.labels(ApiHelper.deserialize("{\"labelkey\":\"value\"}"))
.location("nbg1")
.server(182)
.build();
```



