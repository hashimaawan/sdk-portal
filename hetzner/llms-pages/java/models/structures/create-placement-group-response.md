# Create Placement Group Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkNyZWF0ZVBsYWNlbWVudEdyb3VwUmVzcG9uc2U


# Class Name

`CreatePlacementGroupResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`NullableAction`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/nullable-action.md) | Optional | - | NullableAction getAction() | setAction(NullableAction action) |
| `PlacementGroup` | [`PlacementGroup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/placement-group.md) | Required | - | PlacementGroup getPlacementGroup() | setPlacementGroup(PlacementGroup placementGroup) |


# Example

```java
import cloud.hetzner.api.models.CreatePlacementGroupResponse;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.NullableAction;
import cloud.hetzner.api.models.PlacementGroup;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.StatusEnum;
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
    .build()
)
.action(new NullableAction.Builder(
        "command6",
        new Error.Builder(
            "code2",
            "message4"
        )
        .build(),
        "finished0",
        238,
        143.26D,
        Arrays.asList(
            new Resource.Builder(
                198,
                "type0"
            )
            .build(),
            new Resource.Builder(
                198,
                "type0"
            )
            .build(),
            new Resource.Builder(
                198,
                "type0"
            )
            .build()
        ),
        "started8",
        StatusEnum.RUNNING
    )
    .build())
.build();
```



