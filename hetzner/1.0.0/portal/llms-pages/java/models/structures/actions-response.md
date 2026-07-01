# Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkFjdGlvbnNSZXNwb25zZQ


# Class Name

`ActionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Actions` | [`List<Action>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/action.md) | Required | - | List<Action> getActions() | setActions(List<Action> actions) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/meta.md) | Optional | - | Meta getMeta() | setMeta(Meta meta) |


# Example

```java
import cloud.hetzner.api.models.Action;
import cloud.hetzner.api.models.ActionsResponse;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.Meta;
import cloud.hetzner.api.models.Pagination;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.StatusEnum;
import java.util.Arrays;

ActionsResponse actionsResponse = new ActionsResponse.Builder(
    Arrays.asList(
        new Action.Builder(
            "start_server",
            new Error.Builder(
                "action_failed",
                "Action failed"
            )
            .build(),
            "2016-01-30T23:55:00+00:00",
            42,
            100D,
            Arrays.asList(
                new Resource.Builder(
                    42,
                    "server"
                )
                .build()
            ),
            "2016-01-30T23:55:00+00:00",
            StatusEnum.SUCCESS
        )
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
        .build()
    )
    .build())
.build();
```



