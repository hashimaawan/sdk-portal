# Datacenter 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkRhdGFjZW50ZXIy

Datacenter this Primary IP is located at


# Class Name

`Datacenter2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Description` | `String` | Required | Description of the Datacenter | String getDescription() | setDescription(String description) |
| `Id` | `int` | Required | ID of the Resource | int getId() | setId(int id) |
| `Location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/location.md) | Required | - | Location getLocation() | setLocation(Location location) |
| `Name` | `String` | Required | Unique identifier of the Datacenter | String getName() | setName(String name) |
| `ServerTypes` | [`ServerTypes`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/server-types.md) | Required | The Server types the Datacenter can handle | ServerTypes getServerTypes() | setServerTypes(ServerTypes serverTypes) |


# Example

```java
import cloud.hetzner.api.models.Datacenter2;
import cloud.hetzner.api.models.Location;
import cloud.hetzner.api.models.ServerTypes;
import java.util.Arrays;

Datacenter2 datacenter2 = new Datacenter2.Builder(
    "Falkenstein DC Park 8",
    42,
    new Location.Builder(
        "Falkenstein",
        "DE",
        "Falkenstein DC Park 1",
        1D,
        50.47612D,
        12.370071D,
        "fsn1",
        "eu-central"
    )
    .build(),
    "fsn1-dc8",
    new ServerTypes.Builder(
        Arrays.asList(
            1D,
            2D,
            3D
        ),
        Arrays.asList(
            1D,
            2D,
            3D
        ),
        Arrays.asList(
            1D,
            2D,
            3D
        )
    )
    .build()
)
.build();
```



