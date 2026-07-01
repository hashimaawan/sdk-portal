# Create Placement Group Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNyZWF0ZVBsYWNlbWVudEdyb3VwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`CreatePlacementGroupResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`NullableAction`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/nullable-action.md) | Optional | - | NullableAction getAction() | setAction(NullableAction action) |
| `PlacementGroup` | [`PlacementGroup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/placement-group.md) | Required | - | PlacementGroup getPlacementGroup() | setPlacementGroup(PlacementGroup placementGroup) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.CreatePlacementGroupResponse;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.NullableAction;
import cloud.hetzner.api.models.PlacementGroup;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.Status;
import java.io.IOException;
import java.util.Arrays;
import java.util.LinkedHashMap;

CreatePlacementGroupResponse createPlacementGroupResponse = new CreatePlacementGroupResponse.Builder(
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
.action(new NullableAction.Builder(
        "command6",
        new Error.Builder(
            "code2",
            "message4"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        "finished0",
        238,
        143.26D,
        Arrays.asList(
            new Resource.Builder(
                198,
                "type0"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new Resource.Builder(
                198,
                "type0"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new Resource.Builder(
                198,
                "type0"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        ),
        "started8",
        Status.RUNNING
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



