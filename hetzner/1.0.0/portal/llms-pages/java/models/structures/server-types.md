# Server Types

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlclR5cGVz

The Server types the Datacenter can handle


# Class Name

`ServerTypes`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Available` | `List<Double>` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left | List<Double> getAvailable() | setAvailable(List<Double> available) |
| `AvailableForMigration` | `List<Double>` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left | List<Double> getAvailableForMigration() | setAvailableForMigration(List<Double> availableForMigration) |
| `Supported` | `List<Double>` | Required | IDs of Server types that are supported in the Datacenter | List<Double> getSupported() | setSupported(List<Double> supported) |


# Example

```java
import cloud.hetzner.api.models.ServerTypes;
import java.util.Arrays;

ServerTypes serverTypes = new ServerTypes.Builder(
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
.build();
```



