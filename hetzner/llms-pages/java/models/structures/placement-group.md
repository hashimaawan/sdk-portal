# Placement Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3Vw


# Class Name

`PlacementGroup`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) | String getCreated() | setCreated(String created) |
| `Id` | `int` | Required | ID of the Resource | int getId() | setId(int id) |
| `Labels` | `Map<String, String>` | Required | User-defined labels (key-value pairs) | Map<String, String> getLabels() | setLabels(Map<String, String> labels) |
| `Name` | `String` | Required | Name of the Resource. Must be unique per Project. | String getName() | setName(String name) |
| `Servers` | `List<Integer>` | Required | Array of IDs of Servers that are part of this Placement Group | List<Integer> getServers() | setServers(List<Integer> servers) |
| `Type` | `String` | Required, Constant | Type of the Placement Group<br><br>**Value**: `"spread"` | String getType() | setType(String type) |


# Example

```java
import cloud.hetzner.api.models.PlacementGroup;
import java.util.Arrays;
import java.util.LinkedHashMap;

PlacementGroup placementGroup = new PlacementGroup.Builder(
    "2016-01-30T23:55:00+00:00",
    42,
    new LinkedHashMap<String, String>() {{
        put("key0", "labels4");
        put("key1", "labels5");
        put("key2", "labels6");
    }},
    "my-resource",
    Arrays.asList(
        42
    ),
    "spread"
)
.build();
```



