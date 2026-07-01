# Server Types

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlclR5cGVz

The Server types the Datacenter can handle

*This model accepts additional fields of type Object.*


# Class Name

`ServerTypes`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Available` | `List<Double>` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left | List<Double> getAvailable() | setAvailable(List<Double> available) |
| `AvailableForMigration` | `List<Double>` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left | List<Double> getAvailableForMigration() | setAvailableForMigration(List<Double> availableForMigration) |
| `Supported` | `List<Double>` | Required | IDs of Server types that are supported in the Datacenter | List<Double> getSupported() | setSupported(List<Double> supported) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.ServerTypes;
import java.io.IOException;
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
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



