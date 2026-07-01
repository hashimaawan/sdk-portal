# Placement Groups Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3Vwc1Jlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`PlacementGroupsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/meta.md) | Optional | - | Meta getMeta() | setMeta(Meta meta) |
| `PlacementGroups` | [`List<PlacementGroup>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/placement-group.md) | Required | - | List<PlacementGroup> getPlacementGroups() | setPlacementGroups(List<PlacementGroup> placementGroups) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Meta;
import cloud.hetzner.api.models.Pagination;
import cloud.hetzner.api.models.PlacementGroup;
import cloud.hetzner.api.models.PlacementGroupsResponse;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

PlacementGroupsResponse placementGroupsResponse = new PlacementGroupsResponse.Builder(
    Arrays.asList(
        new PlacementGroup.Builder(
            "2016-01-30T23:55:00+00:00",
            42,
            new LinkedHashMap<String, String>() {{
                put("key0", "labels0");
                put("key1", "labels1");
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
)
.meta(new Meta.Builder(
        new Pagination.Builder(
            77.7D,
            209.18D,
            17.58D,
            13.34D,
            50.02D,
            206.64D
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



