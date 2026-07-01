# Placement Group Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3VwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`PlacementGroupResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `PlacementGroup` | [`PlacementGroup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/placement-group.md) | Required | - | PlacementGroup getPlacementGroup() | setPlacementGroup(PlacementGroup placementGroup) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.PlacementGroup;
import cloud.hetzner.api.models.PlacementGroupResponse;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

PlacementGroupResponse placementGroupResponse = new PlacementGroupResponse.Builder(
    new PlacementGroup.Builder(
        "2016-01-30T23:55:00+00:00",
        42,
        new LinkedHashMap<String, String>() {{
            put("key0", "labels4");
        }},
        "my-resource",
        Arrays.asList(
            42
        ),
        "spread"
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



