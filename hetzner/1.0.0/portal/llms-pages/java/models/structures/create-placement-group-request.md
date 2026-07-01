# Create Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZVBsYWNlbWVudEdyb3VwUmVxdWVzdA


# Class Name

`CreatePlacementGroupRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Labels` | `Object` | Optional | User-defined labels (key-value pairs) | Object getLabels() | setLabels(Object labels) |
| `Name` | `String` | Required | Name of the PlacementGroup | String getName() | setName(String name) |
| `Type` | `String` | Required, Constant | Define the Placement Group Type.<br><br>**Value**: `"spread"` | String getType() | setType(String type) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.CreatePlacementGroupRequest;
import java.io.IOException;

CreatePlacementGroupRequest createPlacementGroupRequest = new CreatePlacementGroupRequest.Builder(
    "my Placement Group",
    "spread"
)
.labels(ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



